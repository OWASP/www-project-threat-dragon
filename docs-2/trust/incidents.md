---

title: Trust
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/incidents/

---

{% include breadcrumb.html %}

## Trust

The automated security scans of Threat Dragon are run on every commit:

* [Dependency management]({{ '/docs-2/dependencies/' | relative_url }})
* [SAST]({{ '/docs-2/sast/' | relative_url }})
* [DAST]({{ '/docs-2/dast/' | relative_url }})
* [Container scanning]({{ '/docs-2/container/' | relative_url }})

### Incident Response

Report security vulnerabilities found within Threat Dragon by following the process in
the [Security Policy](https://github.com/OWASP/threat-dragon/blob/main/security.md).
Every effort will be made to resolve security concerns as they arise.

Threat Dragon is open source software and contains many other open source components.
Threat Dragon's community strives to stay abreast of security vulnerabilities
and incidents impacting upstream providers or Threat Dragon itself.

If there is a high impact or high profile incident or vulnerability,
the Threat Dragon community/maintainers will create a [GitHub Issue](https://www.github.com/owasp/threat-dragon/issues)
and leave it pinned for as long as it is relevant to the community.
This issue will have the "security" label, and is intended to serve as a transparency report,
not necessarily a real-time feed of incident response.

Threat Dragon is maintained by a community of volunteers and so
it will not always be possible to immediately investigate or immediately respond to incidents,
but this community will do its best.

----

Threat Dragon: _making threat modeling less threatening_
