---
title: Chevrolet Volt & GM ASCM/SDGM Hardware
description: Explore StarPilot hardware configurations for Chevrolet Volt and other GM cars using ASCM or SDGM, with steering and speed control requirements.
---

# Required Hardware - Volt & Other ASCM/SDGM Cars

The Volt has a number of possible configurations. 
This page lists hardware and control options for common configurations. Match the vehicle, harness and speed-control setup before ordering parts.

There are two parts to OpenPilot control: Lateral Control (Steering) & Longitudinal Control (Gas/Brake).

On supported ASCM and SDGM setups, the harness can provide steering while the factory ACC keeps speed control. A compatible SASCM setup can allow StarPilot to control speed. If you plan to keep factory ACC, follow the steering-only hardware requirements for your car.

## Recommended Config per Car Model

* 2017-2018 Chevy Volt with Factory ACC: [ASCM Harness & SASCM](#ascm-harness-sascm)
* 2019 Chevy Volt with Factory ACC: [SDGM Harness & SASCM](#sdgm-harness-sascm)
* Volts without Factory ACC: [Volts without ACC](#volts-without-acc)
* Non-Volt Car with ASCM: [ASCM Harness & SASCM](#ascm-harness-sascm)
* Non-Volt Car with SDGM: [SDGM Harness & SASCM](#sdgm-harness-sascm)

{% include-markdown "../hardware/embed/beartech.md" %}
{% include-markdown "../hardware/embed/comma-power.md" %}

## ASCM Harness & SASCM

### Purchase List

1. [Comma 4](../hardware/comma.md)
2. [ASCM Harness Plus + Harness Box](https://shop.beartech.ca/products/ascm-harness?variant=44900990124213) with matching 2×9 connectors
3. For StarPilot speed control where supported, add [SASCM](https://shop.beartech.ca/products/sascm-for-gm-vehicles).
4. [OBD-C Cable](../hardware/obd-c.md) - 15 ft 
5. [Comma Pedal](../hardware/comma-pedal.md) where required for your configuration or supported standstill behavior

### Reference Connection Diagram

![Reference diagram](../assets/images/hardware/volt/ASCM_SASCM_connection_diagram_final.png)

## SDGM Harness & SASCM

### Purchase List

1. [Comma](../hardware/comma.md)
2. [SDGM Harness + Harness Box](https://shop.beartech.ca/products/sdgm-harness). Choose the correct A/B variant, a matching 2×9 box and the required OBD power connection.
3. For StarPilot speed control where supported, add [SASCM](https://shop.beartech.ca/products/sascm-for-gm-vehicles).
4. [OBD-C Cable](../hardware/obd-c.md) - 10 ft 
5. [Comma Pedal](../hardware/comma-pedal.md) where required for your configuration or supported standstill behavior

## Volts without ACC 

### Purchase List

1. [Comma](../hardware/comma.md)
2. Choose a harness:
    1. [OBD-II Harness](../hardware/obd-harness.md)
    2. [GM Harness/Harness box (only for Volts with stock LKAS)](../hardware/gm-harness.md)
3. [Comma Pedal](../hardware/comma-pedal.md) where required for your configuration or supported standstill behavior

Lateral (steering) control:

1. If you have stock LKAS, your volt is capable of openpilot lateral control.
2. If not, you need to [flash LKAS firmware](#flashing-volt-firmware)

Longitudinal (gas/brake) control:

1. A confirmed [ACC firmware retrofit](#flashing-volt-firmware) has its own hardware and control requirements.
1. [CC Long](#what-is-redneck-acc-aka-cc-long) uses factory cruise buttons where supported.
1. A compatible [Comma Pedal](../hardware/comma-pedal.md) can use regen in L mode on supported setups. Confirm availability for your exact vehicle and firmware.

### Flashing Volt Firmware

> [!CAUTION] 
> Flashing your car's firmware is at your own risk.
> Unlike the custom harness installs, 
> flashing is not reversible by simply unplugging hardware.

pinballben is the resident expert on flashing Volt firmware, who will provide the instructions and hardware
for a fee. DM on [Discord](https://firestar.link/discord) (through the member list).

> [!CAUTION] Flashing ACC 
> Flashing ACC will remove stock CC. 
> This can be restored by re-flashing stock firmware. 

## GM Vehicle Settings

In Galaxy, open **Toggles → Vehicle**. Use **Auto** or select the exact registered vehicle configuration if manual identification is needed. With the vehicle off, verify the ACC, harness and pedal options before your next drive.

## What is Redneck ACC (aka CC Long)?

On supported configurations, CC Long uses the factory cruise system’s virtual **+** and **−** button presses to adjust speed. Its speed range and ability to slow depend on the configuration. It can make small adjustments on the highway. Be ready to respond to slowing or stopped traffic and brake manually.

## GM LKAS Faults

Pull over safely, switch the vehicle off and inspect the connections following the hardware guide. If faults recur, [report the exact configuration and logs](../ticketsystem.md).
