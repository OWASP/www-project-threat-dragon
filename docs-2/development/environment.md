---

title: Development environment
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/development-environment/

---

{% include breadcrumb.html %}

## Quickstart

1. [Generate Keys](#generating-keys) for encryption and JWT signing
2. Copy `example.env` to `.env`
3. Update the values in `.env`
4. `npm install`
5. `npm run serve`

___

### Generating Keys

A random 16 byte (32 character, 256 bit) hexadecimal string should be used for encryption,
which needs to be randomly generated and kept secret.
With openssl installed use this command to generate a new 256 bit key: `openssl rand -hex 16`

This command can also be used to generate JWT signing keys.

The Express server documentation on [express-session](https://github.com/expressjs/session#readme)
has advice on managing and rotating encryption keys.

___

## Config Via DotEnv

Environment variables are configured via [dotenv](https://github.com/motdotla/dotenv#readme).
By default, Threat Dragon attempts to read key/value pairs from a `.env` file at the root of this repository.
This can be configured by exporting a file path in your terminal.
For example, on MacOS/Linux: `export ENV_FILE=/home/myawesomeuser/mydir/somefile.env`

To get started, copy `example.env` to `.env` at the root of the project and update the variables as appropriate.

**Note**: Do not use the `export` or `set` keywords inside your `.env` file,
as this will not work from within a docker context.
The `dotenv` package will automatically export the variables for you.

Alternatively, you can also set your environment variables via [command line](#command-line) if you'd prefer.

Here is an example of a minimal DotEnv file, note that keys would need to be generated :

```text
NODE_ENV=development
ENCRYPTION_KEYS='[{"isPrimary": true, "id": 0, "value": "deadbeef2233445566778899aabbccdd"}]'
ENCRYPTION_JWT_SIGNING_KEY=deadbeef112233445566778899aabbcc
ENCRYPTION_JWT_REFRESH_SIGNING_KEY=deadbeef00112233445566778899aabb
SERVER_API_PROTOCOL='http'
```

___

## Environment Errors

The application will throw an error if a required environment variable is missing during application start:

```text
ENCRYPTION_KEYS is a required property.  Threat Dragon server cannot start without it.
Refer to development/environment.md for more information
```

___

## File Based Secrets

If using file based secrets, add `_FILE` to the end of the secret name, and the value should point to the file location.
This is particularly useful if you are running Threat Dragon in docker context,
as you can use docker secrets or orchestrator such as kubernetes.

An example using docker secrets:

- Create your secrets, for example: `echo "01234567890123456789" | docker secret create github_client_id -`
- Create a docker compose file (example below)
- Deploy to your docker swarm, for example: `docker stack deploy --compose-file docker-compose.yaml owasp-threatdragon`

Example compose file:

```text
version: '3.1'
services:
  threatdragon:
    # Always use a specific version tag, as "latest" may be a development build
    # Alternatively, you can use the "stable" tag, as that will always
    # be the most recently released version
    image: owasp/threat-dragon:v2.0.0
    ports:
      - 3000:3000
    environment:
      GITHUB_CLIENT_ID_FILE: /run/secrets/github_client_id
      GITHUB_CLIENT_SECRET_FILE: /run/secrets/github_client_secret
      ENV_FILE: /run/secrets/node_env
      ENCRYPTION_KEYS_FILE: /run/secrets/encryption_keys
      ENCRYPTION_JWT_SIGNING_KEY_FILE: /run/secrets/jwt_signing_key
      ENCRYPTION_JWT_REFRESH_SIGNING_KEY_FILE: /run/secrets/jwt_refresh_signing_key
      SERVER_API_PROTOCOL_FILE: /run/secrets/protocol
    secrets:
      - github_client_id
      - github_client_secret
      - node_env
      - encryption_keys
      - jwt_signing_key
      - jwt_refresh_signing_key
      - protocol

secrets:
  github_client_id:
    external: true
  github_client_secret:
    external: true
  node_env:
    external: true
  encryption_keys:
    external: true
  jwt_signing_key:
    external: true
  jwt_refresh_signing_key:
    external: true
  protocol:
    external: true
```

___

## Command Line

Export all of the your variables from the terminal where you will start Threat dragon.  

### MacOS / Linux

`export GITHUB_CLIENT_ID=01234567890123456789`

`export ...`

### Windows

`set GITHUB_CLIENT_ID=01234567890123456789`

`set ...`
___

## Environment variable reference

| Threat Dragon general variables | Description | Default |
| --- | --- | --- |
| `ENV_FILE` | The location of a dotenv file, if dotenv is used. Exported as it needs to be accessed before the dotenv file is read | `.env` |
| `LOG_LEVEL` | The server logging level: `audit` / `error` / `warn` / `info` / `debug` / `silly` | `warn` |
| `LOG_MAX_FILE_SIZE` | Maximum size of the back-end express server log file, in MB | `24` |
| `NODE_ENV` | Optional run mode; typically 'test', 'production' or 'development' | `production` |
| `PORT` | Defines the listening port for Threat Dragon's server, and used by Heroku | `3000`|
| `SERVER_API_PROTOCOL` | The protocol used between Threat Dragon's server and frontend, used by Heroku: `http` / `https` | `https` |
| `REPO_USE_SEARCH` | | |
| `REPO_SEARCH_QUERY` | | |
| `REPO_ROOT_DIRECTORY` | Optional path where saved models are stored in the repo | |

The secure cookie flag is set only if running in 'production' mode.

| Desktop specific variables | Description | Default |
| --- | --- | --- |
| `IS_TEST` | Enabled during automated testing | false |
| `WEBPACK_DEV_SERVER_URL` | Electron load URL when in development mode | |

The desktop environment variable WEBPACK_DEV_SERVER_URL determines the mode for webpack;
either development/test mode if defined (for example `http://localhost:3000/`) or production mode if not defined.

| Back-end specific variables | Description | Default |
| --- | --- | --- |
| `ENCRYPTION_KEYS` | The encryption keys used to encrypt any high risk data | |
| `ENCRYPTION_JWT_SIGNING_KEY` | The key used to sign JWTs | |
| `ENCRYPTION_JWT_REFRESH_SIGNING_KEY` | The key used to sign refresh tokens | |

**Note**: the JWT refresh signing key should be different from the JWT signing key as they are different tokens.
A JWT is used as a refresh token because it is tamper resistant and provides user context.

Refer to the step by step [GitHub configuration]({{ '/docs-2/github-repo/' | relative_url }}) page
for an example of setting up Github specific variables.

| Github specific variables | Description | Default |
| --- | --- | --- |
| `GITHUB_CLIENT_ID` | Provided by the GitHub OAuth app used for authentication | |
| `GITHUB_CLIENT_SECRET` | Secret generated by the GitHub OAuth authentication app | |
| `GITHUB_SCOPE` | Optional definition of scope: `repo` to access both private and public repos or `public_repo` to access public repos only | `public_repo` |
| `GITHUB_ENTERPRISE_HOSTNAME` | Optional fully qualified github enterprise instance hostname, e.g. github.example.com | |
| `GITHUB_ENTERPRISE_PORT` | Optional if your github enterprise instance uses a nonstandard port | `443` |
| `GITHUB_ENTERPRISE_PROTOCOL` | Optional if your github enterprise instance uses a nonstandard protocol | `https` |
| `GITHUB_USE_SEARCH` | Optional, if true it will only display the github repos matching the search query below| `false`|
| `GITHUB_SEARCH_QUERY` | Optionally specifies the search query to use when searching for Threat Dragon github repos | |
| `GITHUB_REPO_ROOT_DIRECTORY` | Optional path where saved models are stored in a Github repo | |

There is a step by step [Bitbucket configuration]({{ '/docs-2/bitbucket-repo/' | relative_url }}) page
with an example of setting up Bitbucket specific variables.

| Bitbucket specific variables | Description | Default |
| --- | --- | --- |
| `BITBUCKET_CLIENT_ID` | Provided by the Bitbucket OAuth app used for authentication | |
| `BITBUCKET_CLIENT_SECRET` | Secret generated by the Bitbucket OAuth authentication app | |
| `BITBUCKET_WORKSPACE` | The workspace name provided by the Bitbucket repo |  |
| `BITBUCKET_SCOPE` | Optional definition of scope, set to `repository:write` for write permissions to the repo | `repository:read` |
| `BITBUCKET_ENTERPRISE_HOSTNAME` | Optional fully qualified Bitbucket enterprise instance hostname, e.g. bitbucket.example.com | |
| `BITBUCKET_ENTERPRISE_PORT` | Optional if your Bitbucket enterprise instance uses a nonstandard port | `443` |
| `BITBUCKET_ENTERPRISE_PROTOCOL` | Optional if your Bitbucket enterprise instance uses a nonstandard protocol | `https` |
| `BITBUCKET_REPO_ROOT_DIRECTORY` | Optional path where saved models are stored in a Bitbucket repo | |

There is also a step by step [Gitlab configuration]({{ '/docs-2/gitlab-repo/' | relative_url }}) page
to explain the setting up of Gitlab specific variables.

| GitLab specific variables | Description | Default |
| --- | --- | --- |
| `GITLAB_CLIENT_ID` | The 'Application ID' provided by the Gitlab OAuth app used for authentication | |
| `GITLAB_CLIENT_SECRET` | The 'Application Secret' generated by the Gitlab OAuth authentication app | |
| `GITLAB_SCOPE` | The scope provided to the Gitlab OAuth app, for example 'api' provides maximum scope | `read_user read_repository` |
| `GITLAB_HOST` | The URL of Gitlab server, for example `https://gitlab.com/` | |
| `GITLAB_REDIRECT_URI` | The redirect provided to the Gitlab OAuth app, for example `<URL of Threat Dragon app>/api/oauth/return` | |
| `GITLAB_REPO_ROOT_DIRECTORY` | Optional path where saved models are stored in a Gitlab repo | |
