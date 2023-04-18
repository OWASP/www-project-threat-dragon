---

title: Install desktop
layout: col-document
tags: threatdragon
author:
contributors:
document: Threat Dragon version 1.6.1
order: 6
permalink: /docs-1/install-desktop/

---

{% include breadcrumb.html %}
## [OWASP](https://www.owasp.org) Threat Dragon

[Threat Dragon](http://owasp.org/www-project-threat-dragon) comes in two variants, 
desktop application and web application.

## Desktop application install instructions
Installers can be downloaded from the [OWASP GitHub area](https://github.com/OWASP/threat-dragon/releases):

* Windows (64 bit) installer
* MacOS installer
* Linux snap, AppImage, debian and rpm installers

### Linux installer and AppImage
It is probably simpler to use the [AppImage](https://github.com/OWASP/threat-dragon/releases/) for most Linux platforms,
but packages for both Debian and Fedora Linux on AMD64 and X86-64bit platforms can also be downloaded from the
[github release area](https://github.com/OWASP/threat-dragon/releases/).

Alternatively a platform independent Snap image is available via the
[official snapcraft distribution](https://snapcraft.io/threat-dragon).

### MacOS installer
Download the **.dmg** MacOS installer from the
[github release area](https://github.com/OWASP/threat-dragon-desktop/releases/).
Open the download and drag 'OWASP Threat  Dragon' to the application directory. When the copy has
finished then Threat Dragon can be run from Apple Launchpad or using Finder -> Applications.

Threat Dragon is notarized by Apple, but if an error message pops up when running for the first time,
along the lines of 
_'“OWASP-Threat-Dragon” can’t be opened because Apple cannot check it for malicious software'_
then follow [this FAQ](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-apple-cannot-check-it-for-malicious-software-errors-after-installing-on-macos)
to resolve this.

There may be different error messages for older versions of Threat Dragon, in which case try
[this FAQ](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-developer-can-not-be-verified-errors-after-installing-on-macos)
for a solution.

If you decide to use the MacOS **.zip** file then be sure to
[read this FAQ first](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-permissions-failure-opening-mac-desktop-app-when-installing-from-the-zip-file).
If you run into problems then consider using the **.dmg** download instead.

### Windows installer
Download the Windows .exe NSIS installer from the
[github release area](https://github.com/OWASP/threat-dragon/releases/).
Run the installer and invoke the application from the shortcut.

Windows may warn you that this is an application downloaded from the internet and ask you if you want to keep it.
Assuming that you can trust the github download site, agree to keep the file and the installer will then run.

![Windows download warning]({{ '/docs-1/assets/images/win-download.png' | relative_url }})

Run the installer either from the file icon in your download area or from a command line:

```
.\OWASP-Threat-Dragon-Setup-1.6.1.exe /S /D=C:\Test
```

Uninstall using a similar command: `'C:\tmp\Uninstall OWASP-Threat-Dragon.exe'`.
Note the single quotes because there is a space in the uninstall command name.

### Command line using npm

For the latest versions of code between releases, `npm` can be used to install
and run Threat Dragon Desktop locally:

```
git clone https://github.com/owasp/threat-dragon
cd threat-dragon/td.desktop
npm install
npm run build
```

Then to run it:

`npm start`

There is a command line interface, run help to see what commands are available:

`npm run help`

For example to export a given threat model file to pdf :

`npm run pdf ./threat-model.json`
