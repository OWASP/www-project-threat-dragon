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

The Threat Dragon web application uses [GitHub OAuth Applications][githuboauth] as the mechanism to access
the GitHub API of the users repositories.
A GitHub OAuth Application needs to be created for use by the web app to access github,
and the GitHub OAuth Application provides the values `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`.

To create a GitHub OAuth Application you need to know the port number and domain of the Threat Dragon application.
Here port number 8080 is being used along with 'localhost'.

1. Log into your GitHub account and navigate to 'Settings' -> 'Developer settings' -> 'OAuth Apps' -> 'New OAuth App'
2. Fill out the form with the following suggested content:
    1. Application name: a unique identifier for the application.
        This is not critical, something like 'Threat Dragon tests' will do
    2. Homepage URL: local development so use `http://localhost:8080/#`
    3. Application description: for example 'Threat Dragon testing for local development'
    4. Authorization callback URL: for localhost and port 8080 use `http://localhost:8080/api/oauth/return`
3. Proceed by agreeing to Register the application
4. Initially there will be no Client secret; create a client secret via the 'Generate a new client secret' button
5. Note the values for both the Client ID and the Client Secret, **save these somewhere safe**
    1. Client ID will be 20 hexadecimal (10 byte) characters, for example `deadbeef0123456789aa`
    2. Client Secret will be 40 hexadecimal characters, for example `deadbeef0123456789abcdef01234567deadbeef`
    3. Treat these values with the same security as a password; they provide access to your GitHub account

The Threat Dragon server can now be supplied with the values:

- `GITHUB_CLIENT_ID='deadbeef0123456789aa'`
- `GITHUB_CLIENT_SECRET='deadbeef0123456789abcdef01234567deadbeef'`

Example of registering a new OAuth application:

![New GitHub OAuth Application]({{ '/docs-2/assets/images/github-oauth-app.png' | relative_url }})

[githuboauth]: https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app
