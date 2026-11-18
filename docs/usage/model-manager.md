---
title: Models
description: Choose a single driving model, pair steering and speed models, and manage downloads and Jetlink in Galaxy.
---

# Models

<span id="driving-model"></span>
<span id="current-recommendations"></span>
<span id="previous-favorites-newest-to-oldest"></span>

Open **Galaxy → Tools → Models** to choose driving models and manage downloads.

The driving model processes camera video and plans steering and acceleration or braking.
Preferences vary with your car, roads, region and conditions. Use the current catalog and
community favorites, and ask for feedback in [Discord](https://firestar.link/discord).

## Single model

**Active Small · On-device** runs on the comma’s built-in compute. **Active Big · External**
selects a larger model for compatible external hardware. Choose **None — always use Active
Small** to stay with the on-device model.

[Chestnut](../hardware/chestnut.md) is supported on comma 3, 3X and 4. You can download a Big
model before connecting it. Without an external GPU or an active Jetlink host, Active Small
is used and your Big selection stays saved.

Selections take effect the next time the driving model starts. **Running now** reports the
loaded model.

## Model Randomizer

Model Randomizer chooses among eligible installed, verified models at each start, trying a
different model when another is available. Use **Include in Randomizer** to exclude individual
models. Favorites do not change the random pool.

## Model pair

Model pair combines one model’s **Lateral model**—steering and path—with another’s
**Longitudinal model**—speed and lead pacing.

1. Turn off the vehicle. Connect a firmware-ready Chestnut; the pair runtime must also be available.
1. Use **Show pairable models** and download the indicated pair variants. Ordinary on-device downloads alone do not establish readiness.
1. Choose **Model pair**, then two different downloaded models for the lateral and longitudinal roles. Valid selections save automatically and apply when the driving model next starts.
1. Check **Running now** and the pair status.

At least one model must have a Chestnut variant. Two Big models cannot run together; use a
Small model for at least one role. Pairing increases inference time and can cause model-lag
warnings.

Your Small and Big fallback selections remain saved. Choose **Single model** to return to
them at the next start.

## Downloads

Browse **On the comma**, **Needs GPU or Jetlink**, or **All**. Search, filter favorites or
pairable models, and sort by release date, name or size. Download individual models or use
**Download all**. Progress and retry controls appear here. Park before downloading.

## Jetlink

Jetlink requires a comma 3X or comma 4. Under **Jetlink → Remote model connection**, choose **USB computer** or **iPhone / iPad**.
Set up while parked with a USB 3 data cable and separate power. Keep the computer awake,
or the iPhone app open and unlocked. Jetlink stays off while Chestnut is connected.
Disconnect [wired Android Auto](../exclusive/starport.md#connection-choices) before enabling Jetlink.

Jetlink runs Active Big on its host, which downloads the model itself. **Prepared** means
the remote model is built, rather than active. Local Small remains available, and your
Small and Chestnut selections stay saved.

Follow the [Jetlink host setup guide](https://github.com/StarPilotHQ/StarPilot/blob/testing/openpilot/starpilot/models/JETLINK.md).
