## Driving characteristics

In order to find out the best approach we will list architecture characteristics that drive the solution.

### Usability

Main driving characteristic is usability for Customers. The goal of the Government is to encourage people to test for disease because prevention is best method for improving public health. In order to achieve this we need to make system usable to as many Customers as possible. 

We need to assume:
- not everyone has access to internet
- not everyone is proficient with using internet and/or computers
- some people prefer in person (or phone) contact
- some people are proficient with using internet and highly prefer this communication form

### Scalability

Not every part of the system have the same scaling patterns:
- some parts have predictable scaling patterns
	- will be used during workdays in defined time window
	- However after last pandemics Government requires that:
	- system needs to scale to much greater loads than usual business
	- system will be running in different time window (potentially 24/7)
	- system needs to be able to relatively quickly react to scaling up places where test can be carried out (airports, stations, hospitals, borders)
	- it's not required that this scaling will happen in matters of hours, preparing non digital infrastructure is a matter of days (or even weeks)
- other parts will need to be available 24/7
- some components will have moderate traffic (e.g. System service)
- others might experience much higher load
	- e.g. Customer service will store significant amount of data
	- e.g. Test Operator system might encounter significant OP/s
    
### Security

- System will be storing sensitive Customers' data:
	- personal data
	- information about Customer's diseases
- Additionally system will be storing operators personal data:
	- test operators
	- doctors
	
It's essential to ensure security of this data point. Breaches could have catastrophic results:
- personal data leaks
- society trust in the System (and government) will be seriously impacted
 
### Performance

System will not do any sophisticated operations. It will be mainly saving or sending simple data. However smooth operations is required because:
- slow systems tend to discourage people from using
- slow systems break trust
- slow systems will make work of Test Operators harder and slower
 
### Interoperability

The System was requested by the Government. Because of this it will require to integrate with some existing digital public infrastructure. Those could include:
- authentication
- verifying doctors
- existing healthcare digital system
- existing government's BI systems
 
### Instalability

System might be exported to different countries
- we shouldn't make any assumptions about infrastructure (cloud) providers
- Governments might have some preferences or even have their own data centers
 
### Modularity

Some components are country specific and will require custom one for particular country. 
- system must be easily configured for particular government and modules should be easily replaced
