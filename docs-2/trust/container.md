---

title: Container scanning
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/container/

---

{% include breadcrumb.html %}

[Trivy](https://github.com/aquasecurity/trivy) identifies known vulnerable packages inside the container,
and scans the built container as part of each commit and pull-request.
It is also run as a nightly cron job against the default branch.

The GitHub action will fail if Trivy identifies _any_ vulnerabilities; this is strict by design.
If vulnerabilities are discovered then the maintainers are alerted via GitHub's security tab.

A `.trivyignore` file is maintained at the root of this repo.
A comment with a justification should live above the ignored CVE.
