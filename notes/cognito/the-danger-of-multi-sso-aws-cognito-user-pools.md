# The Danger of Multi-SSO AWS Cognito User Pools

**Source:** https://blog.doyensec.com/2026/05/05/cloudsectidbits-masso-cognito-sso
**Date:** 2026-09-17
**Tags:** cognito, sso, identity

In the multi-tenant Cognito pattern (one User Pool, many tenants, each bringing its own external OIDC/SAML IdP), Doyensec map the Lambda trigger execution order for first federated sign-in versus subsequent sign-ins and find they share only the `TokenGeneration` trigger. Any identity constraint (domain allowlisting, tenant restriction, JIT provisioning checks) implemented in only one of the two chains can be bypassed by forcing the other path, and once a malicious external IdP gets a user landed in the pool via `PreSignup`, there is no automatic rollback.
