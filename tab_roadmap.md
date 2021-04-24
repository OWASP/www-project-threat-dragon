---
title: Roadmap
layout: null
tab: true
order: 4
tags: threatdragon
---

Mike Goodwin's initial roadmap for the project is [archived here](https://github.com/OWASP/www-project-threat-dragon/wiki/Original-Roadmap).
The original roadmap had various milestones, most of which were achieved by late 2020.

**Milestone 1**: Alpha release - Basic threat modelling experience
* achieved October 2015

**Milestone 2**: Beta release - Threat/mitigation rule engine
* achieved May 2017 with version 0.1.26

**Milestone 3**: Release 1.0
* production version released February 2020
* version 1.3.1 was released October 2020

**Milestone 4**: - Dev lifecycle integration
* Still to be completed, some CLI interface available mid 2020

## Version 2.0: planned for late 2021
**migrate to a combined application for both webapp and core**
1. written in javascript ES6 / ECMAScript 2015 or compatible
1. run on [node.js](https://nodejs.org/en/) server
1. use [express](http://expressjs.com/en/starter/installing.html) for backend application
1. use [Vue](https://v3.vuejs.org/guide/introduction.html#what-is-vue-js) for frontend application
1. use [mxgraph](https://github.com/jsGraph/mxgraph) for the drawing library. Here is [a good example](https://github.com/lanniu/vue-mxgraph-example) for this
2. provide multiple methods of authentication, inn a simlar  way to [draw.io](https://app.diagrams.net)
3. provide a dockerfile for running in docker, similar to [existing TD](https://github.com/OWASP/threat-dragon/blob/main/Dockerfile)
4. provide an API for CI/CD pipelines, [see here](https://github.com/bbachi/vuejs-nodejs-example/tree/master/api) for an example
5. static code analysis using [ESLint](https://eslint.org)
6. webapp test runner [Karma](http://karma-runner.github.io/6.3/intro/installation.html)
with [Jasmine](https://jasmine.github.io)
for [Vue Test Utils](https://vue-test-utils.vuejs.org/installation/#using-other-test-runners)
5. webapp unit test framework [MochaJS](https://mochajs.org), assertions from [Chai](http://chaijs.com/) and spies from [Sinon](http://sinonjs.org/)
6. backend unit test framework [MochaJS](https://mochajs.org) and assertions from [supertest](https://github.com/visionmedia/supertest#readme)
7. component test [Vue testing library](https://github.com/testing-library/vue-testing-library)
8. end-to-end test [nightwatch](https://github.com/nightwatchjs/nightwatch) or [puppeteer](https://github.com/puppeteer/puppeteer)
9. set up ZAP to provide security testing on commit, similar to [existing TD](https://github.com/OWASP/threat-dragon/blob/main/.github/workflows/zap_scan.yaml)
10. frontend logging using [bunyan](https://github.com/trentm/node-bunyan) and optional logging to the console during development 
11. bundle the application and api for production using [vite](https://vitejs.dev)
12. be strictly open source, avoiding using languages or frameworks maintained outside the open source community

**provide desktop application as a wrapper**
1. use [electron](https://www.electronjs.org/) to wrap webapp for desktop
1. incorporates webapp as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), similar to [drawio](https://github.com/jgraph/drawio) as a submodule for [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
1. provide auto-update similar to [drawio-desktop](https://github.com/jgraph/drawio-desktop/)
1. provide a CLI for scripting based on TD's existing [use of yargs](https://github.com/yargs/yargs)
1. use test framework [electron mocha](https://github.com/jprichardson/electron-mocha)
1. [electron log](https://github.com/megahertz/electron-log) logging level controlled by command line
1. be strictly open source

**file access for both desktop and webbapp**:

 1. load models from various sources similar to [drawio](https://github.com/jgraph/drawio):
* github
* gitlab
* Google Drive
* OneDrive
* Dropbox
* local filesystem device

 2. design files are to be backwardly compatible to Threat Dragon json, along the lines of:
* read json file and convert to mxgraph native xml
* convert from mxgraph native xml and write as json file

**demonstration pages**:
* an online demonstration should be provided on [threat dragon's github pages](https://threatdragon.github.io/demo)
* demo should either be a snapshot or a release version, to be decided

**documention**:
* documentation should be updated at the [threat dragon github pages](https://threatdragon.github.io/docs)
* version 2.0 docs should initially use path /docs/, so that  version 1.x docs are preserved until version 2.0 is ready
* docs should be static pages based on [Jekyll](https://jekyllrb.com) and [markdown](https://docs.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)

