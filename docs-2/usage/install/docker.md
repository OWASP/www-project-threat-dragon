---

title: Docker installation
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/install-docker/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

[Threat Dragon](http://owasp.org/www-project-threat-dragon) comes in two variants,
a desktop application and a web application.

## Docker installation instructions

The web application can be run from a docker container which can either be downloaded or built locally.

### Downloading

The Docker image can either be pulled from dockerhub or built locally.

#### Pulling/Downloading

The released docker images are stored in
[Docker Hub](https://hub.docker.com/r/owasp/threat-dragon/tags?page=1&ordering=name)
and can be accessed using docker `pull`.
For example to download the latest stable release from Docker hub use command :

`docker pull owasp/threat-dragon:stable`

There are step-by-step instructions for [Bitbucket]({{ '/docs-2/bitbucket-repo/' | relative_url }}),
[Gitlab]({{ '/docs-2/gitlab-repo/' | relative_url }}), and [github ]({{ '/docs-2/github-repo/' | relative_url }})
access which explain the configuration needed to provide the environment variables for the docker container.

'Stable' is built for OS linux and architecture amd64 and in future there will be builds for architecture arm64.

The latest builds are available on the [threatdragon-repo], for example:

* `docker pull threatdragon/owasp-threat-dragon:latest-arm64` for architecture arm64
* `docker pull threatdragon/owasp-threat-dragon:latest` for amd64

#### Building

If the docker image needs to be rebuilt then start by cloning the Threat Dragon github project.
The docker image can then be built from the top directory of the project
which contains the `Dockerfile`. Use a command such as :

`docker build -t owasp-threat-dragon:local .`

Note that here tag `local` has been used, but it could be almost anything such as `dev`.

### Environment variables

See the [environment]({{ '/docs-2/development-environment/' | relative_url }}) page
for details on what environment variables are expected.
Threat Dragon currently supports [dotenv](https://github.com/motdotla/dotenv),
as well as file-based loading by setting environment variables with the `_FILE` postfix,
eg: `ENCRYPTION_KEYS_FILE=/run/secrets/td_encryption_keys`
This is also shown in the docker-compose section of the environment documentation.

### Running the docker container

Running a locally built image or a downloaded image are very similar,
just substitute the correct name in the command to run a detached container:

`docker run -d -p 8080:3000 -v $(pwd)/.env:/app/.env owasp-threat-dragon:local`

Note that the container will need access to various environment variables, this can be done using the
`-v $(pwd)/.env:/app/.env` part of the command - assuming that the `.env` file
is on the directory from where you run the command.
Windows users may not have access to the PWD environment variable,
so just substitute an absolute path instead of `$(pwd)`.

Here the container internal port is mapped to external port 8080,
therefore Threat Dragon is accessible from `http://localhost:8080` .

### Debugging

Console output can be displayed using the `-it` options instead of `-d`,
for example `docker run -it -p 8080:3000 -v $(pwd)/.env:/app/.env owasp-threat-dragon:local`.

If the application is not loading from the expected address and port,
logging can be increased using the `LOG_LEVEL` environment variable.
For example if the `.env` file is edited to include `LOG_LEVEL=debug`
then the container console output for an initial access is :

```text
Using config file: /app/.env
warn: app.js: Rate limiting disabled for development environments {"service":"threat-dragon","timestamp":""}
info: app.js: Express server listening on 3000 {"service":"threat-dragon","timestamp":""}
info: app.js: OWASP Threat Dragon application started {"service":"threat-dragon","timestamp":""}
Express server listening at :: on port 3000
debug: controllers/homecontroller.js: API index request,
sendFile /app/dist/index.html {"service":"threat-dragon","timestamp":""}
```

[threatdragon-repo]: https://hub.docker.com/repository/docker/threatdragon/owasp-threat-dragon/tags
