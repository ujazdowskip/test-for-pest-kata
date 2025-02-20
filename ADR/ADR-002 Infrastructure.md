# Context

- The system is planned to be used by government with possibility to export to other countries. It is unreasonable to assume that all countries will accept the same cloud provider. Some might even prefer to use on premise national data center.
- The system must be scalable but
	- load patterns are predictable (mostly used during working hours)
	- scaling the system does not need to be instant
		- even global issue like pandemics will give use days (or even weeks to scale)

# Decision

With this in mind we propose:
- design the whole system to be operated in the kubernetes cluster
- use open source cloud native components (databases, queues, etc)
 
# Consequences

- the environment must support running kubernetes cluster
- all components will be deployed on the kubernetes and thus must be packed as a container
- scaling
	- scaling kubernetes horizontally is solved problem and is possible by adding new nodes
	- scaling particular components is also possible inside the cluster


