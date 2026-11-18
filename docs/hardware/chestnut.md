---
title: Chestnut External GPU Support
description: Learn about StarPilot support for the Chestnut external GPU on comma 3, 3X, and 4, including when larger driving models need an eGPU.
---

# Chestnut (External GPU)

**Chestnut** is comma.ai’s external GPU dock. The cable, power and software requirements depend on the device.

Learn more from comma.ai: [Introducing chestnut](https://blog.comma.ai/chestnut/) · [Chestnut shop](https://comma.ai/shop/chestnut)

## What does Chestnut do?

Chestnut lets the comma run compatible larger models on a desktop GPU.

## Do I need Chestnut?

**Most users do not need Chestnut.** Standard driving models can run on the comma’s built-in hardware.

In Galaxy, you can download compatible GPU models for later without Chestnut connected. Running them requires ready, supported hardware. If a selected model needs unavailable hardware, StarPilot can fall back to an eligible model. See **Running now** in [Models](../usage/model-manager.md) to check what is in use.

## Hardware options

Comma sells the dock on its own and a ready-to-drive kit for comma four. Check the [Chestnut shop](https://comma.ai/shop/chestnut) for current kit contents, compatibility and pricing. Comma 3 and 3X setups have their own connection and power requirements.

## Setup overview

Follow the instructions for your dock, GPU and comma device:

1. Assemble and secure Chestnut and the compatible GPU.
2. Connect the specified power supply and data cable for your hardware.
3. Start StarPilot and check in [Models](../usage/model-manager.md) that the hardware is ready and the expected model is running.

> [!NOTE] Firmware
> The device checks that supported firmware is ready before enabling GPU models. If GPU models stay unavailable after connecting Chestnut, ask in [Discord](https://firestar.link/discord).

> [!TIP] Driving models
> See [Models](../usage/model-manager.md) for model selection and hardware requirements, including [Jetlink](../usage/model-manager.md#jetlink) for a supported USB host.
