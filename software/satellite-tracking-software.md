---
title: Satellite Tracking Software
description: Software for predicting and tracking amateur radio satellite passes — pass prediction, Doppler correction, rotor control, and TLE management
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, satellites, tracking, tle, doppler, rotator
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Satellite Tracking Software

Amateur radio satellites orbit the Earth at altitudes ranging from a few hundred kilometres (low Earth orbit, or LEO) to over 35,000 km (geostationary). LEO satellites are only in range for a few minutes per pass, and their frequencies shift due to the Doppler effect as they move toward and away from your station. Satellite tracking software solves these challenges by predicting when satellites will be visible from your location, showing their path across the sky in real time, calculating Doppler-corrected frequencies, and — in many cases — automatically controlling your radio and antenna rotors.

## What Satellite Tracking Software Does

### Pass prediction

The core function of any satellite tracker is predicting when a satellite will rise above your horizon, how high it will get (maximum elevation), and when it will set. From your station's geographic coordinates and the satellite's orbital elements, the software calculates a table of upcoming passes with rise and set times, directions (azimuth), and maximum elevation. You can filter for passes above a minimum elevation — typically 10° or higher for reliable communication.

### Real-time tracking

During a pass, the software shows the satellite's current position on a map or polar plot, updating in real time. The polar plot (centred on your station with north at the top) is the most useful view during a pass because it directly corresponds to where you need to point your antenna.

### Doppler correction

A satellite in LEO is moving at roughly 7.5 km/s relative to the Earth's surface. This creates a significant Doppler shift — the received frequency is higher when the satellite approaches and lower when it recedes. For a 145 MHz uplink, the shift can be ±3.5 kHz; at 435 MHz, it can be ±10 kHz. The software calculates the instantaneous Doppler shift and can send corrected frequencies to your radio via CAT control, keeping you tuned to the satellite throughout the pass.

### Rotor control

If you have an azimuth-elevation (az-el) rotor system, the tracking software can drive the rotors to follow the satellite across the sky automatically. This frees you to focus on operating rather than manually aiming the antenna.

### Footprint and coverage maps

Some trackers show the satellite's footprint — the area on the ground from which the satellite is currently accessible. This tells you which other stations you could potentially work through the satellite at any given moment.

## Orbital Elements (TLEs)

Satellite tracking software relies on **Two-Line Element sets (TLEs)** to describe each satellite's orbit. A TLE is a standardised data format maintained by the US Space Force's 18th Space Defense Squadron (via Space-Track.org) and distributed through amateur radio organisations like AMSAT.

A TLE looks like this:

```
ISS (ZARYA)
1 25544U 98067A   26091.50000000  .00016717  00000-0  10270-3 0  9025
2 25544  51.6416 247.4627 0006703 130.5360 325.0288 15.72125391484597
```

The two lines encode the satellite's orbital parameters — inclination, eccentricity, argument of perigee, mean motion, and epoch — from which the software computes the satellite's position at any future time using the SGP4 propagation model.

**TLEs decay in accuracy over time** because satellites experience atmospheric drag, solar radiation pressure, and occasional manoeuvres. You should update your TLE data at least weekly for LEO satellites. Most tracking software can download updated TLEs automatically from the internet.

> **Tip:** AMSAT maintains curated TLE files specifically for amateur radio satellites at amsat.org. These are generally more reliable for ham satellites than the full Space-Track catalogue, which contains thousands of objects.
{.is-info}

## Popular Satellite Tracking Software

### Desktop applications

| Program | Platforms | Licence | Notable features |
|---------|-----------|---------|-----------------|
| GPredict | Windows, macOS, Linux | Free (open source) | Full-featured tracker with pass prediction, real-time tracking, Doppler control, rotor control, and multi-satellite support |
| SatPC32 | Windows | Free (from AMSAT-DL) | Popular among amateur satellite operators; CAT and rotor control; transponder tuning with automatic Doppler correction |
| Orbitron | Windows | Free | Lightweight tracker with visual pass prediction and real-time satellite position display; large satellite database |
| MacDoppler | macOS | Commercial | Native Mac tracker with radio and rotor control; polished interface |
| PstRotator | Windows | Commercial | Advanced rotor and radio control; supports many rotor interfaces; includes satellite tracking among other features |

### Web-based trackers

Web-based tools are useful for quick pass checks when you do not have your tracking software at hand, or when you are planning operations from a different location.

| Tool | Notable features |
|------|-----------------|
| N2YO | Real-time satellite tracking on a world map; pass predictions for any location; 3D visualisation |
| AMSAT Pass Predictions | AMSAT's online pass predictor for amateur satellites |
| Heavens-Above | Pass predictions for ISS, amateur satellites, and other visible spacecraft; useful for visual observation planning as well |
| SatNOGS | Open-source satellite ground station network with live observation data and pass predictions |

### Mobile apps

Several mobile applications provide satellite pass predictions and real-time tracking on your phone or tablet. These are particularly handy for portable and field operations. Search for "amateur satellite tracker" or "ISS tracker" in your device's app store for current options. Look for apps that support amateur radio transponder frequencies and Doppler correction, not just visual tracking.

## Setting Up for Satellite Tracking

### Enter your station location

The first step in any tracking program is entering your station's geographic coordinates (latitude, longitude, and altitude). Be as accurate as possible — errors of more than a few hundred metres can cause noticeable pointing errors for high-elevation passes. Use a GPS receiver, a mapping application, or a grid square converter to find your coordinates.

### Load and update TLEs

Download the latest TLE files for amateur radio satellites. Most programs can fetch TLEs automatically from AMSAT, CelesTrak, or Space-Track. Set up automatic updates if the software supports it, or make a habit of updating manually before each operating session.

### Configure radio control

If your tracking software supports CAT control, configure it with your radio's model, COM port (or network address), and baud rate. Set the software to send Doppler-corrected frequencies to the radio. For satellites with linear transponders, the software should correct both the uplink and downlink frequencies simultaneously.

### Configure rotor control

If you have an az-el rotor, connect it to the computer via a rotor interface (many rotor controllers support serial or USB connections). Configure the tracking software with your rotor type and interface. Test the rotor movement manually before enabling automatic tracking — verify that the software's azimuth and elevation readings match the rotor's actual position.

### Plan your passes

Use the pass prediction function to generate a schedule of upcoming passes for the satellites you are interested in. Focus on passes with maximum elevation above 20° or 30° for the best signal strength and longest communication windows. Passes directly overhead (near 90° elevation) give the strongest signals but move across the sky very quickly, making them more challenging to track.

## Doppler Correction in Practice

For FM satellites (like those carrying FM repeater transponders), Doppler correction is relatively simple — the signal is either on frequency or it is not. Most operators manually adjust frequency during the pass in 5 kHz steps, or let the tracking software handle it automatically.

For satellites with **linear transponders** (SSB/CW), Doppler correction is more critical because even small frequency errors are audible. The tracking software must correct both the uplink and downlink frequencies. A common convention is to tune the downlink to a fixed frequency and let the software adjust only the uplink — this way, the station you hear on the downlink stays at a constant frequency while the software tracks the uplink for you. The opposite approach (fixed uplink, corrected downlink) is also used. Check your tracking software's documentation for how it handles dual-frequency correction.

## Working with the ISS

The International Space Station carries amateur radio equipment and is one of the easiest satellites to work. It transmits on 145.800 MHz (worldwide downlink for voice and APRS) and uses various uplink frequencies depending on the current configuration. The ISS is a large, bright object in a well-known orbit, so pass predictions are very accurate.

Because the ISS is in a relatively low orbit (approximately 400 km altitude), passes are short — typically 5 to 10 minutes — and Doppler shift is significant. Tracking software makes ISS contacts much more manageable by handling the frequency correction and showing you exactly where to point your antenna.

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [Amateur Satellites Overview](/satellites/overview) — Introduction to working amateur satellites
- [Getting Started with Satellites](/satellites/getting-started) — Your first satellite contact
- [Satellite Equipment](/satellites/equipment) — Radios and antennas for satellite work
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — Operating on the bands used by most satellites
- [Online Tools & Resources](/software/online-tools) — Web-based utilities and databases
