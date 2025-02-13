
Main goal of this session was to find out more details about the business processes. As a result we carved out most important flows. We identified the following:
- actors
- use cases
- system components
- business events

Event storming board

![[test-pest-event-storming.png]]

## Actors

- **System operator** - admin that will configure the System
- **Test Coordinator** - local operator that coordinates testing over specified local area
	- could be an administrative unit
	- or even a single place in a city
	- manages Test Operators
- **Test operator**
	- actual person that carries out the disease test for a Customer
- **Customer** - person that wants to be tested
- **Local Government** - an administrative unit that has access to statistics
- **Government** - a government agency that has advanced access to statistics
- **Doctor** - doctor that can use the System to see Customers' test history
- **System** - the System that carries out some scheduled actions

## Components

- **Customer system** - component that will provide an application for Customer
- **Test Operator system** - component that will provide an application for Test Coordinators
- **Backoffice system** - component that will provide an application for System Operators and Test Coordinators
- **Customer service** - backend service for managing Customers
- **Appointment service** - backend service for managing appointments
- **Test Result service** - backend component for managing Test Results
- **System service** - backend component for managing system configuration
- **Notification service** - backend component for sending notifications (email, SMS)
- **Auth server** - service for providing authentication

