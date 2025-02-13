## Context

We need a authentication server to provide secure access for all the actors. We need to support the following approaches:
- email + password - the most common one that people are familiar with
- social connections - logging with providers such google will make creating an account and logging in even simpler and making access as easy as possible is strategic goal
- integrations - some actors are government officials. It is not uncommon that governments have their own authentication systems so our auth server should be extensible (e.g. Active Directory/LDAP)
- we need a solution that uses standard protocols and is battle tested

## Decision

We will use keycloak.

https://www.keycloak.org/

- battle tested solution
- supports lots of protocols and is highly customizable

## Consequences

- this is complex tool that might require configuration but because government money is unlimited this is not a problem