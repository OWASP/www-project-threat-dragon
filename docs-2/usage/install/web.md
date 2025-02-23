---

title: Install Web App
layout: col-document
tags: threatdragon
document: OAWSP Threat Dragon version 2.x
permalink: /docs-2/install-webapp/

---

{% include breadcrumb.html %}

[Threat Dragon](http://owasp.org/www-project-threat-dragon) comes in two variants,
a desktop application and a web application.

## Web application install instructions

The web application can be run locally or from a server.

### Installing

Threat Dragon is a node.js single page application using Vue on the client and Express on the server.
To build and run locally follow these steps:

Install [node.js][download], which includes the node package manager `npm`,
and also install [git](https://git-scm.com/downloads).
To get the code, navigate to where you want your code to be located and run

```text
git init
git clone https://github.com/owasp/threat-dragon.git
```

This installs code in two sub-folders. One for the main application (`td.site`) and one for the server (`td.server`).
To install use npm (or pnpm if that is installed) :

`npm install`

### Environment variables

See the [environment]({{ '/docs-2/install-environment/' | relative_url }}) page
for details on configuring your environment variables.

### Running the application

Once your environment variables are set up, if running on Linux or MacOS start the node web server with :

`npm start`

When running on Windows the front-end and back-end are started separately using commands:
`npm run dev:server` and `npm run dev:vue`.

If you then browse to `http://localhost:8080` you should see the running application.

[download]: https://nodejs.org/en/download/package-manager
