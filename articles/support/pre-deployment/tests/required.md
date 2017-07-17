---
description: Fixes you must make to your Auth0 Client prior to production deployment
---

# Pre-Deployment Tests: Required Fixes

The following tests check to see if you've completed all requirements for successful deployment to Production.

::: note
See [How to Read Your Results Set](/support/pre-deployment-tests/how-to-run-test#How-to-Read-Your-Results-Set) for additional information on your testing output.
:::

| Test | Description |
| ---- | ----------- |
| [Allowed Callback Urls](tutorials/redirecting-users) Not Localhost | Validates the [Client Allowed Callback URLs do not point to localhost](${manage_url}/#/clients), 127.0.0.1, etc |
| Configure [Guardian SMS Provider](/multifactor-authentication/administrator/twilio-configuration) (Dependency: Guardian is Configured) | Ensures that [Twilio SMS is configured](${manage_url}/#/guardian) if you're using Guardian MFA |
| Configure Tenant Environment Tag | Ensures the [tenant environment tag is set](https://support.auth0.com/tenants/public) appropriately to Production, Staging or Development |
| [Email Provider](/email/providers) Configured | Verifies that the [custom email provider has been configured](${manage_url}/#/emails/provider) |
| [Social Connections](/connections/social/devkeys) Auth0 Dev Keys | Verifies that [Social Connections are not using the default Auth0 developer keys](${manage_url}/#/connections/social) |
| Support Email is Configured | Ensures the [Support Email is configured](${manage_url}/#/account) in Tenant Settings |
| Support URL is Configured | Ensures the [Support URL is configured](${manage_url}/#/account) in Tenant Settings |