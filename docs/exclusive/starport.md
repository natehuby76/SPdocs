---
title: StarPort — Setup & Troubleshooting
description: Show StarPilot on a car screen or tablet, configure audio and layout, and troubleshoot connections.
---

# StarPort

<span id="android-auto"></span>

Open **Galaxy → Tools → StarPort** while parked. StarPort shows StarPilot on your car screen
or tablet. Choose built-in wireless Android Auto, a wireless adapter, USB where available,
or a tablet app. Tested adapters include **AAWireless** and **Motorola MA1**. The supported
tablet apps are **HeadunitPad** on iPad and **Open Headunit** on Android tablets.

## Set up

### StarPort Support

Under **StarPort Support**, choose **Install support**. Follow Galaxy’s download instructions
for a stable Android Auto package by Google LLC. Use **Choose File** to select the package
as downloaded, then choose **Install** or **Turn On and Install**. Wait for **Ready**. For
wireless car or adapter pairing, enable Bluetooth if Galaxy prompts you. Use a local
network connection for the package download and upload.

### Connection choices

<span id="wireless-adapters"></span>

| Choose | What to do |
| --- | --- |
| **Built-in wireless** | Open the car’s phone pairing screen. Tap **Find car**, select the car and confirm the code on both screens. |
| **Wireless adapter** | Use the car’s wired Android Auto data port. Select **Wireless adapter** in StarPort and follow the [adapter pairing steps](#pair-a-wireless-adapter). |
| **USB cable** | If **Wired AA** is available, connect the car’s Android Auto USB data port to the comma with a data-capable cable. |
| **Tablet app** | Put the tablet on the same Wi-Fi as the comma or join the Galaxy hotspot. Follow the steps Galaxy shows for the selected app. |

Tap **Connect** when prompted. Keep the car on and its screen awake for the first connection.
Enable **Automatic Connection** to connect when you start driving.

Disconnect wired Android Auto before enabling [Jetlink](../usage/model-manager.md#jetlink).
Both use the comma's USB-C port.

### Pair a wireless adapter

1. Verify wired Android Auto works in the car’s USB data port, then plug the adapter into that port. In StarPort, select **Wireless adapter** and choose the matching adapter model.
2. If an old phone is already using the adapter, disconnect it or temporarily turn off that phone’s Bluetooth and Wi-Fi. Leave the adapter powered.
3. Open pairing mode on the adapter. On an **AAWireless TWO**, hold the button for about two seconds until the light is solid purple. Look for **AAWireless-XXXX**. For another AAWireless model, follow its model-specific pairing steps. On a **Motorola MA1**, hold the button and release as soon as the light flashes blue. Look for **AndroidAuto-XXXX**.
4. Tap **Find adapter**, or **Pair another adapter** if one is already selected. If more than one device appears, match the advertised name and suffix to yours. Select it and follow the pairing prompts. Use the adapter entry for this connection. If Galaxy asks you to connect a paired car in Bluetooth, do that and return to StarPort.
5. If discovery or pairing times out, confirm the adapter is still in pairing mode and the old phone is disconnected. Restart discovery. If the adapter keeps hanging up, briefly unplug it and reconnect it while the car screen stays on. For a stale pairing, follow [Start over](#start-over).

[AAWireless pairing guide](https://www.aawireless.io/en/articles/best-wireless-android-auto-adapter-2026-aawireless-two-vs-two-plus) · [Motorola MA1 user guide](https://www.motorolasound.com/media/44kdgyve/ma1_ug_en_na_v18.pdf)

## Connection problems

| What Galaxy shows | What to check |
| --- | --- |
| **Finding Android Auto** or **Waiting for car Wi-Fi** | Check that StarPort Support shows **Ready**, the right car or adapter is selected, and wireless Android Auto is enabled in the car. |
| **Waiting for your USB cable** | Use the car’s Android Auto data port and a data-capable cable. |
| **Connected · car screen in use** | Open Android Auto on the car screen to return to StarPilot. |
| **Trying your connection again** | Let StarPort retry and follow the prompts. |

If the screen is black or frozen, tap **Disconnect**, wait a few seconds, then reconnect.
If it keeps happening, restart the car or adapter.

### Connection Logs

1. Try to reproduce the issue while parked. Open **Connection Logs** in StarPort and find the attempt by time, car and connection type. The list shows up to 20 sessions, newest first.
2. Check the outcome. **Projected** means the connection reached the projection stage. **Failed** shows the recorded error. A stop at **RFCOMM** means the attempt ended during Bluetooth setup. Include the last status shown in Galaxy if the log gives little detail.
3. For a StarPort issue, use **Send StarPort logs** if it is available. Add a short description of what happened. You can also use **Download all logs** over a network connection and attach the zip to a [support ticket](../ticketsystem.md). Include the car year/model, adapter model, connection type and steps you tried. Bluetooth-only access shows summaries and can send the archive from the comma when **Send StarPort logs** is available.

## Other phones and audio

### Keep another phone from taking over

1. On the car’s screen, open its paired devices or phone projection list. Select the comma and set it as the preferred or first device if the car offers that option. For an adapter, use its phone-switching or priority control if available.
2. On the other Android phone, search Settings for **Android Auto**. Turn off **Wireless Android Auto** if the phone offers that switch. If you only want to stop it for this car, disable projection for that phone in the car’s device list. If the car has no separate projection control, remove the other phone’s car or adapter pairing.
3. Reconnect StarPort with the other phone disconnected. Re-enable the other phone’s Bluetooth afterward if you still use it for calls.

### Play music from your phone

1. In Galaxy, open **Bluetooth → Pair phone**. Follow any media-audio pairing prompts.
2. Open **StarPort → Spotify and Phone Audio**. Choose **Phone over Bluetooth**, select your phone, and turn on **Phone Audio**.
3. On your phone, select the comma as the media audio output and play music. Calls and microphone audio stay on the phone.

### Set up Spotify Connect

1. In **Spotify and Phone Audio**, choose **Spotify Connect on the comma**. Follow **Install** under **Spotify Soloist** to download and upload the ARM64 Linux archive. Keep the archive as downloaded.
2. With Spotify Premium, use **Create Your API Key** in Galaxy. Save the key and select **Car speakers via StarPort (Android Auto)** under **Send audio to** when prompted.
3. Start StarPort. Put the phone and comma on the same network for first pairing. Open Spotify on your phone, play something, and select the comma from the device picker. Keep both devices online for playback.

[Spotify Connect setup](https://support.spotify.com/article/spotify-connect/)

## Layout, maps and upkeep

<span id="settings-and-upkeep"></span>

**Customize Layout** opens the editor for the StarPort display. **Offline Road Maps**
saves road lines for the map overlay.

Wireless projection can interrupt the comma’s usual Wi-Fi connection. Use the Galaxy
hotspot for local access. Remote Galaxy still needs Internet on the comma.

If the support certificate expires soon or has expired, use **Update** or **Reinstall**
under **StarPort Support**.

## Start over

For a saved wireless setup, try **Reset handshake** if Galaxy offers it. This returns
to the standard handshake and keeps your Bluetooth pairing.

- **Built-in wireless:** In Galaxy, open **Tools → Bluetooth**, find the car and choose **Forget**. On the car screen, remove the comma from paired phones or the Android Auto list. Then use **Find car** again.
- **Wireless adapter:** Forget the adapter in Galaxy under **Tools → Bluetooth**. In the adapter’s own settings, remove the comma if the adapter provides a paired-device list. If it only offers pairing mode, open that mode to pair again. Use the manufacturer’s reset instructions only if stale pairings still block setup. A factory reset clears the adapter’s other saved pairings too.
- **USB or tablet:** Return to the matching connection steps. Reconnect the data cable or reconnect the tablet app to the comma’s network.
