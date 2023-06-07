---

title: Utilities
layout: col-document
tags: threatdragon
document: Threat Dragon version 1.6.1
permalink: /docs-1/utilities/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

### Utilities

Threat Dragon has a growing collection of utilities and scripts which can be used to
convert file formats, interface to bug tracking, and so on.
If you have scripts of your own that you would like to contribute to the Threat Dragon
community then this would be most  welcome, see the [contributing guide]({{ '/docs-1/contribute/' | relative_url }}).

### Conversion from Microsoft Threat Modeling Tool

The [TMT2TD python script](https://raw.githubusercontent.com/owasp/threat-dragon/main/utils/TMT2TD/TMT2TD.py)
converts an Microsoft Threat Modeling Tool file `.tm7` file to a Threat Dragon `.json` file.

Run the script using python and select the TM7 file, the script will then output a
file with the same name but using a `.json` extension.
Included [with the script](https://github.com/OWASP/threat-dragon/tree/main/utils/TMT2TD)
is an example TM7 file and the transpiled Threat Dragon file.

```text
threat-dragon$ python --version
Python 3.9.5
threat-dragon$ python tmt2td.py
```

### Integration Threat Modeling with Jira (ITMJ)

The [ITMJ project](https://github.com/OWASP/threat-dragon/tree/main/utils/threat-mvp)
aims to have a greater visibility of the possible threats
and a better tracking of the actions taken to mitigate them.

- TM data generated automatically within the backlog of each project.
- Dual sync between Threat Dragon and project management.

#### Prerequisite

- You need to install requests library for python: pip install requests
- You need to add credentials in config.ini file

#### Run the code

- To run the code: `python3 itmj.py [path threat dragon file] [key project] [epic project]`
- Example: `python3 itmj.py td_json/test1.json ITMJ ITMJ-2`
