---
title: Winlink
description: Email over radio — the Winlink global radio email system for off-grid and emergency communication
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, winlink, email, emergency, vara
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Winlink

**Winlink** (formally the Winlink Global Radio Email System) is a worldwide network that allows amateur radio operators to send and receive email over HF and VHF/UHF radio, without any internet connection at the user's end. Originally developed for the maritime community, Winlink has become a critical tool for [emergency communications](/emergency-communications/overview), off-grid operation, and any situation where internet access is unavailable or unreliable.

When you send an email through Winlink, your radio connects to a **Radio Message Server (RMS)** gateway — another amateur station with internet access — which relays your message to the Winlink server infrastructure and from there to the internet email system. The recipient receives a normal email. Replies come back the same way, waiting at the server until you connect again by radio to download them.

## How Winlink Works

### Architecture

The Winlink system has several components:

**Client stations** — Your station. You run Winlink client software, connect to a gateway via radio, and send/receive email.

**RMS gateways** — Volunteer-operated stations that bridge between radio and the internet. There are hundreds of RMS gateways worldwide on both HF and VHF/UHF. Gateway operators run the RMS software and maintain internet-connected radio stations that listen for incoming connections.

**Common Message Servers (CMS)** — Cloud-based servers that store and forward messages between gateways, clients, and the internet email system. The CMS infrastructure is operated by the Winlink Development Team.

**Winlink.org** — You can also access your Winlink email through a web browser at winlink.org (when you have internet), or via a Telnet connection for testing.

### Transport protocols

Winlink supports several radio transport protocols for the actual over-the-air data transfer:

**[VARA](/digital-modes/vara) HF** — The most popular HF protocol for Winlink. VARA offers significantly higher throughput than older protocols and adaptive speed control. Most HF Winlink gateways now support VARA.

**VARA FM** — VARA's VHF/UHF variant, optimised for FM radio channels. Very high throughput on VHF.

**Winmor** — An older HF protocol, now largely superseded by VARA HF. Free and open.

**ARDOP** — Another HF protocol (Amateur Radio Digital Open Protocol). Open-source, but slower than VARA.

**Packet (AX.25)** — Traditional [packet radio](/digital-modes/packet-radio) at 1,200 baud (VHF) or 300 baud (HF). Very slow by modern standards but simple and reliable.

**Pactor** — A commercial protocol available in versions I through IV. Pactor modems are expensive (especially Pactor III/IV), but Pactor IV is the fastest HF protocol available. Used mainly by maritime and expeditionary stations.

For most operators getting started with Winlink, **VARA HF** (for HF) or **VARA FM** (for VHF/UHF) is the recommended choice.

### What you can send

Winlink supports standard email features including text messages, attachments (with size limitations), and form templates. Message size is limited — typically around 120 KB for HF connections — because radio bandwidth is slow compared to the internet. Large attachments should be avoided.

Winlink also includes a library of **standard forms** (ICS-213 General Message, HICS forms, welfare inquiry/reply, situation reports, and many others) that are essential for emergency communications. These forms are built into the client software and format messages in a structured way that served agencies expect.

## Setting Up for Winlink

### Software

**Winlink Express** — The primary Winlink client for Windows. Free to download from winlink.org. Winlink Express handles all transport protocols, message composition, form filling, and gateway selection. It is the recommended client for most users.

**Pat** — An open-source, cross-platform Winlink client that runs on Windows, macOS, Linux, and Raspberry Pi. Pat is popular with Linux users and for building portable/go-kit stations on Raspberry Pi.

### Hardware

**For HF Winlink:**
- An HF transceiver with CAT control and audio interface (USB audio or [sound card interface](/digital-modes/sound-card-interface))
- A computer running Winlink Express or Pat
- VARA HF software (free limited version available; full version requires a paid licence of approximately $70 USD)

**For VHF/UHF Winlink:**
- A VHF/UHF FM transceiver
- A sound card interface or radio with built-in audio codec
- VARA FM software
- Alternatively, a traditional TNC for packet radio connections

### Connecting to a gateway

Winlink Express includes a gateway listing that shows all available RMS gateways, their frequencies, protocols, and current status. For HF, you select a gateway within propagation range, tune to its frequency, and initiate a connection. For VHF/UHF, you connect to a local gateway (often co-located with a repeater site).

The connection process is automatic — Winlink Express and VARA handle the handshaking, message transfer, and disconnection. A typical HF session to send and receive a few short emails takes 2–5 minutes.

## Winlink in Emergency Communications

Winlink is one of the most important tools in the amateur radio [emergency communications](/emergency-communications/overview) toolkit. During disasters, when internet and telephone infrastructure is damaged or congested, Winlink provides a way to send detailed messages — including structured forms — to emergency management agencies, served organisations, and individuals.

Key emergency communication features include:

**Standard forms** — ICS-213 (General Message), Situation Reports, Welfare Inquiry/Reply, Hospital Bed Availability (HICS), and many others. These forms ensure information is transmitted in formats that emergency managers can immediately use.

**Peer-to-peer mode** — Winlink clients can connect directly to each other via radio, without any gateway or internet connection. This is critical when all infrastructure is down.

**Radio-only mesh** — Multiple Winlink stations can relay messages to each other, creating a store-and-forward network that operates entirely on radio.

**Winlink Wednesday** — Many ARES/RACES groups hold weekly Winlink exercises (often on Wednesdays) to maintain proficiency and test equipment.

## Winlink Accounts and Addressing

To use Winlink, register for a free account at winlink.org. Your Winlink email address is **yourcallsign@winlink.org**. Anyone on the internet can send email to this address, and you can download it the next time you connect via radio (or check via the web interface).

You can also send email from your Winlink account to any internet email address. The email will appear to come from your callsign@winlink.org address.

> **Important:** All Winlink messages on amateur radio frequencies must comply with amateur radio regulations — no encryption, no commercial traffic, and station identification requirements apply. Third-party traffic rules also apply (this varies by country).
{.is-info}

## Where to Go Next

- [VARA](/digital-modes/vara) — The most popular transport protocol for Winlink
- [Packet Radio](/digital-modes/packet-radio) — The original data networking mode
- [Emergency Communications Overview](/emergency-communications/overview) — EmComm tools and training
- [Go Kit](/emergency-communications/go-kit) — Portable stations for deployment
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station configuration
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
