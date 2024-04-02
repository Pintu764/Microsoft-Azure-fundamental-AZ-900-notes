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

  
### Describe subscriptions
A way of organizing resources in terms of 
1. billing
2. access

Subscriptions can be comprised of multiple resouce groups, and any property assigned to a subscription will also be assigned to the resource groups.


### practice questions:
1. You need to identify the type of failure for which on Azure Availability Zone can be used to protect access to Azure services. What should you idntify?
    A.a physical server failure
    B. on Azure region failure
    C. a storage failure
    D. an Azure data center failure
2. Availability zones can be implemented in all Azure regions? Yes/no
3. Only windows VM can be created in Availability zones ? Yes/No
4. AZ are used to replicate data and application to multiple regions ? Yes/No
5. You can use AZ to protect VM from a data center failure ? Yes/No
6. An Azure region----
   -Contains one or more data centers that are connected by a low latency network
   - Is found in each countary where MS (microsoft ) has an office
   - Can ne found in every Europe and Americas countary
   - Contains ane or more date centers that are connected by a high latency network
  7. You can use AZ to protect VM from a region failure: Yes/No 


