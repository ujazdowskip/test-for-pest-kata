# Context

Each microservice will need its own data storage system. Some data sets might get large and might require
partitioning. We need to ensure that our data storage system is:
- scalable
- reliable
- industry standard

The biggest data sets will be:
- customers
- test results
  - though we could clean this regularly

# Decision

We will use PostgreSQL as our primary data storage system. 

- it is battle tested and has strong backing from the industry.
- it's very flexible in terms of data modeling and offers both SQL and NoSQL capabilities. 
- in cloud providers this will be used as a managed service
- on-premises deployments we will have to provision it 

# Context

Platform will need to provide database for each microservice. We need to ensure that our database system is:
- observable
- secure
- regularly backed up

