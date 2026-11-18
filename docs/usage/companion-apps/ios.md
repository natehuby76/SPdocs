---
title: StarPilot BT for iOS
description: Set up StarPilot BT on iPhone, choose a connection, use Galaxy features and submit diagnostic logs through Discord.
---

# StarPilot BT for iOS

StarPilot BT brings [Galaxy](../galaxy.md) to your iPhone. [Download StarPilot BT on the App Store](https://apps.apple.com/ca/app/starpilot-bt/id6821039119). Maintained by **natehuby76**. [Source repository](https://github.com/natehuby76/starpilot-galaxy-ios).

Controls and features can vary with the installed app and StarPilot build.

## Set up StarPilot BT

1. Install the app on an iPhone running iOS 17 or later. Your comma needs a compatible StarPilot build with the Bluetooth bridge. Initial bridge setup needs Internet access on the comma.
2. While parked, join the same Wi-Fi network as your comma or join its Galaxy hotspot. Open StarPilot BT and allow Local Network and Bluetooth when prompted.
3. Under **Your comma**, connect on **Local Wi-Fi** and select your device if more than one appears. Let the app load Galaxy from your comma.
4. To set up Bluetooth for later, choose **Bluetooth** and tap **Set up Bluetooth**. The app opens the pairing window on your comma and saves the pairing. If your app asks you to open **Pair phone** first, use **Settings → Bluetooth → Pair phone** on the comma and follow the prompts in the app.

## Choose a connection

| Connection | When to use it |
| --- | --- |
| **Automatic** | Tries Local Wi-Fi, Tunnel and Bluetooth in that order by default. Use **Set order** to change the priority. |
| **Local Wi-Fi** | Connect over Galaxy Wi-Fi or a shared network. Use this for recordings, camera images and network tools. |
| **Bluetooth** | Use supported settings and basic controls close to your paired comma, even without Wi-Fi. Open Galaxy over a network connection first so the app can save its screens. |

### Set up the Galaxy tunnel

If your build shows **Galaxy tunnel**, connect to your comma over Local Wi-Fi or Bluetooth, then tap **Set up** next to it in **Settings**. Scan the remote Galaxy QR code on the comma or paste its private Galaxy link. Sign in and tap **Use tunnel**. Both devices need Internet for Tunnel. See [Remote access](../galaxy.md#pairing) to pair your device for remote access first.

## What you can do

- **Manage settings and update Galaxy screens.** Open Galaxy to view toggles and device information. Under **Settings → Galaxy screens**, tap **Check** for updates. Use Local Wi-Fi or Tunnel to download them.
- **Review footage and logs.** Use Local Wi-Fi for [Routes](../galaxy.md#routes), camera images and downloads. Use the iOS share sheet to save or share a downloaded file.
- **Share a destination.** From a supported maps app, share a place to **StarPilot**. If the comma is unreachable, the app can save the destination to send when it reconnects.
- **Share phone location.** Turn on **Share phone location** in Settings and follow the iOS permission prompts. In [Navigation & Maps](../../exclusive/navigation.md#position-gps), choose how StarPilot uses the phone’s position.
- **Get Sentry phone alerts.** Turn on **Sentry phone alerts** in Settings and allow notifications. When the phone is registered and alerts are configured, use **Advanced connection options → Test Sentry alerts → Test** to check delivery. See [Sentry Mode](../../exclusive/sentry-mode.md#notifications).
- **Play phone music.** While connected, tap **Set up** next to **Phone music**. Pair from the iPhone’s Bluetooth settings and select the comma as an audio output in Control Center.

## Connection problems

Keep the comma powered and nearby. Check the app’s Bluetooth or Local Network permission for the route you selected. If the app can no longer verify the saved pairing, follow its reconnect prompt.

## Submit logs through Discord

1. Open **Settings → Logs & support → Report a problem on Discord**. If the app can’t connect to your comma, use **Submit connection log** on the connection screen instead.
2. Tap **Connect Discord** if prompted and sign in. The phone needs Internet to submit the report.
3. Describe what happened and what you tried. Review the attached diagnostics, then tap **Send**. The app captures fresh diagnostics and the installed app version.
4. Choose **New thread** for a new problem or select an existing report for a follow-up. Tap **Send report** and open the Discord thread to see replies.

Your description and Discord username appear in the support forum. Diagnostics, which can include device names and local network addresses, go to the private support channel. To save a copy separately, use **Logs & support → Troubleshooting → Export logs (.txt)**.

For beta access and help trying new test features, [ask in Discord](https://firestar.link/discord).
