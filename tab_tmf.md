---
title: Threat Model File format
layout: null
tab: true
order: 4
tags: threatdragon
---

### Threat Model File (TMF) format

Threat Dragon version 1.x and Threat Dragon version 2.x use closely related but incompatible JSON file formats.
In addition both these file formats are arranged around diagram elements used by the graph editing engines:
JointJS for version 1.x and AntV/X6 for version2.x.
The  data model use in the Threat Dragon file format would be better centred round threat model information
rather than the data used for the graph editing.

Both Threat Dragon file formats are incompatible with other open source Threat Modeling files
such as pytm, Threagile and Open Threat Model.

The intention is to change the model file format in Threat Dragon version 3.x onwards.
The goal will be to define a schema that is flexible enough to easily convert from the existing:

* [OWASP Threat Dragon] versions 1.x and 2.x
* [OWASP pytm][pytm] pythonic threat modeling
* [Threagile][threagile]
* [Open Threat Model][otm] (OTM)

There is an [open discussion][discussion] for suggestions and debate on this subject.

[discussion]: https://github.com/OWASP/threat-dragon/discussions/1152
[otm]: https://github.com/iriusrisk/OpenThreatModel
[pytm]: https://owasp.org/www-project-pytm/
[threagile]: https://threagile.io
