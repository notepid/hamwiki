---
title: D-STAR
description: Digital Smart Technologies for Amateur Radio — the first digital voice system designed specifically for amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, dstar, digital-voice, icom
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# D-STAR

**D-STAR** (Digital Smart Technologies for Amateur Radio) is a digital voice and data protocol developed by JARL (Japan Amateur Radio League) in the early 2000s, with radio hardware primarily manufactured by Icom. It was the first digital voice system designed specifically for amateur radio use, and it introduced several concepts — internet gateway linking, callsign-based routing, and simultaneous voice and low-speed data — that were later adopted by other digital voice systems.

## How D-STAR Works

D-STAR defines several modes of operation, but the most commonly used is **DV (Digital Voice)** mode on VHF and UHF. In DV mode, the radio digitises voice using the **AMBE** vocoder (an older version than the AMBE+2 used by [DMR](/digital-modes/dmr)) at 3,600 bps, and adds a 1,200 bps data channel that runs simultaneously. This data channel can carry GPS position, text messages, or other information alongside the voice stream.

D-STAR also defines a **DD (Digital Data)** mode that provides an Ethernet-compatible 128 kbps data link on the 23 cm (1.2 GHz) band, though this mode is rarely used in practice.

### Callsign routing

One of D-STAR's distinguishing features is **callsign-based routing**. Every D-STAR user registers their callsign with the network, and the system tracks which repeater or gateway they were last heard on. You can call a specific station by entering their callsign into your radio, and the network will route your call to whichever repeater or gateway that station is currently using — even if they are on the other side of the world, connected through the internet backbone.

This is fundamentally different from [DMR's](/digital-modes/dmr) talkgroup approach, where you join a virtual channel and talk to everyone monitoring it. D-STAR can do group communication through reflectors (see below), but the callsign routing capability means you can also "ring" a specific person directly.

### Reflectors

D-STAR **reflectors** are conference servers that allow multiple repeaters and users to be linked together for group communication. A reflector is identified by a designator like REF001, DCS006, or XLX123. When a repeater or user connects to a reflector, everyone else connected to that reflector hears the conversation.

Reflectors serve a similar function to DMR talkgroups, though the mechanism is different. You connect to a reflector by sending a brief command from your radio (or through the repeater's dashboard), and disconnect when you are done.

## Getting Started with D-STAR

### What you need

- **A D-STAR compatible radio** — Icom is the primary manufacturer (IC-705, IC-9700, IC-5100A, ID-52A, ID-31A Plus, and others). Some third-party radios support D-STAR through add-on boards or firmware.
- **Registration** — Register your callsign on a D-STAR gateway. The most common registration point is the US Trust or ircDDB network, though many gateways accept registration through their own web portal. Without registration, you can use local repeaters but not the internet-linked features.
- **Programming** — D-STAR radios need to be programmed with repeater frequencies, RPT1 and RPT2 fields (which control local and gateway routing), and your personal callsign settings.

### Programming concepts

D-STAR programming involves several fields that are unique to the mode:

**MY** — Your callsign (up to 8 characters).

**UR** — The destination callsign. Set to "CQCQCQ" for general calls. For callsign routing, enter the specific callsign. For reflector commands, enter the reflector designator.

**RPT1** — The callsign of the local repeater module you are accessing (e.g., "VE3XXX B" for the 70 cm module of repeater VE3XXX).

**RPT2** — The callsign of the repeater's gateway (e.g., "VE3XXX G") when you want internet-linked communication. Leave blank or set to the repeater callsign for local-only use.

This four-field addressing system is more complex than DMR codeplug programming in some ways, though D-STAR radios generally require less up-front configuration because there are no talkgroups, colour codes, or receive group lists to define.

### Hotspots

As with DMR, **hotspots** are popular for D-STAR. A Pi-Star or WPSD hotspot with an MMDVM board can function as a personal D-STAR gateway, connecting to reflectors and the D-STAR network over the internet. This lets you use D-STAR from home even if there are no local repeaters.

## D-STAR Networks and Infrastructure

D-STAR's networking infrastructure consists of several interconnected systems:

**US Trust / K5TIT Trust** — The original D-STAR gateway trust system for the Americas. Gateways registered here can route calls to each other.

**ircDDB** — An alternative routing database that provides more dynamic and reliable callsign lookup. Most modern D-STAR gateways use ircDDB alongside or instead of the trust system.

**REF reflectors** — The original D-STAR reflector system.

**DCS reflectors** — A newer reflector system with improved features.

**XLX reflectors** — Multi-protocol reflectors that can bridge D-STAR, DMR, and other modes together. XLX reflectors have become very popular because they allow cross-mode communication.

## D-STAR Features

**Simultaneous voice and data** — The 1,200 bps data channel alongside voice can carry GPS positions, short text messages, and weather data. When you transmit on D-STAR with GPS enabled, your position is sent along with your voice.

**DPRS (D-STAR Position Reporting System)** — D-STAR GPS data can be gated to the [APRS](/digital-modes/aprs) network, appearing on APRS maps alongside stations using traditional APRS on 2 metres.

**Low-speed data mode** — Independent of voice, D-STAR supports a low-speed data mode for applications like D-RATS, a peer-to-peer messaging and file transfer application.

**Repeater linking** — Repeaters can be linked to each other directly (without a reflector), creating temporary point-to-point connections between specific repeaters.

## D-STAR vs Other Modes

D-STAR was the pioneer of digital voice in amateur radio, and many of its concepts influenced later systems. Compared to [DMR](/digital-modes/dmr), D-STAR has a smaller network and fewer radio choices (primarily Icom), but offers callsign routing and a slightly simpler conceptual model. Compared to [System Fusion](/digital-modes/system-fusion), D-STAR has better internet linking infrastructure but less seamless backwards compatibility with analogue FM. Compared to [M17](/digital-modes/m17), D-STAR uses a proprietary voice codec but has a much more mature network and wider radio availability.

Icom continues to develop D-STAR radios, and the mode has a dedicated user base, particularly in Japan, North America, and Europe.

## Where to Go Next

- [DMR](/digital-modes/dmr) — The most widely adopted digital voice mode
- [System Fusion](/digital-modes/system-fusion) — Yaesu's digital voice system
- [M17](/digital-modes/m17) — Open-source digital voice
- [APRS](/digital-modes/aprs) — Position reporting (D-STAR positions can be gated to APRS)
- [Repeaters](/operating/repeaters) — How repeaters work
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
