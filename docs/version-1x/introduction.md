---

title: Home
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon version 1.6.1
order: 1
permalink: /docs-1/introduction/

---

{% include breadcrumb.html %}

<style type="text/css">
.image-left {
  display: block;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
.image-right {
  display: block;
  margin-left: auto;
  margin-right: auto;
  float: right;
}
</style>

## [OWASP](https://www.owasp.org) Threat Dragon

![Cupcake Image](/assets/images/threatdragonx256.png){: .image-left }

Threat Dragon is an open-source threat modelling tool from OWASP.
It is used both as a [web application](/docs-1/install-webapp/)
and as a [desktop application](/docs-1/install-desktop/) installed for MacOS, Windows and Linux.

The desktop application saves your threat models on your local file system,
and the online version stores its files in GitHub.
This means that to use web application you have to sign in with a GitHub account and give it write access to your public repos.
Other than that, the user experience is currently almost identical between the web and desktop variants.
In the future, there should be deeper integration with GitHub and other code repositories.

You can find the source code for Threat Dragon on GitHub
[OWASP][owasp] / [threat-dragon][dragon] where you can also ask for changes or report any issues.
Threat Dragon is an OWASP Lab project but there will still be bugs - if you find one then please [raise a bug report][bug].

![OWASP logo](/assets/images/owasp.png){: .image-right }

[bug]: https://github.com/OWASP/threat-dragon/issues/new?assignees=&labels=bug&template=bug_report.md&title=
[dragon]: https://github.com/OWASP/threat-dragon)
[owasp]: https://github.com/owasp
