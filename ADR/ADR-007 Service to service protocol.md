# Context

Our microservices will need to exchange some data between each other. This might include:
- customer data
- appointment data
- test results

We need robust and reliable way to exchange this data.

# Decision

We will use HTTP/REST as our communication protocol. 

- it's simple and well known
- it's easy to implement
- there are many libraries that can help us with that
- it's easy to debug
- our system does not have high throughput requirements (see [calculations](../Scale.md))

## Alternatives

We could use gRPC, but it's more complex, and our system does not have high throughput requirements.

# Consequences

1. We will use HTTP/REST in our applications
2. Each microservice should use OpenAPI to expose documentation
