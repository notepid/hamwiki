---
title: Digital Modes
description: An introduction to digital communication modes in amateur radio — from weak-signal to digital voice and data networking
published: true
date: 2026-04-05T17:40:51.151Z
tags: 
editor: markdown
dateCreated: 2026-04-05T17:40:51.151Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Digital Modes Overview

Digital modes use a computer or dedicated hardware to encode and decode information sent over radio. Rather than speaking into a microphone or tapping a key, you type a message, select a contact, or let software handle the exchange automatically — and the radio transmits a carefully structured audio or digital signal that the receiving station's computer decodes. Digital modes have transformed amateur radio, opening up possibilities that would be impractical or impossible with voice or CW alone: making contacts with stations too weak to hear by ear, sending email over HF radio without the internet, tracking positions worldwide, and carrying crystal-clear digital voice across repeater networks.

## Why Digital?

Digital modes offer several compelling advantages over traditional analogue communication:

**Weak-signal performance** — Modes like [FT8](/digital-modes/ft8) and [FT4](/digital-modes/ft4) can decode signals far below the noise floor, well beyond what a human ear could ever pick out. FT8 routinely decodes signals at −24 dB below the noise — that is more than 200 times weaker than what you could hear. This makes contacts possible with very low power, compromise antennas, or difficult propagation.

**Error correction** — Many digital modes include forward error correction (FEC) that allows the receiving station to reconstruct a message even if parts of it were corrupted by noise or interference. This is especially valuable for passing messages, email, and data where accuracy matters.

**Automation** — Some digital protocols handle the entire contact sequence automatically, including calling CQ, responding, exchanging signal reports, and logging. This makes it possible to make dozens of contacts per hour, or to leave a station running unattended for message relay.

**Efficient use of spectrum** — Digital signals can be extremely narrow. [PSK31](/digital-modes/psk31) occupies only about 31 Hz of bandwidth — you could fit roughly 80 PSK31 signals in the space of a single SSB voice signal. Weak-signal modes like FT8 use about 50 Hz per signal.

**Data networking** — Digital modes enable capabilities that go well beyond voice conversation: email via [Winlink](/digital-modes/winlink), position tracking and messaging via [APRS](/digital-modes/aprs), and general-purpose data transfer via [Packet Radio](/digital-modes/packet-radio) and [VARA](/digital-modes/vara).

## Categories of Digital Modes

Digital modes in amateur radio fall into several broad families, each with different characteristics and use cases.

### Weak-Signal Modes

These modes are designed to pull signals out of the noise, enabling contacts that would be impossible by voice or CW. They typically use structured, time-synchronised exchanges with heavy error correction.

- **[FT8](/digital-modes/ft8)** — The most popular digital mode in amateur radio. Uses 15-second transmit/receive cycles and can decode signals at −24 dB SNR. Ideal for DX, QRP, and poor conditions.
- **[FT4](/digital-modes/ft4)** — A faster variant of FT8 with 7.5-second cycles, designed for contesting and rapid exchanges. Slightly less sensitive than FT8.
- **[JS8Call](/digital-modes/js8call)** — Built on the FT8 protocol but designed for keyboard-to-keyboard conversation and store-and-forward messaging rather than minimal exchanges.

### Keyboard-to-Keyboard Modes

Older digital modes that allow freeform typed conversation between operators, much like a text chat. These were the original "digital modes" of amateur radio.

- **[PSK31](/digital-modes/psk31)** — Phase Shift Keying at 31 baud. Extremely narrow bandwidth, good for ragchewing on HF. One of the first sound-card digital modes to become popular.
- **[RTTY](/digital-modes/rtty)** — Radioteletype, one of the oldest digital modes (dating to the 1930s). Uses frequency shift keying (FSK) and remains popular in contesting.

### Digital Voice

These modes digitise voice and transmit it as a digital data stream, typically over VHF/UHF. They offer features impossible with analogue FM: simultaneous voice and data, text messaging, GPS position reporting, and internet-linked networks.

- **[DMR](/digital-modes/dmr)** — Digital Mobile Radio. An open standard using TDMA (two time slots per channel). The most widely adopted digital voice mode worldwide, with extensive repeater networks and talkgroup-based routing.
- **[D-STAR](/digital-modes/dstar)** — The first digital voice system designed for amateur radio, developed by JARL (Japan). Features internet gateway linking and data capabilities.
- **[System Fusion / C4FM](/digital-modes/system-fusion)** — Yaesu's digital voice system. Notable for automatic mode selection (AMS) that allows a repeater to handle both analogue FM and digital signals.
- **[M17](/digital-modes/m17)** — An open-source, patent-free digital voice protocol developed by the amateur radio community. Uses the modern Codec2 voice codec instead of proprietary AMBE.

### Data and Networking Modes

These modes focus on moving data — messages, email, position reports, files — rather than real-time voice or brief exchanges.

- **[APRS](/digital-modes/aprs)** — Automatic Packet Reporting System. A real-time tactical communication system for position reporting, weather data, short messages, and telemetry. Operates primarily on 144.390 MHz (North America) and 144.800 MHz (Europe).
- **[Winlink](/digital-modes/winlink)** — A worldwide radio email system. Allows sending and receiving email over HF and VHF radio without the internet. Critical for emergency communications.
- **[Packet Radio](/digital-modes/packet-radio)** — The original digital data networking mode for amateur radio, using AX.25 protocol. Supports bulletin boards, messaging, and data transfer.
- **[VARA](/digital-modes/vara)** — A modern high-speed HF modem used primarily as a transport layer for Winlink and other applications. Offers significantly higher throughput than older protocols.

## What You Need to Get Started

A basic digital mode station requires just a few components beyond a standard radio setup. See [Digital Station Setup](/digital-modes/digital-station-setup) for a full guide.

**For HF digital modes** (FT8, FT4, PSK31, RTTY, Winlink HF):

- An HF transceiver with SSB capability
- A computer (Windows, macOS, or Linux)
- A [sound card interface](/digital-modes/sound-card-interface) connecting the radio to the computer — or a radio with a built-in USB audio codec (most modern HF radios include this)
- Software appropriate for the mode you want to use (e.g., WSJT-X for FT8/FT4, [Fldigi](/digital-modes/fldigi) for PSK31/RTTY)
- A reasonably accurate clock (within ±1 second for FT8/FT4 — most operators synchronise via internet NTP)

**For VHF/UHF digital voice** (DMR, D-STAR, System Fusion):

- A digital-capable transceiver (handheld or mobile) for the relevant mode
- Programming software and cable to configure frequencies, talkgroups, or reflectors
- Access to a local repeater, or a hotspot device for internet-linked access from home

**For APRS:**

- A VHF transceiver (2 metres)
- An APRS-capable radio (with built-in TNC), or a separate TNC/sound card interface, or a smartphone app paired with a radio
- An antenna suited for VHF

## Choosing a Mode

Which digital mode is right for you depends on what you want to do:

| Goal | Recommended modes |
|------|-------------------|
| Make contacts with minimal equipment or power | [FT8](/digital-modes/ft8), [FT4](/digital-modes/ft4) |
| Have typed conversations (ragchewing) | [PSK31](/digital-modes/psk31), [JS8Call](/digital-modes/js8call) |
| Contest operating | [RTTY](/digital-modes/rtty), [FT4](/digital-modes/ft4), [FT8](/digital-modes/ft8) |
| Crystal-clear local voice on VHF/UHF | [DMR](/digital-modes/dmr), [System Fusion](/digital-modes/system-fusion), [D-STAR](/digital-modes/dstar) |
| Send and receive email off-grid | [Winlink](/digital-modes/winlink) with [VARA](/digital-modes/vara) |
| Position reporting, messaging, weather | [APRS](/digital-modes/aprs) |
| Community-driven, open-source voice | [M17](/digital-modes/m17) |
| DX chasing and award hunting | [FT8](/digital-modes/ft8), [RTTY](/digital-modes/rtty) |

## A Brief History

Digital modes in amateur radio evolved in distinct waves. Radioteletype (RTTY) arrived in the 1930s–1940s, initially using surplus military teleprinter machines. Packet radio emerged in the 1980s, bringing computer networking concepts to amateur radio and laying the groundwork for APRS. The sound card revolution of the late 1990s and early 2000s brought modes like PSK31 that required nothing more than a computer's sound card connected to a radio — no specialised hardware needed.

The introduction of WSJT (Weak Signal Joe Taylor) software by Nobel Prize–winning physicist Joe Taylor (K1JT) in 2001 opened a new era of weak-signal digital communication. The release of FT8 in 2017 was a watershed moment: within months it became the most-used mode on HF, fundamentally changing how many operators use the bands. Meanwhile, digital voice modes — D-STAR (2001), DMR (adapted for amateur use around 2012), System Fusion (2014), and M17 (2019) — have brought digital networking capabilities to VHF/UHF.

## Where to Go Next

- [Digital Station Setup](/digital-modes/digital-station-setup) — How to set up your station for digital modes
- [Sound Card Interface](/digital-modes/sound-card-interface) — Connecting your radio to your computer
- [FT8](/digital-modes/ft8) — Get started with the most popular digital mode
- [DMR](/digital-modes/dmr) — Explore digital voice on VHF/UHF
- [APRS](/digital-modes/aprs) — Position reporting and messaging
- [Winlink](/digital-modes/winlink) — Radio email for off-grid communication
- [Software & Tools Overview](/software/overview) — Software for digital modes and more
