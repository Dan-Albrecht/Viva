---
ms.date: 02/02/2024
title: "Add, edit, and remove cards from the Viva Connections dashboard"
ms.reviewer: evanatkin
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - highpri
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Learn how to edit the Viva Connections dashboard"
---

# Create a Viva Connections dashboard and add cards

The Viva Connections dashboard provides fast and easy access to information and job-related tasks. Content on the dashboard can be targeted to users in specific roles, markets, and job functions.
The dashboard consists of cards that engage viewers with existing Microsoft Teams apps, Viva apps and services, third-party apps, custom solutions using the SharePoint Framework (SPFx) framework, internal links, and external links.

![Screenshot that shows a Dashboard example for desktop and mobile.](../media/connections/vc-dashboard-flw.png)

**This article includes:**

- [Edit the dashboard and add cards](#edit-the-dashboard).
- [Add the Approvals card](#add-the-approvals-card).
- [Add an Assigned tasks card](#add-the-assigned-tasks-card).
- [Add a customized card using Card designer](#design-your-own-card-with-a-quick-view).
- [Add a Teams app card](#add-a-teams-app-card).
- [Add a third-party card or Microsoft app](#add-a-third-party-card-or-microsoft-app).
- [Add the News card](#add-the-news-card).
- [Add the People card](#add-the-people-card).
- [Add the Events card](#add-the-events-card).
- [Add a Shifts card](#add-a-shifts-card).
- [Add a Viva Learning card](#add-a-viva-learning-card).
- [Add a Topics card](#add-a-topics-card).
- [Add a Web link card](#add-a-web-link-card).
- [Apply audience targeting to cards](#apply-audience-targeting-to-cards).
- [Preview your dashboard to see how it displays for different audiences and devices](#preview-your-dashboard-to-see-how-it-displays-for-different-audiences).
- [Add the dashboard to your Viva Connections site using the Dashboard web part](#use-the-dashboard-web-part-for-viva-connections).
- [Get more information about how links and Single sign-on works](#how-urls-and-single-sign-on-works).

## Edit the dashboard

The Viva Connections dashboard can be edited right from Microsoft Teams. You’ll need member or owner level permissions to get started.

![Diagram of how to create a Viva Connections Dashboard.](../media/connections/viva-dashboard-step.png)

> [!NOTE]
>
> - When setting up Viva Connections for the first time, you’ll be asked to choose a set of default cards based on the intended audience.
> - You can choose mobile and desktop views interchangeably as you’re authoring.
> - Image recommendations for cards in the dashboard: medium cards should be 300x150 to 400x200 with 2:1 aspect ratio and large cards 300x300 to 400x400 with 1:1 aspect ratio to prevent stretching in the mobile app.
> - Image URLS in card properties must be an absolute URL for the link to work in the mobile app.
> - It's recommended to limit the number of cards to about 20 on the dashboard for the best viewing experience.
> - Users will be able to [customize their dashboard on Viva Connections mobile](https://support.microsoft.com/office/753e0607-0bfd-4712-ad7e-18490dd565a2#bkmk_customize-viva-connections-mobile-dashboard) by reordering, hiding, and showing cards. These changes only affect the mobile experience for the user and will not affect their desktop or tablet experience.

1. Navigate to the Viva Connections app in Teams.
2. Next, select **Edit** in the dashboard section.
3. Select **+ Add a card**.
4. Select **Edit** (pencil icon) for each card to edit properties like the label, icon, image, and audience targeting settings where applicable.
5. Select **Delete** (trash can icon) to remove cards.
6. Preview the experience on all devices to ensure usability before publishing or republishing.
7. **Publish** or **Republish** when you're done to share the edits with others.

## How to edit the dashboard from SharePoint when you have a home site

If your organization has a [SharePoint home site](home-site-plan.md), you'll be able to set up and edit the dashboard from the SharePoint home site or in Microsoft Teams. You’ll need [edit permissions](/sharepoint/customize-sharepoint-site-permissions) for the SharePoint home site.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE53Joj]

<br>
<br>

> [!NOTE]
>Images are an important aspect to making your cards rich and inviting. If you're a SharePoint admin, we recommend enabling a Content Delivery Network (CDN) to improve performance for getting images. Consider when storing images that /siteassets is by default a CDN source when Private CDN is enabled while /style library is the default source when the Public CDN is enabled. [Learn more about CDNs](/office365/enterprise/content-delivery-networks).  

1. From the SharePoint home site, select the **Settings** gear at the top-right of the page.
2. Select **Manage Viva Connections**.
3. Select the **+ Create dashboard** or **View dashboard** button.
4. Select **+ Add a card**.
5. Select the type of card you want to add from the dashboard card toolbox and then use the instructions later in this article to set up each type of card. As you’re building the dashboard, you can preview its appearance in mobile and desktop for different audiences.
6. When you're done adding cards and [applying targeting to specific audiences](use-audience-targeting-in-viva-connections.md), **Preview** the experience to ensure an ideal viewing experience.
7. Once you’re satisfied with how the dashboard looks in preview, select **Publish** or **Republish** at the top-right of your dashboard to make it available for use on your home site, in Teams, and in Teams mobile app.

## Available dashboard cards

   |Card Name    |Toolbox icon   | Description  |
   |:------------|:-------------:|:--------------|
   |[Approvals](#add-the-approvals-card) | ![Image of the approvals card icon.](../media/connections/approvals-card-icon.png) | Use [Approvals](/power-automate/get-started-approvals) for vacation requests, sign off on documents, and approve expense reports.     |
   |[Assigned Tasks](#add-the-assigned-tasks-card) | ![Image of the assigned tasks card icon.](../media/connections/assigned-tasks-card-icon.png) |   Use [Tasks](https://support.microsoft.com/office/use-the-tasks-app-in-teams-e32639f3-2e07-4b62-9a8c-fd706c12c070) to manage your team's work, assign tasks, and track tasks.     |
   |[Card designer](#design-your-own-card-with-a-quick-view) | ![Image of the card designer icon.](../media/connections/card-designer-card-icon.png) | Create your own cards and quick views using the [adaptive cards framework.](/adaptive-cards/templating/)|
   |[Shifts](#add-a-shifts-card)     |![Image of the shifts card icon.](../media/connections/shifts-card-icon.png) | Display information about the next or current shift from the Shifts app in Teams.          |
   |[Teams app card](#add-a-teams-app-card) | ![Image of the Teams app icon.](../media/connections/teams-app-icon.png) |   Use to open a Teams personal app or bot specified by the dashboard author.     |
   |[Third-party cards](#add-a-third-party-card-or-microsoft-app) | Varies |    Use cards that integrate [third-party services.](https://cloudpartners.transform.microsoft.com/resources/viva-app-integration)     |
   |[News card](#add-the-news-card)    | ![Image of the News card icon.](../media/connections/news-card-icon-no-border.png) |   Promote news from a variety of sources that you wish to prominently display, including [boosted news from SharePoint.](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83)     |
   |[People card](#add-the-people-card)    | ![Image of the People card icon.](../media/connections/people-card-icon-no-border.png) |   Provide an option to look up contact information and directly chat, email, or call with others in your organization.     |
   |[Events card](#add-the-events-card)    | ![Image of the Events card icon.](../media/connections/events-card-icon-no-border.png) |   View and join upcoming events within your organization.     |
   |[Viva Learning](#add-a-viva-learning-card)    | ![Image of the Viva Learning card icon.](../media/connections/create-dashboard/viva-learning-card-icon-2.png) |  Provide a link to the Viva Learning app that can be targeted to show to certain audiences.  |
   |[Topics](#add-a-topics-card)    | :::image type="icon" source="../media/knowledge-management/viva-topics-cards-toolbox.png"::: |  Use Topics cards to encourage knowledge discoverability, engagement, and sharing. |
   |[Web link](#add-a-web-link-card)    | ![Image of the web link card icon.](../media/connections/web-link-icon.png) |  Access a site without leaving the Viva Connections app  |

## Add the Approvals card

The Approvals card connects to [Approvals in Microsoft Teams](https://support.microsoft.com/office/what-is-approvals-a9a01c95-e0bf-4d20-9ada-f7be3fc283d3) and is a way to streamline all of your requests and processes with your team or partners. You can create new approvals, view the ones sent your way, and see all of your previous approvals in one place.

![Example of an approvals card.](../media/connections/approvals-card-example.png)

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **Approvals** from the dashboard toolbox.

   ![Adding a approvals card.](../media/connections/approvals-card-1.png)

3. Select the pencil icon to **Edit** the card. In the property pane that opens on the right side of the screen, choose your card size from the **Card size** drop-down list.

   ![Adding an approvals card in the dashboard.](../media/connections/approvals-edit.png)

4. Once you’re satisfied with how the dashboard looks in preview, select **Publish** or **Republish** at the top-right of your dashboard to make it available for use on your SharePoint home site, in Teams, and in the Teams mobile app.

## Add the Assigned tasks card

The Assigned tasks card enables automatic display of information to users about their assigned tasks. This information is retrieved from the [Tasks app in Teams](https://support.microsoft.com/office/use-the-tasks-app-in-teams-e32639f3-2e07-4b62-9a8c-fd706c12c070).

![Example of an assigned tasks card.](../media/connections/assigned-tasks-card-example.png)

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **Assigned Tasks** from the dashboard toolbox.

   ![Adding a tasks card in the dashboard.](../media/connections/assigned-tasks.png)

3. In the property pane on the right, choose your card size from the **Card size** drop-down list.

   ![Choosing card size.](../media/connections/choosing-card-size.png)

4. To target your card to specific audiences (that is, only the audience you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Design your own card with a quick view

You can choose the **Card designer** option to design your own card that includes a quick view. To design your own cards, you should be familiar with JSON and Adaptive Card templates. For more information, see [Adaptive Cards Templating](/adaptive-cards/templating/).

   > [!IMPORTANT]
   > The quick view will need to be set up first (see the [Set up a quick view](#set-up-a-quick-view) section).

![Example of a card designer card.](../media/connections/card-designer-card-example.png)

1. While in **edit** mode, select **+ Add a card** from the dashboard.

2. Select **Card designer**.

   :::image type="content" alt-text="This screenshot shows the icon to select to add a Card designer card." source="../media/connections/card-designer-card-icon.png":::

3. In the **property** pane, select your card options.

   ![property pane](../media/connections/card-designer-panel.png)

4. From the **Card size** drop-down list, choose either **Medium** or **Large**.
   A medium-sized card allows you to add one button, while a large-sized card allows you to add two buttons.

5. Enter a title for your card in the **Title** text box.
6. Enter a URL in the **Icon** text box. This URL is the icon's location.
7. Select a template type from one of the following options in the **Template type** drop-down list:
    - **Text**: Provides you with the option to add only a heading.
    - **Text and image**: Provides you with the option to add a heading and an image.
    - **Text and description**: Provides you with the option to add your own heading and a description, but without an image option.

   > [!NOTE]
   > You may provide alternative text (alt text) as descriptive text which conveys the meaning and context of a visual item in a digital setting, such as on an app or web page. [Learn more about alt text](https://support.microsoft.com/office/everything-you-need-to-know-to-write-effective-alt-text-df98f884-ca3d-456c-807b-1a1fa82f5dc2).

8. Depending on the template type you’ve chosen, enter values for the properties. For example, if you have chosen the **Text and description** template type, you have to enter values for the **Heading** and **Description** properties in their respective text boxes.

   > [!NOTE]
   > If you want a specific property to display that allows users to enter a value, but that property is not displayed, choose a different template type.

9. Toggle **Enable card action** to **On** if you want the card to either go to a link or show a quick view when the user selects it.

10. Set the number of buttons to be displayed under **Number of buttons**.
    For a medium-sized card, you can show only one button. For a large-sized card, you can show one or two buttons.

11. Enter values for the following properties of the button:
    - **Title**: Title for the button.
    - **Action**: The result on clicking the button.
    - **Link**: The URL of the destination the user is directed to, on clicking the button.

## Set up a quick view

Under **Quick view layout and data**, enter JSON template code for your quick view layout, and add the code for the data you want to use. For more information on templating and data with some examples, see [Adaptive Cards Templating](/adaptive-cards/templating/). You can find more examples at [Adaptive Cards](/adaptive-cards/).

To target your card to specific audiences (that is, only audiences you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Add a Teams app card

A Teams app card allows you to create a card for an existing Teams app.

![Example of a teams app card.](../media/connections/teams-app-card-example.png)

1. While in **edit** mode, select **+ Add a card** from the dashboard.

2. Select **Teams app** from the web toolbox.

   :::image type="content" alt-text="This screenshot shows the icon to select to add a Teams app card." source="../media/connections/teams-app-icon.png":::

3. In the **property** pane on the right side of the page, select your options.

   ![Teams app property pane.](../media/connections/teamsapp.png)

4. Select a size for the card from the **Card size** drop-down list.

5. Search for the Teams app you want to use, and then select it from the list.
6. Set the card-display options:
    - Enter a title for the card in the **Card title** text box. (This title won't change your page title; it's the title that will be displayed on the top of the card.)
    - Enter a description for the card in the **Card description** text box. This description will be displayed in larger text under the title.
7. If you want to target your card to specific audiences (that is, only the audience you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Add a third party card or Microsoft app

The Viva Connections dashboard and mobile experience can be extended and customized using cards, which are based on [adaptive cards](https://adaptivecards.io/) and the [SharePoint Framework (SPFx)](/sharepoint/dev/spfx/sharepoint-framework-overview). These adaptive cards are used to display data, complete tasks, and connect to Teams Apps, Websites, and mobile apps on Viva Connections. They provide a low-code solution to bring your line-of-business apps into the dashboard.

To create custom experiences on Viva Connections dashboard and Viva Connections Mobile App, developers must use the SPFx to create custom ACEs. To learn more about creating ACEs, see the following tutorial: [Build your first SharePoint Adaptive Card Extension](/sharepoint/dev/spfx/viva/get-started/build-first-sharepoint-adaptive-card-extension). Learn more about [Viva Connections extensibility.](/sharepoint/dev/spfx/viva/overview-viva-connections)

### Add a third party card

There are three ways to get third-party apps and solutions integrated with the Viva Connections dashboard. There are three ways to get third-party apps and solutions integrated with the Viva Connections dashboard. The following is an example of a third-party card.

![Example of a third-party card.](../media/connections/third-party-card-example.png)

#### Option 1: Discover and request apps from the Viva Connections card toolbox

Third-party cards and an entry point to browse more cards in the app store will automatically display in the card toolbox. Depending on your level of permissions, you may need to request the app before it can be used on the dashboard. [Learn more about managing third-party apps](/sharepoint/use-app-catalog).

> [!NOTE]
>
> - Site owners managing the Viva Connections dashboard will need to request third-party apps before they are available in the card toolbox.
> - Some third-party apps require a service plan agreement with your organization.

   :::image type="content" alt-text="This screenshot is of the card toolbox section that displays third party cards." source="../media/connections/third-party-card-toolbox.png":::

1. While in edit-mode, select **+ Add** card from the dashboard.
2. You’ll see third-party options in the **Suggested cards** section. Select one of the cards that’s displayed or browse more cards by selecting **Add more cards**.
3. Request the cards you’d like to add to the toolbox and the requests will be sent to the App Catalog Admin for their approval.
4. You'll receive an email to confirm if your request has been approved or denied.
5. Once your request has been approved, refresh the page, and you’ll see the new card display in the toolbox.

#### Option 2: Acquire the app from a Microsoft AppSource or the SharePoint store

- If you're building a dashboard, you can [request the app directly](https://techcommunity.microsoft.com/t5/microsoft-sharepoint-blog/explore-and-deploy-sharepoint-framework-solutions-from-partners/ba-p/2645289), but you'll need approval from an admin of the tenant-level app catalog to continue with the installation
- If you're an **admin** of a tenant-level app catalog, you can deploy business apps directly.
You can acquire apps from third- party developers by browsing the [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps?product=sharepoint) or [SharePoint store](https://techcommunity.microsoft.com/t5/microsoft-sharepoint-blog/explore-and-deploy-sharepoint-framework-solutions-from-partners/ba-p/2645289) (recommended).

[Get step-by-step guidance](https://techcommunity.microsoft.com/t5/microsoft-sharepoint-blog/explore-and-deploy-sharepoint-framework-solutions-from-partners/ba-p/2645289) on how to request and deploy an app, and add an app to your site. For tenant admin, [learn how to manage apps](/sharepoint/use-app-catalog#work-with-sharepoint-store-apps) in the App Catalog.

#### Option 2: Acquire the app directly from the third-party developer

 > [!NOTE]
 > SharePoint administrative permissions are required to complete this task.

You can request apps directly from the Viva Connections third-party developers and partners. Admin permissions are required to [add the app to tenant level app catalog.](/sharepoint/use-app-catalog)

### Add a Microsoft app as a card on the dashboard

A Microsoft app card allows you to create a card that links to Microsoft apps (For example: Shifts, Approvals, Task, etc.). Microsoft apps cards are available out of the box when Viva Connections is enabled.

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select the Microsoft App you want to add from the web toolbox.

   ![Image of how to find a Microsoft app in the card picker window.](../media/connections/3p-apps-1.png)

3. Select your options in the property pane on the right side of the page.

4. When you **Republish**, the card will appear on your dashboard.

## Add the News card

Add the News card to the Viva Connections Dashboard to promote news from a variety of sources that you wish to prominently display, [including boosted news from SharePoint](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83). If you choose any news posts that have been boosted, they will display in the News card for the duration of the boost period.

![Example of a News card.](../media/connections/top-news-card-example.png)

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **News** from the dashboard toolbox.

    ![Screenshot of the News card icon.](../media/connections/news-card-icon-border.png)

3. Select the **edit pencil** to the left of the card to open the properties pane for the News card.

4. Add a title and select a card size.

5. To target your card to specific audiences (that is, only audiences you specify will see the card in the dashboard), select one or more groups to target. Refer to this article for more information on [Audience targeting](#apply-audience-targeting-to-cards).

6. For a news source, select one of the following options:

   - **Boosted posts**: Will display any SharePoint news post that has been boosted from the organization's news sites only. The word "Boosted" will display at the top of the card.  

   - **From this site**: Pulls news from the hub site that the current site is a part of.

   - **From all sites in this hub**: Pulls news from all sites within your SharePoint hub.

   - **Select sites**: Pulls news from one or more individual sites (if selected, a list of sites associated with your SharePoint hub will display).

   - **Recommended for current user**: will display news posts for the current user from people the user works with; managers in the chain of people the user works with, mapped against the user's own chain of management and connections; the user's top 20 followed sites; and the user's frequently visited sites.

        :::image type="content" source="../media/connections/news-card-properties.png" alt-text="Screenshot showing the News card properties pane."lightbox="../media/connections/news-card-properties.png":::

## Add the People card

The People Search card will automatically retrieve contact information from members of your organization using [Microsoft Entra ID](/entra/fundamentals/new-name) (formerly Azure Active Directory). Users can access the People Search card to look up contact information and can jump into chat, email, or a call with the contact directly from the card view.

   :::image type="content" source="../media/connections/people-card-demo.png" alt-text="Screenshot demonstrating the People card in action looking up contact information."lightbox="../media/connections/people-card-demo.png":::

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **People** from the dashboard toolbox.

    ![Screenshot of the People card icon.](../media/connections/people-card-icon-border.png)

3. Select the **edit pencil** to the left of the card to open the properties pane for the People card.

4. In the property pane on the right, choose your card size from the **Card size** drop-down list.

5. To target your card to specific audiences (only audiences you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

      :::image type="content" source="../media/connections/people-card-properties.png" alt-text="Screenshot of the People card properties pane."lightbox="../media/connections/people-card-properties.png":::

## Add the Events card

The events card can help your users stay informed and engaged with upcoming events in their organization, such as webinars, trainings, town halls, and celebrations. Users can view additional upcoming events or join via teams via the links on the Events card.  The card can be customized and even targeted to specific audiences so only relevant events are displayed.

The Events card is tied to the SharePoint Events web part. Site owners and members will need to access their SharePoint site and use the SharePoint Events web part to add events to their site. For more information, see the article on [using the Events web part](https://support.microsoft.com/office/5fe4da93-5fa9-4695-b1ee-b0ae4c981909).

   :::image type="content" source="../media/connections/events-card-demo.png" alt-text="Screenshot demonstrating the Events card as it displays upcoming events."lightbox="../media/connections/events-card-demo.png":::

> [!NOTE]
> Recurring events are not supported, even if you manually set up a recurrence in the events list that you are using. You'll need to create a new event for each occurrence.

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **Events** from the dashboard toolbox.

    ![Screenshot of the Events card icon.](../media/connections/Events-card-icon-border.png)

3. Select the **edit pencil** to the left of the card to open the properties pane for the Event card.

4. In the property pane on the right, choose your card size from the **Card size** drop-down list.

5. Enter a **Title** for the event card.

      :::image type="content" source="../media/connections/events-card-properties.png" alt-text="Screenshot of the Events card properties pane."lightbox="../media/connections/events-card-properties.png":::

6. Under Content, select a **Source** for your events: **Events list on this site**, **This site**, **This site collection**, **Select sites**, or **All sites**. If your site is connected to a hub site, you will also have an option to select **All sites in the hub** or **Select sites from the hub**.

> [!NOTE]
>
> - When you choose **Select sites**, you can search for the site you want to add, or select one or more sites from **Frequent sites**, or **Recent sites**. You can select up to 30 sites.
   >   - The **Select sites** option is not available in SharePoint Server, U.S. Government GCC High and DoD, and Office 365 operated by 21Vianet.
> - If there is more than one **events list** on the site, you can select the one you want. If you don't have an existing list, the **Events** card creates an empty Events list for you, with the default settings of a Calendar list.
> - If you choose to show events from multiple sites, and don't see all of your events displayed on the page, see [How events from multiple sites are found and displayed](https://support.microsoft.com/office/51891403-0ff7-44ab-b364-a44e86e50573).

7. If your list has **categories**, you can select one by which to filter the events you show.

8. Select a date range by which to filter your events in the **Date range** drop-down list. You can choose **All upcoming events** (the default), **This week**, **Next two weeks**, **This month**, or **This quarter**.

      :::image type="content" source="../media/connections/events-card-content.png" alt-text="Screenshot of the content section in the Events card properties pane."lightbox="../media/connections/events-card-content.png":::

9. Under the layout section, select how many events to be shown at once from the dropdown. Up to 30 events can be shown on one event card.

      :::image type="content" source="../media/connections/events-card-layout.png" alt-text="Screenshot of the layout section in the Events card properties pane."lightbox="../media/connections/events-card-layout.png":::

10. To target your card to specific audiences (only audiences you specify will see the card in the dashboard), **enable audience targeting**. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

      :::image type="content" source="../media/connections/events-card-audience-targeting.png" alt-text="Screenshot of the audience targeting section in the Events card properties pane."lightbox="../media/connections/events-card-audience-targeting.png":::

11. When finished with your selection, you can close the panel. Your settings will autosave.

## Add a Shifts card

The Shifts card shows users information about their next or current shift from the Shifts app in Teams. They can also clock in and out and track break time when Time clock is enabled in Teams.

![Example of a shifts card.](../media/connections/shifts-card-example.png)

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **Shifts** from the dashboard toolbox.

   ![Adding a Shifts app card](../media/connections/shiftsicon.png)

3. In the property pane on the right, choose your card size from the **Card size** drop-down list.

4. To target your card to specific audiences (only audiences you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Add a Viva Learning card

The [Viva Learning](/viva/learning/overview-viva-learning) card provides users quick-links to recommended trainings, and can be set to target specific trainings to certain individuals. Users can easily access their required trainings by selecting the Viva Learning link.

Content in the cards is dynamic and changes according to settings in Viva Learning. The following are three examples of Viva Learning card states that display different information depending on the viewer and Viva Learning settings.

![Example of the Viva Learning card displaying general learning opportunities.](../media/connections/create-dashboard/viva-learning-card-1.png)  ![Example of the Viva Learning card notifying the user of a required training due.](../media/connections/create-dashboard/viva-learning-card-2.png)  ![Example of the Viva Learning card notifying user of upcoming required trainings.](../media/connections/create-dashboard/viva-learning-card-3.png)  

1. While in edit mode, select **+ Add a card** from the dashboard.

2. Select **Viva Learning** from the dashboard toolbox.

    ![Image of the Viva Learning card icon in the dashboard toolbox.](../media/connections/create-dashboard/viva-learning-card-icon.png)

3. In the property pane on the right, choose your card size from the **Card size** drop-down list.

    ![Image of the Viva Learning property pane.](../media/connections/create-dashboard/viva-learning-card-settings.png)

4. To target your card to specific audiences (that is, only audiences you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Add a Topics card

Topics has two different cards. The **Topics Contribute card** can be used to reach people who are known knowledge managers and are already engaged with topics and knowledge areas. Topics and knowledge areas are dynamically displayed in the card based on the viewers interests, current projects, and expertise. The **Topics Discover card** can be used to view topics and knowledge areas for people who could be interested in learning more or contributing to a topic.

[Learn more about the two different cards](/microsoft-365/topics/topics-card-viva-connections).

![Screenshot Topics Contribute card.](../media/knowledge-management/viva-topics-contribute-card.png)

## Add a Web link card

Add a web link card when you want your users to go to an internal or external link on a web site.

![Example of a web link card.](../media/connections/link-card-example.png)

1. While in **edit** mode, select **+ Add a card** from the dashboard.

2. Select **Web link** from the web toolbox.

   :::image type="content" alt-text="This screenshot shows the icon to select to add a web link card." source="../media/connections/web-link-icon.png":::

3. In the property pane on the right side of the page, select your options.

   ![Choosing options.](../media/connections/choosing-options.png)

4. Select a size for the card from the **Card size** drop-down list.
5. Enter the URL for your link in the **Link** text box.
6. Set the card-display options:
   - Enter a title for the card in the **Card title** text box. (This title won't change your page title; it's the title that is displayed on the top of the card.)
   - Enter a description for the card in the **Card description** text box. This description is displayed in larger text under the title.
7. Under **Thumbnail**, select one of the following options:
   - **Auto-selected**: This option when chosen automatically displays an image at the top of your card that comes from your page.
   - **Custom image**: This option when chosen enables the **Change** button.  You can select this button to choose an image you want to use.
8. Under **Card icon**, select one of the following options that enable the icon to be displayed on the left side of the card title:
   - **Auto-selected**: This option when chosen automatically displays a built-in icon associated with the page.
   - **Custom image**: This option when chosen enables the **Change** button.  You can select this button to choose an image you want to use.
   - **Icon**: This option when chosen enables the **Change** button.  You can select this button to choose from a set of stock icons.
9. To target your card to specific audiences (that is, only audiences you specify will see the card in the dashboard), select one or more groups to target. For more information on audience targeting, see [Audience targeting](#apply-audience-targeting-to-cards).

## Apply audience targeting to cards

[Audience targeting can be applied throughout](use-audience-targeting-in-viva-connections.md) the Viva Connections experience, including cards on the dashboard. Audience targeting creates a personalized viewing experience by filtering the most important content to specific groups. Use audience targeting to:

- Create custom views for distinct roles and regions.
- Generate as many different views as needed to create unique experiences.
- Ensure the intended audience sees the most important content.

### Set the target audiences for a card

1. If your page isn't already in **edit** mode, select **Edit** at the top-right of the dashboard page.
2. Select the card you want to target to one or more audiences, and select the **Edit card** pencil from the toolbar on the left.
3. In the property pane on the right, under **Audiences to target**, type or search for the audience group(s) you want to target.

   > [!NOTE]
   > If you've selected an audience group that you recently created or changed, it may take some time to see targeting applied for that group.

4. When a card is successfully audience targeted, you’ll see a **people** icon in the lower-left corner of the card.

   ![Audience targeting confirmation icon.](../media/connections/audience-targeting-icon.png)

### Preview your dashboard to see how it displays for different audiences

After creating or editing cards on the dashboard, make sure you preview the experience for each audience and on both desktop and mobile devices. What you see in *preview mode* approximates how the dashboard displays for certain audiences and devices. When you apply audience targeting to cards, you can preview how different people view the dashboard depending on the audience or device. While in preview-mode, make sure:

- There aren’t any physical gaps between cards that may appear while previewing different audiences and devices. If you see gaps, rearrange cards so that every audience and device will have a high-quality viewing experience.
- Icons, graphics, and images are easy to identify and understand.
- Buttons and links are active and go to their intended destinations.
- Labels and description text are helpful, easy to read, and make sense for the intended audience.

#### To preview different audiences

   1. While in edit mode, select **Preview** on the top right.

      ![Audience targeting icon.](../media/connections/preview-dashboard.png)

   2. Open the **Select audiences to preview as** drop-down list. (if no cards are audience targeted, you'll see a disabled **Audience targeting** label).

      :::image type="content" alt-text="This screenshot shows the audience targeting group label." source="../media/connections/preview-audiences.png":::

   3. Search for and select a group. Once added, the group will be selected by default. You can select the group again in the **Select audiences to preview as** drop-down list to deselect it.

      ![Audience targeting panel in preview mode.](../media/connections/preview-dash-full-page.png)

      - Cards that targeted to a specific group will display.
      - When one or more audiences are selected, cards that *don't* have audience targeting applied will also display.
      - If no audiences are targeted, only cards that *aren't* audience targeted will display. If there aren't any cards with audience targeting applied, none will display.
      - If you aren't part of one of the audiences you've selected, you'll only see cards that aren't audience targeted. If none of the cards are audience targeted, you won't see any cards.

#### Examples

In the following example, the preview is set for mobile devices and highlights the different views that can be created from a single dashboard.

| View 1                  | View 2                 |
| :-------------------: | :-------------------: |
|![Image of one view created for a specific audiences.](../media/connections/preview-dash-1.png) | ![Image of a second view created for a specific audiences..](../media/connections/preview-dash-2.png) |

## Use the Dashboard web part for Viva Connections

> [!NOTE]
>
> - After editing content on the dashboard, it may take several minutes until the new content is available in the Dashboard web part.
> - For best results, we recommend placing the Dashboard web part in a right vertical section.

Once a dashboard is authored and published, you can use the Dashboard web part to display it on your Connections site. You can add the web part to any section on your page.  

![Image of the Viva Connections Dashboard web part highlighted in the Connections site.](../media/connections/vc-dashboard-web-part.png)

When added, it will automatically be populated with the cards from the existing dashboard on your site. You can set the maximum number of cards you want to display. [Learn how to use the Dashboard web part](/sharepoint/use-dashboard-web-part-on-home-site).

## How URLs and single Sign-on works

For some cards, you'll use links to URLs. Depending on the location of the content, links to URLs may display content in Microsoft Teams or elsewhere and [Single sign-on (SSO)](/azure/active-directory/manage-apps/what-is-single-sign-on) behavior can differ. Get more information about how links to URLs and SSO behave depending on the location of the content you're linking to.

> [!NOTE]
> When SSO is not supported, users will be asked to enter their login credentials.

| Opens URL to… | On Teams mobile | On Teams desktop |
| :------------------- | :------------------- |:---------------|
| Teams App | Teams apps (like Shifts, Approvals, or Kudos) open within Teams and user doesn’t need to authenticate again.  | Teams apps (like Shifts, Approvals, or Kudos) open within Teams and user doesn’t need to authenticate again.  |
| Forms  | Forms open within Teams, user is asked to sign-in on the first time, and user doesn’t need to authenticate again if they stay signed in. | Forms open within Teams, user is asked to sign-in on the first time, and user doesn’t need to authenticate again if they stay signed in.            |
| Viva Engage | Viva Engage opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in.  | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| PowerApps  | PowerApps opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in. | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| Power Portals  | Power portals open within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in.  | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings.  |
| Stream   | Stream opens within Teams, user is asked to sign-in on the first time and user doesn’t need to authenticate again if they stay signed in.   | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings. |
| External Links  | Web view opens within Teams and the user might need to authenticate again (depending on the site.)  | Opens a web browser session and the user might need to reauthenticate depending on browser and machine settings.  |

## More resources

[Step-by-step guide to setting up Viva Connections](set-up-admin-center.md)

[Learn more about how to plan a dashboard](plan-viva-connections.md#step-1-plan-for-viva-connections)
