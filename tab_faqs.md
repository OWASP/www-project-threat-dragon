---
title: Faqs
displaytext: FAQs
layout: null
tab: true
order: 3
tags: threatdragon
---

## FAQs
Q1: What browsers can be used for Threat Dragon?

A1: Threat Dragon has been tested on these browsers, but there are certainly more.


Platform | Browser | Tested
-------- | ------- | ------
Windows | Edge | Microsoft Edge 38 for Windows 10
Windows | IE | Internet Explorer 11 for Windows 10
Windows | Chrome | Windows 10
Windows | Firefox | Windows 10
Linux | Abrowser | Mozilla 68.0.2 for Trisquel / Gnu Linux trisquel 8.0
MacOS | Firefox | Firefox 73.0.1 for macOS version 10.15
MacOS | Safari | Safari 13.0.2 for macOS 10.15
MacOS | Chrome | Google Chrome 80.0 for macOS 10.15

Q2: Hold on...isn't this the same as Mozilla's [SeaSponge](https://github.com/mozilla/seasponge/blob/master/README.md)?

A2: As Mike was working on prototyping this, mostly as a way of getting himself properly up to speed with javascript,
he found out about SeaSponge via the OWASP leaders mailing list. SeaSponge has a lot in common with this project
and Mike based his implementation of the threat model file download feature on theirs. Maybe they could be merged in
the future? Who knows?

Q3: Why do the earlier releases come from Mike Goodwin's repo, not the OWASP repo?

A3: For more than 4 years Mike hosted Threat Dragon on his personal github area, and in mid-2020 he felt that the
time was right for it to migrate to the OWASP organisation github space. This was done through June and July 2020
and with version 1.3 (expected August 2020) the migration will be almost complete. The docs and demo pages are still
sourced from Mike's github space, which gives continuity to the origins of Threat Dragon.
