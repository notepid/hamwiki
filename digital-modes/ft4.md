---
title: FT4
description: The FT4 digital mode — a faster variant of FT8 designed for contesting and rapid exchanges
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, ft4, wsjt-x, weak-signal, contesting
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# FT4

**FT4** is a digital mode developed by Steve Franke (K9AN) and Joe Taylor (K1JT) as a companion to [FT8](/digital-modes/ft8), released in 2019 as part of WSJT-X. Where FT8 was designed primarily for making contacts under difficult propagation, FT4 is optimised for **speed** — its 7.5-second transmit/receive cycles are twice as fast as FT8, making it better suited for contesting and rapid exchanges when conditions are reasonably good.

## How FT4 Differs from FT8

FT4 and FT8 share the same underlying philosophy — structured, automated exchanges with strong error correction — but differ in several key parameters:

| Parameter | FT8 | FT4 |
|-----------|-----|-----|
| Transmit period | 15 seconds | 7.5 seconds |
| Message duration | 12.64 seconds | 6.32 seconds |
| Modulation | 8-GFSK | 4-GFSK |
| Number of tones | 8 | 4 |
| Bandwidth | ~50 Hz | ~80 Hz |
| Minimum SNR for decode | −24 dB | −17.5 dB |
| Message payload | 77 bits | 77 bits |

The key trade-off is clear: FT4 gains speed at the cost of sensitivity. It requires signals to be about 6.5 dB stronger than FT8 for reliable decoding. In practice, this means FT4 works best when conditions are moderate to good — exactly the conditions where you want to move faster through contacts.

Both modes carry the same **77-bit message payload**, so the information in each transmission is identical. The exchange sequence is the same as FT8.

## When to Use FT4 vs FT8

**Use FT4 when:**
- Band conditions are good and signals are reasonably strong
- You are contesting and want to maximise contact rate
- Participating in events that support or require FT4 (e.g., the World Wide Digi DX Contest)
- You want faster exchanges on bands with good propagation

**Use FT8 when:**
- Conditions are poor, marginal, or you are running very low power
- You need maximum sensitivity for DX or weak-signal work
- Working bands where propagation is uncertain

Many operators switch between FT8 and FT4 depending on conditions and activity on each frequency.

## Setting Up for FT4

FT4 uses the same software and hardware as FT8. In WSJT-X, simply select **FT4** from the mode menu. The software handles all the timing and protocol differences automatically.

The same requirements for accurate time synchronisation apply — your clock must be within ±1 second of UTC. Because FT4's periods are shorter, timing errors are proportionally more impactful.

### Common FT4 frequencies

FT4 has its own standard dial frequencies, separate from FT8:

| Band | Dial frequency (MHz) |
|------|---------------------|
| 80m | 3.575 |
| 40m | 7.047.5 |
| 30m | 10.140 |
| 20m | 14.080 |
| 17m | 18.104 |
| 15m | 21.140 |
| 12m | 24.919 |
| 10m | 28.180 |
| 6m | 50.318 |

> Note: Some FT4 frequencies vary by region and may shift over time as usage patterns develop. Check current band plans for your region.
{.is-info}

## FT4 in Contesting

FT4 was specifically designed with contesting in mind. The 7.5-second periods allow a complete contact in about 45 seconds — roughly half the time of an FT8 contact. WSJT-X includes contest-specific message types for events like:

- **ARRL Field Day** — Exchange includes class and section (e.g., "2A ENY")
- **ARRL RTTY Roundup** — Exchange includes state/province or serial number
- **World Wide Digi DX Contest (WW Digi)** — One of the first major contests designed from the ground up for FT4 and FT8

Contest mode is enabled through the WSJT-X settings. When active, the software adjusts message formats to include the required contest exchange instead of the standard grid locator.

## Operating Tips

**Monitor both FT4 and FT8** — Some operators run two instances of WSJT-X (one for each mode) when their station setup allows, or switch between them based on where the activity is. During contests that support both modes, activity may be split.

**Power and audio levels** — The same advice applies as for FT8. Keep your ALC at zero, use only enough power for the conditions, and avoid overdriving.

**Wider bandwidth awareness** — FT4 signals are about 80 Hz wide (vs 50 Hz for FT8), so the waterfall will look slightly different. Ensure you are not transmitting on top of other signals.

## Where to Go Next

- [FT8](/digital-modes/ft8) — The companion mode for weak-signal work
- [Contesting Overview](/contesting/overview) — Getting into amateur radio contests
- [RTTY](/digital-modes/rtty) — Another popular digital contest mode
- [Digital Station Setup](/digital-modes/digital-station-setup) — Station configuration for digital modes
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
