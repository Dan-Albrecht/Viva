---
title: Set up and use Distribution Lists in Viva Glint
description: "Distribution lists define which employees within an organization should receive a survey."
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 04/28/2023
---

# Set up and use Distribution Lists in Viva Glint

Distribution Lists define which employees within your organization should receive a survey. When creating a Distribution List, start with the list of all active employees and then refine this list using employee attributes. This creates a custom list of employees that can be chosen as recipients for any Microsoft Viva Glint program within your organization.

Distribution Lists are essential when a survey program isn't intended to be sent to all active employees.  

## Create, edit, or delete a Distribution List 

In surveys, you can use existing Distribution Lists or edit or create new ones. 

There are two ways to access Distribution Lists: 

From the admin dashboard:
 
1. Select the  **Configure** symbol.
 
1. Select  **Distribution Lists**  under the  **Employees** section.  

Or, from your survey program: 

1. Select the  **Configure**  symbol at the top right of your Viva Glint dashboard. 

1. Select  **Survey Programs**  in the **Survey** section. 

1. Select the survey for which the Distribution List needs to be edited. 

1. Select the  **Distribution page**  in  **Program Summary**. 

1. Select the pencil symbol to Modify Distribution Lists.  

### Create a new list  

The first page that appears displays all Distribution Lists that exists for your organization and indicates the number of members in each list. 

1. Select  **+ New Distribution List**. 
1. Enter a title for your list by selecting the pencil symbol next to the Untitled Distribution List box. For example, if you're creating a Distribution List for new employees, you could title your list *New Employees* or *New Hires.* 
1. Select  **Add/Edit Employees**.

### Add attribute rules to create a new list 

There are two options:
 
- All active employees 
- Filter all active employees 

#### All Active Employees 

1. Select  **I want to include all active employees only**. 
1. For an Exit survey, consider enabling  **Include Inactive Employees**, located below the selection box. To include inactive employees, contact them via their personal email; ensure you have a personal email when an employee leaves your organization, if possible. 

1. If you need to exclude someone, search for their name and select **Exclude**. 

1. Conversely, if you need to remove someone from the Excluded list, search their name and select  **Remove**. 

1. Confirm your list and select  **Save Changes**. 

#### Filter all Active Employees 

1. Select  **I want to filter all active employees by the following populations**. 

1. Select  **+ New Population**. 

1. Select  **+ Add Filter** to select the attribute you want to use to filter your employee list. Your attribute list is unique to your organization based on your Employee Attribute File. 

1. Select  **Done**. 

1. For an Exit survey, consider enabling "Include Inactive Employees," located below the selection box. To include inactive employees, contact them via their personal email.  

1. If you need to exclude someone, search for their name and select  **Exclude**. 

1. Conversely, if you need to remove someone from the Excluded list, search their name and select  **Remove**. 

1. Confirm list and select  **Save Changes**. 

   > [!NOTE]
   >The date range selected for an attribute should always be equal to or greater to the frequency at which you update your Employee Attribute File. For companies that integrate their Human Resources Information System (HRIS) files automatically, this will work well. For companies that manually update files, ensure that the window you’ve set is wide enough to include the frequency with which employee data is refreshed. For example, if a window is set to 15 days but employee files are only updated once every 30 days, the survey will likely miss people who should get the survey, since the date range is only set to look at people who started 30-45 days earlier. Instead, set the window for at least 30 days so you are sure to include everyone.

After selecting an attribute, you'll see a list of employees that match your criteria. From here, employees can be manually excluded by selecting that employees name in the Included box and then selecting **Exclude** when it appears.

   > [!NOTE]
   >You do not have the option to manually include employees.

## Modify a Distribution List 

Editing a Distribution List is a global change and will affect any program using that list. To modify: 

1. Select the Distribution List you want to modify. 

1. Select  **Add/Edit Employees**  or  **Edit Attribute Rules**  if there are filters available. 

1. Make the necessary changes and select  **Save Changes**. 

After confirming you have the list you want, select  **Save Changes**. 

## Understand why frequency of updating your Employee Attribute File matters 

The date range selected for an attribute should always be equal or greater to the frequency at which you update your employee data files. For companies that integrate their HRIS files automatically, this works well. For companies that manually update employee files, make sure that the window set is wide enough to include the frequency with which employee data is refreshed. For example, if a window is set to 15 days but employee files are only updated once every 30 days, the survey will likely miss people who should get the survey, since the date range is only set to look at people who started 30-45 days earlier. Instead, set the window for at least 30 days so you're sure to include everyone.

> [!TIP]
> Consider using the blended membership functionality, explained below.

## Use the blended membership Distribution List functionality

Dynamic attributes automatically add and remove users to and from a distribution list. They can also include or exclude certain users from a list. Knowing how your distribution list has been populated helps you make decisions about how to add users.

### View how a Distribution List was populated

From the Distribution Lists page, the far-right column entitled **Membership Type** defines if the list in that row has been populated manually, by attribute rules, or both.

> [!Note]
> If a distribution list is populated by an Import, it will have the membership type "manual".

## Use the dynamic Distribution Lists functionality
Your decision whether to use manual population or attribute rule population should be guided by these principles:

<ul><li>If membership type is based on Attribute Rules and a user is manually added in the platform, employee data file imports (i.e. Rubicon) will automatically update the Distribution List.</li>
 <li>If the Distribution List began manually, adding attribute rules will change the list to include both Attribute Rules and Manual.</li>
<li>If a manually added member is deleted and they match the filter criteria, they'll still appear in the Distribution List, but the Added by method will change from Manual to Attribute Rules.</li></ul>

> [!IMPORTANT]
> Importing users to an Attribute Rules Distribution List removes existing rules.
>  <ul><li>Activate the **Preserve the employees already in this distribution** list functionality to convert membership type to **Manual** for existing users.</li>
>  <li> Uncheck to deactivate and remove the users based on the rules, and only include those in the import file. </li><ul>
