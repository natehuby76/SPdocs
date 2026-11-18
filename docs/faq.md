---
title: FAQ & Troubleshooting
description: Answers to StarPilot questions about comma device support, Galaxy, Chestnut, installation, boot issues, vehicle errors, and sharing troubleshooting logs.
---

# StarPilot FAQ and Troubleshooting

Can't find an answer to your question? Post in 
[Discord](https://firestar.link/discord) or [submit feedback through the ticket system](./ticketsystem.md).

## How do I submit feedback?

> [!IMPORTANT]
> StarPilot thrives on the feedback and responsiveness of our community. If you are experiencing an issue, please [open a ticket](./ticketsystem.md) and share what you are seeing. The more people submitting feedback, the better your car (and everyone else's) can drive.

Use the [StarPilot ticket system](./ticketsystem.md) to report bugs, share tuning feedback, request features, or ask for an issue to be investigated. The guide explains which button to choose and what information to include.

---

## What is StarPilot?

StarPilot is a standalone, community-driven fork of openpilot.
It runs on comma 3, 3X, and 4 and adds driving, device management, and customization features.
See the [StarPilot overview](./index.md) and [installation guide](./software/starpilot.md).

---

## What is the Galaxy? Can I change settings from my phone?

[Galaxy](./usage/galaxy.md) lets you manage StarPilot from a browser on the same local network, or remotely after pairing. Local access works without Internet. Remote access requires Internet. See [Companion Apps](./usage/companion-apps/index.md) for iOS and Android.

---

## Does StarPilot support Comma 3, 3X, and 4?

Yes. StarPilot supports comma 3, 3X and 4, including continued support for older devices. Feature availability depends on the device, vehicle and configuration. See [Comma Devices](./hardware/comma.md) for details.

## Does StarPilot support Chestnut (external GPU)?

Yes. You can download compatible GPU models before connecting Chestnut. Running them requires ready, supported hardware. Most users do not need Chestnut. See [Chestnut](./hardware/chestnut.md) and [Models](./usage/model-manager.md).

---

## Why is my car driving terribly?

If a custom setting may be contributing, try [Safe Mode](./usage/settings.md#safe-mode). It temporarily bypasses supported custom features and tuning without erasing their saved settings. To restore default toggle values, back up your settings first and follow [Backup and reset](./usage/settings.md#backup-and-reset).

If the behavior persists, include your vehicle, hardware, software version and route details in a [support ticket](./ticketsystem.md).

---

## Will installing openpilot void my warranty?

<https://comma.ai/support#will-installing-a-comma-device-void-my-warranty>

---

## Is the openpilot install reversible?

A standard plug-in harness installation can generally be removed. Firmware flashing and hardware retrofits may require separate restoration. See the [Volt firmware guidance](./cars/volt.md#flashing-volt-firmware) for an example.

---

## Will openpilot navigate on its own?

StarPilot is driver assistance. Stay attentive and ready to take control. [Navigation & Maps](./exclusive/navigation.md) can provide guidance for supported low-speed turns with the matching turn signal on and blind spot clear. It can also request slowing for an upcoming maneuver when StarPilot controls speed. See [Operation](./usage/operation.md#navigation) for driving behavior.

---

## How do I clear the "LKAS Fault: Restart the car" error?

Pull over safely and turn the vehicle off. Follow the fault recovery guidance for your vehicle. If the fault recurs, report the exact configuration and include the route or logs.

---

## How do I avoid LKAS faults?

Switch the vehicle off before rebooting, unplugging or turning off the comma. Interrupting the connection while the vehicle is on can cause an LKAS fault.

---

## How do I clear the "Cruise Fault: Restart the car" error?

Park safely and turn the vehicle off before following the restart guidance for your vehicle. If the fault persists, include the hardware, software version and route details in a [support ticket](./ticketsystem.md).

---

## How do I clear the "Controls Mismatch" error?

Park and switch the vehicle off before restarting the comma. If the error persists, report your exact vehicle configuration, how you started the car and the matching route or log.

---

## How do I upload logs for troubleshooting?

Logs are sent as routes. A route is a single drive (from car on to car off), 
with one-minute segments. Log data can include video, vehicle messages and GPS. If support accepts a local export, use [Routes in Galaxy](./usage/galaxy.md#routes) to download the recording or logs. Downloading them does not upload anything to comma Connect.

1. Navigate to [connect.comma.ai](https://connect.comma.ai)
2. Find the route your issue happened on and click on it. 
3. Click and drag the video slider over the section where the error happened.
The video will loop over this selected section, make sure the error is within. 
To undo your last selection, click the back arrow just above the video slider. 
Once you are happy with the segments selected, proceed to the next step.
4. Click `Files`, then next to `All logs`, click `(upload ## logs)`
5. Wait for data to be uploaded (you can check the progress using `Files` > `View Upload Queue`)
6. If you choose to share the route publicly, open **More info**, enable **Public access** and copy the route information. Turn public access off when sharing is no longer needed.
7. [Create a ticket](./ticketsystem.md) using the buttons in
[the #submit-feedback-and-reports channel of the Discord server](https://firestar.link/discord).
Be as descriptive as possible. 
Also include the approximate minute(s) in the route it happened.
StarPilot has a unique, community-focused ticketing system that helps users and developers make sure no problem goes unresolved. [Learn how it works and what to include in your report](./ticketsystem.md).

> [!TIP]
> Ending a route log early
> While safely parked, open **Settings → System → Force Drive State → Offroad** on
> the comma to stop driving services and end the route. In Galaxy, the equivalent control is
> **Tools → System Tools → Software & Updates → Advanced options → Force device offroad**.
> Return the comma to **Auto**, or turn off **Force device offroad** in Galaxy, when you are
> done.

---

## I'm stuck on the boot logo screen. How do I fix it?

If Galaxy is reachable, try the [backup and reset tools](./usage/settings.md#backup-and-reset). Save any recordings or logs you need before resetting the device.

If Galaxy is unavailable, follow [If You Cannot Open Settings](./software/starpilot.md#if-you-cannot-open-settings) for your device. A factory reset erases stored content and settings. If the problem persists, ask in [Discord](https://firestar.link/discord).

---

## My device is behaving oddly. What is a "saveme"?

For a settings problem, open [Backup and reset](./usage/settings.md#backup-and-reset) in Galaxy. Use **Back up toggles** first. You can then **Restore toggles** from a compatible backup, or use **Reset toggles to default** while parked. The toggle reset keeps your recordings and other device data.

---

## How do I fix the "CAN bus disconnected" Error?

With the vehicle off, inspect and reseat connections according to the hardware guide for your setup. Check the harness, OBD-C cable and pedal connection where applicable. If the error persists, ask for [support](./ticketsystem.md) with your vehicle, hardware and logs.
