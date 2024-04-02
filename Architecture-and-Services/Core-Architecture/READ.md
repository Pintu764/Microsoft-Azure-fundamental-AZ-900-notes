### Describe Azure resources and resource groups
Resources are the "fundamental" unit in Azure. A VM instance is an Azure resource. Resource groups are collections of resources. 

- A resource must be part of a resource group
- A resource can _only_ be part of a single resource group
- Properties of the resource group get inherited by all the resources it contains

### Describe management groups
Management groups have one or more subscriptions.

### Describe the hierarchy of resource groups, subscriptions, and management groups
In order of descending specificity:
resouce -> resouce group -> subscription -> management group

![](https://github.com/Pintu764/Microsoft-Azure-fundamental-AZ-900-notes/assets/159055209/a7aa7327-a782-4c8c-826b-f6d6a8aa9c29)

![](https://github.com/Pintu764/Microsoft-Azure-fundamental-AZ-900-notes/assets/159055209/a91f3dc0-e253-48b3-8e0a-24e8c4cbb23f)

![](https://github.com/Pintu764/Microsoft-Azure-fundamental-AZ-900-notes/assets/159055209/ed40180f-d18c-40e7-bdb8-d42e7fa8c704)

### Describe Azure regions, region pairs, and sovereign regions

An **Azure region** is a geographical designation of several physical data centers. Some regions have **availability zones** which are themselves (smaller) geographical designations of one or more data centers. Each availability zone is able to run on its own, so that if one goes down, any data that's been replicated will still be available in another availability zone of the same region.  

**Region pairs** are two regions that, in the case of a natural disaster or some other occurrence that may affect an entire region, can compensate for the other when one goes down. Not all region pairs are two-way, some are one-way. Region pairs must be _at least_ 300 miles away from each other.  

**Sovereign regions** are Azure instances that are isolated from the "main" Azure instance, and are used for organizations that need to comply with certain regulations.  

### Availability Zone
 - Think of Availability Zones as physical locations within an Azure region.
Just like a city has multiple neighborhoods, an Azure region has multiple Availability Zones.
- Each Availability Zone is essentially a separate data center facility, with its own power, cooling, and networking infrastructure.
- Azure services can be deployed across multiple Availability Zones to ensure high availability and fault tolerance.
- If one Availability Zone fails due to unforeseen circumstances, services deployed in other zones remain unaffected, ensuring continuous availability.

### Resource Group
  - A Resource Group is more like a virtual container or a folder that holds related Azure resources such as virtual machines, databases, storage accounts, etc.
- It acts as a logical grouping mechanism to organize and manage resources that share common lifecycle, management, and security requirements.
- You can think of a Resource Group as a way to manage your Azure resources as a single unit, regardless of their geographical location.
- Resources within a Resource Group can be located in different Azure regions, but they are still grouped together for management purposes.
- Operations like monitoring, access control, and billing can be applied to a Resource Group collectively.


In Microsoft Azure,***Availability*** Sets are a feature designed to improve the availability and reliability of virtual machines (VMs) by providing redundancy at the infrastructure level. Here's how Availability Sets function:

Fault Domain Isolation: Azure data centers are divided into fault domains, which represent groups of hardware that share a common power source and network switch. When you deploy VMs within an Availability Set, Azure ensures that these VM instances are spread across multiple fault domains. If a hardware failure occurs within one fault domain, VM instances in other fault domains remain unaffected, thus ensuring high availability.

Update Domain Isolation: Azure periodically performs maintenance tasks such as updates and patches on the underlying hardware infrastructure. To minimize the impact of maintenance events on VM availability, Azure divides the VM instances within an Availability Set into update domains. During maintenance, only one update domain is taken offline at a time, ensuring that a subset of VM instances remains available while others are undergoing maintenance.

Redundancy and Load Balancing: By distributing VM instances across fault domains and update domains within an Availability Set, Azure provides redundancy and load balancing at the infrastructure level. This helps ensure that your applications remain available and responsive even in the event of hardware failures or maintenance activities.

High Availability: The primary function of Availability Sets is to improve the availability of your applications by providing fault tolerance and resilience at the infrastructure level. By deploying VMs within an Availability Set, you can achieve higher levels of availability and reliability for your applications, reducing the risk of downtime due to hardware failures or maintenance events.
  
### Describe subscriptions
A way of organizing resources in terms of 
1. billing
2. access

Subscriptions can be comprised of multiple resouce groups, and any property assigned to a subscription will also be assigned to the resource groups.


### practice questions:
##### AZ=availability zone
1. You need to identify the type of failure for which on Azure Availability Zone can be used to protect access to Azure services. What should you idntify?
   
    - a physical server failure
    - on Azure region failure
    -  a storage failure
    -  n Azure data center failure
3. Availability zones can be implemented in all Azure regions? Yes/no
4. Only windows VM can be created in Availability zones ? Yes/No
5. AZ are used to replicate data and application to multiple regions ? Yes/No
6. You can use AZ to protect VM from a data center failure ? Yes/No
7. An Azure region----
   -Contains one or more data centers that are connected by a low latency network
   - Is found in each countary where MS (microsoft ) has an office
   - Can ne found in every Europe and Americas countary
   - Contains ane or more date centers that are connected by a high latency network
  8. You can use AZ to protect VM from a region failure: Yes/No


# Knowledge Checks
1. You can create resource group inside resource group. True/False
2. A VM can be in multiple resource groups. True/ False
3. A resource group can contain resources from multiple azure regions ? True/False
4. A resource should be part of one resource group True/False
5. You plan to deploy several Azure Virtual machines. You need to ensure that the services running on the virtual machines remain available if a single data center fails. What are two possible solutions ? Each correct answer presents a complete solution.
    - Deploy the virtual machines to two or more availability zones.
    - Deploy the virtual machine to two or more resource groups.
    - Deploy the virtual machine to a scale set.
    - Deploy the virtual machines to two or more regions.



# knowledge checks
1. You plan to deploy several Azure Virtual machines. You need to ensure that the services running on the virtual machines remain available if a single data center fails.
    - You deploy the virtual machines to two or more availability zones
    - Deploy the virtual machine to a scale set.
    - You deploy the virtual machine to two or more subscriptions
    - All of the above

   2. If VMs were deployed in an Availability set, they would be placed on separate physical servers, so if one server fails, the other Virtual Machine will still be available. Yes/No
   3. There are no charges of using Availability sets and VMSS but you pay for the underline resources that it provisions? Yes/No
   


