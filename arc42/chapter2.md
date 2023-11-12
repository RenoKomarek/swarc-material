# Solution Strategy

<div class="formalpara-title">

</div>

The three most important goals and their architectural approaches are:

| Goal/Requirements                               | Architectural Approach                                                                                                                                                 |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image Editing and Sharing                       | Microservices - Enables the easy addition of new filters and photo functions. Ensures professional image editing capabilities with extensibility.                      |
| Third-party Integration of cloud-based software | Service-Oriented Architecture (SOA) - Seamless integration of a service, developed by the partner.                                                                     |
| User-generated Challenges and Competitions      | Microservices - A central challenge creation service and additional services for challenge validation. Facilitates user-generated challenges, competitions, and feeds. |


# Fundamental Decisions

<div class="formalpara-title">

We have opted to maintain our Microservices architecture. Microservices offer agility and flexibility, allowing us to respond quickly to evolving requirements and reducing the complexity associated with a monolithic architecture.

Three important architectural decisions are:

| Problem                                                           | Considered Alternatives                       | Decision                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------|---------------------------------------------------------------------------------------------------------|
| A microservice is necessary for a new challenge                   | Adapt old microservice for new challenges     | We chose to create a new microservice for every new challenge, to be able to reactivate old challenges. |
| If every filter has its own microservice, they are too dependent  | Do not give every filter its own microservice | Filtering is a single microservice and all filters are saved in a database                              |
| Testing is complex, because every single service has to be tested | With SOA, there would be less testing expense | Because we do not have liquidity problems, we stay with microservices                                   |


</div>



<div class="formalpara-title">

# Risks and Technical Debts

<div class="formalpara-title">

</div>

The three most important risks/technical depts are:



- Data Management
 The influx of inconsistent data poses challenges in terms of organization and distribution. Ensuring the consistency and accuracy of data across the system becomes a complex task. Failure to manage data effectively can lead to data quality issues, potentially impacting decision-making and system performance.

- Security
  Implementing security measures in each Microservice incurs significant costs. Additionally, securing sensitive data across multiple services is both cost and time-intensive.

- Complexity
 The increasing complexity of the architecture demands more resources for inter-service communication and the seamless integration of new services into the existing network. 



<div class="formalpara-title">


