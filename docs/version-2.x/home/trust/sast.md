---

title: SAST
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 6
permalink: /docs-2/sast/

---

{% include breadcrumb.html %}
# Static Application Security Testing (SAST)
Static application security testing is the process of examining code at rest to identify potential vulnerabilities and misconfigurations.
This is provided by [CodeQL](https://securitylab.github.com/tools/codeql/) and is run as part of every pull request.
Pull requests with CodeQL failures will not be accepted unless the alert is proven to be a false/positive.
