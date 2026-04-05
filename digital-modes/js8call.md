---
title: JS8Call
description: Keyboard-to-keyboard weak-signal messaging built on FT8 technology — for real conversations and store-and-forward networking
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, js8call, weak-signal, messaging
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# JS8Call

**JS8Call** is a weak-signal digital mode designed by Jordan Sherer (KN4CRD) that bridges the gap between [FT8's](/digital-modes/ft8) extraordinary weak-signal performance and the freeform keyboard-to-keyboard communication of modes like [PSK31](/digital-modes/psk31). Built on the same WSJT-X modulation technology as FT8, JS8Call can decode signals deep in the noise — but instead of the rigid, automated exchanges of FT8, JS8Call lets you type actual messages and have real conversations.

JS8Call also introduces features that go beyond simple point-to-point communication: directed calling, group messaging, relay/store-and-forward networking, and heartbeat beacons that let you see who is active and reachable.

## How JS8Call Differs from FT8

JS8Call and FT8 share the same underlying 8-GFSK modulation, but they serve fundamentally different purposes:

| Feature | FT8 | JS8Call |
|---------|-----|---------|
| Purpose | Minimal contact exchange (callsigns + signal reports) | Keyboard-to-keyboard conversation and messaging |
| Message format | Fixed, structured (77-bit payload) | Freeform text, any content |
| Automation | Highly automated exchange | Operator-driven conversation |
| Networking | None (point-to-point) | Relay, store-and-forward, groups |
| Sensitivity | ~−24 dB SNR | ~−24 dB SNR (comparable) |
| Speed options | Fixed (15-second periods) | Multiple speeds (see below) |

Think of FT8 as a machine-to-machine protocol that happens to involve human operators, and JS8Call as a human-to-human communication system that happens to use the same radio technology.

## Key Features

### Freeform messaging

You type whatever you want, and JS8Call transmits it character by character using the weak-signal modulation. Messages can be any length — the software breaks long messages into transmission-sized frames and reassembles them at the receiving end.

### Speed modes

JS8Call offers multiple speed settings that trade speed for sensitivity:

- **Slow** — 30-second frames. Maximum sensitivity, best for the weakest signals.
- **Normal** — 15-second frames (same as FT8). Good balance of speed and sensitivity.
- **Fast** — 10-second frames. For stronger signals when you want faster exchanges.
- **Turbo** — 6-second frames. For strong signals and rapid conversation.

You can change speed mid-conversation, and stations on different speed settings can coexist on the same band segment.

### Directed calls and groups

JS8Call supports several calling modes:

**CQ calls** — General calls, just like FT8 or any other mode.

**Directed calls** — Call a specific station by callsign. JS8Call handles the routing.

**Group calls** — Send messages addressed to a group name (like @APRN or @EMCOMM). Any station monitoring that group receives the message. This is useful for nets and topical discussions.

**@ALLCALL** — A broadcast to all listening stations.

### Heartbeat beacons

JS8Call stations can transmit periodic **heartbeat** beacons — short automatic transmissions that announce the station's presence, grid square, and status. Other stations decode these beacons and maintain a list of active, reachable stations. This gives you a real-time picture of who is on the air and what paths are available, similar to how [APRS](/digital-modes/aprs) works for position data.

### Store-and-forward relay

One of JS8Call's most innovative features is its **relay** capability. If Station A cannot directly reach Station C, but both can reach Station B, JS8Call can automatically route the message through Station B. Station B's software handles the relay without operator intervention (if the operator has enabled relay mode).

This creates a mesh-like network where messages can hop through intermediate stations to reach their destination — a concept similar to [packet radio](/digital-modes/packet-radio) digipeating but operating at weak-signal levels on HF.

## Setting Up for JS8Call

### Software

JS8Call is free software available for Windows, macOS, and Linux, downloadable from the JS8Call website. It is a standalone application (not part of WSJT-X), though it shares WSJT-X's modulation codebase.

### Hardware

The hardware requirements are identical to [FT8](/digital-modes/ft8):

- HF transceiver with USB/SSB capability
- Computer with sound card interface or radio with built-in USB audio
- CAT control for frequency and PTT management
- Accurate clock (within ±2 seconds of UTC — slightly more forgiving than FT8)

If you are already set up for FT8, you are ready for JS8Call with no additional hardware.

### Configuration

JS8Call's setup is similar to WSJT-X: enter your callsign and grid square, configure your radio and audio devices, and set your transmit power. JS8Call also lets you configure a station status message, heartbeat interval, and group memberships.

### Common frequencies

JS8Call has established calling frequencies on each band:

| Band | Dial frequency (MHz) |
|------|---------------------|
| 80m | 3.578 |
| 40m | 7.078 |
| 30m | 10.130 |
| 20m | 14.078 |
| 15m | 21.078 |
| 10m | 28.078 |

## Operating JS8Call

### Typical workflow

1. **Start JS8Call** and tune to the appropriate band frequency.
2. **Watch the waterfall and decode pane** — You will see heartbeats, CQ calls, directed messages, and conversations appearing as they are decoded.
3. **Check the station list** — JS8Call maintains a list of stations heard, with their signal strength, grid square, and last-heard time.
4. **Call CQ or send a directed message** — Type your message, select the destination (CQ, a specific callsign, or a group), and transmit.
5. **Converse** — Type and send messages back and forth. JS8Call handles the framing and timing.

### Emergency and off-grid use

JS8Call has gained particular interest in the emergency communications and preparedness communities because it combines weak-signal performance (long range, low power) with the ability to send actual messages — not just signal reports. Features like store-and-forward relay, group messaging, and heartbeat monitoring make it a practical tool for coordination when infrastructure is down.

The @EMCOMM group is monitored by many operators interested in emergency communications practice.

## Where to Go Next

- [FT8](/digital-modes/ft8) — The weak-signal mode JS8Call is built on
- [PSK31](/digital-modes/psk31) — Another keyboard-to-keyboard mode (stronger signals needed)
- [Winlink](/digital-modes/winlink) — Radio email for longer-form off-grid messaging
- [Emergency Communications Overview](/emergency-communications/overview) — JS8Call in emcomm
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station setup guide
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
