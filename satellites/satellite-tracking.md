---
title: Satellite Tracking
description: How to track amateur radio satellites and predict passes using TLE data, software, and apps
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, tracking, TLE, pass prediction, Doppler
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Satellite Tracking

Working amateur satellites requires knowing when a satellite will be visible from your location, where it will appear in the sky, how long the pass will last, and what frequencies to use after accounting for Doppler shift. Satellite tracking tools answer all of these questions and are essential for anyone doing satellite work — from casual FM contacts to serious linear transponder operation.

## How satellite tracking works

### Orbital mechanics basics

Satellites in low Earth orbit (LEO) travel at roughly 7.5 km/s (27,000 km/h or 17,000 mph) and complete an orbit every 90–110 minutes. The Earth rotates beneath them, so each successive pass traces a different ground track. A satellite that passes over your location on one orbit may be hundreds or thousands of kilometres to the east or west on the next.

From any given location on the ground, a LEO satellite is typically visible (above the horizon) for only 5–15 minutes per pass, and you may get 4–8 usable passes per day for any particular satellite. The exact number depends on the satellite's orbit inclination, altitude, and your latitude.

### Two-Line Element sets (TLEs)

Satellite positions are predicted using **Two-Line Element sets (TLEs)** — a standardized data format that describes a satellite's orbit. TLEs contain information about the satellite's inclination, eccentricity, argument of perigee, mean anomaly, mean motion, and other orbital parameters. Tracking software uses these parameters along with mathematical models (SGP4/SDP4) to calculate where the satellite will be at any given time.

TLEs are published by several sources:

- **CelesTrak** (celestrak.org) — one of the most widely used TLE sources, curated by Dr. T.S. Kelso. Provides TLE sets for amateur satellites, the ISS, weather satellites, and many more.
- **Space-Track** (space-track.org) — the official source of TLE data from the US Space Force's 18th Space Defense Squadron. Requires a free account.
- **AMSAT** — publishes TLEs specifically for amateur radio satellites, often via the AMSAT website or through Keplerian elements distributed on the AMSAT mailing lists.

TLEs degrade in accuracy over time because they cannot perfectly account for atmospheric drag, solar radiation pressure, and gravitational perturbations. For LEO satellites, TLEs are typically updated every few days. Most tracking software can automatically download fresh TLEs from the internet.

### Pass geometry

A satellite pass is described by several key parameters:

- **AOS (Acquisition of Signal):** The time and direction where the satellite rises above your horizon. Expressed as an azimuth bearing (e.g., 210° = southwest).
- **LOS (Loss of Signal):** The time and direction where the satellite sets below your horizon.
- **Maximum elevation:** The highest point the satellite reaches in the sky during the pass, measured in degrees above the horizon. A 90° pass goes directly overhead; a 10° pass barely clears the horizon. Higher passes generally produce stronger signals and longer contact windows.
- **Duration:** The total time from AOS to LOS. For LEO satellites, this ranges from a few minutes for low-elevation passes to around 15 minutes for a high overhead pass.

Passes with maximum elevation below about 10° are typically marginal — the signal must travel through more atmosphere, and terrain or buildings may block the view. Most operators focus on passes above 20–30° for reliable contacts.

## Tracking software and apps

### Desktop software

**GPredict** (free, open source) is one of the most popular desktop satellite tracking programs. It runs on Linux, macOS, and Windows and provides real-time satellite tracking on a world map, pass prediction tables, polar plots showing the satellite's path across the sky, and rotator control integration for automated antenna tracking. GPredict can automatically download TLE updates and supports tracking hundreds of satellites simultaneously.

**SatPC32** is a Windows application popular among satellite operators, particularly for its radio control features. It can automatically adjust your transceiver's frequency to compensate for Doppler shift during a pass and control antenna rotators to follow the satellite. SatPC32 is available from AMSAT-DL.

**Orbitron** is another free Windows tracking program that has been popular for many years. It provides a visual display of satellite positions and pass predictions. While no longer actively developed, it remains functional and has a loyal user base.

**MacDoppler** is a macOS application that provides satellite tracking with integrated Doppler correction and radio control.

### Mobile apps

Smartphone apps are particularly convenient for satellite work because you often operate portable in a field or on a hilltop. Several apps provide real-time tracking, pass predictions, and even augmented reality views where you can hold up your phone and see the satellite's predicted position overlaid on the sky.

Popular satellite tracking apps include:

- **AMSAT satellite tracking apps** — AMSAT provides or endorses apps for both iOS and Android with amateur satellite frequencies and status built in.
- **Look4Sat** (Android, free and open source) — specifically designed for amateur satellite operators, with built-in pass prediction, Doppler correction, and satellite frequency databases.
- **Heavens-Above** (Android) — tracks satellites, the ISS, and other objects with pass predictions and sky charts.
- **Various ISS tracker apps** — many free apps track the ISS specifically, useful if your main interest is [ISS contacts](/satellites/iss-contacts).

### Web-based tracking

Several websites provide satellite tracking without any software installation:

- **N2YO** (n2yo.com) — real-time satellite tracking on a world map with pass predictions for any location.
- **Heavens-Above** (heavens-above.com) — detailed pass predictions, sky charts, and satellite visibility forecasts.
- **SatNOGS** (satnogs.org) — in addition to tracking, SatNOGS operates a network of automated ground stations that receive satellite telemetry, providing real-time information about whether a satellite is actually active and transmitting.

## Understanding Doppler shift

When a satellite approaches your station, the signals it transmits are compressed — the received frequency is higher than the satellite's actual transmit frequency. As the satellite recedes, the signals are stretched and the received frequency drops. This is the Doppler effect, and it is a significant factor in satellite communication.

For a typical LEO satellite pass, the total Doppler shift on a 435 MHz (70 cm) downlink is roughly ±10 kHz. On 145 MHz (2 m), it is about ±3.5 kHz. The shift is greatest when the satellite is near the horizon (moving most directly toward or away from you) and is near zero at the point of closest approach (when it is moving mostly across your sky).

### Doppler correction strategies

For **FM satellites**, the Doppler shift is usually manageable because FM receivers can tolerate a few kHz of offset. Many operators pre-program their radio with three frequency pairs — one for the approaching phase, one for the overhead phase, and one for the departing phase — and switch between them during the pass.

For **SSB/CW satellites (linear transponders)**, Doppler correction is more critical because even a small frequency error makes an SSB signal sound distorted. The standard approach is to keep the downlink frequency constant by tuning the radio and compensate on the uplink. Software like SatPC32, MacDoppler, or GPredict can automate this by sending frequency commands to your radio via CAT (Computer Aided Transceiver) control.

An important subtlety: on many linear transponder satellites, the transponder is **inverting** — an uplink frequency increase results in a downlink frequency decrease. This affects how you calculate Doppler corrections. Tracking software handles this automatically if configured correctly.

## Antenna tracking

### Manual (hand) tracking

For portable satellite operation, many operators hand-track satellites using a handheld directional antenna (such as an Arrow or Elk). This means physically pointing the antenna at the satellite and following it across the sky during the pass. A phone or tablet running a tracking app can help you visualize where to point.

Hand-tracking is surprisingly effective and is how most casual satellite operators work FM passes. With practice, you can smoothly follow a satellite from horizon to horizon.

### Automated rotator tracking

For a fixed satellite station, an **azimuth/elevation (az/el) rotator** can automatically track satellites. The rotator holds the antenna(s) and motors move it to follow the satellite's position as computed by tracking software. This is essential for longer, more demanding contacts (such as SSB/CW satellite work or EME) where precise, steady antenna pointing matters.

Rotator tracking requires a computer running tracking software that communicates with the rotator controller. GPredict, SatPC32, and other programs support the most common rotator interfaces, including the Yaesu GS-232 protocol and SPID rotator controllers.

For more details on rotator systems and antennas, see [Satellite Station Equipment](/satellites/satellite-equipment).

## Planning your satellite operating sessions

Effective satellite operation starts with planning. Before heading out to operate, check:

1. **Which satellites are active** — consult the AMSAT status page or SatNOGS dashboard to confirm the satellites you want to work are operational.
2. **Pass schedule** — run predictions for your location and note the best passes (high elevation, convenient time, minimal overlap with other operators' likely schedules).
3. **Frequencies** — confirm the current uplink and downlink frequencies and any required CTCSS tones. These occasionally change or may differ from older references.
4. **TLE freshness** — make sure your tracking data has been updated within the last day or two. Stale TLEs can cause your predictions to be off by several minutes or more.

## See also

- [Amateur Radio Satellites](/satellites/amateur-satellites) — Overview of satellite types and how to get started
- [Satellite Station Equipment](/satellites/satellite-equipment) — Antennas, radios, and rotators for satellite work
- [ISS Contacts](/satellites/iss-contacts) — Tracking and contacting the International Space Station
- [Satellites & Space Overview](/satellites/overview) — Category overview
