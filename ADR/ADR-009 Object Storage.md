# Context

Our system will need to store some file. This might include:
- test results
- customer documentation
- test operator documentation

We need robust storage system that will be:
- secure
- scalable
- industry standard

# Decision

We will use object storage that is S3 compliant. That does not specifically mean we will use AWS S3. Depending on the
deployment platform we might use:
- AWS S3 for AWS
- GCP Cloud Storage for GCP
- MinIO for environments that do not have S3 compliant storage

# Consequences

1. Deployment platform must support S3 compliant storage
2. We will use S3 API in our application

