---

title: Configure GitLab access
layout: col-document
tags: threatdragon
document: OWASP Threat Dragon version 2.4
permalink: /docs-2/gitlab-repo/

---

{% include breadcrumb.html %}

[Threat Dragon](http://owasp.org/www-project-threat-dragon) can be run as a web application and
if GitLab repository access is required then some configuration is needed
for the necessary environment variables.
The GitLab specific environment variables are listed at the [end of this page](#gitlab-environment-variables),
other variables are described in
the [installation instructions]({{ '/docs-2/install-environment/#environment-variables-reference' | relative_url }}).

## GitLab repository access

Most of steps are the same as the [GitHub configuration]({{ '/docs-2/github-repo/' | relative_url }})
but there are some parts that are different:

1. Web App GitLab Access
2. Environment variables

### 1. Web App GitLab Access

It's recommended to follow the [gitlab official guide](https://docs.gitlab.com/ee/integration/oauth_provider.html)
to set up the OAuth Application.

The recommended configuration is similar to below:

- Redirect URI: `{BaseURL of your Threat Dragon Instance}/api/oauth/return`
- Scopes: Check `read_user read_repository write_repository profile read_api api`

Other options like `Trusted` are according to personal preference.

After finishing the OAuth Application you will get `Application ID` and `Application Secret`,
which are used for the environment variables.

### 2. Environment variables

To help your threat dragon instance to support GitLab access, you have to set the environment variables like below

```bash
GITLAB_CLIENT_ID=00112233445566778899aabbccddeeff
GITLAB_CLIENT_SECRET=gloas-deadbeef0123456789abcdefdeadbeef
GITLAB_SCOPE=read_user read_repository write_repository profile read_api api
GITLAB_REDIRECT_URI=http://threat-dragon-instance/api/oauth/return
GITLAB_HOST=http://gitlab-instance
```

where:

- GITLAB_CLIENT_ID: the `Application ID` you got from Gitlab
- GITLAB_CLIENT_SECRET: the `Application Secret` you got from Gitlab
- GITLAB_SCOPE: the functionalities you allow the threat dragon to use
- GITLAB_REDIRECT_URI: set it like this pattern ``{BaseURL of your Threat Dragon Instance}/api/oauth/return``
- GITLAB_HOST: the BaseURL of your GitLab Instance, if you're using official GitLab instance,
  remove this variable or set it to `https://gitlab.com/`

Now you have successfully configured the GitLab access for your Threat Dragon instance,
for anything not mentioned in this guide check [the GitHub configuration]({{ '/docs-2/github-repo/' | relative_url }}) guide.

### GitLab environment variables

| GitLab specifics | Description | Default |
| --- | --- | --- |
| `GITLAB_CLIENT_ID` | The 'Application ID' provided by the Gitlab OAuth app used for authentication | |
| `GITLAB_CLIENT_SECRET` | The 'Application Secret' generated by the Gitlab OAuth authentication app | |
| `GITLAB_SCOPE` | The scope provided to the Gitlab OAuth app, for example 'api' provides maximum scope | `read_user read_repository` |
| `GITLAB_HOST` | The URL of Gitlab server, for example `https://gitlab.com/` | |
| `GITLAB_REDIRECT_URI` | The redirect provided to the Gitlab OAuth app, for example `<URL of Threat Dragon app>/api/oauth/return` | |
| `GITLAB_REPO_ROOT_DIRECTORY` | Optional path where saved models are stored in a Gitlab repo | |

----

Threat Dragon: _making threat modeling less threatening_
