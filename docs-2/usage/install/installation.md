---

title: Installation
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/install-options/

---

{% include breadcrumb.html %}

[Threat Dragon](http://owasp.org/www-project-threat-dragon) comes in two variants,
a desktop application and a web application.

### Web application

The web application can be run locally or from a server, and is downloaded from the [Threat Dragon repo][releases].
There is some configuration necessary, so see the
[install instructions]({{ '/docs-2/install-webapp/' | relative_url }}) for configuring the application.

The web application is also provided in a Docker image, and this is provided by [dockerhub][docker].
Follow the Docker [instructions]({{ '/docs-2/install-docker/' | relative_url }})
to download, configure and run a Docker container.

### Desktop application

Various installers can be downloaded from the Threat Dragon [releases area][releases]:

* Windows (64 bit) executable / installer
* MacOS installers (.dmg) for X86 and Apple silicon
* Linux snap, AppImage, debian and rpm installers

See the desktop [install instructions]({{ '/docs-2/install-desktop/' | relative_url }}).

----

Threat Dragon: _making threat modeling less threatening_

[docker]: https://hub.docker.com/r/owasp/threat-dragon/tags
[releases]: https://github.com/OWASP/threat-dragon/releases
