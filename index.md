---

layout: col-sidebar
title: OWASP Threat Dragon
tags: threatdragon
project: true
level: 3.5
type: tool
pitch: OWASP Threat Dragon is a threat modeling tool for both developers and defenders alike. Run it as a local application or as a web application.

---

<style type="text/css">
.image-right {
  display: block;
  margin-left: auto;
  margin-right: auto;
  float: right;
}
</style>

![cupcake logo](assets/images/cupcake-256x256.png){: .image-right }

## What is Threat Dragon?

OWASP Threat Dragon is a modeling tool used to create threat model diagrams as part of a secure development lifecycle.
It can be used to record possible threats and decide on their mitigations, as well as giving a visual indication
of the threat model components and threat surfaces.
Threat Dragon runs either as a web application or as a desktop application.

Threat Dragon supports STRIDE / [LINDDUN](https://linddun.org/) / CIA / DIE / [PLOT4ai](https://plot4.ai/),
provides modeling diagrams and implements a rule engine to auto-generate threats and their mitigations.

This project has [OWASP Production status][project] and follows the values and principles
of the [threat modeling manifesto][manifesto].

### Resources

Use the [version 2][docs-2] documentation to get started,
along with the recording of Mike Goodwin giving a [lightning demo][demo]
during the OWASP Open Security Summit in June 2020.
The [version 1.x][docs-1] are available if you are using legacy versions of Threat Dragon.

An [introduction](https://www.youtube.com/watch?v=hUOAoc6QGJo) to Threat Dragon is provided by
the [OWASP Spotlight](https://www.youtube.com/playlist?list=PLUKo5k_oSrfOTl27gUmk2o-NBKvkTGw0T) series,
and the [Threat Modeling Gamification](https://www.youtube.com/watch?v=u2tmLrwv-nc) seminar by Vlad Styran
shows how using Threat Dragon can make threat modeling fun.

There are a couple of OWASP community pages that give overviews on Threat Modeling and how to get started:
[Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
and [Threat Modeling Process](https://owasp.org/www-community/Threat_Modeling_Process).

### Contact

The easiest way to get in contact with the Threat Dragon community is
by emailing the [OWASP google group](mailto:threat-dragon-project@owasp.org).
The OWASP Slack channel [#project-threat-dragon][td-slack] is a good source of information,
although you may [need to subscribe][subscribe] first.

### Related OWASP projects

* [pytm (Pythonic Threat Modeling)][pytm]
* [Threat Modeling Cheat Sheet][tmcs]
* [Threat Modeling Project][tmproject]
* [Threat Model Library][tm-library]

----

Threat Dragon: _making threat modeling less threatening_

[demo]: https://youtu.be/n6JGcZGFq5o
[docs-1]: https://threatdragon.github.io/
[docs-2]: https://www.threatdragon.com/docs/
[manifesto]: https://www.threatmodelingmanifesto.org/
[project]: https://owasp.org/www-project-threat-dragon/
[pytm]: https://owasp.org/www-project-pytm/
[subscribe]: https://owasp.org/slack/invite
[td-slack]: https://owasp.slack.com/messages/CURE8PQ68
[tmcs]: https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html
[tmproject]: https://owasp.org/www-project-threat-modeling/
[tm-library]: https://github.com/OWASP/www-project-threat-model-library
