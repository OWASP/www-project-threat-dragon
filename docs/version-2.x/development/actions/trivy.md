---

title: Trivy scan
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 37
permalink: /docs-2/trivy/

---

{% include breadcrumb.html %}
# GitHub Actions

[GitHub Actions](https://docs.github.com/en/actions/reference) are used to test, build and deploy Threat Dragon.
These actions live in the `.github/workflows` directory.

## Trivy Container Scan

[Trivy](https://github.com/aquasecurity/trivy) is an open-source container and artifact vulnerability scanning tool.

The trivy action is configured to run once a day to identify unpatched vulnerabilities in the docker image.
This is run per commit, as well as on a cron.
The cron-based action will alert maintainers in GitHub's security tab, as it will check the main branch daily.
The per-commit check will fail a build and print the results in the corresponding action.
This is only run against the production docker image at the time of writing.
