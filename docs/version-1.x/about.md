---

title: About
layout: col-document
tags: Threat Dragon
author:
contributors:
document: Threat Dragon
order: 2
permalink: /docs/version-1.x/

---

{% include breadcrumb.html %}
## [OWASP](https://www.owasp.org) Threat Dragon

[Threat Dragon](http://owasp.org/www-project-threat-dragon) is a free, open-source, 
cross-platform [threat modeling](https://owasp.org/www-community/Threat_Modeling)
application including system diagramming and a rule engine to auto-generate threats/mitigations.
[Mike Goodwin](https://github.com/mike-goodwin) created Threat Dragon as an open source community project
that provides an intuitive and accessible way to model threats.

Threat Dragon is an [OWASP Lab Project](https://owasp.org/www-project-threat-dragon/)
and follows the values and principles of the threat modeling [manifesto](https://www.threatmodelingmanifesto.org/).
An [introduction](https://www.youtube.com/watch?v=hUOAoc6QGJo) to Threat Dragon is provided by
the [OWASP Spotlight](https://www.youtube.com/playlist?list=PLUKo5k_oSrfOTl27gUmk2o-NBKvkTGw0T) series,
and a different take on Threat Dragon is provided by [Threat Modeling Gamification](https://www.youtube.com/watch?v=u2tmLrwv-nc).

Threat Dragon supports STRIDE<sup>[1](#footnote1)</sup>, LINDDUN<sup>[2](#footnote2)</sup> and CIA<sup>[3](#footnote3)</sup>.

There is a good overview of [threat modeling and risk assessment](https://owasp.org/www-community/Application_Threat_Modeling)
from OWASP, and this expands on what the Threat Dragon project aims for: 
* ease of use and accessible
* designing a data flow diagram
* suggesting threats
* entering mitigations and counter measures

The application comes in two variants:

1. [**A desktop application**](https://github.com/OWASP/threat-dragon/releases): This is based on
[Electron](https://electron.atom.io/), with model files stored on the local filesystem.
There are installers available for both Windows and Mac OSX, as well as rpm and debian packages for Linux.

1. [**A web application**](https://github.com/owasp/threat-dragon/releases): For the web application model files
are stored in GitHub, with other storage methods to follow.

<sup><a name="footnote1">1</a>: Spoofing, Tampering, Repudiation, Information disclosure, DoS, Elevation of privilege</sup><br>
<sup><a name="footnote2">2</a>: Linkability, Identifiability, Non-repudiation, Detectability, Disclosure of information, Unawareness, Non-compliance</sup><br>
<sup><a name="footnote3">3</a>: Confidentiality, Integrity, Availability</sup><br>
