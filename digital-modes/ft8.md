---
title: FT8
description: The FT8 weak-signal digital mode — setup, operation, and tips for the most popular digital mode in amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, ft8, wsjt-x, weak-signal
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# FT8

**FT8** (Franke–Taylor design, 8-FSK modulation) is a weak-signal digital mode created by Steve Franke (K9AN) and Joe Taylor (K1JT). Released in 2017 as part of the WSJT-X software suite, FT8 quickly became the most widely used digital mode in amateur radio — and arguably the most-used mode on HF overall. Its ability to decode signals buried deep in the noise, combined with a structured and largely automated exchange, makes it possible to make confirmed contacts with very low power, compromise antennas, and marginal propagation.

## How FT8 Works

FT8 uses **8-tone Gaussian frequency shift keying** (8-GFSK). Each transmission occupies approximately 50 Hz of bandwidth and lasts exactly **12.64 seconds**, fitting neatly within a 15-second time slot. Stations take turns transmitting in alternating 15-second slots synchronised to UTC — one group transmits from 0 to 15 seconds, the other from 15 to 30 seconds, and so on.

Each FT8 message is compressed into **77 bits** of payload, protected by a low-density parity-check (LDPC) error-correcting code, producing a total of 174 channel symbols. This heavy error correction is what allows FT8 to decode signals down to approximately **−24 dB signal-to-noise ratio** (measured in a 2500 Hz reference bandwidth) — meaning the signal can be more than 200 times weaker than the background noise and still be decoded perfectly.

A standard FT8 exchange consists of a sequence of structured messages:

```
CQ W1ABC FN42          ← Station 1 calls CQ with grid square
W1ABC G4XYZ IO91       ← Station 2 responds with their grid
G4XYZ W1ABC -12        ← Station 1 sends signal report
W1ABC G4XYZ R-15       ← Station 2 confirms and sends their report
G4XYZ W1ABC RRR        ← Station 1 confirms receipt
W1ABC G4XYZ 73         ← Station 2 says goodbye
```

The entire contact takes about 90 seconds — six transmissions of 15 seconds each. WSJT-X automates much of this sequence; once you double-click on a calling station, the software handles the exchange with minimal intervention.

### What FT8 doesn't do

FT8 is not a conversational mode. You cannot type freeform messages or ragchew. Each message is limited to a fixed set of structured formats (CQ calls, signal reports, grid squares, and a handful of other message types). If you want keyboard-to-keyboard weak-signal conversation, consider [JS8Call](/digital-modes/js8call).

## Setting Up for FT8

### Equipment needed

- An HF transceiver capable of SSB operation (USB on most bands; LSB on 160m by convention in some regions, but USB is standard for WSJT-X)
- A computer running WSJT-X (available free for Windows, macOS, and Linux)
- A [sound card interface](/digital-modes/sound-card-interface) connecting the radio's audio to the computer, or a modern radio with built-in USB audio (Icom IC-7300, Yaesu FT-991A, Elecraft KX3, and many others)
- CAT (Computer Aided Transceiver) control is highly recommended for automatic frequency and PTT management
- An accurate clock — FT8 requires your computer's clock to be accurate within **±1 second** of UTC. Use internet time synchronisation (NTP) or a GPS-disciplined clock.

### WSJT-X configuration

After installing WSJT-X, you need to configure a few things:

**Station details** — Enter your callsign and 4-character Maidenhead grid locator (e.g., FN42, IO91, QF56). You can find your grid square from your latitude and longitude using online tools.

**Audio** — Select your sound card interface or USB audio device as both the input and output audio device.

**Radio** — Configure the CAT connection to your transceiver. WSJT-X supports most radios through Hamlib or manufacturer-specific protocols. Select your radio model, COM port (or network address), and baud rate.

**PTT** — Choose how WSJT-X will key the transmitter: via CAT command, a serial port RTS/DTR line, or VOX (not recommended due to timing delays).

### Power level

FT8's sensitivity means you do not need high power. Many operators run **20–50 watts** and make contacts worldwide. QRP operators regularly make DX contacts with 5 watts or less. Start with low power and increase only if needed — this is both good practice and good etiquette, since FT8 segments can be crowded.

> **Important:** Set your radio to the correct power level and **do not overdrive the audio**. The ALC meter on your radio should show little or no ALC activity during transmission. Overdriving produces splatter that interferes with adjacent signals.
{.is-info}

## Operating FT8

### Common frequencies

FT8 activity is concentrated on standard frequencies within each band. These are the dial frequencies (USB carrier):

| Band | Dial frequency (MHz) |
|------|---------------------|
| 160m | 1.840 |
| 80m | 3.573 |
| 60m | 5.357 |
| 40m | 7.074 |
| 30m | 10.136 |
| 20m | 14.074 |
| 17m | 18.100 |
| 15m | 21.074 |
| 12m | 24.915 |
| 10m | 28.074 |
| 6m | 50.313 |
| 2m | 144.174 |

### Making a contact

1. **Set your radio** to the correct dial frequency in USB mode. WSJT-X will handle audio frequencies within the passband.
2. **Watch the waterfall** — You will see dozens of signals appearing as horizontal traces in the waterfall display. Each trace is a station transmitting.
3. **Decode** — At the end of each 15-second period, WSJT-X decodes all the signals it can detect and displays the results in the main window.
4. **Call CQ** — Click "Enable Tx" and then "CQ" to begin calling. WSJT-X will transmit your CQ message at your chosen audio frequency.
5. **Respond to a CQ** — Double-click on a decoded CQ message to begin a contact. WSJT-X queues up the correct response and starts transmitting on the next appropriate time slot.
6. **Let the software work** — WSJT-X handles the exchange sequence automatically. Watch the messages to track progress. The contact is complete when 73 messages are exchanged.
7. **Log the contact** — When the QSO completes, WSJT-X pops up a logging prompt.

### Tips for successful FT8 operating

**Time accuracy is critical** — If your clock is off by more than about 2 seconds, you will struggle to decode signals and other stations will struggle to decode you. Check your clock synchronisation regularly.

**Choose your transmit frequency carefully** — Look at the waterfall for an open spot before transmitting. Avoid transmitting on top of other stations. The WSJT-X waterfall makes this easy to see.

**Use the right even/odd slot** — When answering a CQ, WSJT-X automatically selects the correct time slot. When calling CQ, you can choose either. By convention, your transmit slot should be opposite to the station you are trying to work.

**Be patient** — Propagation can be fleeting. If you are calling CQ and getting no responses, conditions may not support the path. Try a different band.

**Watch the DX spots** — The PSK Reporter website (pskreporter.info) shows where your signal is being decoded worldwide, and where you are decoding stations from. It is an invaluable tool for understanding real-time propagation.

## FT8 and Contesting

FT8 has become a significant force in award chasing and DX, though some contests now include FT8/FT4 categories. The [FT4](/digital-modes/ft4) mode was specifically designed for faster contest-style exchanges. WSJT-X includes contest-specific modes for events like the ARRL Field Day, the ARRL RTTY Roundup (which now includes FT8/FT4), and World Wide Digi DX Contest.

## FT8 Fox/Hound Mode

For major DXpeditions, WSJT-X includes a special operating mode called **Fox/Hound**. The DXpedition station (Fox) can work multiple stations (Hounds) simultaneously, dramatically increasing contact rates. Fox/Hound mode uses different message sequencing and timing, and Hound stations need to enable a specific setting in WSJT-X to participate. Listen for DXpedition announcements about whether they are using Fox/Hound mode.

## Reception Reports and PSK Reporter

One of the great tools for FT8 operators is **PSK Reporter** (pskreporter.info). When you decode FT8 signals, WSJT-X can automatically upload those reception reports to PSK Reporter. This creates a real-time global map of propagation. You can search for your own callsign to see who is hearing you, or look at band activity maps to decide where propagation is open.

## Common Issues

**No decodes** — Check your clock accuracy first, then verify audio levels. The input audio should register in WSJT-X's audio level meter at around 30–50 dB (shown in the lower left corner).

**Other stations don't respond** — Verify your transmit audio is clean (no ALC) and your power is adequate for the band conditions and distance.

**Delayed decodes** — If decodes appear several seconds into the next period, your computer may be too slow for real-time decoding. Close other applications, or consider a faster machine.

## Where to Go Next

- [FT4](/digital-modes/ft4) — The faster variant designed for contesting
- [JS8Call](/digital-modes/js8call) — Keyboard-to-keyboard messaging built on FT8 technology
- [Digital Station Setup](/digital-modes/digital-station-setup) — How to configure your station
- [Sound Card Interface](/digital-modes/sound-card-interface) — Connecting radio and computer
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
- [HF Operating](/operating/hf-operating) — General HF operating practices
