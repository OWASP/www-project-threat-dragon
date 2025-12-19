---

title: TMF
displaytext: Threat Model Format
layout: null
tab: true
order: 5
tags: threatdragon

---

## Threat model file format

Threat Dragon version 1.x and Threat Dragon version 2.x use closely related but incompatible JSON file formats.
In addition both these file formats are arranged around diagram elements used by the graph editing engines:
JointJS for version 1.x and AntV/X6 for version2.x.
The  data model use in the Threat Dragon file format would be better centred round threat model information
rather than the data used for the graph editing.

Both Threat Dragon file formats are incompatible with other open source Threat Modeling files
such as pytm, Threagile and Open Threat Model.

The intention is to change the model file format in Threat Dragon version 3.x onwards.
The goal will be to define a file format that is flexible enough to easily convert from the existing:

* OWASP Threat Dragon versions 1.x and 2.x
* [OWASP pytm][pytm] pythonic threat modeling
* [Threagile][threagile] open-source toolkit for agile threat modeling
* [Open Threat Model][otm] (OTM) file format

There is an [open discussion][discussion] for suggestions and debate on this subject.

### Threat Model Bill of Materials (TM-BOM)

It is very likely that the model file format used from version 3.x
will follow the Threat Model Bill of Materials (TM-BOM) schema.
This is similar in philosophy to a Software Bill of Materials (SBOM)
and is overseen by the [CycloneDX][cyclone] organization.

The proof of concept [TM-BOM schema][tm-library-schema] is provided
by the OWASP [Threat Model Library][tm-library] project.
An [overview of TM-BOM][tm-bom] is available in the Threat Dragon documentation.

[cyclone]: https://owasp.org/www-project-cyclonedx/
[discussion]: https://github.com/OWASP/threat-dragon/discussions/1152
[otm]: https://github.com/iriusrisk/OpenThreatModel
[pytm]: https://owasp.org/www-project-pytm/
[threagile]: https://threagile.io
[tm-bom]: https://www.threatdragon.com/docs/development/schema.html
[tm-library]: https://github.com/OWASP/www-project-threat-model-library
[tm-library-schema]: https://github.com/OWASP/www-project-threat-model-library/blob/main/threat-model.schema.json
