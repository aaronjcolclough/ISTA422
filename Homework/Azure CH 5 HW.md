1. What is a VNET and what is it used for in Azure?

Virtual networks (VNets) are used in Azure to provide private connectivity for Azure Virtual Machines (Azure VMs) and some Azure services. VMs and services that are part of the same virtual network can access one another.

2. The fully managed service in Azure that is used for cross-premises connectivity, is called what?

A Virtual Network Gateway is a fully managed service in Azure that is used for cross-premises connectivity.

3. List three things you need to know when setting up a virtual network.

When creating a virtual network, there are a few things you need to know, such as the address space, subnets, and DNS servers that you want to use.

4. What is the primary purpose of establishing a subnet?

You do this to break up your network into more manageable sections.

5. When in the deployment process of multiple Virtual Machines(VMs) are the VMs assigned their IP
address?

VMs are assigned an IP address when they are deployed. If you deploy multiple VMs into a virtual network or subnet, they are assigned IP addresses as they boot up.

6. Why should you set the location of the Resource Group?

Although not required, it’s best to specify the same Azure region that will be used for the resources when they are created.

7. What are the four rules to editing a template to redeploy?

If you remove a resource from the template that is not in the resource group, that resource will be unchanged. It won’t be removed simply because it’s gone from the template. (If you want to remove a resource, you have to specifically remove it using the Azure portal, PowerShell, the Azure CLI, etc.) If you add a resource to the template that is not in the resource group, it will create that resource for you when you redeploy the template. Resources that are unchanged but are still in the template will be ignored. Resources that are changed and still in the template will be updated. For example, if we change the address prefixes of our virtual network and redeploy the template, it will change them in the deployed VNet.

8. Why should you not request a complete deployment using PowerShell?

If you use PowerShell it will delete the resources that are in the resource group and you can't recover it.

9. Why did Microsoft create NSGs?

Microsoft created NSGs to provide a flexible method for defining the access rules allowing traffic into and out of a VM in a VNet—or even an entire subnet in the VNet.

10. What is a VPN according to the book?

A VPN Gateway is an Azure managed service that is deployed into a VNet and provides the endpoint for VPN connectivity for point-to-site VPNs, site-to-site VPNs, and ExpressRoute. This gateway is the connection point into Azure from either the on-premises network (site-to-site) or the client machine (point-to-site). 
