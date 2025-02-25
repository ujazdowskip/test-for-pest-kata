# Context 

Our system will be composed of multiple microservices. Despite the fact that each microservice will encapsulate its own
business domain there will be situations when one microservice will need to communicate with another. This communication
will happen over a network inside our cluster. We need to ensure that this communication is:
- secure
- reliable
- observable

Additionally, we need to ensure that services can be easily discovered.

# Decision

1. We will use Istio to create a reliable and secure service mesh.
2. We will use Istio in sidecar mode

Security:
- Istio can provide Mutual TLS (mTLS) between services. We will use this to implement Zero Trust approach.
- Istio can provide authorization policies that can be used to control access to services.

Reliability:
- Istio can provide circuit breaking, retries and timeouts. This will help to make our services more resilient.

Observability:
- Istio will help observe traffic inside our mesh. It can be also integrated with 3rd party observability tools

# Consequences

1. We will need to configure istio and provision istio for our cluster
2. All traffic between services will be controlled by istio
