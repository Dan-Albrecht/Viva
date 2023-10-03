---
title: Understand Advanced Configuration options in Viva Glint
description: For highly trained users, Viva Glint offers Advanced Configuration options, which allow users to view and modify advanced platform settings and perform complex data updates.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Advanced configuration, advanced settings
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 07/17/2023
---

# Understand Advanced Configuration options in Viva Glint

For highly trained users, Microsoft Viva Glint offers Advanced Configuration options, which allow users to view and modify advanced platform settings and perform complex data updates.

:::image type="content" source="../../media/glint/setup/understand-advanced-configuration.png" alt-text="Screenshot that displays the Advanced configuration option icon in Viva Glint tenant.":::

> [!CAUTION]
> Changing certain settings in Advanced Configuration may be irreversible. These options should only be modified by trained Viva Glint users.

## Grant user access to Advanced Configuration

To access, a Global or Company admin must enable Advanced Configuration access on an admin user's profile in Viva Glint.

### Grant access to an existing admin user

1. From the admin dashboard, select the **Configure** symbol, then in **Employees,** choose **People.**
2. In the **Search People** field, enter the user's first and last name or email address.
3. Select the user when they appear as a search result.
4. On the user's detail page, in **Company Admin: Advanced Configuration Access,** select the **pencil symbol** to edit.
5. In the dialog, **turn on Advanced Configuration access** and select **Save**.

After this enablement, when a user selects the **Configure** symbol, then goes to **Client Settings**, they'll see **Advanced Configuration.**

> [!NOTE]
> A user may need to refresh or sign into Viva Glint again to see Advanced Configuration once enabled.

### Grant access to a Support user

To manage external users' access to Viva Glint and Advanced Configuration, follow the guidance in this article: [Manage external users in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2240483).

## Explore Advanced Configuration menu options

### Menu option - Details

View specifics about how data display in Viva Glint reporting and which features are enabled.

| Setting | Description |
| --- | --- |
| **Auto Action Plans** | Enable autogeneration of action plans for eligible users |
| **Custom Surveys Enabled** | Advanced survey customization, no action required. |
| **Confidentiality threshold (minSampleSize)** | Scores don't display for fewer responses than this threshold. Viva Glint standard: 5 |
| **Suppression threshold (minGroupSize)** | To prevent guessing the scores of respondent groups with insufficient data, the next biggest group is suppressed until the total insufficient + suppressed = or exceeds this number. Viva Glint standard: 2 |
| **No suppression parent team size threshold (noSuppressionParentTeamSize)** | Access results for teams that would have been suppressed for parent team respondents greater than or equal to this threshold. Viva Glint standard: 400 |
| **Industry average eSat score** | Industry average for eSat |
| **Industry average response rate** | Industry average for response rate |
| **minSampleSizeSurveyStats** | Response rates don't display for groups smaller than this value. Viva Glint standard: 5 |
| **Rating questions scale** | Number of responses available on rating questions. Viva Glint standard: 5 |
| **insightMinGroupSize** | In the Alerts report, minimum number of respondents for a group to be considered. Viva Glint standard: 20 |
| **insightMinScoreDifference** | In the Alerts report, minimum difference from benchmark score for a group. Viva Glint standard: 8 |
| **insightsMax** | In the Alerts report, the maximum number of alerts to display. Viva Glint standard: 2000 |
| **InsightsMaxAttributesPerGroup** | In the Alerts report, the maximum number of attributes to combine for a group. Viva Glint standard: 2 |
| **InsightsMaxLevels** | In the Alerts report, when hierarchies are selected, the maximum number of levels considered. Viva Glint standard: 3 |
| **insightsPValue** | In the Alerts report, the statistical likelihood that results aren't by chance and are significant. Viva Glint standard: .05 |
| **Scores should represent favorability scores by default** | Not recommended. Viva Glint recommends and displays average scores. |
| **Comments privacy: minimum # of responders for search results** | Comments don't display for fewer question responses than this threshold. Viva Glint standard: 10 |
| **Comments privacy: minimum # of responders for facet/grouping** | Comments don't display by topics for fewer responses than this threshold. Viva Glint standard: 10 |
| **driverImpactMinDifferenceFromBaseline** | In the Driver Impact report, the minimum difference from the item score for the entire company. Viva Glint standard: 5 |
| **driverImpactMinSamples** | In the Driver Impact report, the minimum number of respondents to display results. Viva Glint standard: 20 |
| **Exclude negative strengths and positive weaknesses?** | Exclude negative strengths and positive weaknesses for Driver Impact calculation. |
| **Whether to allow the users to look up questionnaires without a kiosk** | Allow users to access attribute-based surveys without a registered kiosk. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230745) |
| **Self-Serve Mode** | EDIT_AND_CREATE allows admins to edit and create survey programs |
| **Support Users for Pulse Notifications** | No action needed, leave blank |
| **Action Plans to Goals enabled?** | No action needed, leave as true |
| **Questionnaire Theme** | Default theme selected. No action needed, leave blank |
| **Enable Cross Program Filtering?** | Filter results across multiple surveys programs. Viva Glint standard: true |
| **Does the client have LinkedIn Learning LSEP license?** | Employees have unlimited access to all LinkedIn Learning content |
| **Percentage Probability of following up on marked question** | To encourage open-ended comments, percentage of users that will be prompted with follow-up questions in surveys. Viva Glint standard: 15 |
| **Frequency of in-product feedback shown on non-MLE Dashboard** | Percentage of users that will see in-product feedback questions in their dashboard. Viva Glint standard: 10 |
| **Enable Filter Suppression on Scores** | Disable users' ability to filter to teams whose scores are suppressed |

### Menu option - Surveys

For a simpler view of existing survey programs, from the admin dashboard, select the **Configure** symbol, then in **Surveys** select **Survey Programs**. Use the **Advanced Configuration Surveys** option to view advanced technical details related to your survey programs including:

- Last modified by user
- Name
- Type
- State
- Program template name
- Start Date
- Frequency
- Recurrence Rule

Select a survey program to view more details and options:

| Setting | Description |
| --- | --- |
| **State** | ACTIVE (ready to be enabled) or DRAFT (edit mode) |
| **Domain** | No action needed, leave blank |
| **Survey Trigger Type** | How surveys generate: Schedule, Event (example: Hire Date), User Initiated |
| **Event Trigger Survey Questionnaire Shelf Life** | Days to complete survey |
| **Generate DISABLED survey cycle in Self Serve** | True. Recurring/upcoming surveys don't enable until an admin enables them |
| **Resubmit Submit Enabled** | Allow users to resubmit their own surveys |
| **Survey Type** | Recurring, On demand, Employee Lifecycle (ELC), or Always-On |
| **Event Trigger Survey Minimum Pulsing Interval (Days)** | Minimum days before a user can be surveyed again |
| **Icon Name (css class)** | No action needed, leave blank |
| **Contact Method** | Company Email or Company and Personal Email |
| **Minimum Sample Size** | Blank. Refer to platform-level settings in Details |
| **Minimum Group Size** | Blank. Refer to platform-level settings in Details |
| **No Suppression Parent Team Size** | Blank. Refer to platform-level settings in Details |
| **Minimum sample Size Survey Stats** | Blank. Refer to platform-level settings in Details |
| **Minimum Respondent size for Driver Impact Report** | Blank. Refer to platform-level settings in Details |
| **Minimum Respondent Size for Comments** | Blank. Refer to platform-level settings in Details |
| **Minimum Group Size for Comments** | Blank. Refer to platform-level settings in Details |
| **Manager Report Default Question 1** | Displays selection from Survey Programs: Survey: Reporting |
| **Manager Report Default Question 2** | Displays selection from Survey Programs: Survey: Reporting |
| **Run action plans** | True. Generate action plans for eligible users |
| **Default survey locale** | Displays selection from Survey Programs: Survey: Program Setup |
| **Additional Survey Locales** | Displays selection from Survey Programs: Survey: Program Setup |
| **Enable Follow Up** | Enable follow up questions that encourage more open-ended comments in surveys |
| **Sensitive Comments** | Enable sensitive comment flagging in the admin view of the Comments report for personally identifiable information (PII), sensitive topics, and profanity [Learn more](https://go.microsoft.com/fwlink/?linkid=2247846) |

### Menu option - Users

To export Viva Glint users, go to the admin dashboard, select the **Configure** symbol, then in **Employees** choose **People** and then **Export** and follow on-screen guidance.

### Menu option - External Import

Import external data from non-Viva Glint survey results to see trend for past items that will continue to be asked in Viva Glint survey programs. [Learn more](https://go.microsoft.com/fwlink/?linkid=2244872).

### Menu option - Data Apps

Use Viva Glint Data Apps to export recipients or update attribute values for users in closed surveys. [Learn more](https://go.microsoft.com/fwlink/?linkid=2245700).

| App UUID | Description |
| --- | --- |
| **EXPORT_USERS_FROM_SURVEY_CYCLE** | Export survey recipients, attributes, and hierarchies as they existed when a survey launched |
| **RETROACTIVE_PULSE_UPDATE** | Update employee attributes associated with a closed survey cycle |

### Menu option - Uploads

Use the Uploads option to:

- View file upload details.
- Update users' custom data access in bulk.
- Perform basic retroactive data updates to correct employee attributes in reporting.

#### Upload types:

- **MANAGERS_UPLOAD:** To upload custom results data access for dashboard users in bulk. [Learn more](https://go.microsoft.com/fwlink/?linkid=2247341).
- **USERS_UPLOAD:** 
   - To upload employee data, follow the guidance in this article: [Upload your employee attributes to Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742).
   - Use the guidance in this article to perform a Retroactive USERS_UPLOAD: [Use Advanced Configuration Uploads](https://go.microsoft.com/fwlink/?linkid=2247341).
- **ROLE_UPLOAD:** To upload users to a Viva Glint User Role, follow the guidance in this article: [Import and export Viva Glint User Roles](https://go.microsoft.com/fwlink/?linkid=2230866).

### Menu option - Running Jobs

Review details, statuses, and start times for Advanced Configuration tasks performed within the last 15 minutes to 48 hours, depending on the selected time-frame.
