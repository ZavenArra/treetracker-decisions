# Provisions for the use of single sign on when accessing treetracker web applications

* Status: proposed 
<!-- {proposed | rejected | accepted | deprecated | … | superseded by [ADR-0005](0005-example.md)} --> <!-- optional -->
* Deciders: @ZavenArra @Dadiorchen @nmcharlton @gwynndp
<!-- Find deciders here: https://github.com/orgs/Greenstand/people  -->
* Date: 2022-05-11

Technical Story: 
* https://greenstand.gitbook.io/auth-system/
* https://github.com/orgs/Greenstand/projects/47

## Context and Problem Statement

Keycloak is being implemented to replace the current auth system used by the admin panel, and to provide a more generalized auth system for web apps and microservices.  Keycloak offers single sign on (SSO) integrations for accounts from other providers, most notably Google and Facebook.  We should decide which, if any, SSO providers to allow our users to use when accessing our systems.

## Decision Drivers <!-- optional -->

* Ease of use for our users
* Ease of implementation
* Exposing our users to negative consequences from other providers
* Implicit support of other providers technology philosophy

## Considered Options

1. Do not implement SSO
2. Implement SSO for all providers supported by Keycloak
3. Implement SSO only for providers that are deemed philosophically aligned with values shared by Greenstand engineers.

<!--
## Decision Outcome

Chosen option: "{option 1}", because {justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force {force} | … | comes out best (see below)}.

### Positive Consequences <!-- optional -->

* {e.g., improvement of quality attribute satisfaction, follow-up decisions required, …}
* …

### Negative Consequences <!-- optional -->

* {e.g., compromising quality attribute, follow-up decisions required, …}
* …
-->

## Pros and Cons of the Options <!-- optional -->

### 1. Do no implement SSO

{example | description | pointer to more information | …} <!-- optional -->

* Good, because {argument a}
* Good, because {argument b}
* Bad, because {argument c}
* … <!-- numbers of pros and cons can vary -->

### 2. Implement SSO for all providers supported by Keycloak

* Good, because with supporting popular provider like Google, Facebook, the end user to Greenstand don't need to maintain the account on Greenstand, and the account creation workflow could be smoother and safer. It is like: 

  1. End user try to login to Greenstand
  2. End user selects the provider and authorize the application. 
  3. The administrator of Greenstand receives the notification.
  4. The administrator of Greenstand confirm the end user, and assign the user appropriate role/permission.

  Without this support:

  1. End user give the administrator their info.
  2. Administrator receive the info and create user, password, assign the user appropriate role/permission.
  3. The administrator give the user the account along with password.

  So the former have no password and detailed user info exchange;

{example | description | pointer to more information | …} <!-- optional -->

* Good, because {argument a}
* Good, because {argument b}
* Bad, because {argument c}
* … <!-- numbers of pros and cons can vary -->

### 3. Implement SSO only for providers that are deemed philosophically aligned with values shared by Greenstand engineers.

{example | description | pointer to more information | …} <!-- optional -->

* Good, because {argument a}
* Good, because {argument b}
* Bad, because {argument c}
* … <!-- numbers of pros and cons can vary -->

## Links <!-- optional -->

* {Link type} {Link to ADR} <!-- example: Refined by [ADR-0005](0005-example.md) -->
* … <!-- numbers of links can vary -->
