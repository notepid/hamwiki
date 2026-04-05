---
title: APRS
description: Automatic Packet Reporting System — real-time position reporting, messaging, and telemetry over amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, aprs, packet, position-reporting
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# APRS

**APRS** (Automatic Packet Reporting System) is a real-time tactical communication system designed by Bob Bruninga (WB4APR, SK 2022). First developed in the late 1980s, APRS combines position reporting, two-way messaging, weather data, telemetry, and other information sharing into a single system that runs over amateur radio. If you have ever tracked a ham's position on a map in real time, you have seen APRS in action.

APRS is not just a position tracker — though that is its most visible feature. It was designed as a local tactical communication network where everyone in an area can see the same real-time picture of stations, objects, weather, and messages.

## How APRS Works

APRS uses **AX.25 packet radio** at **1,200 baud** on a shared VHF frequency. In North America, the primary APRS frequency is **144.390 MHz**; in Europe it is **144.800 MHz**; other regions have their own coordinated frequencies. All stations transmit and receive on this single frequency using a random access protocol (stations transmit their beacons at intervals, with timing designed to minimise collisions).

### Digipeaters

Because APRS uses VHF, range is limited to roughly line-of-sight. To extend coverage, APRS uses **digipeaters** — stations (often on hilltops or tall structures) that receive APRS packets and retransmit them. A network of digipeaters provides coverage over a wide area. APRS uses a standardised path system to control how many times a packet is digipeated:

- **WIDE1-1** — One hop through a fill-in digipeater (typically low-level, meant to help stations that can't reach a high-level digi directly)
- **WIDE2-1** — One hop through a wide-area digipeater
- **WIDE2-2** — Two hops through wide-area digipeaters

The recommended path for most stations is **WIDE1-1,WIDE2-1**, which provides good coverage without creating excessive traffic.

### Internet gateways (IGates)

**IGates** (Internet Gateways) are stations that bridge between the RF APRS network and the APRS-IS (APRS Internet System). When an IGate hears an APRS packet on RF, it forwards it to the APRS-IS servers, making it visible worldwide on websites like aprs.fi. Some IGates also relay packets from the internet back to RF (bidirectional gating), enabling messages to reach stations that might not be in direct range.

### APRS-IS

The **APRS Internet System** (APRS-IS) is a worldwide network of servers that collects, distributes, and archives APRS data. Websites and applications connect to APRS-IS to display real-time APRS information on maps. The most popular web interface is **aprs.fi**, which shows station positions, tracks, weather data, and message status on a map.

## What APRS Can Do

**Position reporting** — The most common APRS use. Stations (fixed, mobile, or portable) transmit their GPS position at regular intervals. This creates a real-time map of amateur radio activity in an area.

**Two-way messaging** — APRS supports short text messages between stations, with delivery confirmation. Messages can be sent from radio to radio, radio to internet, or internet to radio (through bidirectional IGates).

**Weather reporting** — Weather stations connected to APRS transmit temperature, humidity, barometric pressure, wind speed and direction, rainfall, and other data. This information is fed into citizen weather networks and is used by the National Weather Service in the US.

**Objects and items** — Any APRS station can place "objects" on the map — markers representing events, hazards, net frequencies, or other points of interest. This is widely used in [emergency communications](/emergency-communications/overview) to mark shelters, staging areas, and incidents.

**Telemetry** — APRS supports numeric telemetry channels for remote monitoring (battery voltage, temperature, signal levels, etc.).

**Bulletins and announcements** — Stations can transmit general messages visible to all APRS users in range.

## Getting Started with APRS

### Option 1: Dedicated APRS radio

Several radios have built-in APRS capability, with a TNC (Terminal Node Controller) and GPS receiver integrated:

- **Yaesu FT5DR / FT3DR / FT2DR** — Handheld radios with built-in APRS
- **Yaesu FTM-400XDR / FTM-300DR** — Mobile radios with built-in APRS
- **Kenwood TH-D75A / TH-D74A** — Handheld radios with full APRS, including messaging
- **Kenwood TM-D710G** — Mobile radio widely regarded as one of the best APRS radios ever made

With a dedicated APRS radio, you power it on, set the APRS frequency, enter your callsign and SSID, and it starts beaconing and receiving. Messaging is handled through the radio's interface.

### Option 2: Radio + TNC + software

You can add APRS to any VHF radio (including a basic FM handheld) by connecting a **TNC** or sound card interface and running APRS software on a computer:

- **Mobilinkd TNC** — A popular Bluetooth TNC that connects between a radio and a smartphone or tablet.
- **Dire Wolf** — Free, open-source software TNC that runs on a computer or Raspberry Pi. Connects to the radio through a [sound card interface](/digital-modes/sound-card-interface) and provides full APRS functionality.
- **aprx** — A lightweight Linux daemon for running an IGate or digipeater.

### Option 3: Smartphone apps (internet-only)

Apps like **APRSdroid** (Android) and **APRS.fi** (iOS/Android) can connect to the APRS-IS network over the internet, allowing you to send position reports and messages without a radio. This is useful for monitoring but does not put a signal on the air (no RF component).

Some apps can also connect to a radio via a Bluetooth TNC (like Mobilinkd), providing a smartphone-based APRS station with RF capability.

### SSID

APRS uses **SSIDs** (Secondary Station Identifiers) to distinguish between different stations operated by the same callsign. Your callsign is appended with a number: W1ABC-9 for a mobile station, W1ABC-7 for a handheld, W1ABC-1 for a digipeater, etc. Common SSIDs:

| SSID | Typical use |
|------|------------|
| -0 | Fixed station or home station |
| -1 | Digipeater |
| -2 | Digipeater (secondary) |
| -5 | Smartphone (APRSdroid, etc.) |
| -7 | Handheld radio |
| -8 | Boat or marine mobile |
| -9 | Car or mobile station |
| -10 | Internet (IGate, etc.) |
| -15 | Weather station |

## APRS Best Practices

**Set an appropriate beacon rate** — Fixed stations should beacon every 30 minutes (they don't move, so frequent updates waste bandwidth). Mobile stations typically beacon every 1–2 minutes. Many APRS implementations support **SmartBeaconing**, which adjusts the beacon rate based on speed and direction changes.

**Use a sensible path** — For most situations, **WIDE1-1,WIDE2-1** provides adequate coverage. Avoid long paths like WIDE2-2 or WIDE3-3 in areas with dense APRS activity, as they create excessive traffic.

**Include useful information** — Set a meaningful status text or comment. For a home station, include your location description. For a weather station, ensure your data is calibrated and accurate.

**Don't rely on APRS for safety-critical communication** — APRS uses a shared channel with no guaranteed delivery. Messages may be lost. For [emergency communications](/emergency-communications/overview), APRS is a valuable supplementary tool but should not be the sole communication method.

## APRS in Emergency Communications

APRS is widely used in [emergency communications](/emergency-communications/overview) and public service events. During emergencies, APRS provides:

- Real-time tracking of deployed resources (vehicles, personnel)
- Object placement to mark shelters, hazards, command posts, and staging areas
- Two-way messaging when voice channels are congested
- Weather data from local stations

[ARES](/emergency-communications/ares) and [RACES](/emergency-communications/races) groups often train specifically on APRS deployment for served agency support.

## Where to Go Next

- [Packet Radio](/digital-modes/packet-radio) — The underlying technology behind APRS
- [Winlink](/digital-modes/winlink) — Radio email, another data application
- [Emergency Communications Overview](/emergency-communications/overview) — APRS in emcomm
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — Operating on VHF where APRS lives
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station configuration
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
