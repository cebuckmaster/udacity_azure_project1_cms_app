# Write-up

### Analyze, choose, and justify the appropriate resource option for deploying the app.
#
The CMS App can be deployed on either a Azure Virutal Machine or an Azure App Service.  

A Virtual Machine (VM) in Azure removes the need for a you to manage the hardware and infrastucture, but still gives 
you the control over the operating system. The cost of a VM ranges based on the number of processors/cores, amount of RAM and storage needed.
A single VM system has limited scalability, but utilizing Azure VM scale sets allow for load balancing and scaling across multiple VM, which comes at additiona cost. 
VMs can be grouped into an availability set to increase redundancy and availabilty.  This increase the fault tolarene of a VM but requires you to use Azure managed disk
at an additonal cost.  Having control over the operating system comes with a downside.  It is up to the user/developer to maintain the OS patches and updates.  

An Azure Apps service removes all requirements of maintaining a virtual machine and allows the user/developer to focues on application and data development. App Services range in price based on size.   App Services has autoscaling as a built in service and has integrated load balancer.  Apps Servers can have integrated workflow into a code repository or Azure Dev Ops for continues integration and continues deployment of application changes.  

## Detail differences across resources

| Criteria | Virtual Machine | App Service |
|----------|-----------------|-------------|
| Application composition| Agnostic      | Applicaitons, containters|
| Density| Agnostic| Multiple apps per instance|
|State Management| Stateless or Stateful | Stateless|
| Web Hosting | Agnostic | Built in|
|Autoscaling | Need VM Scale Sets| Built-in Service|
|Load Balancer| Need Azure LB | Integrated|





#
## Choice for CSM App

For the CMS Article application I am choosing Azure App Services to quickly deply this python based web application.  Since will will be the most cost effective and provide the reliabilty and scaling I might need as this application popularity increases.

#

## Change from App Service to VM

Since the CMS Artical is a web application based on a supported language, in this case python, with low expected processor requirements and disk space and utilizing build pipelines via GITHUB it makes seens to select Azure App Services for this deployment.   If the CMS Artical appliction requires 3rd party software or requires remote desktop access then utilizing Azure Virtual Machines would be a better choice.  Additional factors would be based on Azure App Services maximum size limitations of 8vCPU and 32GB of memory and needing to auto scale above 20 instances.  If the CMS application required more resources then Azure Virtual Machine would be better solution.  Also if the CMS Applicaiton reqired more control of the operating system libraries then Azure VMs would be a better solution.  


