# Cross-cutting Concepts

<div class="formalpara-title">

## *Development concept*

*Developers should name Variables etc. after a strict concept/pattern/system to ensure consistency across Services*

## *Organizational concept*

*The backup-server runs at reduced speed during maintenance of the main-servers to enusure stability*

## *Security concept*

*Passwords are stored with encryption via a hashcode converting system from an external library to ensure security*

<div style="page-break-after: always;"></div>

                              

# Architecture Decisions

<div class="formalpara-title">

| Context                                                                                      | Decision                                       | Consequences                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| We want to manage the code on GitHub and need to decide if, we want one or more repositories | We will only use a single repository           | The whole code is in a single place and one can find it faster. There might be organizational problems.                                                                       |
| We have multiple teams and not everyone can code the same language                           | We will use multiple coding languages          | We have a microservices architecture, which means that every code of a microservice can be written in a different language. Not everybody will be able to work on every code. |
| We have a lot of user passwords and need to store them                                       | We will store passwords in a hash code library | Database performs worse due to computationally intensive process. An extra library has to be implemented. The passwords are more secure.                                      |


<div style="page-break-after: always;"></div>
