# What is EC2
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. Amazon EC2 reduces the time requested to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change.

## EC2 Options
- **On Demand** - allow you to pay a fixed rate by the hour with no commitment.
- **Reserved** - provide you with a capacity reservation, and offer a significant discount on the hourly charge for an instance. 1 Year or 3 Year Terms
- **Spot** - enable you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexibl start and end times.
- **Dedicated Hosts** - Physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.

### On Demand
- Users that want the low cost and flexibility of Amazon EC2 without any up-front payment or long-term commitment
- Applications with short term, spiky, or unpredictable workloads that cannot be interrupted
- Applications being developed or tested on Amazon EC2 for the first time

### Reserved
- Applications with steady state or predicatable usage
- Applications that require reserved capacity
- Users able to make upfront payments to reduce their total computing costs even further

### Spot
- Applications that have flexible start and end times
- Applications that are only feasible at very low compute prices
- Users with urgent computing needs for large amounts of additional capacity

### Dedicated Hosts
- Useful for regulatory requirements that may not support multi-tenant virtualization.
- Great for licensing which does not support multi-tenancy or cloud deployments.
- Can be purchased On-Demand (hourly)
- Can be purchased as a Reservation for up to 70% off the On-Demand price.

> **Spot Prices - Exam Tip**: If the Spot instance is terminated by Amazon EC2, you will not be charged for a partial hour of usage. However, if you terminate the instance yourself, you will be charged for any hour in which the instance ran.

## EC2 Instance Types

Family | Speciality | Use case
-------|------------|----------
D2 | Dense Storage | Fileservers / Data Warehousing / Hadoop
R4 | Memory Optimized | Memory Intensive Apps / DBs
M4 | General Purpose | Application Servers
C4 | Compute Optimized | CPU Intensive Apps / DBs
G2 | Graphics Intensive | Video Encoding / 3D Application Streaming
I2 | High Speed Storage | NoSQL DBs, Data Warehousing, etc.
F1 | Field Programmable Gate Array | Hardware acceleration for your code
T2 | Lowest Cost, General Purpose | Web Servers / Small DBs
P2 | Graphics/General Purpose GPU | Machine Learning, Bit Coin Mining, etc.
X1 | Memory Optimized | SAP HANA/Apache Spark, etc.

> How to easily remember: **DR Mc GIFT PX**
```
**D** for Density
**R** for RAM
**M** - main choice for general purpose apps
**C** for compute
**G** - graphics
**I** for IOPS
**F** for FPGA
**T** for cheap general purpose (think T2 Micro)
**P** - graphics (think pics)
**X** - Extreme Memory
```
