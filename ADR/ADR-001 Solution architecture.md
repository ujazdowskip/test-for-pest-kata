## Context

- we have couple domains that are isolated problems spaces
	- handling Customer data
	- configuring system (adding diseases)
	- processing Test Results
- components might have different scaling patterns
	- some should be available 24/7others could be scaled down (or even shut down) for non working hours (days)
	- some will experience heavy load and other will be used not so often
     
## Decision

With this in mind we propose microservices architecture.
- each component will be a deployment unit
	- although might contain multiple deployable artifacts (e.g. frontend + backend)
- each component could be scaled accordingly
 
## Consequences

Deployment platform should support
- defining deployment units
- scaling components according to the needs
- a component should have one team that is responsible
- components should not share databases
- communication between microservices should be done via network protocols
	- call and response
	- or event based

