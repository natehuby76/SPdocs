---
title: Support Tickets & Bug Reports
description: Report StarPilot bugs, vehicle tuning issues, and feature requests through Discord. Learn which ticket to open and how to try fixes on Testing.
---

# Ticket System

StarPilot thrives on the feedback and responsiveness of our community. If you are experiencing an issue, please open a ticket and share what you are seeing. The more people submitting feedback, the better your car (and everyone else's) can drive.

## What is it?

The Discord ticket system is the main way to report problems and request support for StarPilot. Create a ticket if your car meets Comma's requirements but is not yet supported by StarPilot, if you experience ping-ponging or steering wobble, or if you encounter another issue that requires investigation. For basic configuration questions, ask in the appropriate public support channel instead. Firestar will review your ticket when available and may release an update to address the issue.

## Before creating a ticket!

You must first be a member of the [StarPilot Discord server](https://discord.com/invite/b8EzGp5RtE).

If a maintainer asks you to test a fix, follow the [branch-switching guide](#how-do-i-switch-to-the-testing-branch) and report the version you tested.

## How do I create a ticket?

1. Open the StarPilot Discord.
2. Go to the [#submit-feedback-and-reports](https://discord.com/channels/1387432184121393333/1506463404863389806) channel.
3. Select the appropriate report button.

    <img src="../assets/images/ticket_buttons.jpg" alt="Ticket Buttons" width="300">

4. Fill out the form, then select **Submit**. For an issue, include:

    - Your comma device, vehicle year and trim, and installed hardware
    - The branch and software version you tested
    - The approximate time, route or bookmark, and any [relevant logs](./faq.md#how-do-i-upload-logs-for-troubleshooting)
    - What you expected and what actually happened

    Choose whether to make a route public before sharing it.

### Which button should I choose?

<details>
   <summary>
      Bug Report
   </summary>
   Use Bug Report when something is not working correctly. For example, use it if a steering-wheel button no longer works as expected.
</details>

<details>
   <summary>
      Feedback
   </summary>
   Use Feedback for non-urgent tuning concerns, such as insufficient steering performance or steering wobble.
</details>

<details>
   <summary>
      Feature Request
   </summary>
   Use Feature Request to suggest a new StarPilot feature. If you request a feature, be prepared to test it.
</details>

<details>
   <summary>
      View My Reports
   </summary>
   Use View My Reports to see a list of your reports and their current status.
</details>

> [!Tip]
> If you can reproduce the issue, open a bookmark on your device shortly before it occurs and close the bookmark shortly afterward. Include the bookmark information in your ticket to help Firestar locate and investigate the issue.

## How do I switch to the testing branch?

<span id="how-do-i-switch-from-the-starpilot-branch-to-dom"></span>
<span id="how-do-i-switch-from-the-starpilot-branch-to-testing"></span>
<span id="through-your-comma-device"></span>
<span id="through-galaxy"></span>

Park and turn off the vehicle. Keep the comma powered and online, then follow [Changing branches](./software/starpilot.md#changing-branches) and choose **Testing** in Galaxy. Once the fix is in Stable, follow the same steps and choose **Stable** to switch back.

## What do the colored circles on my ticket mean?

Each colored circle represents the current status of your ticket.

| Color | Meaning | What you should do |
| --- | --- | --- |
| 🟠 | Your ticket is new and has been submitted. | Wait for Firestar to review it. |
| ⚪ | Firestar has reviewed your ticket, but an update is not ready yet. The circle will turn purple when the update is ready to test. | Please be patient and wait for the circle to turn purple. |
| 🟣 | Your ticket has been reviewed and a potential fix is ready. | Update to the requested testing build and test the fix. If the problem remains, submit a new route and updated logs. |
| 🔴 | Your ticket was sent back for further investigation. | Wait for the ticket to return to purple status. |
| 🟢 | You closed the ticket yourself. | No further action is required. |
| 🔵 | A staff member or the bot closed your ticket. | No further action is required. |
