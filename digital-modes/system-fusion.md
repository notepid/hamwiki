---
title: System Fusion (C4FM)
description: Yaesu System Fusion — a digital voice mode with automatic mode selection for seamless analogue/digital coexistence
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, fusion, c4fm, digital-voice, yaesu
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# System Fusion (C4FM)

**System Fusion** is Yaesu's digital voice and data system for amateur radio, introduced in 2014. It uses **C4FM** (Continuous 4-level Frequency Modulation) as its modulation scheme. System Fusion's most notable feature is **AMS (Automatic Mode Selection)** — a Fusion repeater can automatically detect whether an incoming signal is analogue FM or digital C4FM and handle both, eliminating the "analogue vs digital" divide that can split a repeater's user base.

## How System Fusion Works

System Fusion uses C4FM modulation within a standard 12.5 kHz channel. The system supports several voice and data modes:

**DN (Digital Narrow)** — Digital voice using the AMBE+2 vocoder at half rate, plus a simultaneous data channel. Voice quality is slightly lower than VW mode, but the accompanying data channel can carry GPS position, text messages, and other information alongside the voice stream. This is the most commonly used mode.

**VW (Voice Wide)** — All bandwidth is allocated to digital voice using AMBE+2 at full rate. Higher voice quality than DN, but no simultaneous data. Used when voice quality is the priority.

**Data FR (Full Rate)** — All bandwidth allocated to data transmission. Used for high-speed data transfer rather than voice.

### Automatic Mode Selection (AMS)

AMS is System Fusion's signature feature. When a Fusion repeater has AMS enabled, it listens for incoming signals and automatically detects whether the signal is analogue FM or digital C4FM. It then repeats the signal in the format it was received — an analogue FM signal goes out as analogue FM, and a C4FM signal goes out as C4FM. On the receiving end, Fusion radios with AMS enabled automatically switch between analogue and digital decoding.

This means a club can upgrade its repeater to System Fusion without forcing all users to immediately buy new radios. Members with legacy analogue FM radios continue to use the repeater as before, while members with Fusion radios get the benefits of digital voice. Over time, as more users upgrade, the repeater transitions organically to digital.

### WIRES-X

**WIRES-X** (Wide-coverage Internet Repeater Enhancement System) is Yaesu's internet linking system for System Fusion. It connects Fusion repeaters and nodes through the internet, allowing users to communicate with others worldwide. WIRES-X organises communication through:

**Rooms** — Persistent conference areas where multiple nodes and repeaters can connect. Similar to DMR talkgroups or D-STAR reflectors. Rooms are identified by a 5-digit number.

**Nodes** — Individual repeaters or personal nodes that can connect to rooms or link directly to other nodes.

Users can access WIRES-X rooms through their radio's interface (Fusion radios have a dedicated WIRES-X button) to browse available rooms, connect, disconnect, and see which nodes are currently linked. This is one of the more user-friendly implementations of internet linking in amateur digital voice.

## Getting Started with System Fusion

### What you need

- **A System Fusion / C4FM compatible radio** — Yaesu is the sole manufacturer. Popular models include the FT-70DR and FT-5DR (handheld), FTM-300DR and FTM-500DR (mobile), and FT-991A (HF/VHF/UHF base). All current Yaesu VHF/UHF radios include C4FM capability.
- **No registration required** — Unlike [DMR](/digital-modes/dmr) (which requires a DMR ID) or [D-STAR](/digital-modes/dstar) (which requires gateway registration), System Fusion works out of the box. Program in a repeater frequency, set the mode to digital or AMS, and start talking.
- **Programming** — Fusion radios are programmed similarly to analogue FM radios. Enter the repeater frequency and offset, set the mode (FM, DN, VW, or AMS), and optionally set a DG-ID (see below). Programming software is available from Yaesu.

### DG-ID (Digital Group ID)

**DG-ID** is System Fusion's access control mechanism, replacing the older DSQ (Digital Squelch Code) system. A DG-ID is a number from 00 to 99 that functions similarly to a CTCSS tone — your radio must be set to the same DG-ID as the repeater to access it. DG-ID 00 is "all call" and will accept any DG-ID.

Some repeaters use different DG-IDs to separate different WIRES-X rooms or user groups on the same frequency.

### Hotspots

System Fusion is supported by the same hotspot platforms as DMR and D-STAR. A **Pi-Star** or **WPSD** hotspot with an MMDVM board can function as a personal Fusion node, connecting to WIRES-X rooms or YSF reflectors over the internet.

**YSF reflectors** are community-run reflectors (similar to D-STAR's DCS/XLX reflectors) that provide additional rooms and connectivity beyond the official WIRES-X network. Many operators use YSF reflectors through their hotspot for access to cross-mode bridges and international groups.

## System Fusion Features

**Snapshot and picture transmission** — Fusion supports transmitting small images (camera snapshots) between radios that support the feature, such as the FT-5DR.

**GPS and APRS** — Fusion radios with GPS can transmit position data, which can be gated to the [APRS](/digital-modes/aprs) network through WIRES-X nodes or repeaters.

**Group Monitor (GM)** — A feature that displays nearby Fusion users, showing callsigns, distance, and direction. Useful at events and gatherings.

**Backwards compatibility** — Any Fusion radio works on analogue FM. If you buy a Yaesu Fusion radio, you get a fully capable analogue FM radio with digital capability included.

## System Fusion vs Other Modes

System Fusion's greatest strength is its simplicity and analogue compatibility. Unlike DMR, there is no complex codeplug to program, no ID to register for, and no talkgroup system to learn — you program a frequency, set the mode, and go. The AMS feature makes it the friendliest digital voice mode for clubs transitioning from analogue.

Its main limitations are that it is a single-vendor system (only Yaesu makes Fusion radios), it uses the same proprietary AMBE+2 voice codec as DMR, and its WIRES-X network is somewhat smaller than DMR's Brandmeister or D-STAR's reflector network.

## Where to Go Next

- [DMR](/digital-modes/dmr) — The most widely used digital voice mode
- [D-STAR](/digital-modes/dstar) — Icom's digital voice system
- [M17](/digital-modes/m17) — Open-source digital voice
- [APRS](/digital-modes/aprs) — Position reporting (Fusion positions can be gated to APRS)
- [Repeaters](/operating/repeaters) — How repeaters work
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
