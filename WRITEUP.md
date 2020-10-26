# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*
VMs provide infrastructure as a service (IaaS), which means they allow full access and control of the host OS and are an excellent choice for migrating from an on-premises server to the cloud. They offer lower up-front cost compared to purchasing and maintaining hardware on-premises, while multiple VMs can be grouped to provide high availability, scalability, and redundancy using the Virtual Machine Scale Sets and Load Balancers options in Azure.
The limitations of VMs are that they can be more expensive that other suitable options in Azure and they require more time for the developer to setup.

On the other hand, Azure App Service is an HTTP-based service suitable for hosting web applications, REST APIs, and mobile back ends. It is a Platform as a Service (PaaS) that allows a developer to focus on the application rather than the infrastructure details. It supports multiple programming languages and continuous deployment using Git. It offers high-availabeility and many auto-scaling options depending on the pricing tier (App Service Plan).
The main drawbacks are the limited access to the host OS and hardware limitations (maximum of 14GB RAM and 4vCPU cores).

In our case, an App Service would be the best option since our application does not require any custom software, while the continuous deployment and auto-scaling features will speed up the development of the site.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
One reason that would change our decision is the hardware limitations. If the traffic in our site is increased, then, taking also into account the scaling options, the available RAM and CPU cores might not be adequate. Therefore, in case upgrading the service plan to ahigher tier is not option, it would be better to cahnge to a VM solution.
Another scenario where cahnging to a VM solution might be better is merging the web app with custom on-premises software, e.g. database with confidential data.
