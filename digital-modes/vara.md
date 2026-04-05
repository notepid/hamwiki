---
title: VARA
description: VARA HF and FM modems — modern high-speed data protocols for Winlink and other amateur radio applications
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, vara, winlink, modem
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# VARA

**VARA** is a family of high-performance software modems for amateur radio, developed by EA5HVK (José Alberto Nieto Ros). VARA has become the de facto standard transport protocol for [Winlink](/digital-modes/winlink) and is increasingly used for other data applications. It offers dramatically higher throughput than older amateur radio data protocols, making radio email and file transfer practical where they were previously painfully slow.

VARA comes in two versions: **VARA HF** for high-frequency (shortwave) bands, and **VARA FM** for VHF/UHF FM channels.

## How VARA Works

### VARA HF

VARA HF is a sound card-based modem that operates through an HF transceiver's SSB audio path. It uses **OFDM (Orthogonal Frequency Division Multiplexing)** with multiple subcarriers, adaptive modulation, and forward error correction to achieve high data rates within the constraints of HF radio.

Key characteristics:

- **Bandwidth:** Configurable, typically 500 Hz or 2,300 Hz
- **Maximum throughput:** Up to approximately 8,400 bps in the 2,300 Hz bandwidth mode under good conditions
- **Adaptive speed:** VARA continuously monitors channel quality and adjusts its modulation, coding rate, and number of subcarriers to match conditions. When the signal is strong, it ramps up to higher speeds; when conditions deteriorate, it drops to more robust (slower) modes automatically.
- **ARQ (Automatic Repeat Request):** Reliable data delivery with automatic retransmission of corrupted data blocks.

The adaptive speed control is one of VARA's most important features. An HF channel can change rapidly — fading, interference, and propagation shifts happen constantly. VARA reacts to these changes in real time, squeezing maximum throughput from whatever conditions are available.

### VARA FM

VARA FM is designed for VHF/UHF FM radio channels, where conditions are much more stable than HF. Without the challenges of HF propagation, VARA FM can achieve significantly higher speeds:

- **Maximum throughput:** Up to approximately 25,000 bps on a 12.5 kHz FM channel
- **Typical throughput:** 5,000–15,000 bps in practice, depending on signal strength and radio characteristics

VARA FM connects through the radio's audio path, similar to VARA HF, but optimised for the wider, more stable bandwidth of FM.

## VARA and Winlink

VARA's primary use in amateur radio is as a transport protocol for [Winlink](/digital-modes/winlink). When you send or receive email over Winlink, the Winlink client software (like Winlink Express or Pat) uses VARA as the modem to transfer data between your station and the RMS gateway.

Before VARA, HF Winlink typically used Winmor (~500 bps maximum) or Pactor (expensive hardware modems). VARA brought Pactor-like performance using only a sound card interface — no specialised hardware needed.

### Comparison with other Winlink protocols

| Protocol | Type | Max speed (HF) | Cost |
|----------|------|----------------|------|
| VARA HF | Software modem | ~8,400 bps | Free (limited) / ~$70 (full) |
| ARDOP | Software modem | ~1,200 bps | Free (open-source) |
| Winmor | Software modem | ~500 bps | Free (discontinued) |
| Pactor IV | Hardware modem | ~5,500 bps | ~$1,500–$2,000+ |
| Packet (AX.25) | TNC | 300 bps (HF), 1,200 bps (VHF) | Free (with software TNC) |

VARA's combination of high speed and low cost (software-only, no special hardware) has made it the most popular choice for Winlink by a wide margin.

## Setting Up VARA

### Software

VARA HF and VARA FM are separate software applications, available for **Windows only** (as of the current version). They run as background modem processes that other applications (like Winlink Express) connect to via a local TCP/IP port.

**Free version:** VARA offers a free version with reduced speed (limited to approximately 175 bps for VARA HF). This is functional for basic email but very slow.

**Registered version:** The full-speed version requires a paid licence (approximately $70 USD for VARA HF, with VARA FM sometimes included or available separately). The licence is a one-time purchase tied to your callsign.

> While VARA itself is Windows-only, Linux users can run it under Wine with good results. The Pat Winlink client on Linux integrates with VARA running under Wine. Some community guides document this setup in detail.
{.is-info}

### Hardware

VARA uses the same [digital station setup](/digital-modes/digital-station-setup) as other HF digital modes:

- HF transceiver (for VARA HF) or VHF/UHF FM transceiver (for VARA FM)
- [Sound card interface](/digital-modes/sound-card-interface) or radio with built-in USB audio
- CAT control for PTT and frequency management
- A computer running Windows (or Linux with Wine)

Audio level settings are critical for VARA performance. The VARA software includes a built-in audio level indicator — follow its recommendations and keep ALC at zero on the radio.

### Configuration

VARA's settings include:

- **Audio devices:** Select the sound card interface input and output
- **Bandwidth:** 500 Hz or 2,300 Hz for VARA HF (2,300 Hz recommended when band conditions and regulations permit)
- **VARA FM settings:** Audio device selection and radio-specific parameters

Winlink Express includes automatic VARA integration — when you select a VARA HF or VARA FM channel, it launches and configures VARA automatically.

## VARA Beyond Winlink

While Winlink is VARA's primary application, the modem can be used by other software for general-purpose data transfer over radio. Applications that support VARA as a transport include:

- **VarAC** — A keyboard-to-keyboard chat application that uses VARA as its modem, providing real-time text chat with the speed benefits of VARA's adaptive modulation. VarAC has gained popularity as a modern, fast alternative to [PSK31](/digital-modes/psk31) for text conversations on HF.
- **VARA Chat** — Built-in chat functionality within the VARA software itself.
- **Pat** — The open-source Winlink client supports VARA for Winlink connections.

## Where to Go Next

- [Winlink](/digital-modes/winlink) — Radio email, VARA's primary application
- [Packet Radio](/digital-modes/packet-radio) — The older data protocol VARA has largely replaced
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station configuration for digital modes
- [Sound Card Interface](/digital-modes/sound-card-interface) — Connecting radio and computer
- [PSK31](/digital-modes/psk31) — Keyboard-to-keyboard mode (compare with VarAC)
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
