---

title: CodeQL
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon v2.x
order: 36
permalink: /docs-2/codeql/

---

{% include breadcrumb.html %}
# GitHub Actions

[GitHub Actions](https://docs.github.com/en/actions/reference) are used to test, build and deploy Threat Dragon.
These actions live in the `.github/workflows` directory.

## CodeQL

[CodeQL](https://securitylab.github.com/tools/codeql/) is a static analysis scanner provided by GitHub.
This tool is a Static Analysis Security Tool (SAST) that Threat Dragon uses as an additional measure to identify vulnerabilities.
This is another check that is run against pull requests going into the main branch.
