---
title: PSK31
description: Phase Shift Keying 31 — a popular keyboard-to-keyboard digital mode for HF ragchewing
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, psk31, keyboard
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# PSK31

**PSK31** (Phase Shift Keying, 31.25 baud) is a keyboard-to-keyboard digital mode designed by Peter Martinez (G3PLX) and released in 1998. It was one of the first sound card digital modes to gain widespread popularity, and it demonstrated that a computer's sound card connected to a radio was all the hardware needed for digital communication. PSK31 occupies an astonishingly narrow bandwidth of just 31 Hz — you could fit roughly 80 PSK31 signals in the space of a single SSB voice channel — making it efficient, effective at low power, and a natural fit for crowded HF bands.

## How PSK31 Works

PSK31 uses **binary phase shift keying (BPSK)** to encode text characters. The transmitter generates an audio tone (typically around 1,000 Hz) and shifts its phase by 180° to encode data. At the receiving end, the software detects these phase shifts and converts them back to text.

The **31.25 baud** rate was chosen to match comfortable typing speed. At roughly 50 words per minute, PSK31 transmits about as fast as most people can type — fast enough for a comfortable conversation but slow enough to keep the bandwidth extremely narrow.

### Varicode encoding

PSK31 uses a variable-length encoding scheme called **Varicode**, where common characters (like "e" and space) use fewer bits than rare characters (like "Z" or punctuation). This is similar in concept to Morse code, where common letters are shorter. The result is efficient encoding that matches real-world text patterns.

### BPSK vs QPSK

PSK31 comes in two variants:

**BPSK31** — The standard mode. Simple, robust, and the most commonly used. No error correction, but the narrow bandwidth and signal processing provide good performance.

**QPSK31** — Quadrature Phase Shift Keying. Uses four phase states instead of two, allowing forward error correction (FEC) at the same baud rate. QPSK31 is more robust in noisy conditions but is less commonly used in practice, partly because BPSK31 is already very effective and partly because the FEC adds overhead.

Most operators use BPSK31 for general use. You will sometimes see "PSK31" and "BPSK31" used interchangeably.

## What Makes PSK31 Special

**Extremely narrow bandwidth** — At 31 Hz wide, PSK31 is one of the narrowest modes in amateur radio. This means minimal interference with other stations and excellent spectral efficiency.

**Conversational** — Unlike structured modes like [FT8](/digital-modes/ft8), PSK31 allows freeform typing. You can have extended conversations (ragchews), exchange detailed information, discuss equipment, antennas, weather — anything you would talk about in a voice QSO. This makes it the closest digital equivalent to a phone conversation.

**Low power effectiveness** — The narrow bandwidth concentrates all transmitted energy into a tiny slice of spectrum, giving PSK31 excellent signal-to-noise performance. Many operators work PSK31 with 5–25 watts and make contacts across continents.

**Simple equipment** — Any SSB transceiver, a computer, a [sound card interface](/digital-modes/sound-card-interface), and free software. No specialised modem or TNC required.

## Setting Up for PSK31

### Software

Several programs support PSK31:

- **[Fldigi](/digital-modes/fldigi)** — Free, open-source, cross-platform. The most popular choice for PSK31 and other keyboard-to-keyboard modes.
- **DigiPan** — Free Windows software specifically designed for PSK31. Features a wide "panadapter" waterfall view.
- **MixW** — Shareware multi-mode software for Windows.
- **HRD Digital Master** — Part of the Ham Radio Deluxe suite.

### Hardware

The same [digital station setup](/digital-modes/digital-station-setup) used for other HF digital modes works for PSK31:

- HF transceiver set to **USB** mode (or LSB on some bands by convention, though USB is standard for digital modes)
- Computer with sound card
- [Sound card interface](/digital-modes/sound-card-interface) or radio with built-in USB audio codec
- CAT control recommended for frequency management

### Audio levels

Proper audio levels are important for a clean PSK31 signal. The transmitted signal should produce **no ALC activity** on the radio's meter. PSK31 is a constant-carrier mode — any distortion from over-driving creates unwanted sidebands (splatter) that interfere with adjacent stations. This is even more critical than with FT8 because PSK31 signals are spaced very closely together on the waterfall.

A good practice is to set your radio to its lowest power setting, adjust the audio drive from the computer so the radio produces some output, and then increase radio power to the desired level. ALC should read zero or near-zero at all times.

## Operating PSK31

### Common frequencies

PSK31 activity centres on established frequencies within each band:

| Band | Typical centre frequency (MHz) |
|------|-------------------------------|
| 80m | 3.580 |
| 40m | 7.070 |
| 30m | 10.142 |
| 20m | 14.070 |
| 17m | 18.100 |
| 15m | 21.070 |
| 12m | 24.920 |
| 10m | 28.120 |

Activity is usually spread across a few kHz around these centre frequencies. The waterfall display in your software shows all the active signals and lets you click on any one to tune in.

### Making a contact

1. **Set your radio** to the appropriate USB dial frequency.
2. **Watch the waterfall** — PSK31 signals appear as two narrow parallel lines (for BPSK) in the waterfall display.
3. **Click on a signal** — Position your receive cursor on a signal to decode it. You will see the decoded text scroll across your screen.
4. **Call CQ** — Type a CQ message, or use your software's CQ macro. A typical CQ looks like: `CQ CQ CQ DE W1ABC W1ABC W1ABC K`
5. **Respond to a CQ** — Click on a station calling CQ, then use your software's reply macro or type a response manually.
6. **Have a conversation** — Exchange signal reports, names, locations, equipment information, and whatever else you like. There is no rigid format — just type naturally.
7. **Sign off** — End with `73 SK` or similar.

### A typical PSK31 QSO

```
CQ CQ CQ DE W1ABC W1ABC K

W1ABC DE G4XYZ G4XYZ K

G4XYZ DE W1ABC TNX FER CALL OM
UR RST 599 599 NAME IS JOHN QTH BOSTON MA
HW CPY? G4XYZ DE W1ABC K

W1ABC DE G4XYZ GM JOHN TNX FER RPT
UR RST 599 599 NAME IS DAVID QTH LONDON
RIG IS ICOM 7300 50W DIPOLE ANT
W1ABC DE G4XYZ K

G4XYZ DE W1ABC R FB DAVID
NICE SIG INTO BOSTON. MY RIG IS YAESU FTDX10
RUNNING 30W INTO AN END FED WIRE
TNX QSO 73 73 G4XYZ DE W1ABC SK

W1ABC DE G4XYZ R TNX FER QSO JOHN
VY 73 AND HPE CUAGN. G4XYZ SK
```

Unlike FT8, there is no time limit per transmission — you type and transmit at your own pace, and the other station does the same.

### Operating tips

**Don't over-power** — PSK31 is effective at low power. 20–50 watts is plenty for most HF contacts. Running more power than necessary creates wide splatter that covers adjacent signals.

**Use macros wisely** — Most PSK31 software includes programmable macros for CQ calls, exchanges, and sign-offs. These speed up the repetitive parts of a QSO while still allowing freeform typing for the conversation.

**Be patient with decoding** — PSK31 does not have error correction (in BPSK mode). Fading and interference will cause garbled text. Wait for the signal to come back rather than asking for endless repeats — you will usually get the gist from context.

**Tune carefully** — PSK31 requires precise tuning. Most software has an AFC (automatic frequency control) feature that fine-tunes to the signal. Make sure it is enabled.

## PSK31 vs Other Modes

Compared to [FT8](/digital-modes/ft8), PSK31 offers freeform conversation but requires stronger signals and more operator involvement. Compared to [RTTY](/digital-modes/rtty), PSK31 is narrower and more sensitive, but RTTY has a longer history in contesting. Compared to [JS8Call](/digital-modes/js8call), PSK31 is simpler and has a lower learning curve, but JS8Call offers store-and-forward messaging and better weak-signal performance.

PSK31 is an excellent mode if you enjoy the social side of amateur radio and want typed conversations without the constraints of structured modes. It remains widely used on all HF bands, particularly 20 metres.

## Where to Go Next

- [Fldigi](/digital-modes/fldigi) — The most popular software for PSK31
- [RTTY](/digital-modes/rtty) — Another classic keyboard-to-keyboard mode
- [JS8Call](/digital-modes/js8call) — Weak-signal keyboard-to-keyboard messaging
- [Sound Card Interface](/digital-modes/sound-card-interface) — Connecting radio and computer
- [Digital Station Setup](/digital-modes/digital-station-setup) — Full setup guide
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
