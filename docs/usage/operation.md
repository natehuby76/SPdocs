---
title: Operation & Driver Assistance Guide
description: Learn how to use StarPilot driver assistance, including engagement, steering, speed control, navigation, and operating limitations.
---

# Openpilot Operation

## Capabilities

Openpilot is driver assistance, not self-driving. It performs best on highways.

On supported configurations, it provides adaptive cruise control and automated lane centering.
Traffic-light and stop-sign behavior depends on the driving mode, planner, Enhanced Stops and
vehicle. Curves and low-speed turns are limited by the vehicle’s steering capabilities.

You must stay attentive and ready to steer or brake. Driver monitoring helps check your attention.

## Basic Operation

1. Pay attention at all times. You are responsible for your vehicle’s operation.
1. You can steer, accelerate, brake, or disengage openpilot at any time.
1. Use your vehicle’s engagement controls; steering and speed can engage separately.
1. Button and pedal behavior depends on the vehicle and AOL settings. Manual steering or accelerator input may override assistance without disengaging it.
1. To adjust openpilot max speed, use the CC +/- buttons. Depending on the car, your dash may not reflect the max speed, so instead use the openpilot UI’s max speed shown.

## Always On Lateral

With Always On Lateral (AOL), steering assistance can remain active when cruise speed control
is disengaged. AOL can be armed (ready to assist), active or paused. Pedal and Cancel/OFF behavior
depends on the vehicle and settings. You can still override steering manually. Use the controls
for your vehicle to enable or disable AOL.

To permanently disable, [see settings](./settings.md#always-on-lateral).

## Lane Changes

1. Verify it is safe to change lanes.
2. Turn on blinker.
3. Nudge the steering wheel to initiate the lane change.

> [!WARNING] Check your blind spot!
> Openpilot will attempt to use your blind spot monitors on supported cars, 
> but you should always check yourself.

Lane-change assistance depends on the minimum-speed setting and vehicle capabilities.

> [!WARNING] Nudge-less lane changes
> Step 3 can be skipped when **Automatic Lane Changes** is enabled, after the configured delay
> and when lane and blindspot checks allow. If **Require Cruise for Automatic Lane Changes**
> is enabled, engage factory cruise or StarPilot speed control before signaling. Narrower or
> uncertain lanes still require a nudge.
>
> Be careful if you use this non-recommended setting.

## UI Basics

### Border Colors

| Color | Meaning |
|---|---|
| Dark blue | No active StarPilot steering or speed assistance |
| Dark teal | AOL armed and waiting to assist |
| Teal | Steering assistance without active speed control |
| Pink | StarPilot speed control only |
| Green | Steering and speed assistance together, or steering with factory cruise |
| Yellow | Manually selected Chill mode |
| Orange | Experimental or stop-related state |
| Red | Traffic Mode |
| Purple | Switchback Mode |
| Grey | Manual steering or speed override |

Mode and override colors can take precedence over the steering/speed colors. Alerts and
optional turn-signal or blindspot edge indicators can also change the displayed border.

### Max Speed

Your cruise SET speed is shown in the driving UI; its position depends on the layout. SET is
the driver’s cruise ceiling. Speed-limit control, curve-speed control or the active planner
can request a lower speed.

## Speed Limit Controller 

The Speed Limit Controller (SLC) can use map data, dashboard speed limits or camera-detected
signs, depending on your configuration.

When StarPilot controls speed, SLC can limit the target to the accepted speed limit plus your
configured offset, up to your cruise SET speed. Accepting a limit normally does not change SET.

The driving display shows the speed-limit sign and optional offset. Status text explains
whether SLC is using the speed limit, using SET, awaiting confirmation or being overridden.

See the [Speed Limit Controller guide](../exclusive/speed-limit-controller.md) for source, offset, confirmation, and override settings.

### Submitting New Speed Limits

If you see an incorrect or missing map-based speed limit, submit an edit to
[OpenStreetMap](https://openstreetmap.org). The correction reaches StarPilot after it
appears in newer map data and your device uses that coverage. See
[Speed Limit Maps](../exclusive/navigation.md#offline-maps) to download updated coverage
for your region.

### Vision Speed Limit Detection

StarPilot can read speed limit signs with the road camera as an SLC source. See the [Vision speed limits guide](../exclusive/speed-limit-controller.md#vision-speed-limits) for setup and accuracy guidance.

In Galaxy, open **Toggles → Longitudinal (Speed & Following) → Speed Limit Controller**.
Select **Vision** under **Primary source**, **Secondary source** or **Third source**, where available.

**Show speed limit signs** controls the display. Enable **Speed Limit Controller** for
accepted limits to affect speed on supported configurations.

#### Help us improve it

The model gets better with more real-world driving data. If you'd like to help:

1. Select **Vision** as a speed-limit source in **Toggles → Longitudinal (Speed & Following) → Speed Limit Controller**.
2. If you also use **Maps** as a source, install map data for your region.
3. Drive as normal.
4. In [Comma Connect](https://connect.comma.ai), open the route, 
choose **Files -> Upload All Files**, then under **More Info** enable **Public Access** 
and copy the route ID.
5. Submit the route through the 
[vision speed limit submission form](https://forms.gle/TBptqMNbNaW27u7g9).

> [!TIP] Let your uploads finish
> Make sure all files finish uploading before turning the device off or disconnecting 
> from Wi-Fi/hotspot. You can confirm in Comma Connect that `rlog.zst` and `fcamera.hevc` 
> are present for every segment.

## Curve Speed Controller 

![curve speed controller icon](../assets/images/curve_speed.png){: style="height:50px;width:50px"} 

The Curve Speed Controller (CSC) uses learned cornering preferences to reduce speed for curves
when StarPilot controls acceleration and braking on supported configurations.

With **Show Curve status** enabled, the display can show **CURVE** with its speed target,
or **CURVE LEARNING** with learning progress.

With CSC enabled on a supported configuration, it can learn on qualifying curves while you control speed yourself, with no lead vehicle tracked and no turn signal active. Qualifying accelerator or brake feedback during a CSC-controlled curve can also adjust saved preferences.

## Longitudinal Planner and Enhanced Stops

**Use StarPilot Longitudinal Planner** selects the planner for the next drive.

On supported configurations, **Enhanced Stops** improves stopping behavior at traffic lights
and enables stopping at detected stop signs. Release behavior depends on the stop and the vehicle. If Enhanced Stops is holding the vehicle, press the accelerator to continue when it’s safe.

On builds that expose **Always Hold Enhanced Stops** in developer settings, an acquired hold
waits for Resume or accelerator input while assistance is active and the required inputs
are valid. Disengaging assistance or losing required data can end the hold. Be ready to
hold the vehicle with the brake. This option applies on the next drive.

## Experimental Mode

Driving Mode offers **Automatic**, **Chill** and **Experimental**.

Experimental mode, also known as end-to-end longitudinal (e2e long), lets the driving model
influence acceleration and braking on supported configurations. The active planner and
vehicle limits still apply.

Behavior varies with the driving model and conditions. It may brake or accelerate
unexpectedly; stay attentive and ready to take control.

## Conditional Experimental Mode

Conditional Experimental Mode (CEM) is presented as **Automatic** in Driving Mode. It switches
between Chill and Experimental using your saved conditions. Configure these under
**Automatic conditions**.

### CEM Widgets and Meaning

The on-screen indicator shows the reason for the current mode choice, such as speed, a lead
vehicle, curves, a turn signal or a stop condition.

## Conditional Chill Mode

Older saved Conditional Chill Mode (CCM) selections are handled as Automatic. Current settings
use **Driving Mode** and **Automatic conditions**, rather than a separate CCM editor.

## Navigation

Navigation displays a route and can help the driving model prepare for turns. It does not
drive to the destination for you. Stay ready to steer, especially at intersections and exits.
See [Navigation & Maps](../exclusive/navigation.md) for setup.

On supported configurations, **Turn Signal Guidance** can help the model choose a turning
path at low speed even without a route. Steering assistance must be active. See
[Lateral Tuning](./settings.md#lateral-tuning) for the setting.
