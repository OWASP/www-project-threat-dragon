---
title: Roadmap
layout: null
tab: true
order: 3
tags: threatdragon
---

## Version 2.6: in progress

- [ ] provide an API for CI/CD pipelines
- [ ] provide a CLI for scripting based on TD's existing [use of yargs](https://github.com/yargs/yargs)

### Version 2.5: released August 2025

- [x] add demo models from the Threat Model Cookbook

### Version 2.3: released December 2024

- [x] automated threats (both by element and by OATS)

### Version 2.2: released February 2024

Threat model access for web app:

- [x] load models from various repos :
  - [x]  github enterprise
  - [x]  gitlab
  - [x]  github enterprise
  - [x]  BitBucket

### Version 2.1: released October 2023

Stable version of 2.x.x with bug fixes and usable diagram tools. Still not feature complete:

- missing CLI for scripting based
- missing automated threats (both by element and by OATS)

### Version 2.0: released February 2023

**migrate to a combined application for both desktop and webapp**:

- [x] be strictly open source
- [x] use [Vue](https://v3.vuejs.org/guide/introduction.html#what-is-vue-js) for frontend application
- [x] use @antv/g6 for the drawing library
- [x] frontend logging using [bunyan](https://github.com/trentm/node-bunyan)
    and optional logging to the console during development
- [x] use [electron](https://www.electronjs.org/) to wrap webapp for desktop
- [X] provide auto-update using [electron](https://www.electronjs.org/)
- [X] expand electron unit tests using
    [WDIO Electron Service](https://github.com/webdriverio-community/wdio-electron-service)
- [x] webapp unit test framework [Jest](https://jestjs.io/)
- [x] component test [Vue testing library](https://github.com/testing-library/vue-testing-library)
- [x] end-to-end test [cypress](https://github.com/cypress-io/cypress)
- [x] set up ZAP to provide security testing on commit
- [x] design files are to be backwardly compatible to Threat Dragon json

**demonstration pages**:

- [x] an online demonstration to be provided on [threat dragon's site](https://www.threatdragon.com)
- [x] demo should either be a snapshot or a release version

### Version 1.4: released May 2021

- [x] written in javascript ES6 / ECMAScript 2015 or compatible
- [x] run on [node.js](https://nodejs.org/en/) server
- [x] use [express](https://expressjs.com/en/starter/installing.html) for backend application
- [x] provide a dockerfile for running in docker,
    similar to [existing TD](https://github.com/OWASP/threat-dragon/blob/main/Dockerfile)
- [x] static code analysis using [ESLint](https://eslint.org)
- [x] webapp test runner [Karma](http://karma-runner.github.io/6.3/intro/installation.html)
with [Jasmine](https://jasmine.github.io)
for [Vue Test Utils](https://vue-test-utils.vuejs.org/installation/#using-other-test-runners)
- [x] backend unit test framework
    [MochaJS](https://mochajs.org) and assertions from [chai](https://github.com/chaijs/chai)
- [x] bundle the application and api for production using [webpack](https://webpack.js.org/)
- [x] be strictly open source, avoiding using languages or frameworks maintained outside the open source community

**documentation**:

- [x] documentation should be updated at the [threat dragon github pages](https://threatdragon.github.io/)
- [x] version 1.x docs are preserved and migrated to version 2.0
- [x] docs should be static pages based on [Jekyll](https://jekyllrb.com) and markdown

### Previous versions

Mike Goodwin's initial roadmap for the project is
[archived here](https://github.com/OWASP/www-project-threat-dragon/wiki/Original-Roadmap).
The original roadmap had various milestones, most of which were achieved by late 2020.

**Milestone 4**: Dev lifecycle integration

- Some CLI interface available mid 2020

**Milestone 3**: Release 1.0

- production version released February 2020
- version 1.3.1 released October 2020

**Milestone 2**: Beta release: Threat/mitigation rule engine

- achieved May 2017 with version 0.1.26

**Milestone 1**: Alpha release - Basic threat modelling experience

- achieved October 2015

----

Threat Dragon: _making threat modeling less threatening_
