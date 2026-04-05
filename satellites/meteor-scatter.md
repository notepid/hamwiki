---
title: Meteor Scatter
description: Using ionized meteor trails to reflect VHF signals for contacts beyond line-of-sight range
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, meteor-scatter, VHF, MSK144, WSJT-X, meteor showers
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Meteor Scatter

Meteor scatter communication uses the brief ionised trails left by meteors entering the Earth's atmosphere to reflect VHF radio signals far beyond their normal line-of-sight range. Every day, billions of tiny particles — most no larger than a grain of sand — enter the atmosphere at speeds of 11–72 km/s, creating columns of ionised gas at altitudes of roughly 80–120 km (50–75 miles). These ionised trails can reflect radio signals for anywhere from a fraction of a second to several seconds, providing fleeting but usable communication paths over distances of 500–2,300 km (300–1,400 miles).

Meteor scatter is most commonly used on the 6-metre (50 MHz) and 2-metre (144 MHz) bands, where it can extend the range of VHF communication far beyond the normal horizon.

## How meteor scatter works

### The physics of meteor trails

When a meteoroid (a small particle of space debris, typically from a comet) hits the Earth's atmosphere, it travels so fast that it heats and ionises the atmospheric gases in its path, creating a narrow column of free electrons. This ionised column — the meteor trail — acts as a reflector for radio waves in the VHF range.

The trail's usefulness for radio reflection depends on several factors:

- **Electron density:** Denser trails (produced by larger or faster particles) reflect stronger signals and last longer. Trails are classified as "underdense" (lower electron density, short-lived, typically under 1 second) or "overdense" (higher electron density, lasting several seconds or occasionally tens of seconds).
- **Trail orientation:** A meteor trail reflects signals most effectively when it is oriented roughly perpendicular to the path between the two communicating stations. This geometric requirement means that not every meteor produces a usable reflection for a given pair of stations.
- **Altitude:** Trails form between about 80 and 120 km altitude. This altitude determines the maximum distance over which the reflection can occur — geometry limits the path to roughly 2,300 km (1,400 miles) at most.
- **Decay time:** Trails dissipate as the ionised gas diffuses and recombines. Underdense trails typically last less than a second; overdense trails can persist for several seconds. At 144 MHz, trail duration tends to be shorter than at 50 MHz because higher frequencies require denser ionisation for effective reflection.

### Sporadic meteors vs. meteor showers

Meteors arrive in two categories. **Sporadic meteors** — random particles that arrive from all directions — produce a baseline rate of about 5–10 visible meteors per hour (the radio rate is higher, since radio can detect meteors too small to be visible). Sporadic activity is always present and makes meteor scatter possible at any time of year.

**Meteor showers** occur when the Earth passes through debris streams left by comets. During a strong shower, the meteor rate increases dramatically — the Perseids (August) and Geminids (December) can produce over 100 visible meteors per hour, with correspondingly higher radio reflection rates. Showers dramatically increase the number of usable openings and are the peak periods for meteor scatter activity.

Major annual meteor showers for radio operators include:

- **Quadrantids** (early January) — short but intense peak
- **Lyrids** (April) — moderate activity
- **Eta Aquariids** (May) — good southern hemisphere shower
- **Perseids** (August) — one of the strongest and most reliable showers, excellent for meteor scatter
- **Orionids** (October) — moderate activity
- **Leonids** (November) — variable, occasionally spectacular
- **Geminids** (December) — consistently strong, one of the best showers of the year

### Time of day effects

Meteor scatter activity varies with time of day. The early morning hours (roughly 04:00–10:00 local time) tend to produce the highest meteor rates because the observer's location on Earth is facing into the direction of orbital motion, sweeping up more particles. The afternoon and evening hours generally have lower rates. This diurnal pattern affects both sporadic and shower meteors.

## Operating modes for meteor scatter

### MSK144 — the modern standard

MSK144 is a digital mode designed specifically for meteor scatter, developed by Joe Taylor, K1JT, as part of the WSJT-X software suite. It uses rapid 72-millisecond transmission frames and forward error correction to extract information from extremely brief signal reflections — even sub-second underdense trails can carry a complete message frame.

MSK144 has become the dominant mode for meteor scatter communication. Its speed and sensitivity make it far more efficient than older analogue approaches. A complete contact (exchange of callsigns, grid squares, signal reports, and confirmations) can be completed in as little as a few minutes during good conditions.

MSK144 contacts follow a structured protocol with alternating 15-second transmission periods, synchronised to the clock. One station transmits for the first 15 seconds of each 30-second cycle; the other transmits for the second 15 seconds. The software automatically detects and decodes any frames received during the listening period.

### FSK441 — the predecessor

FSK441 was the earlier WSJT-mode for meteor scatter (4-tone FSK at 441 baud). It has been largely superseded by MSK144, which offers better performance, but some operators still use it. FSK441 contacts follow a similar alternating-period structure but require longer signal bursts for successful decoding.

### SSB (voice) meteor scatter

Before digital modes, SSB was the primary mode for meteor scatter. Operators would transmit short, rapid voice bursts and listen for replies reflected from meteor trails. SSB meteor scatter requires stronger signals (larger meteor trails) than digital modes, but it remains a popular and exciting operating style, particularly during major showers when overdense trails are frequent.

SSB meteor scatter contacts use rapid exchanges — operators repeat their callsign, grid square, and signal report in rapid cycles, listening between transmissions for the other station's signal bursting through via a meteor reflection. A complete SSB meteor scatter contact can take anywhere from a few minutes to over an hour, depending on conditions.

### CW (Morse code) meteor scatter

CW was historically used for meteor scatter and offered better weak-signal performance than SSB due to its narrow bandwidth. High-speed CW (HSCW) was also employed, with operators sending at speeds too fast to copy by ear and recording the signals for later playback at reduced speed. CW meteor scatter is now uncommon, having been superseded by digital modes.

## Equipment for meteor scatter

Meteor scatter does not require exotic equipment. A typical meteor scatter station consists of:

- **Transceiver:** An all-mode VHF radio covering the 6 m (50 MHz) or 2 m (144 MHz) band. SSB and digital mode capability is essential. Most operators use 50–100 watts on 6 m and 100–400 watts on 2 m, though contacts have been made with less power.
- **Antenna:** A horizontally polarised Yagi antenna is standard. On 2 m, a 6–10 element Yagi at 10–15 m (30–50 ft) height is typical. On 6 m, a 3–6 element Yagi works well. The antenna should be pointed toward the target area (or halfway between your location and the other station's location, which is where meteor reflections are most likely to occur at the optimal geometry).
- **Computer and software:** WSJT-X running MSK144. The computer must have accurate time synchronisation (within a second or better, typically maintained via internet NTP) because MSK144 transmission and reception periods are tightly synchronised.
- **Feedline:** Low-loss coaxial cable, especially at 144 MHz where cable losses are significant. LMR-400 or equivalent is recommended for longer runs.

### Antenna pointing for meteor scatter

Unlike satellite or EME operation, where you point the antenna at a specific target, meteor scatter antenna pointing is aimed at the **reflection point** — the area of sky where meteors at the right altitude and orientation will produce reflections along the path between you and the other station. For most contacts, this means pointing the antenna roughly toward the distant station's direction, at an elevation of 5–15° above the horizon. Many operators simply point their beam at the compass heading of the target station and leave it fixed for the duration of the contact attempt.

## Making meteor scatter contacts

### Scheduling and random operation

Meteor scatter contacts can be made in two ways. **Scheduled contacts** are pre-arranged between two stations who agree on a time, frequency, and mode (usually via online loggers, chat rooms, or email). Scheduling ensures both stations are listening at the same time, which is important because meteor scatter conditions are unpredictable.

**Random (CQ) operation** means calling CQ on a standard meteor scatter calling frequency and waiting for replies. Random operation is more productive during major meteor showers when many stations are active. On 144 MHz, activity typically concentrates near 144.200 MHz (the SSB calling frequency) for voice work, while MSK144 activity uses frequencies designated by convention (often 144.150 MHz in many regions, though local conventions vary).

### A typical MSK144 contact

1. Both stations synchronise their clocks to within a second of UTC.
2. Station A transmits during the first 15 seconds of the cycle; Station B transmits during the second 15 seconds (by prior agreement or convention).
3. Each station transmits its callsign and grid square repeatedly.
4. When a meteor trail provides a usable reflection, the receiving station's software decodes one or more message frames. These brief signal bursts may last only a fraction of a second — far too short for human perception, but enough for MSK144 to decode.
5. As the contact progresses, stations exchange signal reports and acknowledgements following the standard WSJT-X protocol.
6. The contact is complete when both stations have received the required information (both callsigns, both grid squares, signal reports, and a final "73" or "RR73" confirmation).

A contact can complete in a few minutes during active conditions or may take 30 minutes or longer during quiet periods with only sporadic meteors.

## Meteor scatter and VHF contesting

Meteor scatter is an important mode during VHF contests, where operators try to make as many contacts as possible on VHF and higher bands. During [contests](/contesting/overview), meteor scatter allows contacts over much longer distances than are possible via direct tropospheric propagation, adding valuable grid squares and multipliers to contest scores. Major meteor showers that coincide with popular VHF contests are especially productive.

## Meteor scatter vs. other propagation modes

Meteor scatter sits in a middle ground between several other VHF propagation modes:

- **Tropospheric propagation** (tropo) provides stronger signals but is limited in distance and dependent on weather. See [Propagation Overview](/propagation/overview).
- **Sporadic E** can support contacts over similar or greater distances on 6 m but is unpredictable and seasonal.
- **EME (moonbounce)** allows worldwide VHF contacts but requires much more capable stations. See [EME / Moonbounce](/satellites/eme-moonbounce).
- Meteor scatter is the most **predictable and repeatable** way to make VHF contacts in the 500–2,300 km range, because the meteor flux is constant and increases reliably during known shower periods.

## See also

- [EME / Moonbounce](/satellites/eme-moonbounce) — Another weak-signal VHF technique
- [Propagation Overview](/propagation/overview) — How radio signals travel
- [Satellites & Space Overview](/satellites/overview) — Category overview
- [Contesting Overview](/contesting/overview) — VHF contests where meteor scatter is used
