---

title: API
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.4
permalink: /docs-2/api/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

At present it there is a minimal application programming interface for
[Threat Dragon](http://owasp.org/www-project-threat-dragon) .
This API is used to access threat models stored by repository providers such as github, bitbucket or gitlab.

APIs protected by authorisation, including threat model Create, Read, Update (but no Delete):

| Path | Action | Description |
| ---- | ---- | ---- |
|      |      |      |
| `/api/logout` | POST | Logout from provider when already authorised |
| `/api/token/refresh` | POST | Refresh the access token |
| `/api/threatmodel/repos` | GET | List repositories for the authorised user |
| `/api/threatmodel/:organisation/:repo/branches` | GET | List branches for a given repository |
| `/api/threatmodel/:organisation/:repo/:branch/models` | GET | List models for a given branch and repository |
| `/api/threatmodel/:organisation/:repo/:branch/:model/data` | GET | Reads the threat model contents for a given model |
| `/api/threatmodel/:organisation/:repo/:branch/:model/create` | PUT | Create a new model in the branch and repository |
| `/api/threatmodel/:organisation/:repo/:branch/:model/update` | PUT | Update a model in the branch and repository |

APIs with no authorisation:

| Path | Action | Description |
| ---- | ---- | ---- |
| `/` | GET | Provides the Threat Dragon Single Page Application |
| `/healthz` | GET | Health check that provides server statistics such as uptime |
| `/api/login/:provider` | GET | Login to a repository provider|
| `/api/logout` | GET | Logout that will always succeed |
| `/api/oauth/return` | GET | OAuth return request |
| `/api/oauth/:provider` | GET | Provides access and refresh tokens if authorised |
| `/api/threatmodel/organization` | GET | Provides repository provider hostname |

Support for CI/CD pipelines is being worked on, and this API may include:

* project status
* pdf report output
* threat diagram provider (for embedding in other reports)
* unmitigated threat list
* mitigated threat list
* statistics
