---
title: Navigation & Maps
description: Set a destination, configure Mapbox and GPS, and download offline maps in Galaxy.
---

# Navigation & Maps

<span id="navigation"></span>

Galaxy sends a destination to your comma and shows route choices. Steering and speed follow
your normal engagement settings.

## Set up

<span id="setup-checklist"></span>

While parked, open **Galaxy → Tools → Navigation & Maps → Setup**. Turn on **Navigation** and
save a public Mapbox token, starting with `pk.`.

An optional Google key adds Google maps, traffic-aware routing and place search. Mapbox
remains required.

## Plan a route {#how-to-use-it}

On **Destination**, search for a place or choose a saved or recent one. Tap a result to start
guidance and choose an alternate route if offered. **Change destination** searches again;
**End navigation** clears the route. The star saves a place as Home, Work or another favorite.

Routes show traffic-aware choices and ETA when available. Galaxy can reroute after a route
deviation. You can start or end guidance through your remote Galaxy link.

## Position / GPS

Under **Setup → Position**, choose:

- **Comma and car, phone as backup:** uses phone GPS when neither comma nor car has a fix.
- **Comma and car only:** does not use phone GPS.
- **Phone first:** uses a recent phone fix, otherwise comma or car GPS.

Enable location sharing in a [supported companion app](../usage/companion-apps/index.md) to supply phone GPS. Updates reach the comma over Bluetooth or local Wi-Fi.

## Offline Maps

**Offline Map Management** saves Mapbox road lines for the map overlay. Downloads use Wi-Fi
and require your Mapbox key. Google map tiles cannot be saved offline.

**Speed Limit Maps** downloads regional coverage for map-based speed limits. The selected
coverage applies the next time the Maps service starts. Choose **Maps** as a source in the
[Speed Limit Controller](./speed-limit-controller.md#speed-limit-sources) to use those readings.

Planning a new route still needs Internet.

## How it helps while driving

<span id="features"></span>
<span id="galaxy-vs-the-comma-device"></span>

Galaxy manages destinations and saved places; the comma displays turn-by-turn instructions.

Turn assistance is limited to supported low-speed turns with the matching turn signal and
corresponding blindspot clear. Upcoming maneuvers can also reduce the target speed when
StarPilot controls speed.

Navigation does not complete turns or exits for you. Stay attentive and ready to steer or
brake.

## Credits

Thanks to **Chubbs** ([discountchubbs](https://github.com/discountchubbs)) for the navigation work StarPilot builds on, including his work in sunnypilot.
