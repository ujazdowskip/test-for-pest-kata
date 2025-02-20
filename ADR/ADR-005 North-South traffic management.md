# Context

We will expose some endpoints to public traffic. Our system will use auth server to authenticate front end applications that will send tokens.

We need API gateway that will provide:
- resolving auth tokens against our auth server
- provide common functionalities like rate limiting, logging

# Decision

We will use istio Gateway for controlling our North-South traffic.

## Alternative

Use kubernetes Gateway API specification for provisioning cloud provider specific gateway.
- while the core of this specification is finished some parts are still in progress
  - example would be authentication https://gateway-api.sigs.k8s.io/geps/gep-1494/?h=

# Consequences

- we need to configure istio and provision istio for our cluster
- all ingress traffic will be controlled by istio
