# Deployment View

The deployment section outlines the strategy and procedures for introducing the system into its operational environment, utilizing the CAP theorem and a deployment diagram.

## CAP

The CAP theorem tells us that a distributed system can only provide two of the three desired properties: Consistency, Availability and Partition Tolerance.
<br><br>
Finstergram chooses Availability and Partition Tolerance (AP):
<br><br>
Availability (A) is crucial because it ensures that Finstergram is consistently accessible and usable by its users. It guarantees that they can interact with the application whenever they need to without encountering frequent downtime or unavailability. It is essential for maintaining a positive user experience and to meet the stakeholders expectations.
<br><br>
Partition Tolerance (P) is important because it gives Finstergram the ability to operate and function effectively despite potential network issues or partitions. It ensures that even if certain parts of the system cannot communicate with each other temporarily because of hardware failures, communication delays, etc., the system as a whole can continue to operate without complete failure.
<br><br>
On the other hand, Consistency (C) could guarantee that every user has the same view of the data at the same time. However, strong Consistency has to be sacrificed in favor of Availability and Partition Tolerance. It has to be accepted that various users do not always have immediate access to the latest version of the data.

## Deployment-Diagram

![alt text](images/deploymentv5.png)

This deployment-view-diagram describes the technical infrastructure of Finstergram. Users communicate via client devices with the internet. A web server hosts the app's interface, while an application server manages its functions. The application server also interfaces with third-party integrations like Pixlr. Amazon S3 Cloud Storage is used to store the images and user data.
