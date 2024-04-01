# <u>Introduction to Cloud Computing</u>

### Define the cloud ?
In cloud computing, "the cloud" refers to a network of servers (typically hosted in data centers) that provide various services over the internet. These services can include storage, processing power, networking capabilities, and software applications. Rather than storing data or running applications on a local computer or server, users access these resources remotely via the internet.

The term "cloud" is derived from the use of a cloud-shaped symbol in network diagrams to represent the complex infrastructure of the internet. In the context of cloud computing, this symbol represents the abstraction of the underlying infrastructure and the idea that users don't need to know or manage the physical hardware that powers the services they use.

### Define cloud computing.
Computing services provided over the internet

Cloud computing is the delivery of computing services, including servers, storage, databases, networking, software, over the internet ("the cloud") to offer faster innovation, flexible resources, and economies of scale. Users can access resources from anywhere with an internet connection, paying only for what they use, without the need for upfront infrastructure investments. It encompasses various service models like Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS).

### Extra: Give examples of computing services.
1. Compute power: Pay for the amount of RAM and quality of processor.
2. Storage: Pay for how much disk space you use. Added bonus of easily replicating data across several servers.

### Extra: Difference between RAM and processor.
RAM is the maximum "quantity" of work your computer can do at any given time. The processor is the speed at which you do the work.

### Extra: Why would I use a cloud service provider?
* Pay only for the services used.
* Don't have to manage your own hardware resources.
* Scale or de-scale quickly.

### Describe the shared responsibility model.
The responsibilities of maintaining your cloud-hosted applications are shared between you and the cloud service provider.

How those responsibilities are split depend on the service you use.

The consumer will always be responsible for the data you store, as well as who can access the data and on what kind of device (e.g. cell phone, computer, etc.).

The CSP will always be responsible for the physical data center, physical host (i.e. the computer itself, I think), and physical network.

Infrastructure as a Service (IaaS) is a service giving minimal responsiblity to the CSP.
Software as a Service (SaaS) gives minimal responsiblity to the user.
Platform as a Service (PaaS) falls somewhere in between.

### Extra: What responsibilities fall "in-between" a IaaS and SaaS?
1. Identity infrastructue management (e.g. if you use Azure Active Directory vs Auth0 for identity management)
2. Applications
3. Network controls (i.e. who can access your cloud-hosted resources on a network level)
4. Operating System (i.e. choosing the underlying OS, updating it, etc.)
   
### Extra: Is the Azure Virtual Machines (VM) service SaaS, PaaS, or IaaS?
IaaS because the user must update and secure the OS, manage network-level accessibility, provide any applications hosted on the VM, and specify how identity management will be provided.

### Define cloud models, including public, private, and hybrid.
Cloud models "define the deployment type of cloud resources." They're the "types" of clouds, where a cloud is just a collection of services provided via the internet.

1. private: A private cloud is only used by a single organization.
   * The data centers can be hosted on-site or by a third-party.
   * You data isn't colocated with data from other orgs, which may be required (e.g. HIPAA).
   * More control but also more costly.
2. public: A cloud built, controlled, and maintained by a CSP.
   * Less control but cost advantages from economies of scale (i.e. hardware resources purchased in "bulk" by CSP, savings distributed to consumers)
3. hybrid: A cloud utilizing both private and public clouds.
   * Start with private cloud, then surges in demand can be handled by public cloud (because they're quicker to set up).

| Public       | Private | Hybrid |
|:------------ |:--------------:| -------------:|
| In a public cloud, resources are shared among multiple users, and customers only pay for the resources they use.| Resources are not shared with other Organizations, providing greater control and security.         | Uses both public and private cloud in an inter-connected environment.         |
| Hosted and operated by a third-party cloud services provider, such as AWS, Azure or GCP          | Operated and maintained by a single organization. A private cloud may be hosted on-premises or in a data center.         | Providers extra layer of security, user can choose which resources to keep in private cloud and which resources to deploy in public cloud.         |
| NO CapEx to scale up         | High CapEx        | include both        |
| Resources can be provisioned or decommissioned on demand         | Hardware to be purchased        | Recources can be added on demand by scaling up in the public cloud environment.        |
| think like buplic bus         | Private Bus         | public and private bus        |

### Extra: What is multicloud?
Using multiple CSPs. You may want to use a mish-mash of services. Or you may be migrating from one CSP to another.

### Compare cloud pricing models.
2 types:
 1. Capital expenditure: Pay up-front, saves money if you know your costs ahead of time.
2. Operational expenditure: On-demand payment, can pay for more resources if needed and stop paying for resources that aren't used.
CSPs are OpEx.
