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
2. provide a dockerfile for running in docker
3. use frameworks for unit, component and end-to-end testing
4. provide an API for CI/CD pipelines

**create a desktop application**
1. use [electron](https://www.electronjs.org/) to wrap webapp for desktop
1. incorporates webapp as a git submodule, similar to [drawio](https://github.com/jgraph/drawio) as a submodule for [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
1. provide auto-update similar to [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
2. provide a CLI for scripting

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
