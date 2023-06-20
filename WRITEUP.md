# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*


### Cost Analysis:

- VM: The cost of a Virtual Machine (VM) includes the cost of the operating system and the hardware it runs on. VM costs vary based on the type of VM instance you choose, storage, and network bandwidth usage. Other costs, such as backup, recovery, and monitoring, can add to the overall cost.

- App Service: Azure App Service is a fully managed platform with built-in infrastructure maintenance, security patching, and scaling. The cost is primarily based on the pricing tier you choose. App Services may offer more value as many additional services like SSL, custom domains, auto-scaling, and backups are included in the package.

### Scalability:

- VM: Scaling in a VM environment involves either increasing the capacity of the VM or adding more VM instances. Preferred for apps which are going to scale in future.

- App Service: App Services have built-in high availability. Azure manages the underlying infrastructure, performing automatic OS patching, network maintenance, and critical updates without any downtime. However, there are some regards when it comes to scalability.


### Availability:

- VM: For VMs, high availability is achieved by configuring VM scale sets, Availability Sets, and Azure Load Balancer. This requires significant configuration and management efforts.

- App Service: App Services have built-in high availability. Azure manages the underlying infrastructure, performing automatic OS patching, network maintenance, and critical updates without any downtime.


### Decission and Comparisons

- VM: VMs provide maximum control over the environment. You have full administrative access to the VM, so you can install any software and do any system-level modifications. This is beneficial for workflows that require high levels of customization. However, VMs require more maintenance and management.

- App Service: App Service supports automated deployments and continuous integration/delivery workflows using e.g. GitHub, Azure DevOps. It supports a wide range of programming languages and frameworks. However, it offers less control over the environment compared to VMs.

### Decission

Overall, the Azure App Service seems to be a more convenient and cost-effective solution for deploying the CMS application. It provides built-in high availability, and reduced maintenance and management overhead, all of which could lead to cost savings in the long term. Therefore I would suggest going with Azure App Service.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

- Custom Software Requirements: If the CMS app would require to run some specific custom software or dependencies that are not supported in the Azure App Service environment. VMs provide full control over the environment, allowing for installation and management of any available software.

- Specific Hardware Requirements: Azure App Service runs on shared resources, and you don't have control over the specific hardware your app runs on. If the CMS app would require to run some specific hardware e.g. GPU you would need to configure the VM's to meet these requirements.

- Increased Security and Isolation: App Service is a shared resource, meaning your app runs alongside other apps in the same environment.  If the CMS application needs to meet certain security requiriments e.g. an isolated environment a VM would be a better choice as it offers dedicated resources and higher levels of isolation.

