# High Availability

## Definition

High availability (HA) is the ability of a system to operate continuously without failing for a designated period of time. HA works to ensure a system meets an agreed-upon operational performance level. In information technology (IT), a widely held but difficult-to-achieve standard of availability is known as five-nines availability, which means the system or product is available 99.999% of the time.

## Notes

- The following three principles are used when designing HA systems to ensure high availability:
  - **Single points of failure**. A single point of failure is a component that would cause the whole system to fail if it fails. If a business has one server running an application, that server is a single point of failure. Should that server fail, the application will be unavailable.
  - **Reliable crossover**. Building redundancy into these systems is also important. Redundancy enables a backup component to take over for a failed one. When this happens, it's necessary to ensure reliable crossover or failover, which is the act of switching from component X to component Y without losing data or affecting performance.
  - **Failure detectability**. Failures must be visible and, ideally, systems have built-in automation to handle the failure on their own. There should also be built-in mechanisms for avoiding common cause failures, where two or more systems or components fail simultaneously, likely from the same cause.
- Three metrics used to measure availability include the following:
  - **Mean time between failures (MTBF)** is the expected time between two failures for the given system.
  - **Mean downtime (MDT)** is the average time that a system is nonoperational.
  - **Recovery time objective (RTO)**, also known as estimated time of repair, is the total time a planned outage or recovery from an unplanned outage will take.
- The six steps for achieving high availability are as follows:
  - **Design the system with HA in mind**. The goal of designing an HA system is to create one that adheres to performance conventions while minimizing cost and complexity. Points of failure should be eliminated with redundancy provided, as needed.
  - **Define the success metrics**. It's necessary to determine the level of availability the system needs, and which metrics will be used to measure it. Service providers involve customers in this process through an SLA.
  - **Deploy the hardware**. Hardware should be resilient and balance quality with cost-effectiveness. Hot swappable and hot pluggable hardware is particularly useful in HA systems because the hardware doesn't have to be powered down when swapped out or when components are plugged in or unplugged.
  - **Test the failover system**. Once the system is up and running, the failover system should be checked to ensure it is ready to take over in case of a failure. Applications should be tested and retested as time goes on, and a testing schedule should be in place.
  - **Monitor the system**. The system's performance should be tracked using metrics and observation. Any variance from the norm must be logged and evaluated to determine how the system was affected and what adjustments are required.
  - **Evaluate**. Analyze the data gathered from monitoring, and then find ways to improve the system. Continue to ensure availability as conditions change and the system evolves.
- A highly available system should be able to quickly recover from any sort of failure state to minimize interruptions for the end user. High availability best practices include the following:
  - Eliminate single points of failure or any node that would impact the system if it becomes dysfunctional.
  - Ensure all systems and data are backed up for fast and easy recovery.
  - Use load balancing to distribute application and network traffic across servers or other hardware. An example of a redundant load balancer is HAProxy.
  - Continuously monitor the health of back-end database servers.
  - Distribute resources in different geographical regions in case of power outages or natural disasters.
  - Implement reliable failover. In terms of storage, a redundant array of independent disks (RAID) or storage area network (SAN) are common approaches.
  - Set up a system that detects failures as soon as they occur.
  - Design system parts for high availability and test their functionality before implementation.

## HA for Databases

- A High Availability (HA) Database is a database system designed to operate continuously with no interruptions in service. So database errors and failures must be handled by automatically failing over to redundant nodes when problems occur.
- High availability is typically achieved using redundancy and isolation constructs. Redundancy is implemented by duplicating some of the database components. Isolation is achieved by placing the redundant components in independent hosts.
- The term cluster refers to the entirety of the components of a database deployment, including its redundant ones. Together, these components ensures the availability of the solution.
- Instance-level clustering. In this type of clustering, we protect the database instance part by deploying several instances in different hosts. The database resides, typically, on a remote storage visible to all the concerned hosts.
  - Active/Active type where the instances are actively processing database clients requests in parallel. This is the case of Oracle database’s Real Application Cluster. When there is an issue with one instance, the database clients requests will be routed to the remaining, healthy instances.
  - Active/Passive type where, at any given time, there is only one instance actively processing database clients requests. When there is an issue with the old active instance, the clients requests will be transferred to the newly elected active instance. Microsoft SQL Server’s Failover Cluster Instance (FCI) and Veritas’s Cluster Server offer this kind of clustering.
- Database-level clustering
  - In this type of clustering, we protect both the database instance and the database. Protecting only the database might result in a situation where your data is protected but there is no way to access it quickly. Note that we can create offline copies of the database for backup purposes. Yet, the main purpose, in such a case, is data protection.
    - Storage-based replication, where a storage/filesystem level protocol pushes the changes happening in one database to the other databases. This is the type of clustering offered by the combination of Microsoft SQL Server’s Failover Cluster Instance (FCI) and Storage Space Direct. In this type of replication, the additional instances are typically on standby mode and the replication protocol is usually synchronous.
    - Database solution-based replication, where a database level protocol pushes the changes happening within one database to the other databases. This is the kind of clustering provided by solutions like MongoDB’s ReplicaSet, Microsoft SQL Server’s AlwaysOn Availability Group and Oracle database’s Data Guard. We can have 2 subtypes for database solution-based replication:
      - Logical replication: where we replicate the database client requests from one instance to the other. Oracle Golden Gate and MySQL statement based replication support this type of replication.
      - Physical replication: where we replicate the effect of database client requests on the data from one database to the other (going through the instance). Oracle Data Guard and MySQL row based replication support this kind of replication.

## Isolation

![Isolation](https://res.cloudinary.com/canonical/image/fetch/f_auto,q_auto,fl_sanitize,c_fill,w_720/https://ubuntu.com/wp-content/uploads/1a95/image-1.png)



## Sources

- <https://www.techtarget.com/searchdatacenter/definition/high-availability>
- <https://www.scylladb.com/glossary/high-availability-database/>
- <https://ubuntu.com/blog/database-high-availability>
