---

title: Install web app
layout: col-document
tags: threatdragon
document: Threat Dragon version 1.6.1
permalink: /docs-1/install-webapp/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

[Threat Dragon](http://owasp.org/www-project-threat-dragon) comes in two variants,
desktop application and web application.

## Web application install instructions

The web application can be run locally or by using a remote server.

### Using a Docker container

Pull the Threat Dragon docker image using `docker pull owasp/threat-dragon:stable`.
The `stable` tag will always be the latest official release, alongside the specific release versions.

To obtain a specific version, for example v1.6.0, use a command such as `docker pull owasp/threat-dragon:v1.6.0`

**Do not use the latest tag (which may be the default) because it could be a development release.**

The environment variables will need configuration so there is
a [step-by-step guide]({{ '/docs-1/setup/' | relative_url }}) to help with this.
Once the environment is set up and the docker image is ready, run the docker container using a command such as:

`docker run -it --rm -p 3000:3000 -v $(pwd)/.env:/app/.env owasp/threat-dragon:v1.6.0`

assuming:

* use of port 3000, this can be changed to another port for example `-p 3000:5000` for port 5000
* you are running from the directory  which contains the `.env` file
* it was version `1.5.8` that was pulled from dockerhub. Replace with later versions as necessary

Note that a valid environment must  be provided, otherwise the container will halt with errors
such as `Error: GITHUB_CLIENT_ID is a required property`.

### Installing from source

Threat Dragon is a Single Page Application (SPA) using Angular on the client and node.js on the server.
To build and run locally follow these steps:

Install git and node.js - which includes the node package manager npm.
To get the code, navigate to where you want your code to be located and run command:

`git clone --recursive https://github.com/owasp/threat-dragon.git`

This downloads the code into a directory called `threat-dragon` and contains the application code in two sub-folders,
one for the back-end application (`td.server`) and one for the front-end (`td.site`).

To install, run: `npm install` from the root of the project.
A `postinstall` script is run that will install dependencies in both
the `server` and `site` directories as well.

### Environment variables

Setting up these environment variables has at times caused some confusion,
so there is a [step-by-step guide]({{ '/docs-1/setup/' | relative_url }}) to help with this.

Threat Dragon uses GitHub to store threat models, so you need to go to your GitHub account and
[register it as a GitHub application](https://github.com/settings/applications/new).
Once you have done that you need to set the Client ID and Client Secret as environment variables
(`GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`).
You also need to set a session signing key environment variable (`SESSION_SIGNING_KEY`).

Once a user is signed in, their session information contains an OAuth access token
with write access to their GitHub repos.
For security, this is encrypted before storage in the session.
The session encryption supports multiple keys so that they can be expired
without any interruption to the running application. The primary key is always used for encryption.
Retired keys can be kept available for decrypting existing sessions.
Once all sessions are using the new primary key (typically this will be around 60 minutes maximum),
the old one can be safely removed.
The keys are stored as a JSON string in  the `SESSION_ENCRYPTION_KEYS` environment variable. For example:

`[{\"isPrimary\": true, \"id\": 0, \"value\": \"abcdef\"}, {\"isPrimary\": false, \"id\": 1, \"value\": \"ghijkl\"}]`

If you are developing locally,
you can choose to store the session data in memory using the express-session in-memory store.
To do this set the `SESSION_STORE`environment variable to `local`.
As [mentioned in the express-session docs](https://github.com/expressjs/session) this is
for development only - it is not suitable for production.
To remind you of this, Threat Dragon will write a log message at severity ERROR when
it starts if the in memory session store is used.

By default Threat Dragon will set the `secure` flag on cookies.
To override this for development purposes set the `NODE_ENV` environment variable to `development`.

### Running the application

Once your environment variables are set up, start the node web server:

`npm start`

If you then browse to `http://localhost:3000` you should see the running application.
