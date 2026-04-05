---
title: Packet Radio
description: AX.25 packet radio — the original digital data networking mode for amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, packet, ax25, networking
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Packet Radio

**Packet radio** is a digital data communication method that uses the **AX.25** protocol to transmit data in discrete packets over amateur radio. Emerging in the 1980s, packet radio was amateur radio's first practical digital networking system. It brought concepts like error correction, automatic retransmission, bulletin board systems (BBS), and multi-hop networking to the hobby — years before the internet became widely available. While newer technologies have taken over many of its functions, packet radio remains the foundation for [APRS](/digital-modes/aprs) and continues to be used for messaging, BBS systems, and emergency communications.

## How Packet Radio Works

Packet radio breaks data into **packets** — blocks of data with addressing, error-checking, and control information included. Each packet contains:

- **Source and destination callsigns** (with SSIDs)
- **Digipeater path** (intermediate stations to relay through)
- **Control and protocol information**
- **Payload data** (the actual message)
- **Frame check sequence** (CRC error detection)

The key features of AX.25 packet radio are:

**Error detection and correction** — Each packet includes a CRC (cyclic redundancy check). If the receiving station detects an error, it requests retransmission. This means data arrives correctly or not at all — no garbled text.

**Automatic retransmission** — Connected-mode AX.25 (see below) automatically retransmits lost or corrupted packets without operator intervention.

**Digipeating** — Packets can be relayed through intermediate stations (digipeaters) to extend range, similar to how [APRS](/digital-modes/aprs) digipeating works. APRS is, in fact, built on top of AX.25.

### Connection modes

AX.25 supports two modes:

**Connected mode** — A reliable, acknowledged link between two stations. Packets are numbered, acknowledged, and retransmitted if lost. Similar to TCP in the internet world. Used for BBS connections, file transfers, and any application where reliable delivery matters.

**Unconnected (UI) mode** — Packets are sent without establishing a connection and without acknowledgement. Like UDP in internet terms. [APRS](/digital-modes/aprs) uses UI frames exclusively, since it broadcasts to all listeners rather than connecting to a specific station.

### Speeds

Traditional amateur packet radio operates at two standard speeds:

**1,200 baud** — Used on VHF (typically 2 metres, 144 MHz). Uses Bell 202 AFSK (Audio Frequency Shift Keying) modulation with tones at 1,200 Hz and 2,200 Hz. This is the standard speed for [APRS](/digital-modes/aprs) and most VHF packet activity.

**9,600 baud** — Used on UHF (typically 70 cm, 430 MHz) and requires a radio with a "data port" or direct FSK input, since the modulation is too fast for a standard microphone audio path. Less common but used for higher-speed applications and some satellite links.

Higher speeds are possible with specialised modems and wideband channels, but 1,200 baud remains the dominant speed for packet radio activity.

## Hardware

### TNC (Terminal Node Controller)

Traditionally, packet radio required a **TNC** — a hardware modem that sits between the radio and the computer. The TNC handles the AX.25 protocol, encoding data into audio tones for the radio and decoding incoming audio back into data. Classic TNCs include the Kantronics KPC-3+, MFJ-1270X, and the Timewave PK-232.

### Software TNCs

Modern packet radio often uses **software TNCs** instead of dedicated hardware:

- **Dire Wolf** — Free, open-source software TNC for Windows, Linux, and macOS. Connects to the radio through a [sound card interface](/digital-modes/sound-card-interface) and provides full AX.25 packet capability. Dire Wolf is the most popular software TNC and is widely used for [APRS](/digital-modes/aprs) IGates and digipeaters.
- **UZ7HO SoundModem** — Free Windows software TNC supporting multiple packet speeds.

With a software TNC, all you need is a computer with a sound card interface to your radio — no additional hardware modem.

### Radios

Any FM transceiver can be used for 1,200 baud packet radio. For 9,600 baud, the radio needs a "data" or "packet" port that provides flat audio (before de-emphasis) and direct modulator input. Many modern amateur VHF/UHF radios include this port.

## Packet Radio Applications

### BBS (Bulletin Board Systems)

Packet radio BBS nodes were the original email and message-sharing system for amateur radio. Users connect to a BBS via packet, read and post messages, and forward messages to other BBS nodes across a regional or national network. While less active than in packet radio's heyday, BBS systems are still maintained by some operators and are used in emergency communications exercises.

### APRS

[APRS](/digital-modes/aprs) is the largest and most active application of packet radio today. It uses AX.25 UI frames at 1,200 baud on a dedicated VHF frequency for position reporting, messaging, weather data, and telemetry.

### Winlink

[Winlink](/digital-modes/winlink) supports packet radio as a transport protocol for VHF/UHF email connections, though [VARA FM](/digital-modes/vara) has largely replaced packet for this purpose due to its much higher throughput.

### TCP/IP over AX.25

Some operators run TCP/IP networking over AX.25, effectively creating a radio-based internet (AMPRNet / 44.x.x.x network). This is a niche but active area, especially among technically minded operators.

## The History and Legacy of Packet Radio

Packet radio arrived in amateur radio in the early 1980s, inspired by the ALOHA network at the University of Hawaii (one of the precursors to the internet). The Vancouver Amateur Digital Communication Group (VADCG) developed the first amateur packet radio TNC, and the mode spread rapidly throughout the 1980s and 1990s.

At its peak, packet radio supported extensive BBS networks, real-time chat (converse mode), DX cluster spotting networks, and even early forms of internet access for amateurs. The rise of the internet in the mid-1990s reduced packet radio's role as a general-purpose networking system, but it left lasting legacies: APRS, Winlink, and the broader concept of data networking over amateur radio all grew directly from the packet radio movement.

Today, packet radio is experiencing a modest revival as interest in mesh networking, off-grid communication, and emergency preparedness drives operators back to radio-based data systems. Projects combining packet radio concepts with modern technology (like Meshtastic on ISM bands, or high-speed data links on amateur microwave bands) carry the spirit of packet radio forward.

## Where to Go Next

- [APRS](/digital-modes/aprs) — The most active packet radio application today
- [Winlink](/digital-modes/winlink) — Radio email using packet and other protocols
- [VARA](/digital-modes/vara) — Modern high-speed alternative to packet
- [Emergency Communications Overview](/emergency-communications/overview) — Packet radio in emcomm
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station setup for digital modes
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
