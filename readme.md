# AZ-304

## compute

* Virtual Machine: Windows oor Linux (lift and shift) also called as inrastructure as a service
* App services : you can deploy web or mobile app without worrying about undrlying inrastructure
* Azure container service: single container, lightweight thn actual VM as it does not have OS
* Azure kubernates servive: wehen you have multiple containers in your application
* Azure unction: Serverless offering, executes indivicual functions, 
* SPOT instance: can stop withing 30 seconds o notice so you should not use or critical workload

## storage

![](https://i.imgur.com/3rIpdil.png)


* Bolb storage: object. storage and it can't have hirarchey, multiple tires, HOT, Cool and Archive
*  Azure File stoorage:  use this one if you need hirarchical storage. 
*  Azure Data lake storage: this one is also hirachical but also allows capbility of running Haddooop analytics for data analytics application
* Azure SQL database:  simplar to SQL server tho it's noot 100% compatible
* Opensourece DB solutions:  Azure database or MySQL, postgreSQla nd MariaDB
* Azure Synapse:  I you wanto to build data warehousing
* Cosmos DB(NOSQL): This can scale globally and it's microsot's main NOSQL service
* Azure Cache for redis: for caching

## networking

![](https://i.imgur.com/7xrO1SH.png)


* Vnet, virtual network: You can define subnet within the vnet to define how trafica can low between them
* VNet Peering: if you want vnet to communicate
* VPN: If you want to create a secure connection between a VNet and an on-premises network, then you can use either a VPN, which stands for Virtual Private Network, or Azure ExpressRoute. A VPN sends encrypted traffic over the public internet, whereas ExpressRoute communicates over a private, dedicated connection between your site and Microsoft's Azure network. ExpressRoute is much more expensive than a VPN, but it provides higher speed and reliability since it's a dedicated connection.

![](https://i.imgur.com/DOYs3Oe.png)

## Migration

![](https://i.imgur.com/kq8gPxb.png)

* Azure Migrate: Discovers on premise server both virtual and physical, it will tell you if it's ready to migrate cost etc
* Azure Active. directory: for customer using active directory


## Devops:

![](https://i.imgur.com/YWZn5g0.png)

* Azure Pipelines:  It lets you create automated workflows to continuously build, test, and deploy code.

* Azure DevTest Labs: which makes it easy to spin up non-production environments. You could do this in other ways, but DevTest Labs gives you some extra capabilities, such as allowing administrators to control costs by setting limits on how many VMs can be deployed at once and ensuring that VMs are shut down when they're not in use.

* Azure Content Delivery Network: it's CDN for ast data deleivery

## IoT:

![](https://i.imgur.com/ACm9S9S.png)

* Azure IoT Centeral: Azure IoT Central, which is a fully managed SaaS solution that takes care of the technical details for you. It lets you create IoT applications without writing any code.

* Azure IoT Hub: if you need simething more customized, t's a service that handles secure communications with thousands, or even millions, of IoT devices. In fact, it's the service that IoT Central uses behind the scenes.

* Azure Sphere: make your IoT devices more secure. It includes certified chips, the Azure Sphere operating system, and the Azure Sphere Security Service, all of which provide layers of protection for your IoT devices.

## Azure Analytics:

![](https://i.imgur.com/fofU6Rq.png)

* HDInsight:  It supports a wide variety of open-source big data frameworks, including Hadoop, Spark, Hive, Storm, and many others

* Azure Databricks:   it runs Spark as well, but it's more user-friendly and easier to manage than HDInsight.

* Azure Synapse Analytics: new version of Azure SQL Data Warehouse. It includes all of the old data warehouse functionality, but it also supports Spark analytics.

* **NOTE**: `Apache Spark seems to be the king of big data analytics, and it's just a question of which service you want to use to run it.`

## Artiicial Intelligence:

![](https://i.imgur.com/1ZOE8zW.png)

`Even though AI seems like it must be incredibly complex, the basic idea is fairly simple. The most common method is called machine learning. The way it works is you feed lots of real-world data into a program and the program tries to make generalizations about the data. This is known as training a model. It then uses these generalizations to make predictions when it's given new data.`

* Azure Cognitive Services: This is a collection of pre-built artificial intelligence tools. These services let you add AI capabilities to applications even if you don't know anything about machine learning. They're grouped into five categories: decision, language, speech, vision, web search

*  Azure Bot Service: chatbot.

* Azure Machine Learning Studio:  Basic knowledgeo machine learning, train and deploy models without coding. 

*  Azure Machine Learning Services: ull control over all the machine learning mprocess.You can use any Python-based machine learning framework, such as TensorFlow or PyTorch, train models using services such as Azure Databricks, and deploy models using services such as Azure Kubernetes Service. Azure Machine Learning Services is usually the best solution when you need to build your own custom artificial intelligence application.

## Integration tools: 

![](https://i.imgur.com/3bJ6yFh.png)

* Azure Logic Apps: that lets you automate this sort of task without writing any code.
* Azure Event Grid: to notify your logic app of particular events.

## Architecture and best practices:

https://docs.microsoft.com/en-us/azure/architecture/

## Management:

![](https://i.imgur.com/E1Byfqg.png)

# Designing or Azure operations

## Application monitoring and alerting

* **Azure monitorr**: Azure Monitor is sort of your ‘base camp’ for metrics in Microsoft Azure. Azure Monitor, ‘provides base level infrastructure metrics and logs for most services in Microsoft Azure. 
![](https://i.imgur.com/PDrhpZ0.png)


![](https://i.imgur.com/ZZvCrQE.png)

* **Log Analytics**:  Azure Log Analytics is the ecosystem of additional plugins, known as ‘management solutions:

* **App Monitoring**: Application Insights is similar in that you will need to add it to your code base before you can start getting metrics. Like many such frameworks the library is pretty lightweight and should not cause much performance overhead. Tracking calls are non-blocking, batched, and sent in a separate thread.Application Insights can be used to monitor applications running anywhere

* **Azure Moonitoring ALert**:

![](https://i.imgur.com/MjpA5pc.png)


* **Application Insight alerts**

![](https://i.imgur.com/gNaCnah.png)

* **Alerting based on queries**: Queries run by azure lig analytics

![](https://i.imgur.com/Zt7eLd3.png)


## Platform monitoring and analytics: This is mainly about azure resources monitoeing, platorm resoorces, network and security

![](https://i.imgur.com/CeA1vMN.png)

![](https://i.imgur.com/QoAw8cA.png)


* **Azure Health**: Offeres threee basic level of information

* ** Azure Status**: which is simply a dashboard with information about the health of all of Azure’s different components. This information is not specific to your account; rather it will tell you if there is a global issue with a particular Azure service, such as virtual machines or storage.


* **Azure Service Health**: similar to Azure Status but focused only on Azure resources in your account. Like Azure Status it is a dashboard only this one is customizable.Azure Service Health will notify you of planned maintenance that may affect your system. It will also warn you if you are approaching a resource quota or if a feature you use is about to become deprecated.

* **Azure Resource Health**: the most granular level of inspection in the Azure Health suite. With Azure Resource Health you can get the status of specific instances of Azure resources, such as a single VM. You can see if an Azure platform SLA was violated at any point. 

* **Azure Advisor**:  is a personalized cloud consultant. It automatically examines all of your Azure resources and identifies ways to optimize them. It will spit out tons of recommendations automatically focusing on security, availability, performance, and cost.

* **Azure Activity Log**: log that records events using event data from Azure Resource Manager. It records eight specific types of events: Administrative, Service Health, Security, Alert, Autoscale, Recommendation, Policy, and Resource Health.

## Azure Network Monitoring: 

* **Network Watcher** is a comprehensive network topology monitoring and analytics solution. It is comprised of several features.  Full list is below. 

![](https://i.imgur.com/6Ei94Pg.png)


* **Topology App** : This gives you a network level view showing the various interconnections between network resources within a given resource group.

* **Variable Packet Capture tool**: This lets you capture packets flowing in and out of virtual machines, much as you might do with tcpdump or wireshark.

* **Next Hop tool**: Basically it just determines the next hop for packets routed in the Azure Network Fabric. It is great for identifying problems with user-defined routes.

* **NSG Flow Logging, Security Group View, and IP Flow**: Verify tools, all of which are really great for identifying where exactly packets are permitted to go and not go.

* **Azure Log Analytics**:  supplemental feature  to your overall network monitoring system. They are activated through the Log Analytics UI and so need to be addressed separately. Most are just additional levels of instrumentation.For example there are the **DNS Analytics and Traffic Analytics components**. The former is for DNS administrators and aggregates DNS logs. The latter is for aggregating and visualizing public internet traffic against Azure systems.


* **Azure Log Analytics's Network Performance Monitor**: all it is meant to do is track performance between various parts of your infrastructure

* **Azure Log Analytics's Network Performance Monitor**: can track loss and latency across  various subnets and set alerts. The Application Gateway analytics solution will provide you with an additional level of network logging, specifically firewall logs, performance logs, and access logs for application gateways


## Security: 

* Azure Security Center service you have one full-featured centralized solution for hardening your entire Azure infrastructure.

* **security policy system**: Security policies let you defined the configuration of your workloads such that they satisfy specific company or regulatory security requirements. When you access the Security Center UI you will discover that there are default policies for all Azure subscriptions. These policies include recommendations that can be turned on or off.


## Operation Automation technologies:

*  Azure Automation is comprised of two core pieces: **Runbooks and Configurations**

* Once done you are ready to start writing **PowerShell runbooks and PowerShell Desired State Configurations (DSC)**. A **runbook** is a simply a collection of scripts. These scripts use the Azure SDK API to execute changes to your Azure system.

* **Desired State Configurations** are special methods within PowerShell that let you predefine a configuration state for your servers. For example you can enforce that specific ports are open or that only a specific set of software is installed.Be warned that DSC Configurations sometimes do tasks in a manner or order you don’t expect. If you have very delicate requirements regarding how and when things change in your system it may be better to write more explicit PowerShell code instead of relying on DSC.

* **Azure Event Grid** and it lets you automate responses to relevant events across both Azure and non-Azure services. Event Grid uses a publish-subscribe model and is configurable in the portal or by using Azure CLI or Powershell scripts.

* **Chef and Puppet**: are two cloud infrastructure automation tools. Both have open source offerings that have integrations with not only Azure, but other providers like Google Cloud and AWS. Chef, modules are described as ‘cookbooks’ with scripts called ‘recipes.’ In Puppet these things are called ‘manifests’ and ‘modules.’ 


## Autoscalig: 

* **Azure Monitor’s built-in autoscale feature**. This lets you automatically scale up and down compute resources based on metrics.
![](https://i.imgur.com/BKbhH07.png)

* Azure VM’s also have a concept known as **‘Scale Sets.’** A Scale Set is simply a group of VM’s that can be given autoscaling rules. They are similar to AWS autoscale groups and make for a handy way to organize and think about your VM’s in terms of large groups instead of individual machines. 
![](https://i.imgur.com/YerVwZu.png)

* **Azure App Service**,  It will allow you to scale based on a designated metric. **Azure Cloud Services** The difference here is that scaling is based on number of cores being used. Depending on your subscription you may have a limit for a maximum number of cores for autoscaling. 

*  If you can adopt a serverless paradigm wherein your app logic is defined using **Azure Function**s, then you won’t need to think about autoscaling at all. The Azure platform automatically allocates computer resources as necessary to any code running as an Azure Function in your account.


## Task Automation: 

![](https://i.imgur.com/cc46u88.png)

* you are already very comfortable with Chef, then it trivial to automate any task defined in your Chef code on subsets of your servers. There is an easy to use cron Chef cookbook that lets you define cronjobs. One common use-case is to automate the chef-client run itself to run every few minutes. This ensures that configuration changes are automatically propagated quickly.

![](https://i.imgur.com/ZEG1iAi.png)

* **An Azure Powershell Workflow uses runbooks** to execute a series of tasks. Workflows add a number of useful features to your Runbooks. For one, they can be scheduled, and they can include automated failure recovery and retry logic. Workflows can help automate many simple maintenance tasks. **For example**, you can create workflows that save your environment state every day at 8 pm and then delete unneeded resources. Then you can have another workflow that executes a runbook to recreate everything the next day at 8 am. This would cut your Azure hourly costs in half.

![](https://i.imgur.com/w6idiYt.png)


* **Azure has its Logic Apps system**. if you are not comfortable with scripts. Azure Logic Apps let you automate and schedule workflows. Logic Apps are similar to Powershell scripts in that they can include conditional statements, switches, loops, and branches. 

# Optimizing Azure Costs

## Analyze current cost
![](https://i.imgur.com/cesY7j8.png)

## Optimize compute cost

![](https://i.imgur.com/uEtC9TV.png)


![](https://i.imgur.com/HDwhgqA.png)

## Virtual machine scale set

* it is recommended that you only use the auto-scale feature of scale sets with the eviction policy set to delete to avoid the costs of the associated disks and hitting your scale set instance quota limit. 

![](https://i.imgur.com/8pI6ckt.png)

![](https://i.imgur.com/htS2S4l.png)


## Low priority scale set

* do not qualiy for microsoft's SLA

![](https://i.imgur.com/1NvixSx.png)

![](https://i.imgur.com/OBw8F7J.png)

## Virtual machine storage

![](https://i.imgur.com/0BpQPYQ.png)

## Virtual machine disks

![](https://i.imgur.com/NWgy3SP.png)

## Dellocating VM's

![](https://i.imgur.com/1QO8qAi.png)

## reserved VM instances

![](https://i.imgur.com/4lO8DmJ.jpg)

## Bring your own lisence

![](https://i.imgur.com/tGahQW0.jpg)

## Azure's platform as a service

![](https://i.imgur.com/D2M8AZC.png)

## Azure functions

![](https://i.imgur.com/t9jO0eE.png)

![](https://i.imgur.com/5zn9VM6.png)

## Optimize Network Cost

![](https://i.imgur.com/7kvipt7.png)


![](https://i.imgur.com/rlZxvR4.png)

![](https://i.imgur.com/6vsJ5gO.png)

![](https://i.imgur.com/Seb1RkO.png)

## VPN connection and express route

![](https://i.imgur.com/Qkfvrw7.jpg)

![](https://i.imgur.com/x13cCGS.png)

![](https://i.imgur.com/L3ULow5.png)

## Optimize storage cost

![](https://i.imgur.com/fDJX34T.png)


![](https://i.imgur.com/Ew66vF9.png)

## Unmanaged Disks 

* Unmanaged disks are stored as Page Blobs in your storage account. The cost for Page Blobs depends upon the amount of Page Blob storage used, IOPs per Page Blob, throughput per Page Blob, and the type of disk: Premium SSD or Standard HDD. The complications of managing unmanaged disks are why Microsoft recommends that IAAS virtual machines always use managed disks.


![](https://i.imgur.com/biAh0UW.png)

## managed disks 

![](https://i.imgur.com/iynv9cD.png)

![](https://i.imgur.com/kqjhJ1o.png)

![](https://i.imgur.com/vUxQRwu.png)

## Disk Snapshots

* If you are doing it daily basis, it can get out of control so you should use **Azure recovery vault** instead. 

![](https://i.imgur.com/UuZFg73.jpg)

![](https://i.imgur.com/1dFJ2wq.png)

![](https://i.imgur.com/QTEW1dm.png)

* You can create policies for the liecycl of the data hot to cold to archive to delete

![](https://i.imgur.com/YYuCfYO.png)


## optimize identity cost

![](https://i.imgur.com/WPFxjVl.png)

![](https://i.imgur.com/Q1rmNWB.png)

![](https://i.imgur.com/ZUTgUtq.png)

![](https://i.imgur.com/rqe6cfW.png)

## Optimize app services and cloud services

![](https://i.imgur.com/IPsWG66.png)


![](https://i.imgur.com/SzrWUqm.png)

* basic plan B sereis instances no auto scaling

![](https://i.imgur.com/efbeA6J.png)

* standard service plan S sereis instance with auto scale

![](https://i.imgur.com/VOb2Ruk.png)

![](https://i.imgur.com/dN9anfB.png)

![](https://i.imgur.com/GbLR39I.png)

![](https://i.imgur.com/HlWjAXC.png)

* Cloud service is essentially a container for your web app deployment

## Azure cloud services

![](https://i.imgur.com/cW9xhpH.png)

![](https://i.imgur.com/fX027Wl.png)

## Staging slots

* staging slots are used in cloud services

![](https://i.imgur.com/bOre53y.png)

![](https://i.imgur.com/C8Oq4Oc.png)

