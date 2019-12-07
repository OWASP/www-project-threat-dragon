---

layout: col-sidebar
title: OWASP threat dragon
tags: example-tag
level: 0
type: tool

auto-migrated: 1
---

This is an example of a Project or Chapter Page.
# Main

<div style="width:100%;height:160px;border:0,margin:0;overflow: hidden;">

![OWASP_Project_Header.jpg](OWASP_Project_Header.jpg
"OWASP_Project_Header.jpg")

</div>

<table>
<tbody>
<tr class="odd">
<td><h2 id="owasp_threat_dragon_project">OWASP Threat Dragon Project</h2>
<p>An online threat modelling web application including system diagramming and a rule engine to auto-generate threats/mitigations. The focus will be on great UX a powerful rule engine and alignment with other development lifecycle tools.</p>
<p>An online threat modelling web application including system diagramming and a rule engine to auto-generate threats/mitigations. The focus will be on great UX a powerful rule engine and alignment with other development lifecycle tools.</p>
<h2 id="description">Description</h2>
<h2 id="description">Description</h2>
<p>Threat modelling is widely regarded as a powerful way to build security into the design of applications early in the development lifecycle. At its best, it is especially good for</p>
<p>Threat modelling is widely regarded as a powerful way to build security into the design of applications early in the development lifecycle. At its best, it is especially good for</p>
<ul>
<ul>
<li>Ensuring defence-in-depth</li>
<li>Ensuring defence-in-depth</li>
<li>Establishing consistent security design patterns across an application</li>
<li>Establishing consistent security design patterns across an application</li>
<li>Flushing out security requirements and user stories</li>
<li>Flushing out security requirements and user stories</li>
</ul>
</ul>
<p>However, effective adoption by organisations can be difficult. Reasons for this include:</p>
<p>However, effective adoption by organisations can be difficult. Reasons for this include:</p>
<ul>
<ul>
<li>There are no cross-platform, free tools (that I am aware of)</li>
<li>There are no cross-platform, free tools (that I am aware of)</li>
<li>The usability of existing tools is not great - productivity for the team is therefore poor, especially in the early stages of adoption</li>
<li>The usability of existing tools is not great - productivity for the team is therefore poor, especially in the early stages of adoption</li>
<li>The learning curve for teams is steep - threat modelling often ends up being left to a small "expert" subset of a team and ignores the valuable perspectives from the wider team</li>
<li>The learning curve for teams is steep - threat modelling often ends up being left to a small "expert" subset of a team and ignores the valuable perspectives from the wider team</li>
<li>Integration with other development lifecycle tools (e.g. issue tracking tools) is poor - leading to models being ignored</li>
<li>Integration with other development lifecycle tools (e.g. issue tracking tools) is poor - leading to models being ignored</li>
</ul>
</ul>
<p>OWASP Threat Dragon will address this by providing a free, open-source, threat modelling web application for teams implementing the STRIDE approach. The key areas of focus for the tool will be:</p>
<p>OWASP Threat Dragon will address this by providing a free, open-source, threat modelling web application for teams implementing the STRIDE approach. The key areas of focus for the tool will be:</p>
<ul>
<ul>
<li><strong>Great UX</strong> - using Threat Dragon should be simple, engaging and fun</li>
<li><strong>Great UX</strong> - using Threat Dragon should be simple, engaging and fun</li>
<li><strong>A powerful threat/mitigation rule engine</strong> - this will lower the barrier to entry for teams and allow non-specialists to contribute</li>
<li><strong>A powerful threat/mitigation rule engine</strong> - this will lower the barrier to entry for teams and allow non-specialists to contribute</li>
<li><strong>Integration points with other development lifecycle tools</strong> - this will ensure that models slot easily into the development lifecycle and remain relevant as the project evolves</li>
<li><strong>Integration points with other development lifecycle tools</strong> - this will ensure that models slot easily into the development lifecycle and remain relevant as the project evolves</li>
</ul>
</ul>
<h2 id="licensing">Licensing</h2>
<h2 id="licensing">Licensing</h2>
<p>This program is free software: you can redistribute it and/or modify it under the terms of the <a href="http://www.apache.org/licenses/LICENSE-2.0">Apache 2.0 License</a></p></td>
<p>This program is free software: you can redistribute it and/or modify it under the terms of the <a href="http://www.apache.org/licenses/LICENSE-2.0">Apache 2.0 License</a></p></td>
<p>The source code for the project can be found here:</p>
<p><a href="https://github.com/mike-goodwin/owasp-threat-dragon">https://github.com/mike-goodwin/owasp-threat-dragon</a></p>
<p>You can click here to see a working prototype:</p>
<p><a href="https://threatdragon.org">https://threatdragon.org</a></p>
<p>And (draft) end-user documentation can be found here:</p>
<p><a href="http://docs.threatdragon.org">http://docs.threatdragon.org</a></p>
<h2 id="project_leader">Project Leader</h2>
<p><a href="mailto:mike.goodwin@owasp.org">Mike Goodwin</a></p>
<h2 id="related_projects">Related Projects</h2>
<h2 id="classifications">Classifications</h2>
<table>
<tbody>
<tr class="odd">
<img src="Project_Type_Files_TOOL.jpg" title="Project_Type_Files_TOOL.jpg" alt="Project_Type_Files_TOOL.jpg" /><figcaption>Project_Type_Files_TOOL.jpg</figcaption>
</figure></td>
</tr>
<tr class="even">
<img src="Owasp-incubator-trans-85.png" title="Owasp-incubator-trans-85.png" alt="Owasp-incubator-trans-85.png" /><figcaption>Owasp-incubator-trans-85.png</figcaption>
</figure></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

# FAQs

**Q1:** Hold on...isn't this the same as [Mozilla's
SeaSponge](https://github.com/mozilla/seasponge)?

**A1:** As I was working on prototyping this, mostly as a way of getting
myself properly up to speed with javascript, I found out about SeaSponge
via the OWASP leaders mailing list. SeaSponge has a lot in common with
this project and I based my implementation of the threat model file
download feature on theirs. Maybe they could be merged in the future?
Who knows?

# Acknowledgements

## Contributors

[Mike Goodwin](mailto:mike.goodwin@owasp.org)

# Road Map and Getting Involved

## Roadmap

**Vision for the project:**

The overall vision for the project is to implement a tool that removes
as many barriers as possible for organisations wanting to embed threat
modelling into their development lifecycle. Barriers I have seen are:

  - Lack of cross platform tooling: Tool needs to be x-platform
  - Poor UX in existing tools, productivity is poor: Great UX is a must
  - Steep learning curve for adopting teams: Tool to build in expert
    knowledge to help the team get started
  - Models are ignored: Integration with other lifecycle tools is key

**Initial high level plan:**

Milestone 1: Alpha release - Basic threat modelling experience

  - Architecture review of the existing prototype with refinement/change
    where required - **complete: Confirmed JointJs works fine, Storage
    model changed and addition of Electon based desktop variant. TBC
    replacement for Nools rule engine, since it is no longer maintained,
    shift from Grunt/Bower to NPM/Browserify**
  - Secure design review and implementation of findings
  - Development of tests (unit and manual) - **complete: [Codecov
    report](https://codecov.io/github/mike-goodwin/owasp-threat-dragon?branch=master)**
  - Draft end user documentation - **complete: [GitHub
    pages](http://mike-goodwin.github.io/owasp-threat-dragon/)**
  - "Publicity drive" to sign up alpha/beta users and generate feedback

Milestone 2: Beta release - Threat/mitigation rule engine

  - Refinement of UX based on feedback from the alpha release
  - (Some) feature enhancements based on feedback from the alpha release
  - Implementation of a rule engine for generation of
    threats/mitigations
  - Updated tests and end-user documentation

Milestone 3: Release 1

  - Key refinements, bug fixes and new features based on feedback from
    the beta release
  - Complete end user documentation
  - Penetration test

Milestone 4 - Dev lifecycle integration

  - Detailed scope to be defined, but in general the vision is to
    support hooks into issue tracking and requirements management tool
    so that threats/mitigations can be tracked through to implementation
    and test

**Timeframes**

This is hard to estimate as it could change a lot if there were other
developers involved. Based on my current velocity with just me, I would
say release 1 could be complete in 1 year (optimistically).

**Technology**

The technical architecture is javascript from top to bottom. In the
client the key libraries are Angular for the MVC architecture and
JointJS for the diagramming. JointJS has a log of great features, but is
not a perfect fit for Angular. This needs a review. In the prototype,
all storage is done on the client using browser local storage.

Following an architecture review the following key changes were made:

  - A new Electron based, installable desktop variant was introduced
    using the local file system for model storage
  - The web variant was changed to use GitHub for model storage - other
    source control systems will follow (e.g. BitBucket)
  - Seperation of common code into a new NPM package, shared between the
    web and desktop variants
  - The Nools rule engine will be replaced since it is no longer
    maintained

**Challenges**

  - Getting enough usage of the alpha and beta to get the UX and rule
    engine right
  - Finding a sustainable way to host it, especially to support deeper
    GitHub/BitBucket/Etc. integration

## Getting Involved

### Alpha testers

Great user experience is one of the key goals for the project and to get
that right it needs some users\! If you would like to try the tool out,
that would be great. A working prototype can be found at:

<https://threatdragon.org/>

The desktop variant (for Windows and OSX) can be downloaded from:

<https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases>

To help you get started, take a look at the (draft) docs:

[<http://docs.threatdragon.org/>](http://mike-goodwin.github.io/owasp-threat-dragon/)

If you are still having problems, let me know and I will be pleased to
help (mike.goodwin@owasp.org). All feedback is *very* welcome. Either
email me or put an issue on GitHub

<https://github.com/mike-goodwin/owasp-threat-dragon/issues>

### Coding

Coding help of any kind is always welcome. The project builds easily
(let me know if you have any problems) so getting up and running should
be simple.

### Threat rule engine

If you are not into javascript, you can still help\! We need to build a
powerful threat generation rule engine to replace the stubbed one that
is in place for the prototype. If you can contribute in this area by
defining rule, that would be great.

# Minimum Viable Product

1\) Application source code for a threat modeling tool

2\) End user documentation for the tool

3\) An online hosted version of the tool

4\) An installable, cross-platform desktop version of the tool

__NOTOC__ <headertabs></headertabs>

[Category:OWASP Project](Category:OWASP_Project "wikilink")
[Category:OWASP_Builders](Category:OWASP_Builders "wikilink")
[Category:OWASP_Defenders](Category:OWASP_Defenders "wikilink")
[Category:OWASP_Tool](Category:OWASP_Tool "wikilink")
