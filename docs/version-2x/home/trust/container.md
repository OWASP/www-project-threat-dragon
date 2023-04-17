---

title: Container Scanning
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon version 2.0
order: 8
permalink: /docs-2/container/

---

{% include breadcrumb.html %}
# Container Scanning
[Trivy](https://github.com/aquasecurity/trivy) scans the built container as part of each commit and PR.
The GitHub action will fail if it identifies _any_ vulnerabilities.  This is strict by design.
It identifies known vulnerable packages inside the container.  It is also run as a cron job, daily, against the default branch.
If _any_ vulnerabilities are discovered, it will alert maintainers via GitHub's security tab.

A `.trivyignore` file is maintained at the root of this repo.  A comment with a justification should live above the ignored CVE.
