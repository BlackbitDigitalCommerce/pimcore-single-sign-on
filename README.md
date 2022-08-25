# Pimcore Single Sign-on

This bundle provides single-sign on support for Pimcore backend login. This allows to maintain user credentials and roles on an external auth provider. 

Currently the bundle supports OpenID and LDAP authentication providers. Support for SAML and OAuth2 will come soon.

OpenID is supported by a [wide range of applications](https://openid.net/certification/) like
- [Microsoft Azure Active Directory](https://docs.vmware.com/en/Single-Sign-On-for-VMware-Tanzu-Application-Service/1.14/sso/GUID-azure-oidc-config-azure.html)
- [Auth0](https://auth0.com/docs/authenticate/identity-providers/enterprise-identity-providers/oidc)
- [Google](https://developers.google.com/identity/protocols/oauth2/openid-connect)
- Okta
- and others

## Configuration

Configuration can be done directly in Pimcore backend (no need to edit YAML files):
![Auth provider configuration](config-menu.png)

You can add as many auth providers as you want (e.g. if your internal users use a different auth provider as your Pimcore agency).

You can also configure default roles for each authentication provider. Those rules will get applied to newly created users. If an existing user logs in the default roles will not get applied.

## Login

### Single sign on as an optional login method

For each authentication provider a new button will be added to Pimcore's login screen:
![Auth provider configuration](login-screen.png)

After the user clicks this button, he will get redirected to the authentication provider. There he can log in (or perhaps already is logged in). Afterwards he will get redirected to your Pimcore and logged in. Internally a usual Pimcore user will get created based on the information of the authentication provider (e.g. username, email, roles).

### Single sign on as default login method

You can configure one authentication provider to be the default one. When this is done and a not logged-in user accesses `https://your-pimcore.com/admin` he will automatically get redirected to the authentication provider to login there. Afterwards he will get sent back to Pimcore backend being logged in.