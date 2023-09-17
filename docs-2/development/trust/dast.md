---

title: DAST
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/dast/

---

{% include breadcrumb.html %}

## Dynamic Application Security Testing (DAST)

Dynamic application security testing is the process of testing code that is running to identify
potential vulnerabilities and misconfigurations.
This is provided by [OWASP ZAP](https://www.zaproxy.org/docs/docker/about/) and is run as part of every commit.

ZAP scan results are attached to the output of an action.
An ignore-list is maintained as a TSV (tab separated values, careful what editor you use).
Any modifications to the exclusions should be approved by a maintainer as part of a pull request.
