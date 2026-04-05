---
title: RTTY
description: Radioteletype (RTTY) — one of the oldest digital modes, still popular for contesting and general HF operation
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, rtty, contesting, fsk
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# RTTY

**RTTY** (Radioteletype, pronounced "ritty") is one of the oldest digital modes in amateur radio, with roots going back to the 1930s when amateurs first connected surplus military Teletype machines to their radios. Despite its age, RTTY remains one of the most popular digital modes — especially in contesting, where its combination of speed, simplicity, and reliability has kept it relevant for decades.

## How RTTY Works

RTTY uses **frequency shift keying (FSK)** to encode text. The transmitter shifts between two audio frequencies — called **mark** and **space** — to represent binary 1s and 0s. The standard amateur RTTY parameters are:

- **Shift:** 170 Hz (the frequency difference between mark and space)
- **Baud rate:** 45.45 baud
- **Character set:** Baudot (ITA2), a 5-bit code supporting letters, numbers, and some punctuation

The Baudot code is simpler and older than ASCII. It uses 5 bits per character, giving only 32 possible codes. To accommodate letters, numbers, and punctuation, Baudot uses two "shift" states: **LTRS** (letters) and **FIGS** (figures/numbers). A shift character toggles between the two sets. This means RTTY supports uppercase letters only and has a limited set of punctuation — you won't be typing semicolons or curly braces.

At 45.45 baud, RTTY transmits at roughly **60 words per minute** — faster than typical CW operating and comparable to comfortable typing speed.

### AFSK vs FSK

There are two ways to generate the RTTY signal:

**True FSK** — The radio directly shifts its transmitter frequency between mark and space. This produces the cleanest signal and is preferred when the radio supports it. Many HF transceivers have a dedicated FSK or RTTY mode.

**AFSK (Audio Frequency Shift Keying)** — The computer generates two audio tones and feeds them into the radio's SSB audio input. The radio transmits these tones as-is within the SSB passband. AFSK is simpler to set up and works with any SSB radio, but the signal quality depends on proper audio levels. Most operators today use AFSK through a [sound card interface](/digital-modes/sound-card-interface).

Both methods produce a compatible signal — a station using FSK can communicate with one using AFSK without any issues.

## Setting Up for RTTY

### Software

Many programs support RTTY:

- **[Fldigi](/digital-modes/fldigi)** — Free, open-source, cross-platform. Excellent RTTY support.
- **MMTTY** — Free Windows software. A long-standing favourite for RTTY, widely used in contesting.
- **2Tone** — Free Windows software by G3YYD, designed for contest RTTY with excellent decoding.
- **N1MM Logger+** — Free contest logging software with built-in RTTY support (via MMTTY or 2Tone engine).
- **WriteLog** — Contest logging software with integrated RTTY.

For contesting, many operators use **N1MM Logger+** with the MMTTY or 2Tone decoding engine integrated directly, so logging and decoding happen in one application.

### Hardware

RTTY uses the same basic [digital station setup](/digital-modes/digital-station-setup) as other HF digital modes:

- HF transceiver (USB/AFSK mode, or dedicated FSK mode if available)
- Computer with sound card
- [Sound card interface](/digital-modes/sound-card-interface) or radio with built-in USB audio
- CAT control recommended

If your radio has a dedicated **RTTY or FSK mode**, using it with true FSK produces the cleanest signal. Otherwise, USB mode with AFSK works well.

### Important settings

**Do not use the radio's built-in RTTY filters for AFSK operation** — If you are using AFSK through the SSB input, keep the radio in USB mode with a normal SSB filter. The radio's built-in RTTY demodulator is a separate system from sound card decoding and the two should not be mixed.

**Audio levels** — As with all digital modes, avoid over-driving. ALC should read zero. RTTY is a constant-duty-cycle mode — the transmitter is at full power for the entire duration of the transmission, so ensure your radio can handle the thermal load. Many operators reduce power to 50–75% of the radio's rated SSB output for extended RTTY transmissions.

## Operating RTTY

### Common frequencies

RTTY activity is found in the digital segments of each band:

| Band | Typical activity (MHz) |
|------|----------------------|
| 80m | 3.580–3.600 |
| 40m | 7.025–7.045 (Region 1), 7.080–7.100 (Region 2/3) |
| 20m | 14.080–14.100 |
| 15m | 21.080–21.100 |
| 10m | 28.080–28.100 |

During contests, RTTY activity often spreads well beyond these ranges as the bands fill up.

### A typical RTTY contact

A casual RTTY QSO follows the same general pattern as other modes:

```
CQ CQ CQ DE W1ABC W1ABC W1ABC K

W1ABC DE G4XYZ G4XYZ K

G4XYZ DE W1ABC GA OM UR RST 599 599
NAME JOHN JOHN QTH BOSTON MA
HW CPY? G4XYZ DE W1ABC K

W1ABC DE G4XYZ TNX JOHN UR RST 599 599
NAME DAVID QTH LONDON
RIG ICOM 7300 100W DIPOLE
W1ABC DE G4XYZ K

G4XYZ DE W1ABC R FB DAVID TNX FER QSO
73 73 G4XYZ DE W1ABC SK

W1ABC DE G4XYZ 73 SK
```

Contest exchanges are much shorter — typically just a signal report and a serial number, state, or zone, depending on the contest rules.

### Contest RTTY

RTTY is one of the "big three" modes in HF contesting, alongside CW and SSB. Major RTTY contests include:

- **CQ WW RTTY DX Contest** — One of the largest RTTY contests globally. Held annually in September.
- **ARRL RTTY Roundup** — A popular ARRL contest (January). Now also includes FT8/FT4.
- **CQ WPX RTTY Contest** — Prefix-based multipliers, held in February.
- **BARTG RTTY contests** — Run by the British Amateur Radio Teledata Group.
- **Makrothen RTTY Contest** — Distance-based scoring.

Contest RTTY operating is fast and formulaic. Software macros handle the exchange, and the operator's job is to find stations, start the exchange, and confirm the log entry. Experienced contest operators can sustain rates of 100+ contacts per hour in good conditions.

> RTTY contesting is an excellent entry point into contesting for digital mode operators. The exchanges are short and standardised, and the software handles most of the work.
{.is-info}

## RTTY vs Other Digital Modes

Compared to [PSK31](/digital-modes/psk31), RTTY is wider (about 250 Hz vs 31 Hz) and less sensitive, but it is more robust in the presence of multipath fading and has a much longer contesting tradition. Compared to [FT8](/digital-modes/ft8), RTTY allows freeform text and has a more "human" feel, but it cannot decode signals anywhere near as weak.

RTTY's main niche today is **contesting** and **ragchewing by operators who enjoy the mode's character and history**. The distinctive warbling sound of RTTY on the bands is instantly recognisable and, for many operators, part of the charm.

## Where to Go Next

- [Fldigi](/digital-modes/fldigi) — Popular software for RTTY and other modes
- [PSK31](/digital-modes/psk31) — Another keyboard-to-keyboard mode
- [FT8](/digital-modes/ft8) — The most popular weak-signal mode
- [Contesting Overview](/contesting/overview) — Getting started with contests
- [Digital Station Setup](/digital-modes/digital-station-setup) — Full station setup guide
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
