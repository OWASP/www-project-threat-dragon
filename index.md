---

layout: col-sidebar
title: OWASP Threat Dragon
tags: threatdragon
project: true
level: 3
type: tool
pitch: OWASP Threat Dragon is a threat modeling tool; great for both developers and defenders alike. Use on your desktop or as a web application.

---

<style type="text/css">
.image-right {
  display: block;
  margin-left: auto;
  margin-right: auto;
  float: right;
}
</style>

![cupcake logo](/assets/images/cupcake-256x256.png){: .image-right }

## What is Threat Dragon?

OWASP Threat Dragon is a modeling tool used to create threat model diagrams as part of a secure development lifecycle.
Threat Dragon follows the values and principles of the [threat modeling manifesto][manifesto].
It can be used to record possible threats and decide on their mitigations, as well as giving a visual indication
of the threat model components and threat surfaces.
Threat Dragon runs either as a web application or as a desktop application.

Threat Dragon supports STRIDE / [LINDDUN](https://www.linddun.org/) / CIA / DIE / [PLOT4ai](https://plot4.ai/),
provides modeling diagrams and implements a rule engine to auto-generate threats and their mitigations.

### Resources

Use the [version 1][docs-1] or [version 2][docs-2] documentation to get started,
along with the recording of Mike Goodwin giving a [lightning demo][demo]
during the OWASP Open Security Summit in June 2020.

An [introduction](https://www.youtube.com/watch?v=hUOAoc6QGJo) to Threat Dragon is provided by
the [OWASP Spotlight](https://www.youtube.com/playlist?list=PLUKo5k_oSrfOTl27gUmk2o-NBKvkTGw0T) series,
and the [Threat Modeling Gamification](https://www.youtube.com/watch?v=u2tmLrwv-nc) seminar by Vlad Styran
shows how using Threat Dragon can make threat modeling fun.

There are a couple of OWASP community pages that give overviews on Threat Modeling and how to get started:
[Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
and [Threat Modeling Process](https://owasp.org/www-community/Threat_Modeling_Process).

The easiest way to get in contact with the Threat Dragon community is via the OWASP Slack
[#project-threat-dragon](https://owasp.slack.com/messages/CURE8PQ68) project channel,
you may need to [subscribe](https://owasp.org/slack/invite) first.

### Related Projects

* [OWASP pytm (Pythonic Threat Modeling)][pytm]
* [Threat Modeling OWASP Cheat Sheet][tmcs]
* [Threagile - Agile Threat Modeling][threagile], an (non-OWASP) open source project

----

Threat Dragon: _making threat modeling less threatening_

[demo]: https://youtu.be/n6JGcZGFq5o
[docs-1]: https://threatdragon.github.io/
[docs-2]: https://www.threatdragon.com/docs/
[manifesto]: https://www.threatmodelingmanifesto.org/
[pytm]: https://owasp.org/www-project-pytm/
[threagile]: https://threagile.io
[tmcs]: https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html
