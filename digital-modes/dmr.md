---
title: DMR
description: Digital Mobile Radio — the most widely adopted digital voice mode in amateur radio, using TDMA talkgroups and repeater networks
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, dmr, digital-voice, tdma
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# DMR

**DMR** (Digital Mobile Radio) is a digital voice and data standard originally developed by ETSI (European Telecommunications Standards Institute) for commercial two-way radio. Amateur radio operators adopted DMR around 2012, and it has since become the most widely used digital voice mode in the hobby. DMR's combination of affordable radios, two simultaneous conversations per channel (TDMA), talkgroup-based routing, and extensive worldwide repeater networks has made it a dominant force on VHF and UHF.

## How DMR Works

DMR uses **TDMA (Time Division Multiple Access)** to divide a single 12.5 kHz channel into **two time slots**. Each time slot carries an independent voice or data stream, meaning a single DMR repeater can handle two simultaneous conversations on one frequency pair — effectively doubling the capacity compared to analogue FM.

Voice is digitised using the **AMBE+2** (Advanced Multi-Band Excitation) vocoder, which compresses speech into a 3,600 bits per second data stream. The AMBE+2 codec is proprietary, developed by DVSI (Digital Voice Systems, Inc.), and requires a licensed chip or software implementation. This is one of the criticisms of DMR (and D-STAR and System Fusion, which also use AMBE variants) — the voice codec is not open-source. The [M17](/digital-modes/m17) project was created partly in response to this.

### Talkgroups

The most distinctive feature of amateur DMR is the **talkgroup** system. A talkgroup is essentially a virtual channel — a group of users who want to talk to each other. When you transmit on a talkgroup, everyone monitoring that talkgroup on connected repeaters hears you.

Talkgroups can be local (just one repeater), regional, national, or worldwide. For example:

- **TG 91** — Worldwide English
- **TG 93** — North America
- **TG 235** — United Kingdom
- **TG 302** — Canada
- **TG 3100** — United States

Each repeater's administrator configures which talkgroups are available on each time slot. A typical setup might have a local talkgroup and a regional talkgroup on Time Slot 2, with national and international talkgroups on Time Slot 1.

### DMR Networks

Amateur DMR repeaters are interconnected through network infrastructure. The major networks include:

**Brandmeister** — The largest worldwide amateur DMR network. Brandmeister supports dynamic talkgroup activation (you can connect to any talkgroup on the fly by briefly keying up on it), hotspot support, and bridging to other digital voice modes. Most new amateur DMR users end up on Brandmeister.

**TGIF** — A community-oriented network with a focus on simplicity. Originally stood for "Thank God It's Friday" from the weekly nets that inspired it.

**DMR-MARC** — One of the original amateur DMR networks. Uses a more static talkgroup configuration model.

**FreeDMR** — An open-source network infrastructure project.

Different repeaters may be connected to different networks, and talkgroups are not always consistent between networks (the same number may mean different things). Check your local repeater's information to know which network it uses.

## Getting Started with DMR

### What you need

- **A DMR radio** — Handheld (HT) or mobile. Popular amateur DMR radios include models from Anytone (AT-D878UV, AT-D578UV), TYT (MD-UV390, MD-9600), Radioddity, and Ailunce. More expensive commercial radios from Motorola and Hytera also work but are overkill for most amateur use.
- **A DMR ID** — You must register for a unique DMR ID at radioid.net. This is a 7-digit number that identifies you on the network, linked to your callsign. Registration is free.
- **A codeplug** — DMR radios require programming with a "codeplug" — a configuration file that defines channels, talkgroups, contacts, and zones. Creating your first codeplug is often the biggest hurdle for new DMR operators.

### The codeplug

A codeplug is DMR's equivalent of a memory channel list, but more complex. It defines:

- **Channels** — Each entry specifies a frequency, time slot, talkgroup, and colour code (analogous to a CTCSS tone for access control).
- **Contacts** — A list of talkgroups and individual DMR IDs.
- **Zones** — Groups of channels organised by purpose or location (e.g., "Local Repeaters", "Hotspot Channels").
- **Receive groups** — Lists of talkgroups your radio will monitor.

Programming a codeplug from scratch is tedious. Most operators start with a pre-built codeplug for their area and radio model, available from local DMR groups, repeater websites, or tools like the **Brandmeister Codeplug Generator**. Codeplug programming software is specific to each radio manufacturer.

### Hotspots

If you don't have a local DMR repeater, or you want to access the network from home without tying up a repeater, a **hotspot** is the solution. A hotspot is a low-power personal "repeater" (typically a Raspberry Pi with a MMDVM hat or a standalone device like the openSPOT or Pi-Star) that connects to the DMR network over the internet. You talk to the hotspot with your DMR radio at very low power, and it relays your audio to the network.

Popular hotspot platforms include:

- **Pi-Star** — Free, open-source software for Raspberry Pi–based hotspots. Supports DMR, D-STAR, System Fusion, and more.
- **WPSD** — A fork of Pi-Star with additional features.
- **openSPOT** — A commercial standalone hotspot device (no Pi needed).

Hotspots have become enormously popular because they give you access to the entire worldwide DMR network from your desk with just a handheld radio.

## Operating on DMR

### Making a call

1. **Select the appropriate channel** — Choose a channel programmed with the talkgroup you want to use, on the correct time slot.
2. **Listen first** — DMR repeaters often carry multiple talkgroups. Listen for a few moments to make sure the time slot is clear.
3. **Key up briefly** — Press the PTT for about 1–2 seconds, then release. This "kerchunks" the repeater and activates the talkgroup on Brandmeister (if it's a dynamic talkgroup).
4. **Make your call** — Press PTT and call CQ or the station you want to reach. Speak clearly and at a normal pace.
5. **Release PTT and wait** — DMR has a slight delay during the transition between transmit and receive. Wait about 1 second after the other station stops before keying up, to avoid cutting off the beginning of your transmission.

### DMR etiquette

**Wait for the "bonk"** — When a DMR transmission ends, most radios make a characteristic sound (sometimes called the "bonk" or "kerchunk"). Wait for this before transmitting to avoid doubling.

**Keep talkgroup selection appropriate** — Don't ragchew on a worldwide talkgroup when a regional or local one would do. Worldwide talkgroups tie up repeaters across multiple countries.

**Don't "kerchunk" excessively** — A brief key-up to activate a dynamic talkgroup is fine, but repeatedly keying up without identifying is poor practice.

**Identify as you would on any mode** — FCC and other regulatory requirements for station identification still apply on DMR.

## DMR vs Other Digital Voice Modes

| Feature | DMR | [D-STAR](/digital-modes/dstar) | [System Fusion](/digital-modes/system-fusion) | [M17](/digital-modes/m17) |
|---------|-----|-------|---------------|-----|
| Standard | ETSI (open standard) | JARL (proprietary) | Yaesu (proprietary) | Community (open-source) |
| Voice codec | AMBE+2 (proprietary) | AMBE (proprietary) | AMBE+2 (proprietary) | Codec2 (open-source) |
| Time slots | 2 (TDMA) | 1 | 1 | 1 |
| Routing | Talkgroups | Reflectors / callsign routing | Rooms / WIRES-X | Reflectors |
| Radio cost | Low–Medium | Medium–High | Medium–High | Low (DIY) to Medium |
| Network size | Very large | Large | Medium | Growing |

DMR's main advantages are affordable radios, dual time slots, and the largest network. Its main drawbacks are the complexity of codeplug programming and the proprietary voice codec.

## Where to Go Next

- [D-STAR](/digital-modes/dstar) — Another popular digital voice mode
- [System Fusion](/digital-modes/system-fusion) — Yaesu's digital voice system
- [M17](/digital-modes/m17) — Open-source digital voice
- [Repeaters](/operating/repeaters) — How repeaters work
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — Operating on VHF and UHF
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
