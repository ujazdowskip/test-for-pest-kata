# Context

Our system needs strong observability features. It's crucial that we could monitor and trace our system. We need to be
able to:
- inspect logs from all services
- inspect metrics from the cluster
- trace requests between services
- trace requests from the client to the services
- create custom metrics
- visualize all of the above

# Decision

We will use OpenTelemetry as our observability framework.

- it is vendor neutral
- has strong backing from the industry

We will use Grafana stack as our observability stack.

- Prometheus - metrics database
- Loki - logs database
- Tempo - traces database
- Grafana - visualization

# Consequences

1. Each service will need to have OpenTelemetry agent (TODO: clarify what it means)
2. Services will need to be instrumented with OpenTelemetry SDKs
3. We will need to provision Grafana stack
4. We will need to integrate platform components (e.g. Istio)
