# Context

Our system will need to serve static content. This content will include:
- front end applications
- domain specific files
  - test results
  - customer documentation
  - test operator documentation

# Decision

We will use S3 to store static content. We will use nginx to serve this content.

# Consequences

- we need our platform to support S3 compliant storage
  - described in [ADR-008 Object Storage](ADR-008%20Object%20Storage.md)
- we need to provision nginx to serve static content
