---
title: "Organize a Viva Engage live event"
description: "How group admins host live video events for Viva Engage users."
ms.reviewer: ethli
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/13/2025
audience: Admin
ms.topic: overview
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
ms.collection:
- m365solution-spcomms
- m365solution-scenario
- highpri
search.appverid:
- MET150
---

# Organize a Microsoft Teams live event in Viva Engage

Microsoft Viva Engage uses Microsoft Teams to process and record video for all live events. To understand how Viva Engage and Teams work together, see [Overview of live events](/microsoftteams/teams-live-events/what-are-teams-live-events).

This article provides guidance for Viva Engage group admins to produce the best live event experiences for their groups and communities. If you're planning a large event (up to 100,000 attendees), the Microsoft 365 live events assistance team offers the best options for your live event. [Learn more about this program.](https://adoption.microsoft.com/virtual-event-guidance/assistance)

> [!NOTE]
> Use [Microsoft Teams live events](/microsoftteams/overview-meetings-webinars-town-halls) to schedule events.

## Choose a setup for your live event

The size and complexity of your live event determines whether you create the event in Viva Engage or in Microsoft Teams. Review these descriptions to determine which best fits your needs.

> [!IMPORTANT]
> When you set up a live event, to provide the best experience you should configure your video, community, and user permissions at least 24 hours before the event. Setup includes settings to add users, update video permissions, and to change a community from private to public. Certain changes can take up to two hours to propagate across Microsoft Teams and Viva Engage. Allowing 24 hours or more provides time for tests and necessary adjustments.

- **Microsoft Teams QuickStart**

  Use this method to produce simple live events. You only need the audio and video devices that are connected to the presenter’s computer. This setup is great when you invite a remote presenter for the event.

  - Microsoft Teams encodes the broadcast stream.
  - Content shared from the presenter’s webcam and screen is shared across Teams.
  - Attendees can view the event on Viva Engage.
  - The Viva Engage community's SharePoint library stores the video. The video appears on the Viva Engage event page for 180 days after the event is over.

- **Teams external app or device**

  This type of production is best for large-scale events, such as executive town halls. Here, a single stream from a media mixer is broadcast to the audience.
  - Teams broadcasts the live event.
  - Production setup requires an external encoder (app or device) to produce the event.
  - Attendees can view the event in Viva Engage.
  - The Viva Engage community's SharePoint library stores the video. The video appears on the Viva Engage event page for 180 days after the event is over.

## Review licenses and permissions

As a live event organizer, make sure that you and your audience have the necessary licensing and permissions to participate in live events.

### Create and schedule a live event

Observe the following requirements to produce live events:

- You must be an admin in the Viva Engage group or community in which you create and schedule the event. 
- You must own a Teams license and set up specific policies. For details, see [Who can create and schedule live events in Teams](/microsoftteams/teams-live-events/plan-for-teams-live-events) and [Set up live events policies](/microsoftteams/teams-live-events/set-up-for-teams-live-events#step-3-set-up-live-events-policies).
- You must be an admin to assign roles for the live event (producers, presenters, and so on). Only assigned roles receive an invite, which allows them to join the event through a link. Learn more about [roles assigned through Teams](https://support.microsoft.com/office/schedule-and-produce-a-live-event-in-new-yammer-using-teams-d891bff6-eda2-493f-8b0d-d87932e7937d#roles).

- Co-producers and presenters that you assign must also have a Teams license and Teams must be enabled. (Select Microsoft 365 Copilot and look for a Teams icon.)

- Your public or private group must be connected to Microsoft 365 and **Enforce Office 365 identity** setting must be selected for the organization. To restrict attendance to members only, use a private community. Non-members can attend and participate in live events scheduled in a public community.  

For more information, see [Enforce Office 365 identity for Viva Engage users](/yammer/configure-your-yammer-network/enforce-office-365-identity) and Viva Engage and Microsoft 365 groups.

### Attend a live event

- Attendees must have a Microsoft 365 or Office 365 plan with a license for Viva Engage and Microsoft Teams (for example, Office 365 A3, A5, F1, E1, E3, or E5).
- To attend a live event in a public group, you must be a member of the Viva Engage network that's hosting the event. **Guests and external users have no access to live events.**
- To attend a live event in a private group, you must be a member of the private group that's hosting the event.

## Configure video and permissions in advance

Before you create a live event, you must configure video, community, and user permissions. Other tasks involve adding users, updating video permissions, and changing a community from private to public. Permissions take up to two hours to propagate across Teams and Viva Engage.

We suggest you configure these settings at least 24 hours in advance to allow time to test and adjust your settings.

## Learn by creating a test event

Let your first live event be a dress rehearsal for the real thing. A practice session helps you and your team members get comfortable with your responsibilities and what needs to happen. Practice is especially important when you’re producing live events that broadcast to thousands of people.

Enlist helpers for the key roles: organizer, presenter, and attendee. If you produce events through an external app or device, include someone on the Audio/Video staff to run the mixer to provide the encoder information. Consider creating a separate Viva Engage community of your volunteers specifically for the test.

## Restrict creation of live events in Viva Engage

You can block the creation of live events produced in Teams, live events produced with other tools, or both.

- To prevent creation of live events produced in Teams, remove permissions in Teams for live event scheduling. Unlicensed and unauthorized users don't see the **Produce in Teams** option if they try to create a live event in Viva Engage.

## FAQ

**Q: Can I create a live event in All Company?**

If your network’s All Company community is a Microsoft 365 connected group, then you can host events in this community. The All Company community functions like other Viva Engage communities.

**Q: How many attendees can view a live event at once?**

A. Currently, the limit is 10,000 attendees. For larger attendee sizes, contact the Microsoft 365 [Live Events Assistance Program](https://adoption.microsoft.com/virtual-event-guidance/assistance/).

**Q: What media player is used for live events?**

The new live events are broadcast using the Teams media player. You can view them live or on-demand on the Viva Engage web and mobile apps (iOS and Android).

**Q: Why can't I view the video?**

To maintain the privacy of live event content, only authorized users can join a live event and are authenticated as they load the live event page. Authentication must be successful for video to be viewable. Use your browser's settings to enable cookies, and disable any extensions that block tokens. After changing the settings, refresh the event page.

**Q: Where are the videos stored after they're produced?**

The Video-on-Demand is stored in the SharePoint Community where the event was hosted. The video is automatically shared with members of the private community. If the event was produced in a public community, the video is shared with everyone across the Viva Engage network.

**Q: Can Event Producers edit videos?**

You can edit videos in the SharePoint folder. After you make your changes, the edited video automatically updates in SharePoint for attendees to watch. It can take up to 10 minutes before producers can edit their videos after the event completes.

**Q: What happens to old live events videos that were produced using Microsoft Stream?**

For now, attendees can watch events videos created with Stream on the Microsoft Stream app. We recommend that you [migrate Stream videos to SharePoint](/stream/streamnew/stream-classic-to-new-migration-overview).

**Q: How can I cancel a scheduled live event?**

Take the following steps:

1. In Viva Engage, go to the group page to view the event.

2. In the Group Events section, select the event, and then select **Cancel Event**.  

>[!Tip]
>If the event announcement has been live for a while, post a message in the community saying that the event was cancelled. If you sent out a calendar invite, send out a cancellation.

**Q: Can our event team moderate the conversations, or will all attendees see all the questions?**

All questions and conversations are visible in the Viva Engage community.

**Q: Do I have to create a transcript or does the tool transcribe the video? How does closed captioning work after the event?**

Teams powered AI closed captioning is available in real-time during and after the event is over.

**Q: Can I customize the event landing page?**

You can edit the title, description, date, and time for the event landing page. The landing page includes the recording after the event occurs.

**Q: What are good ways to promote an event?**

When you invite attendees to join your event, include the link from the event page in your Outlook emails and announcements.

- For public communities, post an announcement in the community with a link to the event page. For wider reach, you can also post an announcement in the All Company community.

- For private communities, post an announcement in the community with a link to the event page.

- For all communities, pin announcements to the top of the community feed.

## Related articles

[Organize a live event in Viva Engage](https://support.office.com/article/organize-a-live-event-in-yammer-105dd7af-9caf-4a5e-8a44-56d203e96551)

[Microsoft Teams lives events overview](https://support.office.com/article/get-started-with-microsoft-teams-live-events-d077fec2-a058-483e-9ab5-1494afda578a)

[Get help producing a live event](https://support.office.com/article/0cedb557-cbe4-40d3-8147-112633f087eb)
