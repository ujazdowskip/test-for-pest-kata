# Context

Our system will need to exchange some events between services. This might include:
- appointment scheduled
- test result submitted

We need robust message broker that will be:
- allow to send messages between services
- support push based communication
- allow to easily implement fan-out pattern
- will support traffic that is below 1000 OP/s
  - see [calculations](../Scale.md)

# Decision

We will use RabbitMQ as our message broker.

- it supports various messaging patterns
- it is industry standard
- it can deliver needed throughput
  - https://aws.amazon.com/compare/the-difference-between-rabbitmq-and-kafka/

# Consequences

1. Platform will need to provide RabbitMQ
2. Applications will use RabbitMQ to send and receive messages


