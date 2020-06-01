---
title: Roadmap
layout: null
tab: true
order: 4
tags: threatdragon
---

<style type="text/css">
.image-left {
  display: block;
  margin-left: auto;
  margin-right: auto;
  float: right;
}
</style>

![logo](/assets/images/cupcake-256x256.png){: .image-left }

## Roadmap
### Vision for the project:

The overall vision for the project is to implement a tool that removes as many barriers as possible for
organisations wanting to embed threat modelling into their development lifecycle. Barriers I have seen are:
* Lack of cross platform tooling: Tool needs to be x-platform
* Poor UX in existing tools, productivity is poor: Great UX is a must
* Steep learning curve for adopting teams: Tool to build in expert knowledge to help the team get started
* Models are ignored: Integration with other lifecycle tools is key

### Initial high level plan:

Milestone 1: Alpha release - Basic threat modelling experience
* Architecture review of the existing prototype with refinement/change where required - complete: Confirmed JointJs works fine, Storage model changed and addition of Electon based desktop variant. Nools rule engine (no longer supported) replaced by json-rules-engine. Shifted from Grunt/Bower to NPM/Browserify
* Secure design review and implementation of findings
* Development of tests (unit and manual) - complete: Codecov report
* Draft end user documentation - complete: GitHub pages
* "Publicity drive" to sign up alpha/beta users and generate feedback
Some progress on this. The desktop app has had 13k downloads - unclear how many people are actually using it.
The GH repo for the desktop version has 79 stars. The web version gets about 94 unique visitors per day on average
and the GH repo has 229 stars.

Milestone 2: Beta release - Threat/mitigation rule engine
* Refinement of UX based on feedback from the alpha release
* (Some) feature enhancements based on feedback from the alpha release
Implemented some feature requests (e.g. snap-to-grid) and fixed issues reports (e.g. save bugs) by users
* Implementation of a rule engine for generation of threats/mitigations
* Updated tests and end-user documentation

Milestone 3: Release 1
* Key refinements, bug fixes and new features based on feedback from the beta release
* Complete end user documentation
* Penetration test

Milestone 4 - Dev lifecycle integration
* Detailed scope to be defined, but in general the vision is to support hooks into issue tracking and requirements management tool so that threats/mitigations can be tracked through to implementation and test

### Timeframes
This is hard to estimate as it could change a lot if there were other developers involved. Based on my current velocity with just me, I would say release 1 could be complete in 1 year (optimistically).

### Technology
The technical architecture is javascript from top to bottom. In the client the key libraries are Angular for the MVC architecture and JointJS for the diagramming. JointJS has a log of great features, but is not a perfect fit for Angular. This needs a review. In the prototype, all storage is done on the client using browser local storage.

Following an architecture review the following key changes were made:

* A new Electron based, installable desktop variant was introduced using the local file system for model storage
* The web variant was changed to use GitHub for model storage - other source control systems will follow (e.g. BitBucket)
* Seperation of common code into a new NPM package, shared between the web and desktop variants
* The Nools rule engine will be replaced since it is no longer maintained

### Challenges
* Getting enough usage of the alpha and beta to get the UX and rule engine right
* Finding a sustainable way to host it, especially to support deeper GitHub/BitBucket/Etc. integration

## Minimum Viable Product
1. Application source code for a threat modeling tool
2. End user documentation for the tool
3. An online hosted version of the tool
4. An installable, cross-platform desktop version of the tool
