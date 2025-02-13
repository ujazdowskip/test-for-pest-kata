## Context

The stakeholders strategic goal is to create easy to use system that encourages people to test themselves. We need to support a way that is known to many people and is easy to use.

## Decision

We will use web technologies to give all the actors access. Native mobile applications will not be used.
- modern devices and web technologies are mature enough to create what we need
- people will more likely to use online application rather than installing another native app
- our use case are simple enough and native applications is an overkill

# Consequences

- we will use modern web stack to create front end applications
- the apps must be fast because slow and unresponsive applications will be problematic for:
	- Customers - it will decrease a chance that people will use the system
	- Test Operators - it will destroy productivity and decrease number of tests we can carry out
