<p align="center">
  <img src = "https://dmsiworks.com/wp-content/uploads/Is-Business-Central-on-Azure.jpg" width=600 height=400>
</p>


## 🚩 Table of Contents

- [Resource Manager](#resource-manager)
- [Azure Resource Terminology](#azure-resource-terminology) 

---


## Resource Manager:

<p align="center">
  <img src = "https://learn.microsoft.com/en-us/training/wwl-azure/use-azure-resource-manager/media/resource-manager-016a1bac.png" width=600 height=400>
</p>


- Your application’s infrastructure is composed of many interrelated and interdependent components. These could include a virtual machine, storage account, virtual network, web app, database, database server, and third-party services.
- These components are not separate, but parts of a single entity that you want to deploy, manage, and monitor as a group.
- Azure Resource Manager allows you to manage the resources in your solution as a group.

### Benefits:

- You can deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
- You can repeatedly deploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.
- You can manage your infrastructure through declarative templates rather than scripts.
- You can define the dependencies between resources so they're deployed in the correct order.
- You can apply access control to all services in your resource group because Role-Based Access Control (RBAC) is natively integrated into the management platform.
- You can apply tags to resources to logically organize all the resources in your subscription.
- You can clarify your organization's billing by viewing costs for a group of resources sharing the same tag.



---



## Azure Resource Terminology: 

- resource - A manageable item that is available through Azure. Some common resources are a virtual machine, storage account, web app, database, and virtual network, but there are many more.
- resource group - A container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you want to manage as a group. You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization.
- resource provider - A service that supplies the resources you can deploy and manage through Resource Manager. Each resource provider offers operations for working with the resources that are deployed. Some common resource providers are Microsoft.Compute, which supplies the virtual machine resource, Microsoft.Storage, which supplies the storage account resource, and Microsoft.Web, which supplies resources related to web apps.
- template - A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group. It also defines the dependencies between the deployed resources. The template can be used to deploy the resources consistently and repeatedly.
- declarative syntax - Syntax that lets you state "Here is what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure.

The name of a resource type is in the format: {resource-provider}/{resource-type}. For example, the key vault type is Microsoft.KeyVault/vaults.



---



## Entra ID:

- Microsoft Entra ID is a cloud-based, multi-tenant directory service included in Azure subscriptions.
- It provides advanced features like multi-factor authentication and identity protection.
- It’s used for secure access to cloud resources, managing users, and configuring access to applications.
- It differs from traditional AD DS, focusing more on web-based apps and modern management.
- Each Azure subscription is associated with one Microsoft Entra tenant, but a tenant can be associated with multiple subscriptions.
- The Microsoft Entra schema is simpler than AD DS and is extensible.

When comparing AD DS with Microsoft Entra ID, it’s important to note the following characteristics of AD DS:

    AD DS is a true directory service, with a hierarchical X.500-based structure.
    AD DS uses Domain Name System (DNS) for locating resources such as domain controllers.
    You can query and manage AD DS by using Lightweight Directory Access Protocol (LDAP) calls.
    AD DS primarily uses the Kerberos protocol for authentication.
    AD DS uses OUs and GPOs for management.
    AD DS includes computer objects, representing computers that join an Active Directory domain.
    AD DS uses trusts between domains for delegated management.

When comparing Microsoft Entra ID with AD DS, it’s important to note the following characteristics of Microsoft Entra ID:

    Microsoft Entra ID is primarily an identity solution, and it’s designed for internet-based applications by using HTTP (port 80) and HTTPS (port 443) communications.
    Microsoft Entra ID is a multi-tenant directory service.
    Microsoft Entra users and groups are created in a flat structure, and there are no OUs or GPOs.
    You can't query Microsoft Entra ID by using LDAP; instead, Microsoft Entra ID uses the REST API over HTTP and HTTPS.
    Microsoft Entra ID doesn't use Kerberos authentication; instead, it uses HTTP and HTTPS protocols such as SAML, WS-Federation, and OpenID Connect for authentication, and uses OAuth for authorization.
    Microsoft Entra ID includes federation services, and many third-party services such as Facebook are federated with and trust Microsoft Entra ID.
    
- When you deploy cloud services such as Microsoft 365 or Intune, you also need to have directory services in the cloud to provide authentication and authorization for these services. Because of this, each cloud service that needs authentication will create its own Microsoft Entra tenant.

- Directory-synchronized identity	User accounts that have a directory-synchronized identity are defined in an on-premises Active Directory. A synchronization activity occurs via Microsoft Entra Connect to bring these user accounts in to Azure. The source for these accounts is Windows Server Active Directory.

### Create group accounts:

- Use security groups to set permissions for all group members at the same time, rather than adding permissions to each member individually.
- Add Microsoft 365 groups to enable group access for guest users outside your Microsoft Entra organization.
- Security groups can be implemented only by a Microsoft Entra administrator.
- Normal users and Microsoft Entra admins can both use Microsoft 365 groups.

## Resource tags:

- Each resource tag has a name and a value.
- The tag name remains constant for all resources that have the tag applied.
- The tag value can be selected from a defined set of values, or unique for a specific resource instance.
- A resource or resource group can have a maximum of 50 tag name/value pairs.
- Tags applied to a resource group aren't inherited by the resources in the resource group.


## Management Groups:

- By default, all new subscriptions are placed under the top-level management group, or root group.
- All subscriptions within a management group automatically inherit the conditions applied to that management group.
- A management group tree can support up to six levels of depth.
- Azure role-based access control authorization for management group operations isn't enabled by default.
