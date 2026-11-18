---
title: Lane Centering
description: Learn how StarPilot Lane Centering uses detected lane lines alongside the end-to-end driving model, including corrections and fallback behavior.
---

# Lane Centering

Lane Centering is a StarPilot feature that helps keep your vehicle centered between detected lane lines while still allowing the End-to-End (E2E) model to control the driving path.

Instead of replacing the E2E model, Lane Centering works alongside it.

## How Does Lane Centering Work?

When both lane lines are detected clearly and confidently, StarPilot compares the E2E model's predicted path with the center of the lane.

If they differ, StarPilot applies a small, smooth correction toward the lane center while still allowing the E2E model to make driving decisions.

With one reliable lane line, StarPilot can sometimes adjust the model path to maintain clearance using other reliable geometry, such as a road edge. If neither path correction has enough evidence, or a lane change or another condition prevents correction, StarPilot falls back to the normal E2E path.

## How Can I Tell Which Direction Lane Centering Is Correcting?

The lane line on the side StarPilot is pulling toward can change color when a correction is active. The indicator depends on the driving display and your color settings.

## How Do I Enable Lane Centering?

In Galaxy, open **Toggles → Lateral (Steering) → Lane Centering**. You can also search for **Lane Centering** in Toggles. Availability depends on the vehicle and configuration.

## Lane offset

<span id="what-is-lane-center-offset"></span>

**Lane offset** lets you adjust the preferred position within the lane, for example slightly closer to the right side.

## Model path preference

<span id="what-is-e2e-authority"></span>

Higher **Model path preference** lets a confident model path reduce the centering correction when it differs from the lane center.

## Lane Centering Strength

**Lane Centering Strength** adjusts the amount of correction. Use 100% for the normal correction. Lower values reduce it and higher values strengthen it.

## Pause on signal

**Pause on signal** temporarily pauses the centering correction when the turn signal is active.

> [!IMPORTANT]
> Lane Centering works alongside the driving model and falls back to its normal path when required conditions aren’t met.
