---

title: Webapp github access
layout: col-document
tags: threatdragon
document: Threat Dragon version 2.0
permalink: /docs-2/install-environment/

---

{% include breadcrumb.html %}

## [OWASP](https://www.owasp.org) Threat Dragon

### Create A GitHub OAuth Application

This web application uses GitHub OAuth applications as the authentication mechanism.

To create a GitHub OAuth Application:

1. Log into your GitHub account, go to `Settings -> 'Developer settings' -> 'OAuth Apps' -> 'New OAuth App'`
2. Fill out the form with the following:
    1. **Application name**: A unique identifier for the application.
        This is not critical, we suggest something like 'Threat Dragon'
    2. **Homepage URL**: For local development, use `http://localhost:8080`
        If you configure Threat Dragon to listen on another port, use that port here instead of 8080
    3. **Application description**: A description for your OAuth app.
        This is not critical, we suggest something like 'Threat Dragon for local development'
    4. **Authorization callback URL**: `http://localhost:3000/api/oauth/return`
        If you configure Threat Dragon's server away from the default port 3000,
        be sure to use that port for the auth callback url
3. Register the application, an [example screenshot](#github-oauth-app-screenshot) is at the bottom of this document
4. Create a client_secret
5. Note the values for Client ID and Client Secret. **Save these somewhere safe**
    - Client ID will look similar to `01234567890123456789`
    - Client Secret will look similar to `0123456789abcdef0123456789abcdef01234567`
    - Treat these values like you would a password.
        If these values get out, someone could gain full access to your GitHub account

___

### Github OAuth App Screenshot

Example screenshot of registering a new OAuth application:

![Register new OAuth application]({{ '/docs-2/assets/images/register-new-OAuth-application.png' | relative_url }})
