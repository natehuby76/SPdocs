---
title: Comma Pedal Requirements & Behavior
description: Learn how the comma pedal works with StarPilot, including accelerator control, non-ACC regen braking, and vehicle-specific hardware requirements.
---

# Comma Pedal

The Comma Pedal is an interceptor that sits between your accelerator pedal and the car. When assistance is disengaged, your accelerator works normally. When engaged, StarPilot can use the pedal for speed control on supported setups.

On supported non-ACC setups, the pedal can provide acceleration and regen braking in one-pedal mode. On supported ACC-plus-pedal configurations, StarPilot can blend pedal-based regen with ACC friction braking. Standstill behavior depends on the vehicle. See [Bolt hardware](../cars/bolt.md) for specific examples.

You can override assistance with the accelerator. What engages or disengages depends on your vehicle and configuration. See [Operation](../usage/operation.md#basic-operation).



## Pedal Purchase List

{% include-markdown "./embed/see-car-guide.md" %}

* [Comma Pedal](https://shop.beartech.ca/products/comma-pedal)
* Ethernet cable. The [pedal supplier](https://docs.innoisle.com/beartech/comma-pedal-description-and-installation-guide) recommends round Cat6. Choose a length for the route from your harness box to the accelerator.
* Optional: [DFU Key](https://shop.beartech.ca/products/dfu-key)
    * If the firmware is ever updated, you need a DFU key (or DIY if you are mechanically inclined) to
apply new firmware. See [the Bolt pedal firmware instructions](../cars/bolt.md#pedal-firmware-flashing) for details.

> [!TIP] Bundle your pedal with a harness box.
> If you already have a Harness Cable, 
> but your Harness Box does not have an RJ45 port (or you do not have one), 
> you can bundle your Pedal with a 2x9 or 2x13 pin Harness Box - check your specific cable to 
> ensure you purchase the correct box.
