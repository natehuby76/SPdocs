---
title: Supported Cars & Vehicle Compatibility
description: Check the vehicles StarPilot adds or improves over stock openpilot, including GM, Honda, Hyundai, Kia, and more. Find car setup guides and support.
---

# Vehicle Compatibility

StarPilot adds support for cars that stock openpilot doesn't cover, and re-tunes a number
of cars that *are* supported by stock so they drive better.

Support depends on your car’s model year, trim, region, steering system, ACC configuration,
and installed hardware. Check the requirements for your exact configuration before choosing
hardware or enabling controls.

Trim, package, and harness notes describe specific configurations. Check the car guide
or ask in [Discord](https://firestar.link/discord) about other setups.

> [!TIP] Stock support list
> For everything stock openpilot already supports, see the official
> [comma supported vehicles list](https://comma.ai/vehicles).
> The cars below are *in addition to* (or improvements on) that list.

> [!NOTE] This is a snapshot
> Car support changes often. If your car isn't listed,
> ask in the [Discord](https://firestar.link/discord) — it may have been added since.

> [!INFO] Want special tuning for your vehicle?
> With your help, we can improve your vehicle's tune. Ask in the
> [Discord](https://firestar.link/discord)

## Supported & improved cars

### GM (Buick / Cadillac / Chevrolet / GMC)

**No-ACC** configurations use different speed-control methods, including factory cruise
buttons, a pedal interceptor, or a vehicle-specific retrofit. Braking and standstill behavior
depend on the configuration. Follow the car-specific guide before choosing hardware.

* Buick Baby Enclave 2020-23 — SDGM Harness; Driver Assist Package
* Buick Envision 2016 (Chinese specification) — SDGM retrofit and custom cross-flashed ADAS stack; ACC retains speed control
* Buick LaCrosse 2017-19 ASCM Harness
* Buick LaCrosse 2019 US ASCM Harness
* Cadillac CT6 2016-20 — No-ACC
* Cadillac Escalade 2018 ASCM Harness
* Cadillac Escalade ESV Platinum 2019 ASCM Harness
* Cadillac XT4 2023 — SDGM setup; Driver Assist Package
* Cadillac XT4 2023 — No-ACC
* Cadillac XT5 2022 — SDGM Harness; Driver Assist Package
* Cadillac XT5 2022 — No-ACC
* Cadillac XT6 2020 — SDGM Harness; Driver Assist Package
* Chevrolet Blazer 2019-25 — SDGM Harness; Driver Assist Package
* Chevrolet Bolt EV 2022-23 — factory-ACC setup: 2LT with Adaptive Cruise Control Package
* Chevrolet Bolt EUV 2022-23 — factory-ACC setup: Premier or Premier Redline, without Super Cruise Package
* Chevrolet Bolt EV 2017 — No-ACC
* Chevrolet Bolt EV 2018-21 — No-ACC
* Chevrolet Bolt EV / EUV 2022-23 — No-ACC
* Chevrolet Bolt EV / EUV 2022-23 ACC w/ Pedal
* Chevrolet Bolt EV / EUV 2022-23 *(improved over stock)*
* Chevrolet Equinox 2019-22 — No-ACC
* Chevrolet Equinox 2019-22 *(improved over stock)*
* Chevrolet Malibu 2017-19 ASCM Harness
* Chevrolet Malibu 2019 — SDGM Harness
* Chevrolet Malibu 2023 — No-ACC
* Chevrolet Malibu Hybrid 2017 — No-ACC
* Chevrolet Silverado 1500 2020-21 — No-ACC
* Chevrolet Silverado 1500 *(improved over stock)*
* Chevrolet Suburban Premier 2016-20 — ASCM Harness
* Chevrolet Suburban Premier 2016-20 — No-ACC
* Chevrolet Trailblazer 2021-22 — No-ACC
* Chevrolet Trailblazer 2021-22 *(improved over stock)*
* Chevrolet Traverse 2022-23 — SDGM Harness; RS, Premier, or High Country trim
* Chevrolet TRAX 2024-25 — Camera Harness; manual configuration; recognized vehicle network layout required
* Chevrolet Volt 2016-18 — No-ACC (OBD-C / L&P Harness)
* Chevrolet Volt 2017-18 ASCM Harness
* Chevrolet Volt 2017-18 Camera Harness — manual configuration; recognized vehicle network layout required
* Chevrolet Volt 2017-18 *(improved over stock)*
* Chevrolet Volt 2019 — SDGM Harness; factory ACC and LKAS
* GMC Acadia 2018 ASCM Harness
* GMC Sierra 1500 2020-21 — No-ACC
* GMC Yukon 2019-20 — No-ACC

### Honda / Acura

* Acura ADX 2025-26
* Acura Integra 2023-26
* Acura MDX 2014-16
* Acura MDX 2017-19
* Acura MDX 2020
* Acura MDX 2025-26 (excluding Type S)
* Acura MDX Hybrid 2017-19
* Acura MDX Hybrid 2020
* Acura RDX 2022-26
* Acura RDX 3G *(improved over stock)*
* Acura TLX 2015-21
* Acura TLX 2024-25
* Honda Accord 2016-17
* Honda Accord Hybrid 2017
* Honda Accord Hybrid 2023-26
* Honda Accord *(improved over stock, with supported modified EPS firmware)*
* Honda Civic / Civic Hatchback 2022-26
* Honda Civic / Civic Hatchback Hybrid 2025-26
* Honda Civic Hatchback Hybrid (Europe) 2023
* Honda Civic *(improved over stock, with supported modified EPS firmware)*
* Honda Clarity 2018-21
* Honda CR-V Hybrid 2023-27
* Honda CR-V 5G *(improved over stock, with supported modified EPS firmware)*
* Honda Fit (Taiwan) 2021
* Honda Fit (Taiwan) 2024-25
* Honda HR-V 2023-25 *(improved over stock)*
* Honda Odyssey (Singapore) 2021
* Honda Odyssey (Taiwan) 2018-19
* Honda Pilot *(improved over stock)*
* Honda Prelude 2026

Modified EPS support depends on the vehicle and firmware version. Confirm the exact setup
before flashing.

### Hyundai / Kia / Genesis

* Genesis G70 Non-SCC 2021
* Genesis G90 *(improved over stock)*
* Genesis GV70 3.5T Sport Prestige (with HDA II & LFA2) 2026
* Genesis GV70 Electrified 2026
* Genesis GV80 (3.5T Prestige Trim, with HDA II & LFA2) 2025
* Genesis GV80 Coupe (with HDA II & LFA2) 2025
* Hyundai Azera Hybrid (with HDA II & LFA2) 2025
* Hyundai Bayon Non-SCC 2021
* Hyundai Elantra 2024-25
* Hyundai Elantra Hybrid 2024-26
* Hyundai Elantra Hybrid Non-SCC 2022
* Hyundai Elantra Non-SCC 2022
* Hyundai Ioniq 5 N (with HDA II) 2024
* Hyundai Ioniq 5 PE (with HDA II & LFA2) 2025-27
* Hyundai Ioniq 6 *(improved over stock)*
* Hyundai Ioniq 9 (with HDA II & LFA2) 2025-26
* Hyundai Kona (without HDA II) 2024-25
* Hyundai Kona Electric (without HDA II) 2024
* Hyundai Kona Electric Non-SCC 2019
* Hyundai Kona Hybrid (without HDA II) 2024
* Hyundai Kona Non-SCC 2019
* Hyundai Palisade (with HDA II) 2023-25
* Hyundai Palisade (without HDA II) 2023-25
* Hyundai Santa Cruz (without HDA II) 2025
* Hyundai Santa Fe Hybrid (with HDA II & LFA2) 2024-25
* Hyundai Santa Fe Hybrid (without HDA II, LFA2) 2025-26
* Hyundai Sonata (without HDA II) 2024-25
* Hyundai Sonata Hybrid (without HDA II) 2024-25
* Hyundai Tucson (without HDA II) 2025-26
* Hyundai Tucson Hybrid (without HDA II) 2025-26
* Hyundai Tucson Plug-in Hybrid (without HDA II) 2025
* Hyundai i30 Hybrid 2024
* Kia Carnival 2025 (with or without HDA II)
* Kia Carnival Hybrid 2025-26 (with or without HDA II)
* Kia Ceed Plug-in Hybrid Non-SCC 2022
* Kia EV6 (with HDA I) 2025
* Kia EV9 2025-26
* Kia Forte Non-SCC 2019
* Kia Forte Non-SCC 2021
* Kia K4 (with HDA II) 2025
* Kia K4 (without HDA II) 2025-26
* Kia K5 (without HDA II) 2025
* Kia Niro EV (with HDA II) 2024-25
* Kia Niro Hybrid 2023-24
* Kia Niro Plug-in Hybrid 2022 *(improved over stock)*
* Kia Seltos Non-SCC 2023-24
* Kia Sorento (without HDA II) 2024-25
* Kia Sorento Hybrid 2026
* Kia Sportage (without HDA II) 2026
* Kia Sportage Hybrid 2026
* Kia Telluride (with HDA II) 2023-24
* Kia Telluride (without HDA II) 2023-25
* Kia XCeed Plug-in Hybrid 2021

> [!NOTE] CAN-FD steering
> CAN-FD cars use different steering systems and limits. Some use torque control; others
> use angle control. Available controls depend on the vehicle and configuration.

### Toyota

* Toyotas with a pedal / gas interceptor *(improved over stock)*
* Toyota Matrix 2005 with retrofit
* Toyota Prius 2016-20 with TSS2 EPS retrofit
* Toyota Sienna 2021-25

### Subaru

* Subaru Ascent 2023-25 *(improved over stock)*
* Subaru Crosstrek 2025 *(improved over stock)*
* Subaru Impreza *(improved over stock)*
* Subaru Impreza RS 2025 — angle-steering setup
* Subaru Legacy 2025 *(improved over stock)*
* Subaru Outback 2023-24 *(improved over stock)*

Available Subaru controller options and limits depend on the steering system and vehicle
configuration.

### Chrysler / RAM

* RAM 1500 5th Gen *(improved over stock)*
* RAM HD 5th Gen *(improved over stock)*

### Ford

* Ford Edge 2022
* Ford F-150 Lightning 2022-25
* Ford Mondeo 2014-22
* Ford Transit 2025 (Co-Pilot360 Assist+)

### Nissan

* Nissan Altima 2019-24
* Nissan Leaf 2018-25 — Instrument Cluster

### Tesla

* Tesla Model S (Pre-AP) 2012-14
* Tesla Model S (with HW1) 2014-16

Pre-AP and HW1 use different hardware and control setups. Confirm the exact configuration
before installing.

### Volkswagen Group

* Audi Q4 e-tron 2021-25
* Škoda Enyaq 2021-25
* Volkswagen ID.3 2020-25
* Volkswagen ID.5 2022-23
* Volkswagen Jetta 2018-23

## Vehicle tuning improvements

<span id="brand-wide-tuning-improvements"></span>

StarPilot includes vehicle-specific tuning and optional control settings. Available changes depend on the vehicle, steering system, speed-control configuration and selected controller.

* **Hyundai / Kia / Genesis** — Acceleration changes depend on the vehicle and whether StarPilot controls speed.
* **Honda / Acura** — Stopping behavior depends on the speed-control configuration.
* **Toyota** — Lateral tuning refinements are available on supported torque-steering setups.
* **GM** — Braking and regen behavior depend on the ACC, pedal and retrofit configuration.

Some configurations retain their standard controller settings. Optional StarPilot controllers and vehicle-specific features can change behavior where supported.
