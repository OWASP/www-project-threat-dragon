---

title: Introduction
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/introduction/

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

![cupcake logo](/assets/images/cupcake-128x128.png){: .image-right }

[Threat Dragon][td] is an open-source threat modelling tool from [OWASP][owasp].
Threat Dragon provides an environment to create threat models as
data-flow diagrams, along with associated threats and remediations.
The threats threats can be categorized using STRIDE, [LINDDUN][linddun],
CIA, DIE and [PLOT4ai][plot4ai].

Threat Dragon can be run as a containerized web application or as a desktop application.

The web application can store threat model files on the local file system; in addition access can be configured for :

- GitHub
- Bitbucket
- GitLab
- Github Enterprise

The desktop application saves the threat model files locally
with installers provided for MacOS, Windows and Linux.

Threat Dragon seeks to provide:

- Simplicity - you can install and start using Threat Dragon very quickly
- Flexibility - the diagramming and threat entry allows many types of threat to be described
- Accessibility - different types of teams can benefit from Threat Dragon's simplicity and flexibility

You can find the source code for Threat Dragon on [GitHub][repo],
where you can also ask for changes or report any issues.

----

Threat Dragon: _making threat modeling less threatening_

[linddun]: https://www.linddun.org/
[owasp]: https://www.owasp.org
[plot4ai]: https://plot4.ai/
[repo]: https://github.com/OWASP/threat-dragon
[td]: http://owasp.org/www-project-threat-dragon
