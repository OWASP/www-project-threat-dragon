---

title: GitLab repo testing
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/gitlab-repo/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

### GitLab repository access

Most of steps are the same as the GitHub Guide, but there are several parts different:

1. Web App GitLab Access
2. Environment variables

#### Web App GitLab Access

It's recommended to follow the [gitlab official guide](https://docs.gitlab.com/ee/integration/oauth_provider.html)
to set up the OAuth Application.

The recommended configs are like bellow:

- Redirect URI: `{BaseURL of your Threat Dragon Instance}/api/oauth/return`
- Scopes: Check `read_user read_repository write_repository profile read_api api`

For other options like `Trusted`, you could decide it by yourself.

After finishing the application, you will get `Application ID` and `Application Secret`,
they will be useful in the next part.

#### Example Environment variables

To help your threat dragon instance to support GitLab access, you have to set the environment variables like bellow

```bash
GITLAB_CLIENT_ID=0000000000000000000000000000000
GITLAB_CLIENT_SECRET=gloas-0000000000000000000000000000000
GITLAB_SCOPE=read_user read_repository write_repository profile read_api api
GITLAB_REDIRECT_URI=http://threat-dragon-instance/api/oauth/return
GITLAB_HOST=http://gitlab-instance
```

- GITLAB_CLIENT_ID: the `Application ID` you got from Gitlab
- GITLAB_CLIENT_SECRET: the `Application Secret` you got from Gitlab
- GITLAB_SCOPE: the functionalities you allow the threat dragon to use
- GITLAB_REDIRECT_URI: set it like this pattern ``{BaseURL of your Threat Dragon Instance}/api/oauth/return``
- GITLAB_HOST: it is the BaseURL of your GitLab Instance, if you're using official GitLab instance,
it remove this variable or set it to `https://gitlab.com/`

#### The End

Now you have successfully configured the GitLab Access for your Threat Dragon instance,
for anything not mentioned in this guide, you can check [the Guide of GitHub one](/docs-2/github-repo/)
