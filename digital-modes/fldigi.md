---
title: Fldigi
description: Fldigi — the free, open-source multi-mode digital modem software for amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, fldigi, software, psk31, rtty
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Fldigi

**Fldigi** (Fast Light Digital modem application) is a free, open-source digital mode program for amateur radio, developed by Dave Freese (W1HKJ) and a community of contributors. It runs on Windows, macOS, and Linux, and supports a remarkably wide range of digital modes — from [PSK31](/digital-modes/psk31) and [RTTY](/digital-modes/rtty) to Olivia, MT63, MFSK, Contestia, Thor, and dozens more. If you want a single piece of software that can operate nearly any keyboard-to-keyboard digital mode on HF, Fldigi is the go-to choice.

## What Fldigi Does

Fldigi turns your computer into a multi-mode digital modem. It takes audio from your radio (via a [sound card interface](/digital-modes/sound-card-interface) or built-in USB audio), decodes the digital signals, and displays the decoded text on screen. When you type a message, Fldigi generates the appropriate audio tones and feeds them to the radio for transmission.

The interface centres on a **waterfall display** that shows a visual representation of all signals within the radio's passband. You click on a signal in the waterfall to tune to it, and the decoded text appears in the receive window. The transmit window lets you type text or trigger macros for CQ calls, exchanges, and other common messages.

## Supported Modes

Fldigi supports an extensive list of digital modes, including:

**Phase Shift Keying:** PSK31, PSK63, PSK125, PSK250, PSK500, QPSK31, QPSK63, and multi-carrier variants (PSK-R modes)

**Frequency Shift Keying:** RTTY (Baudot and ASCII), NAVTEX

**MFSK (Multi-Frequency Shift Keying):** MFSK4, MFSK8, MFSK16, MFSK32, MFSK64, MFSK128

**Olivia:** A robust mode designed for difficult HF conditions, with multiple bandwidth and tone configurations (Olivia 8/250, 8/500, 16/1000, 32/1000, and others)

**MT63:** A wideband keyboard mode with strong error correction, popular in some emergency communication networks

**Thor:** A robust MFSK variant with forward error correction

**Contestia:** Similar to Olivia, optimised for contesting

**DominoEX:** An incremental frequency keying mode

**Feld Hell / Hell modes:** Hellschreiber, a fascinating mode that transmits text as a visual bitmap pattern

**WEFAX / Weather Fax:** Decoding weather charts transmitted on HF

**CW:** Fldigi can decode (and send) Morse code, though dedicated CW operators typically prefer other methods

This breadth of mode support is one of Fldigi's greatest strengths. You can experiment with obscure modes, decode unusual signals you encounter on the bands, and try something new without installing additional software.

## Getting Started with Fldigi

### Installation

Fldigi is available from the Fldigi/W1HKJ website as pre-built packages for Windows, macOS, and Linux. On Linux, it is also available through most distribution package managers.

When you first launch Fldigi, a **configuration wizard** walks you through the essential settings:

### Operator settings

Enter your **callsign**, **name**, **QTH (location)**, and **grid locator**. These are used in macros and logging.

### Audio configuration

Select your sound card interface or USB audio device as the audio input (capture) and output (playback) device. If your radio has built-in USB audio, select the radio's audio device.

### Radio (CAT) control

Fldigi uses **Hamlib** (also called RigCAT or FLrig) for radio control. You can either:

- Configure **Hamlib** directly within Fldigi by selecting your radio model, COM port, and baud rate
- Use **FLrig** — a companion program by the same developer that handles radio control separately and communicates with Fldigi via a local network connection. FLrig is often easier to configure and provides a nice standalone radio control interface.

### PTT configuration

Select your PTT method: CAT (via Hamlib/FLrig), serial port RTS/DTR, or hardware VOX. CAT PTT through FLrig or Hamlib is recommended.

## Using Fldigi

### The waterfall

The waterfall is the heart of Fldigi's interface. It scrolls from top to bottom, showing signals as coloured traces. Different modes have distinctive visual signatures:

- **PSK31** signals appear as two thin parallel lines
- **RTTY** signals appear as two slightly wider spaced lines
- **Olivia** signals appear as a wide pattern of multiple tones
- **CW** signals appear as a single dashed line

Click on a signal in the waterfall to place your receive cursor on it. Fldigi will begin decoding whatever mode you have selected. If you're not sure what mode a signal is, Fldigi's **RSID (Reed-Solomon Identification)** feature can automatically identify many modes by detecting a special identification burst that some stations transmit at the beginning of their transmission.

### Macros

Fldigi includes a row of **macro buttons** along the top or bottom of the window. Macros are programmable message templates that insert your callsign, the other station's callsign, signal report, and other variables. Typical macros include:

- **CQ** — Call CQ with your callsign
- **ANS** — Answer a CQ
- **QSO** — Exchange information (signal report, name, QTH)
- **73** — Sign off

You can customise macros extensively using Fldigi's macro language, which supports variables like `<MYCALL>`, `<CALL>`, `<RST>`, `<NAME>`, and many others.

### Logging

Fldigi includes a built-in logging system that records contacts. It can also interface with external logging software (Log4OM, N3FJP, HRD, etc.) via network connections. When you complete a QSO and click the log button, Fldigi records the callsign, frequency, mode, signal reports, and other details.

## The Fldigi Suite

Fldigi is part of a suite of related programs by W1HKJ:

**FLrig** — Standalone radio control software. Many operators run FLrig alongside Fldigi for more flexible radio management.

**FLmsg** — A forms and message handling program designed for [emergency communications](/emergency-communications/overview). It creates structured forms (ICS-213, radiograms, etc.) that can be transmitted as compressed data bursts via Fldigi.

**FLamp** — File transfer software that sends files (images, documents, etc.) over Fldigi using ARQ (Automatic Repeat Request) for reliable delivery.

**FLnet** — Net control logging software for managing amateur radio nets.

Together, these programs form a powerful, free, open-source toolkit for digital communication, message handling, and net management.

## Fldigi for Emergency Communications

Fldigi and its companion programs (particularly FLmsg) are widely used in [emergency communications](/emergency-communications/overview). The combination provides:

- Reliable digital message passing via multiple robust modes (Olivia, MT63, or MFSK)
- Structured forms (ICS-213 and others) via FLmsg
- File transfer capability via FLamp
- All free and open-source, running on standard hardware

Many [ARES](/emergency-communications/ares) and [RACES](/emergency-communications/races) groups train on Fldigi as part of their digital communications capability.

## Where to Go Next

- [PSK31](/digital-modes/psk31) — The most popular mode used with Fldigi
- [RTTY](/digital-modes/rtty) — Another major Fldigi mode
- [Sound Card Interface](/digital-modes/sound-card-interface) — Connecting your radio
- [Digital Station Setup](/digital-modes/digital-station-setup) — Complete station setup guide
- [Emergency Communications Overview](/emergency-communications/overview) — Fldigi in emcomm
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
