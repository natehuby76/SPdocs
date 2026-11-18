---
title: Galaxy & StarPilot Features
description: Find StarPilot features in Galaxy and learn what its pages and key controls do.
---

# Galaxy & Features

<span id="galaxy"></span>
<span id="starpilot-features"></span>

Galaxy is StarPilot’s browser interface for settings, models, routes, and device tools. Feature
availability depends on your [car](../cars/support.md) and [hardware](../hardware/comma.md).
Read [Operation](./operation.md) for driving behavior.

## Access Galaxy

### Companion apps

The iOS and Android apps can connect over Galaxy Wi-Fi or a shared network. Bluetooth supports basic controls. Recordings and replay require Galaxy Wi-Fi or LAN.

See [Companion Apps](./companion-apps/index.md) for downloads, pairing, source repositories and beta access.

### Local access

Put your phone or computer and comma on the same Wi-Fi or Ethernet network. On the comma,
open **Settings → Device → Galaxy** or **Pair with Galaxy**.

Scan the **local** QR code or open `http://<comma-ip>:8082/`.
**Galaxy Access & Install → Local access** also lists the address. Direct local access needs
no Galaxy password.

### Remote access {#pairing}

While parked, choose **Set password & pair** or **Pair with Galaxy** on the comma, or **Pair**
in local **Galaxy Access & Install**. Choose a new password of at least eight characters.

The separate remote QR code opens your device-specific `galaxy.firestar.link` address. Save it
and sign in with your password. Remote access requires Internet and the Galaxy tunnel, which
may take a few minutes to connect. Bookmark each device’s link separately.

### Unpairing

To stop remote access, choose **Unpair remote Galaxy** on the comma or **Unpair** in local
Galaxy. The old remote link stops working; local access remains available. Pair again for
a new remote link.

Keep your password and **App key** private. The App key grants remote access.

### Installed web app and hotspot

Open your remote Galaxy link and choose **Install web app** or your browser’s **Add to Home
Screen**. This web app uses the remote link and needs Internet.

For local access without Internet, enable **Galaxy Wi-Fi Hotspot** while parked, set its
password, then open `http://172.31.254.1:8082/`. The hotspot provides local access; it does
not share Internet.

## Main

**Home** shows device status, drive totals and recent drives. **Toggles** lets you search or
browse settings; follow each change’s save or confirmation prompts. Some changes require
Park. **Tools** opens the device tools.

## Routes

In local Galaxy, **Routes** lists saved drives. Open one and choose **Footage** for camera
video or **Replay with UI** for the driving screen. Replay needs saved driving logs and
road video for the segment. **Export segment** saves one replay clip. **Export route**
combines replayable clips and skips missing ranges.

## Tools {#features}

| Tool | Purpose |
|---|---|
| [Bluetooth](../exclusive/bluetooth-controls.md) | Pair devices, manage audio and map controller buttons |
| [Cameras & Monitoring](../exclusive/cameras-and-monitoring.md) | Camera previews, Sentry and visual monitoring |
| Colors & Layout | Customize widgets, colors and road views |
| Logs & Diagnostics | Inspect crashes, device status and support logs |
| [Models](./model-manager.md) | Single models, model pairs, downloads and Jetlink |
| [Navigation & Maps](../exclusive/navigation.md) | Routes, saved places and offline map data |
| Tuning and Analysis | FLM Auto Learn results and live plots |
| [StarPort](../exclusive/starport.md) | Car-screen display, layout and audio |
| [System Tools](../software/starpilot.md#changing-branches) | Software updates, version history and switching between Stable and Testing |
| [Galaxy Access & Install](#access-galaxy) | Remote pairing, app installation and hotspot |

Vehicle identification is under **Toggles → Vehicle**.

## Features at a glance

| Feature | What you can do | Requirements and limits |
| --- | --- | --- |
| [Galaxy](#access-galaxy) | Manage settings, models, software, logs, and recordings from a browser. | Local access uses your network; remote access requires pairing and Internet. |
| [Driving models](./model-manager.md) | Choose a single model or a steering/speed model pair. | Model availability depends on hardware; some need Chestnut. |
| [Navigation](../exclusive/navigation.md) | Set destinations in Galaxy and give the model route guidance. | Requires a Mapbox key and Navigation enabled in Galaxy. The driver remains responsible for turns and exits. |
| [Lane Centering](../exclusive/lane-centering.md) | Bias the model's path toward the center of detected lane lines. | Experimental; falls back to the normal model path when conditions are unsuitable. |
| [Speed Limit Controller](../exclusive/speed-limit-controller.md) | Configure speed-limit sources, offsets, confirmation, and overrides. | Source availability varies, and reported limits can be wrong. |
| [Sentry Mode](../exclusive/sentry-mode.md) | Review images captured after sustained movement while parked. | Experimental; uses the device accelerometer and requires the device to remain powered. |
| [Bluetooth controls](../exclusive/bluetooth-controls.md) | Pair audio devices and map Bluetooth or USB controller buttons to Quick Select and driving screen actions. | Experimental; configure Controller Buttons in local Galaxy with the vehicle off. |

## Galaxy tuning and support

<span id="galaxy-manage-starpilot-from-your-phone"></span>

Galaxy’s tuning tools include live plots, lateral tuning, and a view of settings that differ
from defaults. These help you describe a problem when [opening a support ticket](../ticketsystem.md).

For connection and pairing instructions, see [Access Galaxy](#access-galaxy).

## Driving models and optional Chestnut support

Use [Models](./model-manager.md) for **Single model**, **Model pair** (formerly Model Laboratory),
downloads, and Jetlink. Most models run on the comma itself; Big models need compatible
external hardware.

You can download GPU models for later without Chestnut connected. Model selections take
effect the next time the driving model starts.

## Navigation through Galaxy

Search for a destination, compare routes, and save favorites in Galaxy. StarPilot sends route
information to the comma device, displays turn instructions, and provides upcoming maneuver
information to the driving model. Turn guidance is limited to supported low-speed turns with
the matching turn signal on and the corresponding blindspot clear. Route guidance can also
help slow for upcoming maneuvers when StarPilot controls speed.

In Galaxy, open **Tools → Navigation & Maps → Setup**. Add a Mapbox key and turn on **Navigation**.
An optional Google key adds Google maps, routing, and place search alongside Mapbox.
Navigation is a driving aid: it does not guarantee the car will complete a route or make an exit.

[Configure navigation](./settings.md#navigation) and [learn how route guidance works](../exclusive/navigation.md).

## Steering, speed, and driving preferences

StarPilot offers settings for lateral tuning, driving personalities, curve speed control,
and **Driving Mode** choices of **Automatic**, **Chill**, and **Experimental**. Automatic switches
between Chill and Experimental using your saved conditions. Availability and behavior depend on
your vehicle's steering and longitudinal capabilities.

The experimental **Lane Centering** feature adjusts the model's path using detected lane
lines when conditions allow. Its settings include **Lane offset**, **Model path preference**,
**Lane Centering Strength**, and **Pause on signal**. This particular feature is separate from the general
lane-centering assistance provided by openpilot.

**Speed Limit Controller** can use map data, supported dashboard limits, and optional
camera-based sign detection. You can require confirmation before applying a new limit,
set offsets, and configure overrides. It can cap speed below
your cruise SET speed; accepting a limit normally does not change SET.

On supported configurations, **Use StarPilot Longitudinal Planner** selects the planner for the
next drive. **Enhanced Stops** improves stopping at traffic lights and enables stopping at
detected stop signs. See [Operation](./operation.md#longitudinal-planner-and-enhanced-stops) for how the hold releases.

Start with the [settings guide](./settings.md), then read the
[operation guide](./operation.md) for the behavior and limitations of driving controls.

## Sentry Mode and Bluetooth accessories

**Sentry Mode** detects sustained movement through the comma device's accelerometer while
parked and captures camera images. Galaxy provides event history, sensitivity settings,
and notification options. It is motion-triggered event capture; it does not continuously
watch camera video for every person passing the car.

**Bluetooth** support is available on comma 3, 3X, and 4 for audio and controller input.
Galaxy provides pairing and **Controller Buttons** mapping for Bluetooth or USB controllers.
Bluetooth management is also available on the comma device. Both Sentry Mode and Bluetooth are documented as experimental.

[Set up Sentry Mode](../exclusive/sentry-mode.md) or [pair Bluetooth accessories](../exclusive/bluetooth-controls.md).

## Supported devices and cars

StarPilot supports comma 3, 3X, and 4, but device support does not establish compatibility
with a particular car. The vehicle's year, trim, steering system, ACC configuration, and
installed harness or pedal determine which controls are available.

StarPilot's vehicle work extends beyond GM. The compatibility guide lists additions and
improvements across multiple manufacturers, while the car guides explain specific hardware setups.

- [Compare comma devices](../hardware/comma.md).
- [Check vehicle compatibility](../cars/support.md).
- [Find car setup guides](../cars/all.md).
- [Install StarPilot](../software/starpilot.md).

## Shared work and project development

StarPilot builds on openpilot and work from the wider community. Features such as Always On Lateral,
Conditional Experimental Mode, themes, and Speed Limit Controller have shared project
history; their presence alone does not make them exclusive to StarPilot. The
[StarPilot project README](https://github.com/StarPilotHQ/StarPilot#features) describes
the project's features.

For questions about a feature on your car or software branch, use the
[StarPilot support channels](../ticketsystem.md). StarPilot remains driver assistance and
requires an attentive driver ready to take control.
