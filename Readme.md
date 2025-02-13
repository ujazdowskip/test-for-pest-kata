Architectural Kata for the following
https://www.architecturalkatas.com/kata.html?kata=TestPest.json

🚧 This is very much WIP

# Test for Pest

Test for Pest is a system that will be supporting governments with providing modern system for disease testing.

Kata description

> The department for disease control wants to offer a system to safely and securely handle test results nationwide.
> 
> Users: thousands of test operators, millions of customers to be tested, hundreds of government officials, thousands of doctors.
> 
> Requirements:
> 
> - Customers can schedule a test appointment with a local test operator.
> - Test operators can verify the customers' appointments and personal data on the spot.
> - Test operators can submit the test result.
> - Customers can view their test result.
> - The system can handle tests for different diseases.
> - Local government officials can view the test statistics for their area of responsibility.
> - Department for disease control can view local and nationwide statistics with different prediction models.
> - Local government can contact customers if they submitted an email address or phone number.
> - Doctors can view the customer's test history if customer enabled them.
> 
> Additional Context:
> - The system must be able to react quickly on outbreaks of new diseases and therefore the availability of new test types.
> - Tests are carried out workdays during office hours.
> - The system will potentially be exported to other countries.
> - You have a contract with the government so money is not important.


[Scale](Scale.md) - some calculations regarding the scale.

## Strategic goals

Polish government is aware that prevention is the most important for improving population health and the following are the strategic goals:
- encourage as many people as possible to test themselves
- gather disease statistics to react accordingly
- in the events of disease outbreaks test as many people as possible
 
## Event storming

In order to discover system's details we carried out event storming session.

[Event Storming](./Event%20Storming.md)

## Architecture characteristics

After analysing requirements and outcomes from event storming session the system characteristics were defined.

[Characteristics](./Characteristics.md)

## Designing architecture

After that we proceeded to defining the [Architecture details](./Architecture/Architecture%20details.md).













