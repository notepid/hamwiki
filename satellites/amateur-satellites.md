---
title: Amateur Radio Satellites
description: Active amateur radio satellites, OSCAR designations, satellite types, and how to make your first satellite contact
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, AMSAT, OSCAR, FM, linear transponder
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Amateur Radio Satellites

Amateur radio operators have been building and launching satellites since 1961, when OSCAR 1 (Orbiting Satellites Carrying Amateur Radio) became the first non-governmental satellite in orbit. Since then, well over 100 amateur satellites have been launched, and at any given time there are typically dozens in orbit providing a variety of communication capabilities.

## What is AMSAT?

AMSAT (the Radio Amateur Satellite Corporation) is the primary international organization that coordinates the design, construction, and launch of amateur radio satellites. Originally founded in the United States in 1969, AMSAT now has affiliated organizations in many countries, including AMSAT-UK, AMSAT-DL (Germany), AMSAT-NA (North America), and AMSAT-India. These groups collaborate to fund, build, and operate satellites for amateur radio use.

The OSCAR designation (Orbiting Satellites Carrying Amateur Radio) is assigned sequentially to amateur satellites. Each satellite receives a number upon reaching orbit — for example, AO-7 (AMSAT-OSCAR 7, launched in 1974) is one of the oldest still partially functioning.

## Types of amateur satellites

### FM voice satellites (easiest to work)

FM satellites carry a simple repeater: they receive signals on one frequency (the uplink) and retransmit them on another (the downlink). Because they use FM — the same modulation that handheld radios use — they are the most accessible satellites for beginners.

The key limitation of FM satellites is that only one conversation can take place at a time, since FM captures the strongest signal. This means passes can be crowded, and operators need to keep transmissions short to share access. Good operating practice is essential.

Notable FM satellites have included SO-50 (SaudiSat-1C OSCAR 50), AO-91, AO-92, and various TEVEL and CAS series spacecraft. The specific satellites available change over time as new ones are launched and older ones fail.

### Linear transponder satellites (SSB/CW)

Linear transponder satellites are more sophisticated. Instead of repeating a single signal, they retransmit an entire passband — typically 20–100 kHz wide. This allows multiple simultaneous contacts on different frequencies within the passband. Operators use SSB (single sideband) or CW (Morse code) on these satellites.

Working a linear transponder requires more skill than FM. You need to account for Doppler shift, manage your transmit power carefully to avoid capturing the transponder's AGC (automatic gain control), and tune continuously as the satellite moves.

Examples include FO-29 (Fuji-OSCAR 29), CAS-4A, CAS-4B, RS-44 (Radio Sport 44), and the QO-100 geostationary satellite.

### Digital and store-and-forward satellites

Some amateur satellites carry digital payloads. These may include BBS (bulletin board system) mailboxes where messages can be uploaded on one pass and downloaded on a subsequent pass (store-and-forward), APRS digipeaters, or experimental digital transponders. The ISS also carries a packet radio digipeater that falls into this category.

### CubeSats and university projects

The CubeSat revolution has dramatically increased the number of amateur satellites in orbit. Many universities and technical schools build small satellites (often 1U, roughly 10 cm × 10 cm × 10 cm) that carry amateur radio payloads as part of educational programmes. These satellites typically have shorter operational lifetimes than purpose-built AMSAT spacecraft, but they contribute to a dynamic and constantly changing satellite landscape.

### QO-100 — the geostationary amateur satellite

Es'hail-2 (designated QO-100, or Qatar-OSCAR 100) is unique among amateur satellites because it sits in geostationary orbit at 25.5°E. Unlike other amateur satellites that orbit every 90–120 minutes and are only visible for a few minutes at a time, QO-100 is always in the same position relative to the ground. It is visible from a wide area covering Europe, Africa, the Middle East, India, and parts of South America and Southeast Asia.

QO-100 has two transponders: a narrowband transponder for SSB and CW on 10 GHz, and a wideband transponder for digital amateur television (DATV) on 10 GHz. Because the satellite does not move relative to your station, there is no Doppler shift and no need for tracking — you simply point a dish at the correct position in the sky.

Working through QO-100 requires 2.4 GHz uplink equipment and a 10 GHz downlink receiver, typically using modified satellite TV LNBs (low-noise block downconverters). The narrowband transponder can be received with a dish as small as 60 cm (24 inches) in many areas.

## Satellite orbits

Most amateur satellites are in **low Earth orbit (LEO)**, typically between 300 and 1,200 km (185–745 miles) altitude. At these altitudes, orbital periods are roughly 90–110 minutes, and a given satellite is visible from your location for only about 5–15 minutes per pass. The geometry of the pass — how high the satellite climbs above your horizon — determines the duration and signal quality.

Satellites in LEO are generally in one of several orbit types:

- **Near-circular orbits** at 400–600 km are common for CubeSats and the ISS. These provide relatively short but consistent passes.
- **Sun-synchronous orbits** at 600–800 km are popular for small satellites. These pass over any given point at roughly the same local time each day.
- **Higher elliptical orbits** like the Molniya-type orbit were used by some older AMSAT satellites (such as AO-40) to provide longer visibility windows. Currently no active amateur satellites use highly elliptical orbits, though future missions may return to this approach.
- **Geostationary orbit** at approximately 35,786 km (22,236 miles) — used only by QO-100.

## Making your first satellite contact

The easiest way to get started with amateur satellites is to work an FM satellite with a handheld radio:

### What you need

- A dual-band (VHF/UHF) handheld transceiver capable of full-duplex operation, or two separate handhelds (one for transmit, one for receive). Full-duplex means you can transmit and receive simultaneously, which lets you hear your own signal coming back through the satellite and confirm you are being received.
- A small directional antenna. Popular choices include the Arrow antenna (a handheld dual-band Yagi) and the Elk antenna (a handheld log-periodic). You can also start with a simple whip antenna, though a directional antenna makes a significant difference.
- Satellite pass prediction software or an app on your phone. See [Satellite Tracking](/satellites/satellite-tracking) for details.

### Steps for your first contact

1. **Identify an active FM satellite.** Check the AMSAT status page or satellite apps to find which FM satellites are currently operational. The available satellites change as new ones are launched and older ones cease functioning.

2. **Predict a pass.** Use tracking software to find when the satellite will be visible from your location. Look for passes with a maximum elevation of at least 20–30 degrees above the horizon for the best chance of success. Higher passes provide stronger signals and longer windows.

3. **Program your radio.** Enter the uplink and downlink frequencies for the satellite, including any required CTCSS (PL) tone on the uplink. Account for Doppler shift — the satellite's downlink frequency will be slightly higher than nominal as it approaches and slightly lower as it moves away. Many operators pre-program several frequency steps to manually correct for Doppler during the pass.

4. **Track the satellite.** When the pass begins, point your antenna toward the satellite's predicted position. Move the antenna to follow the satellite across the sky as the pass progresses. With practice, hand-tracking becomes second nature.

5. **Listen first.** Before transmitting, listen to learn the rhythm of the pass. You will hear other operators making contacts. Satellite operating style is fast and efficient because pass times are short — exchange callsigns, grid squares, and signal reports, then move on.

6. **Make a contact.** When you hear a gap, call CQ or respond to another station. Keep transmissions short. Use only enough power to be heard — excessive power on FM satellites can capture the repeater and block other users.

## Satellite operating etiquette

Because pass times are limited and many operators share the same satellite, good operating practice is critical:

- Use minimum power necessary. On FM satellites, too much power is as bad as too little — it can "capture" the transponder and block everyone else.
- Keep contacts short. Exchange callsigns, grid squares, and signal reports. Save longer conversations for terrestrial repeaters.
- On linear transponder satellites, stay within the transponder passband and do not overdrive the transponder. Monitor your own downlink to ensure your signal is clean.
- Share the resource. If you have made several contacts on a pass, step back and let others have a turn.

## Where to find current satellite information

The amateur satellite landscape changes frequently. Satellites are launched, activated, decommissioned, and sometimes revived. The best way to stay current is:

- **AMSAT website** (amsat.org) — news, status pages, and frequency charts
- **SatNOGS** (satnogs.org) — a crowdsourced network of satellite ground stations that tracks telemetry and status for hundreds of satellites
- **AMSAT satellite status page** — regularly updated list showing which satellites are active, semi-operational, or offline
- **Satellite tracking apps** — many include built-in satellite databases that are updated regularly (see [Satellite Tracking](/satellites/satellite-tracking))

## See also

- [Satellite Tracking](/satellites/satellite-tracking) — Software and tools for predicting passes
- [Satellite Station Equipment](/satellites/satellite-equipment) — Gear for satellite operation
- [ISS Contacts](/satellites/iss-contacts) — Working the amateur radio station on the International Space Station
- [Satellites & Space Overview](/satellites/overview) — Category overview
