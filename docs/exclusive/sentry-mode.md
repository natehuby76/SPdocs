---
title: Sentry Mode — Parked Event Recording
description: Learn how StarPilot Sentry Mode captures activity while parked, with Galaxy event viewing, notification options, and recording settings.
---

# Sentry Mode

Sentry Mode captures events when the comma detects sustained movement while your car is
parked. Set up monitoring and review events through [Galaxy](../usage/galaxy.md).


## How it works

Sentry uses your comma device's **accelerometer** to detect movement while the vehicle is parked, for example if someone bumps or rocks it.

With monitoring enabled, the vehicle off and sufficient power, Sentry arms after 90 seconds of continuous valid conditions. If those conditions are interrupted, it may need to arm again. Motion can create a warning, and further activity can escalate to an alarm.

The comma’s normal parked shutdown and battery cutoff still apply.

## Galaxy dashboard

Open **Cameras & Monitoring → Sentry** to turn monitoring on or off, adjust its settings and review events. The event list refreshes while the page is open. Select **Delete** to remove an event or **Delete All** to clear the list.

For a live parked image, use [Camera Snapshot](./cameras-and-monitoring.md#camera-snapshot).

## Notifications

The Sentry page supports **Browser push**, **Discord**, **General webhook**, **ntfy** and **Galaxy App Alerts** where available. Browser push requires HTTPS and a compatible browser. App alerts require permission on the phone and a configured push relay. Use the test button for each channel you set up.

> [!TIP] iPhone users
> Add Galaxy to your Home Screen as a web app before enabling browser notifications. iOS requires a Home Screen web app for web push to work.

## Settings

| Setting | What it does |
| --- | --- |
| **Use parked motion monitoring** | Turn parked monitoring on or off |
| **Motion sensitivity** | How easily movement triggers Sentry. Lower values catch smaller bumps; higher values require stronger motion |
| **Warning persistence** | How much motion evidence triggers the first warning. Higher values help filter brief vibrations. |

Start with the defaults and adjust sensitivity if you get too many false alerts or not enough real ones.

## What gets captured

Galaxy lists **Motion**, **Alarm**, **Selfie** and **Low battery** events with timestamps. Motion and alarm events can include road and cabin images when the capture succeeds. Low battery entries show the measured battery voltage and the cutoff.

Sentry stores up to 512 events. When storage is full, new events can’t be saved until you clear space. Use a supported network connection to view event images. Bluetooth-only access can show event details.
