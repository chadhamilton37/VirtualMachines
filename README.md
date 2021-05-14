# Virtual Machine ARM Templates

## Domain Joined VMs
In order to use the domain joined VM template, an existing Azure virtual network is required with custom DNS configured on the VNET that can resolve the FQDN of the AD DS domain.

### *Template*
The template and parameters file contained in the "domainJoinedVm" folder will achieve the following:
* Create a new Windows Server 2019 Datacenter VM with a Premium Managed Disk
* Create an Availability Set for the VM
* Join the VM to an existing domain

### *NOTE*
Azure Key Vault is used to store the local admin password and domain join password in this scenario. The template then securely pulls those values at the time of deployment.
