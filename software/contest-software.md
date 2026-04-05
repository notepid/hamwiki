---
title: Contest Software
description: Specialised logging software for amateur radio contests — features, popular programs, and how to set up for contest operating
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, contesting, logging, cabrillo, n1mm
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Contest Software

Amateur radio [contesting](/contesting/overview) is a fast-paced activity where operators try to make as many contacts as possible within a defined time period. Every second counts, and a general-purpose logging program — however good it may be for day-to-day use — is not designed for the speed, accuracy, and specialised features that contest operating demands. Contest software (often called a "contest logger") is purpose-built for this environment.

## What Contest Software Does

A contest logger handles the unique requirements of on-air competition:

**Contest-specific exchange formats** — Each contest defines what information must be exchanged. It might be a signal report and a serial number, a signal report and a state or province, a signal report and a CQ zone, or any of dozens of other formats. Contest software knows the rules for hundreds of contests and prompts for the correct exchange fields.

**Real-time duplicate checking** — Working the same station on the same band and mode twice wastes time and may result in penalty points. Contest loggers check every callsign as you type and alert you instantly if the contact is a duplicate. They also show you which bands and modes you have already worked a given station on.

**Real-time scoring** — The logger calculates your score as you go, applying the correct multiplier and point rules for the active contest. You can see your running total, rate (contacts per hour), and multiplier count at a glance.

**Band map and DX cluster integration** — Contest loggers display a band map showing spotted stations and their frequencies. Clicking on a spot tunes your radio (via CAT control) to that station. The band map also shows which spots are new multipliers, already worked, or duplicates — colour-coded for quick identification.

**CW, voice, and digital keying** — Many contest loggers can send CW directly (via a serial port or Winkeyer), play recorded voice messages (via a sound card or external voice keyer), and control digital mode programs like WSJT-X or MMTTY. Function keys are mapped to common messages (CQ, exchange, acknowledgement), allowing single-keystroke operation.

**Multi-operator networking** — For multi-operator contest stations, contest loggers support networking multiple computers on a shared log. All operators see the same duplicate list and score in real time. Inter-station messaging (for band coordination and passing multipliers) is built in.

**Cabrillo log export** — After the contest, you submit your log to the contest sponsor. The standard format is Cabrillo, a plain-text file with a defined header and one line per contact. Contest loggers generate Cabrillo files automatically with the correct format for each contest.

## Key Features to Evaluate

### Contest database

The most important feature is how many contests the software supports out of the box. Major contest loggers include definitions for hundreds of contests — from the biggest international events like CQ WW and CQ WPX to regional and national contests around the world. Check that the contests you participate in are included, or that the software allows you to define custom contest templates.

### Supported modes

Most contesters operate CW, SSB, RTTY, and increasingly FT8/FT4. Verify that the logger supports the modes you use, including integration with external programs (MMTTY or fldigi for RTTY, WSJT-X for FT8/FT4).

### Rig control and antenna switching

Contest loggers typically support CAT control for multiple radios (for SO2R — single operator, two radios — operation), antenna switch control, and rotor control. If you plan to operate SO2R, verify that the logger handles dual-radio setups with independent bandmaps and audio switching.

### Super Check Partial (SCP)

SCP is a database of callsigns from past contest logs. As you type a partial callsign, the logger shows possible matches, helping you complete callsigns faster and with fewer errors. Most contest loggers include SCP and update the database before major contests.

### Call history

Call history files record the exchanges used by specific stations in previous years' contests. For example, if the contest exchange includes a state, and you have a call history file from last year, the logger can pre-fill the expected exchange when a familiar callsign appears. This speeds up logging and reduces errors.

### Operating statistics and rate display

A good contest logger shows your current rate (QSOs per hour), running score, multiplier progress, band-mode breakdown, and trend graphs. These help you make tactical decisions during the contest — such as when to switch bands or whether to focus on running or search-and-pounce.

## Popular Contest Software

| Program | Platforms | Licence | Notable features |
|---------|-----------|---------|-----------------|
| N1MM Logger+ | Windows | Free | Most widely used contest logger worldwide; supports 200+ contests; SO2R; CW, SSB, digital; extensive networking |
| Win-Test | Windows | Commercial | Popular in Europe; strong multi-op support; fast and efficient interface |
| WriteLog | Windows | Commercial | Long-standing program with strong RTTY and SO2R support |
| SkookumLogger | macOS | Free | Native Mac contest logger; supports major contests; clean interface |
| TLF | Linux | Free (open source) | Console-based (text interface) contest logger for Linux; lightweight and fast |
| TR4W | Windows | Free | Lightweight, fast logger based on the classic TR Log |
| DXLog | Windows | Free | Developed by experienced European contesters; strong multi-op features |

> **Tip:** If you are just getting started with contesting and run Windows, N1MM Logger+ is a strong default choice — it is free, widely supported, well-documented, and handles nearly every contest you will encounter. Whatever you choose, practice with the software before the contest starts.
{.is-info}

## Setting Up for a Contest

### Before the contest

**Install and configure** — Install the contest logger well in advance. Configure your radio(s) for CAT control, set up your audio routing for CW and voice keying, and verify that everything works by making a few test contacts.

**Select the contest** — Open the correct contest definition in the logger. This sets up the exchange fields, scoring rules, multiplier definitions, and Cabrillo format.

**Update databases** — Download the latest Super Check Partial file and country/prefix database (CTY.DAT or similar). These are usually available from community websites shortly before major contests.

**Set up function key messages** — Program your CW, voice, and/or digital messages into the function keys. A typical set includes: F1 = CQ, F2 = exchange, F3 = thank you / QRZ, F4 = your callsign. Practise the flow until it is second nature.

**Configure networking** — For multi-operator entries, set up the network between all logging computers and verify that all machines see the shared log.

### During the contest

**Log as you go** — Enter each contact immediately. Contest loggers are designed for speed — you typically press Enter to log the contact and the logger automatically advances to the next entry field.

**Use the band map** — Watch for spotted multipliers. Click on a spot to tune your radio and check if it is a new multiplier worth calling.

**Monitor your rate** — The rate display tells you whether your current strategy is working. If your rate drops, consider switching bands or changing between running (calling CQ) and search-and-pounce.

### After the contest

**Review your log** — Use the logger's log checking features to scan for obvious errors: invalid callsigns, missing exchanges, or suspicious duplicates.

**Generate the Cabrillo file** — Export your log in Cabrillo format. Double-check the header information (your callsign, category, power level, and so on) before submitting.

**Submit on time** — Most contests require log submission within a few days to a few weeks. Submit promptly to avoid disqualification.

**Export to your main log** — If you keep a separate general-purpose log, export the contest contacts in ADIF format and import them into your [logging software](/software/logging-software).

## Contest Software and Digital Modes

FT8 and FT4 have become significant contest modes, and most major contest loggers now support integration with WSJT-X. The typical setup has WSJT-X handling the encoding and decoding while the contest logger handles logging, duplicate checking, and scoring. Contacts flow from WSJT-X to the contest logger automatically.

For RTTY contests, the integration between contest loggers and MMTTY or fldigi is mature and well-tested. N1MM Logger+ and Win-Test both support running MMTTY or the Two Tone RTTY engine as an embedded decoder window within the contest logger.

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [Contesting Overview](/contesting/overview) — Introduction to amateur radio contests
- [Your First Contest](/contesting/your-first-contest) — Getting started with contesting
- [Major Contests](/contesting/major-contests) — The big events on the contest calendar
- [Logging Software](/software/logging-software) — General-purpose station logging
- [Digital Mode Software](/software/digital-mode-software) — Programs for FT8, RTTY, and more
- [CW Training Software](/software/cw-training-software) — Learning and improving Morse code
