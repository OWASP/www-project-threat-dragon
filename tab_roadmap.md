---

title: Roadmap
displaytext: Road Map
layout: null
tab: true
order: 3
tags: threatdragon

---

## Strategic Roadmap

Threat Dragon maintains a strategic roadmap in a public
[GitHub Discussion](https://github.com/OWASP/threat-dragon/discussions/1480).
Please join us in defining the direction for Threat Dragon!

## Release Log

Threat Dragon creates [GitHub Releases](https://github.com/OWASP/threat-dragon/releases/)
for each release. Each release contains the artifacts and the change log.

The latest release is always available
[on GitHub](https://github.com/OWASP/threat-dragon/releases/latest)

### Versioning & Release Cadence

Threat Dragon adheres to [semantic versioning](https://semver.org/) for all releases.
In practice, this means:

- Patch versions include bug/security fixes, with no breaking changes
- Minor versions include new features or functionality, with no breaking changes
- Major versions include breaking changes, major upgrades, etc.

There is no official release cadence at this time.  Threat Dragon maintainers create
new releases for new features and bugfixes when appropriate.

## Major Version Releases

### Version 3.0: future initiatives

Version 3 is not well defined at this time. The following features may
be included in this future release.

- TM-BOM / [Threat model file format](https://owasp.org/www-project-threat-dragon/#div-tmf)

### Version 2.0: Modernization

Version 2.0 of Threat Dragon was largely done to exist technical debt and improve
the overall maturity of Threat Dragon.  Some highlights from this major version:

- Migration from angular to Vue
- Upgraded the diagram library
- [Met OpenSSF Best Practices](https://www.bestpractices.dev/en/projects/9266/passing#analysis)
- Combined frontend with desktop application
- Updated threat model schema
- Implemented end to end testing
- DAST scanning via Zap
- Public [demo instance](https://www.threatdragon.com/)

### Version 1.0: Initial Release

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
