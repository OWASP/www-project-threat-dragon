---
title: Roadmap
layout: null
tab: true
order: 4
tags: threatdragon
---

Mike Goodwin's initial vision for the project is [archived here](https://github.com/OWASP/www-project-threat-dragon/wiki/Original-Roadmap)

**Milestone 1**: Alpha release - Basic threat modelling experience
* achieved October 2015

**Milestone 2**: Beta release - Threat/mitigation rule engine
* achieved May 2017 with version 0.1.26

**Milestone 3**: Release 1.0
* production version released February 2020
* version 1.3.1 was released October 2020

**Milestone 4**: - Dev lifecycle integration
* Not yet achieved

# Version 2.0: planned for late 2021
**create a combined application for both webapp and core**
1. written in javascript ES6 / ECMAScript 2015 or compatible
1. run on [node.js](https://nodejs.org/en/) server
1. use [express](http://expressjs.com/en/starter/installing.html) for backend application
1. use [Vue](https://v3.vuejs.org/guide/introduction.html#what-is-vue-js) for frontend application
1. use [mxgraph](https://github.com/jsGraph/mxgraph) for the drawing library
1. provide a dockerfile for running in docker, similar to [existing TD](https://github.com/OWASP/threat-dragon/blob/main/Dockerfile)
1. provide an API for CI/CD pipelines, [see here](https://github.com/bbachi/vuejs-nodejs-example/tree/master/api) for a direct example
1. use frameworks for unit ([Mocha](https://github.com/mochajs/mocha)), component ([Vue testing library](https://github.com/testing-library/vue-testing-library)) and end-to-end testing
1. set up ZAP to provide security testing on commit, similar to [existing TD](https://github.com/OWASP/threat-dragon/blob/main/.github/workflows/zap_scan.yaml)
1. be strictly open source, avoiding using languages or frameworks maintained outside the open source community

**create a desktop application**
1. use [electron](https://www.electronjs.org/) to wrap webapp for desktop
1. incorporates webapp as a git submodule, similar to [drawio](https://github.com/jgraph/drawio) as a submodule for [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
1. provide auto-update similar to [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
1. provide a CLI for scripting based on TD's existing [use of yargs](https://github.com/yargs/yargs)
1. be strictly open source, avoiding using languages or frameworks maintained outside the open source community

**desktop and webbapp should**:
load models from similar sources to draw.io:
1. github
1. gitlab
1. Google Drive
1. OneDrive
1. Dropbox
1. local filesystem device

allow design files to be backwardly compatible to Threat Dragon json:
* reads json file and converts to mxgraph native xml
* converts from mxgraph native xml and writes as json file

be strictly open source
* avoid using languages or frameworks maintained outside the open source community
