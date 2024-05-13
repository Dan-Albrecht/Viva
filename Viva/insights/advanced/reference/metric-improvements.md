---
ROBOTS: NOINDEX,FOLLOW
ms.date: 10/26/2023
title: Viva Insights metric improvements
description: This article provides a glossary of terms for the Microsoft Viva Insights advanced insights app. 
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Metric improvements in Viva Insights

Viva Insights is advancing to a new underlying platform to provide improved insights and data-analysis experiences. The new platform uses new technology so that our calculations are faster and more comprehensive than before.

Along with the other updates and improvements, you’ll notice a few differences from the previous platform (Workplace Analytics) in how we calculate metrics. The changes generally fall into a few categories, as follows:

* Improving an existing assumption based on more up-to-date research
* Replacing with explicit measurement where previously it was handled by an assumption
* Using newly available signals to make metrics better represent inferred activity, like multitasking and focus time

In this article, we break down these calculation improvements.

## FAQ

### How has metric calculation logic been improved?

#### Email metrics

*Metric names: **Email hours**; **Emails sent**; **After-hours email hours**; **Working-hours email hours**; **External email hours**; **Weekend emails sent**; **Small-group emails sent, including manager**; **Small-group emails sent, excluding manager**; **Urgent email hours**; **Emails sent x***

In the old platform, email metrics were calculated based on "sent items" in user mailboxes. This method of calculation could impact metric accuracy due to deletion of messages and lack of *message read* signals.

Viva Insights now uses activity signals, which use a separate record of *message send* and *message read* signals. (Other activities, like Teams chats and channels, work the same way.) These signals aren’t impacted when users delete "sent items" in their mailboxes. In addition, automatically generated messages, like meeting responses and out-of-office replies, are filtered out.

|    Signal      | Old platform | New platform |
|----------|-------|--------------|
|Messages sent| Users or company policies could delete sent messages, causing data loss. | Signal ingested for greater accuracy (not impacted by deleting sent items) |
|Messages read| No *message read* signal. It was assumed that users read every email they receive. | Signal ingested for greater accuracy|
|External messages |No signal for emails received from external senders. The time users spent reading external emails was assumed based on the emails they sent to external recipients.  | Signal ingested for greater accuracy |
|Meeting responses| Not filtered out| Filtered out for greater accuracy |

#### Teams chat metrics

The new platform collects both *chat message sent* and *chat message read* signals for greater accuracy, as opposed to just a *chat message sent* signal in the old platform. 

|   Signal               |Old platform |New platform|
|------------------|---------|--------|
|Chat messages sent|Supported  |Supported |
|Chat messages read|No *chat message read* signal. It was assumed that users read every chat message they receive.   | Signal ingested for greater accuracy |

#### Meeting exclusion rules

The new platform’s default meeting exclusion rules cover a bit more ground than the old one’s rules.

In the old platform, we assumed users attended meetings they were invited to unless they declined the invitation. Based on our research, this assumption causes overcounting of meeting hours, because a “Tentative” response, or no response, often indicates that users won’t attend a meeting.

In the new platform, we no longer assume that invitees who responded as “Tentative,” or didn’t respond, attended a meeting. By default, the new platform now also excludes meetings that don’t show as “Busy” on invitees’ calendars.

Here’s how each platform excludes different types of meetings by default:

|  Meeting attribute      |Old platform | New platform |
|--------|-------------|----------------|
|Meeting response| Overcounts meetings where invitee responded as “Tentative” or didn’t respond |Excludes meetings where invitee responded as “Tentative”  or don’t respond |
|“ShowAs” status| Overcounts meetings that don’t show as “Busy” on attendees’ calendars |Excludes meetings that don’t show as “Busy” on attendees’ calendars|
|Meeting length|Excludes meetings longer than eight hours |	Excludes meetings longer than 24 hours|
|Meeting size |	Excludes meetings with more than 249 participants and fewer than two participants |	Excludes meetings with fewer than two accepted participants|
|Canceled meetings |Excludes canceled meetings |Excludes canceled meetings |

#### Multitasking

*Metric name: **Multitasking hours***

The old platform classifies **Multitasking hours** based on the number of emails sent during a meeting. If that number goes over a certain threshold, then the whole meeting duration is marked as multitasking. Let’s say you send two emails right at the start of an hour-long meeting—in the old platform, that whole hour would be tagged as multitasking. This method, as we learned from our data validation, often leads to overcounting of multitasking meeting hours.

The new platform, however, considers the actual time that activities are overlapping—for example, the time you spent reading an email during a meeting.

| Item| Old platform| New platform|
|--|-----|----|
|Multitasking signal| Email only| Email and Teams chat (more comprehensive)|
|Classification logic |Threshold-based, all-or-nothing (less precise)| Granular accumulation (more precise)|

#### Time investment for cross-collaboration queries

*Metric name: **Time investment***

The following changes have been made to the calculation of time investment metrics in group-to-group and person-to-group queries.

**Changes in units from hours to minutes**

Time investment is now measured in minutes instead of hours, as was the case earlier.

**Time investment instead of allocation**

If a person attends a meeting with any person from another group, the person invests the entire time they spend in the meeting in the group, as opposed to the previous method whereby the time was divided across various groups participating in the meeting as a proportion of the number of participants from that group. This difference is illustrated below.

Scenario: 60-minute meeting between 1 member each from groups A, B, and C

| Time investment (Current) | Time allocation (Previous) |
|--|-----
|Time invested by A to B = 60 minutes | Time invested by A to B = 0.5 hours = Time spent by A in meeting x Number of participants from group B / Number of participants in the meeting from groups apart from group A|

The new time invested method helps answer the question, "How much time does group A spend with group B?"

**Why does % Time invested add up to more than 100%?**

% Time invested measures the proportion of a person's collaboration time that is spent with a group (time invested into a group by the person / Total time spent by the person in collaboration activities).

% Time invested by a person into different groups in most cases would not add up to 100%, because a person would have meetings where more than one collaborator group can be present. This can be explained in the following scenario: There was a 60-minute meeting between 1 person each from Groups A, B, and C, and another 60-minute meeting between 1 person each from Groups A and B only.

Meeting 1

* Time invested from A to B is 60 minutes

* Time invested from A to C is 60 minutes

Meeting 2

* Time invested from A to B is 60 minutes

% Time invested calculations

* % Time invested by A on B = 60 (meeting 1) + 60 (meeting 2) / 120 (time spent by A in meetings) = 100%

* % Time invested by A on C = 60 (meeting 1) / 120 (time spent by A in meetings) = 50%

#### Focus hours

*Metric names:* ***Available-to-focus hours*, *Interrupted hours*, *Uninterrupted hours*, *Fragmented hours***

**Focus hours** has undergone bigger changes.

In the old platform, **Focus hours** counted only blocks of two hours or longer between meeting times during working hours. It didn't differentiate between uninterrupted hours, interrupted hours, and fragmented hours. Based on our research, this lack of differentiation led to overcounting of time available for focus, because users can be interrupted by unscheduled meetings or chats.

To make our insights more precise, the new platform defines **Uninterrupted hours**, **Interrupted hours**, and **Fragmented hours**, which all contribute to **Available-to-focus hours**.

Here’s a summary of how focus-related metrics are calculated in the two platforms:

|    Metric    | Old platform | New platform|
|--------|---------------|-------------|
|Uninterrupted hours| Not supported |Blocks 1 hour or longer without interruptions from emails or chats |
|Interrupted hours |Not supported| Blocks 1 hour or longer with interruptions from emails or chats|
|Fragmented hours |Not supported| Blocks shorter than one hour with interruptions from emails or chats|
|Focus hours (Available-to-focus hours) |Blocks 2 hours or longer between meetings |**Available-to-focus hours = Uninterrupted hours + Interrupted hours + Fragmented hours**|

If you're looking for a replacement for the old platform's **Focus hour** metric during your migration, we suggest using **Uninterrupted hours** for insights and analysis in the new platform instead of **Available-to-focus hours** to avoid overcounting.

#### Effective behavior time

The old platform only measured the time taken to perform an activity (for example, the amount of time you spend looking at the screen while reading an email). However, research shows that people often need extra time to refocus after meetings or being interrupted: 29.2 seconds on an average to read an email, and another 58 seconds to refocus after reading the email to transition to another task.

To account for this extra time, the new platform measures **Effective behavior time**. Effective behavior time is the time you spend doing an activity, plus the time it takes for you to refocus—that is, to transition to another task after you complete an activity. Based on the average numbers we gave earlier, the **Effective behavior time** for reading an email would then be 87.2 seconds.

To improve metric accuracy, we have also adjusted the activity time for email, Teams chat, and Teams channel activities according to our latest research.

#### Out-of-office

The old platform didn't take a user’s out-of-office status into consideration for collaboration metrics. The new platform, however, does.

For example, let’s say you accept a meeting that falls on a day you’re out of office. The old platform would assume you attended the meeting. The new platform assumes you didn’t attend, unless a Teams signal indicates otherwise.

#### Organizational data

In the old platform, the only way to get employee attributes and organizational hierarchy was by manually uploading HR data.

In the new platform, we use Microsoft Entra ID to simplify the administrator's experience. By default, employee attributes and organizational hierarchy are pulled from Microsoft Entra ID, but you can still manually upload HR data separately. If your organization doesn't keep Microsoft Entra ID updated regularly, you'll still need to upload data manually.

| Method |Old platform  | New platform|
|-----|--------------|-------------|
|HR data upload |	Supported	| Supported|
|Autoextraction from Microsoft Entra ID	| Not supported	| Supported|
|Third-party connectors| Not supported| Will be supported in the future|

### Why do the numbers for my metrics look different?

Because of the improvements we made to calculation logics, your numbers might look different in the new platform than they did in the old platform. Here’s a quick reference that shows examples of commonly used metrics, and whether, in our research data, we’ve noticed the increase or decrease in these numbers. Keep in mind that this list isn’t exhaustive, and that the changes you see might not fully align with our observations—especially when the group of sample data is small.

|Metric	|Observation in data research|Possible causes|
|--------------|----------------------------------|-----------------------|
|Meeting hours | Decrease	| Reduced overcounting by: <ul> <li> Not counting meetings that invitees don’t respond to or respond as “Tentative” to.</li><li>Only counting meetings that show up as “Busy” on invitees’ calendars.</li></ul>|
|Email hours	| Minor adjustment |	Increased comprehensiveness <ul><li>Adjusting the effective time of email activities</li><li>Adding “email read” signal.<li>Eliminating impact by deletion of messages in mailboxes.</li><li>Filtering out meeting responses.</li>|
|Teams chat hours	| Decrease	| Improved accuracy by: <ul><li> Adjusting the effective time of chat activities.</li><li> Adding *chat messages read* signal.</li></ul>|
|Collaboration hours| Decrease	| Reduced overcounting by improving Meeting hours, email hours, and chat hours as indicated earlier. Collaboration hours is an aggregation of the three.|
| After-hours collaboration hours| Decrease (reduced overcounting)| This metric is largely proportional to collaboration hours, which have reduced due to changes in meeting hours, email hours, and chat hours (indicated earlier).|
| External collaboration hours|	Decrease (reduced overcounting)| This metric is largely proportional to collaboration hours, which have reduced due to changes in meeting hours, email hours, and chat hours (indicated earlier).|
|Focus hours| Decrease (when compared to **Uninterrupted hours**) | Reduced overcounting by excluding time blocks that are interrupted by email and chat activities.|
|Focus hours| Increase (when compared to **Available-to-focus** hours) |	Improved comprehensiveness and accuracy by: <ul><li>Improving collaboration hours metric as indicated earlier. </li> <li>Adjusting the minimum focus-hour time block from two hours to one hour.</li><li>Including fragmented hours, which are blocks of time that are less than one hour and are interrupted with emails or Teams chats.|
|Conflicting meeting hours	| Decrease | Reduced overcounting by: <ul><li>Excluding meetings that invitees don’t respond to or respond as “Tentative” to.</li> <li>Only including meetings that show up as “Busy” on invitees’ calendars. </ul><br>Some people might not respond to invitations for meetings that conflict with other meetings. </br>|
|Recurring meeting hours| Decrease | Reduced overcounting by: <ul><li>Excluding meetings that invitees don’t respond to or respond as “Tentative” to.</li><li> Only including meetings that show up as “Busy” on invitees’ calendars.</ul><br>Some people might not respond to invitations for recurring meetings.</br>|
|Multitasking meetings hours |Increase| Improved accuracy by only counting the actual time taken for multitasking activities (like reading an email during a meeting), instead of an entire meeting period.|
|Decision-making meeting count| Increase| Reduced overcounting of large meetings by: <ul><li>Excluding meetings that invitees don’t respond to or respond as “Tentative” to. (Some people don’t attend/respond to large meetings like all hands.)<li>Only including meetings that show up as “Busy” on invitees’ calendars. (Some large events don't show as “Busy,” like happy hours or out-of-office time.)</li></ul> <br>These two factors have resulted in a decrease in large meetings, and as a result, an increase in decision-making meetings.</br>|
|Long and large meeting count| Decrease | Same as above.|
|Large, not long meeting count| Decrease | Same as above.|
|Long, not large meeting count| Slight adjustment | Same as above.|
|Long or large meeting hours |Decrease |Same as above.|

### Does this mean previous insights were wrong?

No. While numbers might shift, takeaways from those numbers generally stay the same. These shifts in numbers are most likely to happen when, to handle imperfect data, we had to make estimates to determine a number in the old platform. The new platform refines those estimates or replaces them with explicit measures, making the new results more accurate.

Here’s an example. During the same workout session, two different wearable devices show different numbers of calories burned. Even though the numbers aren’t exactly the same, that workout can still help you stay fit, and a longer, more intense session can still help burn more calories.

Similarly, there can be gray areas in calculating employee productivity and wellbeing metrics. Some calendar items look like meetings but are personal appointments. Some meetings happen spontaneously around the office, never appearing on a calendar or as Teams calls where they can be measured. Some meetings look like real meetings, but they’re just participants waiting for a while for their manager in a Teams room, with such meetings being canceled when it's clear that the manager won’t make it.

Even as our technology gets better at what it can measure, it's still going to merely approximate the reality. However, this approximation is useful because we look at numbers in context—check them against our expectations, examine trends, compare across groups, and bring in other information, like direct feedback from employees and teams. If we see that a team spends 78% of their week in meetings, that's a useful insight, even if the true number is 82% or 74%.

So, when you see different numbers in the new platform, that doesn’t mean the old numbers were wrong—they were based on different estimates. And while the new platform’s estimates are more refined, they’re unlikely to change any conclusions!

### What other improvements does the new Viva Insights platform offer?

The new platform offers several advantages:

* Improved product performance: Your queries and weekly data refreshes process faster.
* Regional data storage: For customers worldwide, Viva Insights data is processed and stored in your primary region. For more information, see [Where your Microsoft 365 customer data is stored](/microsoft-365/enterprise/o365-data-locations).
* A more intuitive analyst experience: The app includes a rich first-run experience, video tutorials, and improved navigation.  
* Metric improvements: More intuitive custom metrics provide a more predictable and flexible experience.
