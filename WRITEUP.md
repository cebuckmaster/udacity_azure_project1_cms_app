# Write-up

### Analyze, choose, and justify the appropriate resource option for deploying the app.
#
The CMS App can be deployed on either a Azure Virutal Machine or an Azure App Service.  

A Virtual Machine (VM) in Azure removes the need for a you to manage the hardware and infrastucture, but still gives 
you the control over the operating system. The cost of a VM ranges based on the number of processors/cores, amount of RAM and storage needed.
A single VM system has limited scalability, but utilizing Azure VM scale sets allow for load balancing and scaling across multiple VM, which comes at additiona cost. 
VMs can be grouped into an availability set to increase redundancy and availabilty.  This increase the fault tolarene of a VM but requires you to use Azure managed disk
at an additonal cost.  Having control over the operating system comes with a downside.  It is up to the user/developer to maintain the OS patches and updates.  

A Azure Apps service removes all requirements of maintaining a virtual machine and allows the user/developer to focues on application and data development. App Services range in price based on size.   App Services has autoscaling as a built in service and has integrated load balancer.  Apps Servers can have integrated workflow into a code repository or Azure Dev Ops for continues integration and continues deployment of application changes.  

#
## Choice for CSM App

For the CMS Article application I am choosing Azure App Services to quickly deply this python based web application.  Since will will be the most cost effective and provide the reliabilty and scaling I might need as this application popularity increases.

#

## Change from App Service to VM

If the CMS Article application required 3rd party software or required a mix of Linux and Windows sytems then 
using Virtual Machines would be a better choice for the application enviroment.  Also if you need to have more control over the operating system for special configurations a VM would be a better choice. 


