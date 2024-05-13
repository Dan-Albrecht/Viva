---
title: "Manage admin roles in Viva Engage"
description: "Learn about admin roles and permissions in Viva Engage and how to assign them."
ms.reviewer: ethli
ai-usage: AI-assisted
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 03/25/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
- essentials-manage
search.appverid:
- MET150
---

# Manage administrator roles in Viva Engage

To perform administrative tasks and facilitate many of the premium features in Viva Engage, users need to be assigned specific roles. The table below describes each of the admin roles in Viva Engage and the business functions they enable.  

*Select a role in the table to learn more about it.*

|Admin role|Business function|
|------------|----------------|
|[Microsoft 365 Global Administrator](#microsoft-365-global-administrator)| Manages all aspects of Microsoft 365 Entra and services that use Microsoft 365 Entra identities. This role controls admin role assignment and configuration in Viva Engage. As such, global admins have unlimited access to settings and most of its data, including subscription management.|
|[Engage Administrator](#engage-administrator)| Configures and manages all aspects of Viva Engage including tenant settings, core and premium features, and compliance |
|[Verified Administrator](#verified-administrator)| Configures the Viva Engage network. Performs tasks that have legal implications, such as managing security settings, monitoring keywords for appropriate use, managing data retention, and exporting data. | 
|[Network Administrator](#network-administrator)| Configures the Viva Engage network|
|[Answers Administrator](#answers-administrator)| Configures Answers in Viva Engage, manages topics, and enables badges |
|[Corporate Communicator](#corporate-communicator)| Creates and manages official campaigns, defines leaders, and manages content across the organization |
|[Community Administrator](#community-administrator)| Manages day-to-day activity (including usage) within a community to keep it engaged and productive|

## Who assigns roles and where?

Some admins have more permissions than others and can assign Viva Engage roles to users. The following table lists admins in order of their permissions, with those having the most permissions at the top.

|Admin role | Can assign these roles |Assigned in|
|------------|-------|--------|
|Microsoft 365 Global Administrator|Other global admins, Engage admins, Answers admins (Knowledge manager)|Microsoft Entra ID|
|Engage Administrator|Verified admins, Network admins, Corporate communicators|Microsoft Entra ID|
|Verified Administrator|Verified admins, Network admins, Corporate communicators|Yammer admin center / Viva Engage admin center|
|Network Administrator|Other network admins, Corporate Communicators|Yammer admin center / Viva Engage admin center|
|Community Administrator|Other community admins|Viva Engage community|

## Role hierarchy

:::image type="content" source="../media/engage/admin/engage-admin-hierarchy.png" alt-text="Diagram that shows the hierarchy of administrator roles in Viva Engage, with roles having the most power at the top.":::

## Microsoft 365 Global Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Assigns or removes the [Microsoft 365 Global administrator role](/microsoft-365/admin/add-users/about-admin-roles#commonly-used-microsoft-365-admin-center-roles)</li><li>Manages other Microsoft 365 services</li><li>Views reports in the Microsoft 365 Usage Reporting dashboard</li><li>Sets up and manages Viva Engage</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**| See [Assign admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles)|

## Engage Administrator  

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Configures Viva Engage and its features for the organization, including data management and compliance, network settings</li><li>For Viva Engage core, assigns Corporate Communicator role</li><li>For Viva Engage premium, assigns additional permissions and features:<ul><li>Identify leaders and their audiences</li><li>Storylines, advanced settings, and notifications</li><li>Analytics features and data collected for metrics</li><li>Official campaign creation, management, and analytics</li><li>Answers, and badge management</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**| Assign the Engage admin role either in [Microsoft Entra ID](/microsoft-365/admin/add-users/assign-admin-roles) or [Privileged Identity Management (PIM)](/entra/id-governance/privileged-identity-management/pim-how-to-add-role-to-user)|

## Verified Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Manages content policies, monitors keywords, data retention, security settings, and reading data in private communities</li><li>Assigns verified and network admin roles</li><li>Identify leaders and their audiences</li><li>Exports data and performs integrations with other tools</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator, Engage admin, or verified admin|
|**How to assign**|In the [Yammer admin center](https://www.yammer.com/yammertest10.onmicrosoft.com/), select **Admins**.  Find and select the user's name and select **Make this user an admin**. If the user is already an admin, find their name from the Current Admins list and select **Grant Verified Admin**.</li></ul>|

## Network Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Configures network settings, usage policy, and user profiles</li><li>Manages internal users, outside guests, and unlisted groups</li><li>Can close and reopen conversations in communities and storylines on behalf of any user<li>Identify leaders and their audiences</li><li>Can view reports in the Microsoft 365 Usage Reporting dashboard</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator, Engage admin, or network admin|
|**How to assign**|In the [Yammer admin center](https://www.yammer.com/yammertest10.onmicrosoft.com/), select **Admins**.  Find and select the user's name and select **Make this user an admin**. If the user is already an admin, find their name from the Current Admins list and select **Grant Network Admin**.</li></ul>|

## Answers Administrator  

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Set up, configure, and enable Answers in Viva Engage</li><li>Delete and close Answers posts><li>Manage topics in Answers</li><li>Manage badges</li><li>View global insights</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**|Assign a [Knowledge Manager role in Microsoft Entra ID](/entra/identity/role-based-access-control/permissions-reference)</li></ul>|

## Corporate Communicator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Create and manage official campaigns</li><li>Identify leaders and their audiences</li><li>Send announcements</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator or an Engage admin|
|**How to assign**|Viva Engage admin center</li></ul>|

## Community Administrator

|Function |Details |
|--------|-----------------|
|**Permissions** |Permissions apply only to the community they administer:<ul><li>Adds and removes members and community admins.</li><li>Manages conversations, including marking best answers, removing posts, and closing posts to replies.</li><li>Manages settings, such as customizing the appearance and changing the default post type.</li><li>Posts announcements.</li></ul>
 |**Who can assign**|Engage admins can assign community admins. Additionally, any Engage user who creates a community is automatically assigned the community admin role. Community admins can assign up to 100 other community admins.<br>**Note:** Network admins and verified admins can prevent Engage users from creating communities. In this case, they must assign the initial community admin who performs all community admin tasks. |
|**How to assign**|On the community page, select **Settings** icon > **Manage Members and Admins**. Choose a user and select either **Make Admin** or **Revoke Admin**.|
