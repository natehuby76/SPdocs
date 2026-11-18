---
title: Galaxy for Android
description: Set up Galaxy for Android, choose Wi-Fi, remote access or Bluetooth, and learn about phone GPS, alerts and beta features.
---

# Galaxy for Android

Galaxy for Android brings [Galaxy](../galaxy.md) to your phone through local Wi-Fi, remote access or Bluetooth. [Download Galaxy on Google Play](https://firestar.link/android). Maintained by **dirwin31**. [Source repository](https://github.com/dirwin31/StarPilotAndroid).

## Set up Galaxy

1. Install the app and use a compatible StarPilot build on your comma.
2. While parked, join Galaxy Wi-Fi or the same local network as your comma. Open Galaxy and choose **Wi-Fi & LAN** in **Connections**.
3. To use Bluetooth later, open **Connections → Add Bluetooth Phone Pairing** and follow the **Add pairing** prompts. Allow nearby-device access when Android asks. If the app can’t open pairing over Wi-Fi, open **Settings → Bluetooth → Pair phone** on the comma and try again.
4. Load Galaxy over Wi-Fi if the app says it needs a Wi-Fi visit before Bluetooth can open the saved screens.

## Choose a connection

| Connection | When to use it |
| --- | --- |
| **Automatic** | Tries Wi-Fi and LAN first, then Remote if configured, then a saved Bluetooth connection. |
| **Wi-Fi & LAN** | Use Galaxy Wi-Fi or a shared network for camera images, recordings, replay and downloads. |
| **Remote** | Reach your comma over the Internet when away from the local network. Set up [remote Galaxy](../galaxy.md#pairing) first. Sign in using your Galaxy ID or add the App key from Galaxy Access. Keep the App key private. |
| **Bluetooth** | Use supported settings and basic controls near your paired comma. Switch to Wi-Fi or LAN for media and direct downloads. |

## What you can do

- **Manage settings and routes.** Open Galaxy to configure the comma or review [Routes](../galaxy.md#routes) over a supported connection. Choose **No StarPilot? Explore the demo** on the connection screen to try the interface with sample data.
- **Share phone GPS.** In **Connections → Phone GPS**, select **Share phone GPS with StarPilot** and allow location access. Location updates reach your comma over Bluetooth or local Wi-Fi. Keep the Phone GPS notification active while sharing. See [Position / GPS](../../exclusive/navigation.md#position-gps) for the choices on the comma.
- **Get Sentry alerts.** Allow Android notifications and enable **Galaxy App Alerts** where available in [Sentry](../../exclusive/sentry-mode.md#notifications). Test alert delivery after setup. Delivery depends on the app build and configured notification service.
- **Share a destination.** Share a supported Google Maps place to Galaxy to open it in [Navigation & Maps](../../exclusive/navigation.md).
- **Set up Bluetooth music.** If **Set up music only** appears in **Connections**, follow its prompts to add music pairing while keeping your app pairing.

## Connection problems

Check the connection mode, comma power and Android permissions. For an expired Bluetooth pairing, use **Forget pairing on this phone**, clear the matching saved pairing on the comma, then open **Pair phone** and pair again. For a remote error, confirm both devices have Internet and check that the Galaxy ID or App key matches your paired comma.

## Try a beta build

With the same Google account you use for Google Play, [join the Android beta group](https://groups.google.com/g/galaxy-starpilot-android-beta), then open [Google Play testing](https://play.google.com/apps/testing/com.starpilot.galaxy) and choose **Become a tester**.

Newer testing builds can share destinations from Google Maps or Waze directly to StarPilot, restrict automatic LAN discovery to preferred Wi-Fi networks, and save supported toggle changes to sync on reconnect.

### Report a problem through Discord

If your build shows **Connections → Debugging options → Report a problem**, use it to send app diagnostics to support.

1. Select **Connect with Discord** and sign in.
2. Describe the problem. Choose **New support thread** or an existing thread for a follow-up.
3. Tap **Send report**. After it sends, use **Open Discord thread** to follow replies.

Your description and Discord identity are visible in the support forum. Diagnostics go to a private support channel. If your build does not show this option, use the [Ticket System](../../ticketsystem.md).

For beta access and help trying new test features, [ask in Discord](https://firestar.link/discord).
