# Pimcore Single Sign-on

This bundle provides single-sign on support for Pimcore backend login. This allows to maintain user credentials and roles on external authenticatin providers.

Delegate user management to an authentication provider has a lot of advantages:

- user only has to remember one password for all used services
- encryption and security is expected to be higher on those authentication providers as their whole business model highly depends on it
- administration has a single system where they can create users - so nobody has to create Pimcore accounts manually
- administration has a single system to disable users - when an employee leaves a company, you can disable all logins with a single click

Currently, the bundle supports OpenID, SAML and LDAP authentication providers.

OpenID is supported by a [wide range of applications](https://openid.net/certification/) like

- Microsoft Azure Active Directory / Entra ID
- Auth0
- Google
- Okta
- Keycloak
- and others

## Studio UI

The bundle is fully compatible with new Studio UI

## How to get the plugin

You can buy this plugin in the [Blackbit Shop](https://shop.blackbit.com/pimcore-single-sign-on) or write an email to [info@blackbit.de](mailto:info@blackbit.de).

## Configuration

- [Classic Pimcore UI](configuration.md)
- [Studio UI](studio-configuration.md)