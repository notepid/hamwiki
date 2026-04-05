---
title: NVIS (Near Vertical Incidence Skywave)
description: Using NVIS for reliable regional HF communication within a 0–600 km radius
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, nvis, hf, emergency
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# NVIS (Near Vertical Incidence Skywave)

Near Vertical Incidence Skywave — commonly abbreviated as NVIS — is an HF propagation technique used to provide reliable communication within a radius of roughly 0 to 600 km (0–370 miles). It works by directing radio signals nearly straight up so they reflect off the [ionosphere](/propagation/ionosphere) and come back down at steep angles, blanketing the area directly around the transmitter with coverage that fills in the "skip zone" that conventional HF skywave misses.

NVIS is widely used by military communicators, [emergency communication](/emergency-communications/overview) groups, and amateur radio operators who need reliable regional coverage over mountainous terrain, dense forest, or other environments where VHF/UHF line-of-sight signals struggle.

## The problem NVIS solves

With conventional HF skywave propagation, signals leave the antenna at relatively low angles and return to Earth at a considerable distance — the "skip distance." Between the outer edge of ground wave range (perhaps 50–100 km) and the point where the skywave signal first returns (which might be 500–1,500 km away on some bands), there is a dead zone where the signal cannot be heard.

For DX operators, this skip zone is irrelevant — they want to reach distant stations anyway. But for operators who need to communicate within their own region — say, coordinating disaster relief across a province or state — the skip zone is a serious problem. VHF/UHF repeaters can fill this gap in flat terrain, but in mountainous or heavily forested areas, repeater coverage is often spotty or nonexistent.

NVIS fills this gap by transmitting the signal almost straight up. The ionosphere reflects it straight back down, and the coverage pattern looks like an umbrella centred on the transmitter's location — strong, reliable coverage from directly overhead out to several hundred kilometres in all directions, regardless of terrain.

## How NVIS works

The key to NVIS is a combination of the right frequency, the right antenna height, and the right time of day.

### Frequency selection

NVIS works on frequencies that are *below* the critical frequency of the F layer (foF2) — the highest frequency that the ionosphere will reflect at vertical incidence. In practice, this means NVIS is most effective on the lower HF bands:

- **75/80 metres (3.5–4.0 MHz):** The primary NVIS band. The F layer critical frequency almost always exceeds 3.5 MHz during the day, making 80 m a reliable NVIS choice. This band works particularly well for voice communication.
- **40 metres (7 MHz):** Works well as an NVIS band during times of moderate to high solar activity when the critical frequency is above 7 MHz. During solar minimum, 40 m may exceed the critical frequency and produce skip instead of NVIS coverage, especially at night.
- **60 metres (5 MHz):** Where available, 60 m is an excellent NVIS band, sitting neatly between 80 m and 40 m. Some emergency communication groups use 60 m specifically for NVIS operations.

The key principle: if your operating frequency is above the critical frequency, the signal will pass through the ionosphere instead of reflecting back. Monitoring the foF2 (available from ionospheric soundings and [propagation tools](/propagation/propagation-tools)) tells you the upper limit for NVIS on a given day.

### Antenna height

Conventional HF wisdom says "get your antenna as high as possible" to lower the takeoff angle for DX. NVIS inverts this advice. For NVIS, you want a **low** antenna that radiates most of its energy straight up.

A horizontal dipole or inverted-V antenna mounted at 0.1 to 0.25 wavelengths above ground produces a radiation pattern that is strongly concentrated at high angles (60–90 degrees above the horizon), which is exactly what NVIS needs.

In practical terms:

| Band | 0.1 wavelength height | 0.2 wavelength height |
|------|-----------------------|-----------------------|
| 80 m (3.5 MHz) | ~8.5 m (28 ft) | ~17 m (56 ft) |
| 40 m (7 MHz) | ~4.3 m (14 ft) | ~8.5 m (28 ft) |
| 60 m (5 MHz) | ~6 m (20 ft) | ~12 m (39 ft) |

A 40-metre dipole at just 4–5 metres (13–16 ft) above ground makes an effective NVIS antenna — easy to deploy in the field with simple supports or even hung from tree branches. This makes NVIS especially practical for portable and emergency operations.

### Ground reflection

The ground beneath an NVIS antenna acts as a reflector, reinforcing the upward radiation. The effectiveness of this reflection depends on the ground conductivity. Wet or clay-rich soil provides better reflection than dry, rocky, or sandy ground.

Some operators improve NVIS performance by placing a wire mesh, chicken wire, or a few ground radials beneath the antenna. While not essential, a ground screen can add 2–6 dB of gain in the overhead direction — a worthwhile improvement for emergency communications where every decibel matters.

## NVIS coverage characteristics

A well-configured NVIS station typically provides:

- **Reliable coverage from 0 to approximately 300 km (185 miles)** under most daytime conditions on 80 metres.
- **Extended coverage to 500–600 km (310–370 miles)** under good conditions, especially on 40 metres.
- **Terrain-independent coverage:** Because the signal comes from overhead, it's not blocked by mountains, hills, or buildings. This is NVIS's greatest advantage over VHF/UHF for regional communication in difficult terrain.
- **Coverage directly under the antenna:** Unlike conventional skywave, there is no skip zone. Stations just a few kilometres away can communicate as easily as stations 300 km away.

The tradeoff is that NVIS provides essentially no coverage beyond about 600 km. For longer distances, conventional skywave propagation on higher bands is needed.

## When NVIS works

NVIS effectiveness depends on the ionosphere supporting reflection at the chosen frequency:

**Daytime (best):** The F layer is most strongly ionized during the day, supporting NVIS on both 80 m and 40 m. The D layer does add some absorption, but at the frequencies used for NVIS, the signal still gets through with usable strength.

**Night:** The F layer weakens as the Sun sets, and the critical frequency drops. 40 m may no longer support NVIS at night (especially during low solar activity), but 80 m typically continues to work. On 80 m, nighttime NVIS coverage is usually more limited in radius than daytime coverage.

**Solar cycle effects:** During solar maximum, the critical frequency is higher, which means both 40 m and 80 m work reliably for NVIS, and the coverage radius is larger. During solar minimum, 40 m may only support NVIS during the middle of the day, and 80 m becomes the primary NVIS band.

**Seasonal effects:** Summer daytime produces the highest critical frequencies, favouring NVIS. Winter daytime has lower critical frequencies but also less D-layer absorption.

## NVIS for emergency communications

NVIS is a cornerstone of amateur radio [emergency communications](/emergency-communications/overview) planning. When infrastructure fails — cell towers down, internet out, repeaters offline — NVIS on 80 or 40 metres can provide reliable statewide or regionwide communication using simple, quickly deployable equipment.

Advantages for emergency use include:

- Antennas are simple and quick to set up (a dipole at low height, supported by trees, masts, or vehicles).
- No infrastructure required — no repeaters, no internet, no power grid.
- Coverage fills in valleys and terrain shadows that VHF/UHF cannot reach.
- Works with modest power levels (25–100 watts is typical).
- Equipment is standard HF gear that many amateurs already own.

Organizations like [ARES](/emergency-communications/ares) and [RACES](/emergency-communications/races) in the United States, and similar groups worldwide, train specifically on NVIS techniques. A portable NVIS station can be operational within minutes using a battery-powered transceiver and a dipole hung from whatever supports are available.

## Setting up an NVIS station

### Basic NVIS station

A minimal NVIS station consists of:

1. An HF transceiver capable of operating on 80 m and/or 40 m.
2. A horizontal dipole or inverted-V antenna cut for the chosen band, mounted at low height (0.1–0.2 wavelength above ground).
3. Coaxial feedline (even short runs of RG-58 are fine for this application).
4. A power source (home station power supply, battery, generator, or solar panel).

### Antenna options

**Dipole:** The simplest and most common NVIS antenna. Hang it between two supports at low height. An 80 m dipole is about 40 m (130 ft) long; a 40 m dipole is about 20 m (66 ft).

**Inverted-V:** A dipole with the centre raised on a single support and the ends sloping down. This is easier to deploy in the field (only one high support needed) and still works well for NVIS.

**Fan dipole:** Two dipoles (one for 80 m, one for 40 m) fed from the same point, providing NVIS coverage on both bands without an [antenna tuner](/equipment/antenna-tuners).

**Loop antenna:** A full-wavelength horizontal loop at low height also works well for NVIS, with the bonus of slightly broader bandwidth.

### Tips for effective NVIS operation

- Keep the antenna as horizontal as possible. The flatter the antenna, the more energy goes straight up.
- If using an inverted-V, keep the included angle between the wire elements above 90 degrees. Steeper angles shift radiation away from the desired high angles.
- Choose your frequency carefully. Monitor the foF2 (via ionosondes or propagation tools) and operate below it.
- On 80 m, the 3.8–3.9 MHz voice segment is commonly used for NVIS nets in the US. International allocations vary.
- Consider a ground screen beneath the antenna for improved performance, especially over dry or poor soil.

## Further reading

- [HF Propagation](/propagation/hf-propagation) — Overview of all HF propagation modes
- [The Ionosphere](/propagation/ionosphere) — Understanding the layers that make NVIS work
- [Emergency Communications Overview](/emergency-communications/overview) — How amateur radio supports emergencies
- [Antennas Overview](/antennas/overview) — Choosing and building antennas
- [Propagation Tools](/propagation/propagation-tools) — Monitoring critical frequency and foF2
- [Propagation Overview](/propagation/overview) — Introduction to all propagation types
