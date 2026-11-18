---
title: Hyundai & Kia HDA2 Longitudinal Setup
description: Configure StarPilot longitudinal control for the listed Ioniq 6, Kia EV9, and Ioniq 5 HDA2 vehicles, including vehicle identification and startup checks.
---

# How to Set Up Long on Some HDA2 Vehicles

This guide covers specific configurations of the Hyundai Ioniq 6 HDA II, Kia EV9 HDA II and Hyundai Ioniq 5 PE with HDA II and LFA2. Check [Vehicle Compatibility](./support.md) for the applicable model and configuration.

## First-Time Things to Toggle

In Galaxy, open **Toggles → Vehicle**. Verify the recognized model and use the exact registered configuration if manual selection is needed. On setups where **openpilot Longitudinal Control (Alpha)** is available, follow the [Openpilot Toggles](../usage/settings.md#openpilot-toggles) guidance before enabling it. Availability depends on the vehicle and configuration.

## Startup by vehicle

<span id="every-time-startup-procedure"></span>

Startup checks differ by vehicle. Use the startup instructions confirmed for your exact vehicle and control configuration.

On an **Ioniq 5 PE with HDA II and LFA2**, the vehicle can retain factory speed control
when takeover is unavailable.

A cruise or HDA indicator on the dashboard does not by itself confirm that StarPilot is
controlling speed. If you're unsure how to confirm the handoff or a startup check fails,
leave the controls disengaged and ask in [Discord](https://firestar.link/discord) with
your vehicle, hardware, software version and what you saw at startup.

## Engaging speed control

<span id="engaging-long-after-you-see-mphkph"></span>

Use the controls for your vehicle. Depending on the configuration, steering and speed control can engage separately. Use the applicable SET, RES and Cancel controls as described in [Operation](../usage/operation.md#basic-operation). SET adjustments can differ between factory cruise and StarPilot speed control. See [Wheel Controls](../usage/settings.md#wheel-controls).

## Troubleshooting

Verify the recognized vehicle and check the displayed availability or startup status. If the **openpilot Longitudinal Control (Alpha)** control is unavailable for your configuration, keep factory cruise settings. Switch the vehicle off before restarting the comma. If the expected handoff is still unavailable, include the startup status and route details in a [support ticket](../ticketsystem.md).
