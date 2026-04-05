---
title: Contest Logging
description: An overview of contest logging software, Cabrillo log format, and best practices for accurate contest record-keeping
published: true
date: 2026-04-05T09:30:00.000Z
tags: contesting, logging, software
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Contest Logging

Logging is the backbone of contesting. Your logging software is not just a record-keeper — it is your real-time scoring engine, duplicate checker, multiplier tracker, and the tool that produces the electronic log you submit after the event. Choosing the right software and knowing how to use it effectively will improve your contest experience immediately.

This page covers the major contest logging programs, the Cabrillo log format, and best practices for accurate, efficient logging.

## Why Contest Logging Software Matters

You might wonder why you cannot simply use a general-purpose [station logger](/operating/logging) for contests. Technically you can, but dedicated contest logging software provides features that make a significant difference during the event:

**Real-time duplicate checking.** The software instantly tells you whether you have already worked a station on the current band and mode, saving you from wasting time on a contact that will not count.

**Automatic scoring.** Your score updates with every contact, showing QSO points, multipliers, and total score. This lets you make informed strategic decisions throughout the contest.

**Exchange validation.** The software knows what exchange the contest requires and flags entries that look wrong — an invalid zone number, a state abbreviation that does not exist, or a serial number out of sequence.

**Band map and cluster integration.** In the assisted category, your logging software can display DX cluster spots and CW skimmer data on a bandmap, showing you exactly where stations are and which ones you still need.

**Cabrillo export.** After the contest, you export your log in Cabrillo format — the standard electronic format accepted by virtually all contest sponsors. General loggers often lack this capability.

**Rate displays.** Logging software tracks your contact rate over time, which helps you evaluate your strategy and identify your most productive operating periods.

## Major Contest Logging Programs

Several well-established programs dominate the contest logging landscape. All of them are capable and well-supported — the best choice depends on your operating system, personal preference, and the features you value most.

### N1MM Logger+

N1MM Logger+ is the most widely used contest logging program in the world. It is free, open-source, and runs on Windows.

**Key features:** supports virtually every contest, highly configurable, SO2R support, networked multi-operator capability, integrated voice and CW keyer, extensive bandmap and cluster support, active development community.

**Best for:** operators who want maximum flexibility and are comfortable with a feature-rich interface. N1MM is the standard against which other loggers are measured.

### Win-Test

Win-Test is a high-performance contest logger popular with serious competitors and multi-operator stations, particularly in Europe. It was originally a commercial product and is now freely available.

**Key features:** fast and lightweight, excellent multi-operator support, advanced SO2R features, built-in voice keyer, sophisticated scoring engine.

**Best for:** experienced contesters and multi-operator teams who value speed and reliability above all else.

### WriteLog

WriteLog is a long-established Windows-based contest logger with a loyal user base. It offers a clean interface and solid feature set.

**Key features:** easy to learn, good SO2R support, integrated voice keyer, supports most major contests, sound card interface for digital modes.

**Best for:** operators who prefer a straightforward interface and are primarily interested in phone and CW contests.

### SkookumLogger

SkookumLogger is the leading contest logger for macOS. If you use a Mac, this is your primary option.

**Key features:** native macOS application, clean interface, supports most major contests, CAT control, CW keyer, Cabrillo export.

**Best for:** Mac users who want a native contest logging experience without running Windows.

### TR4W

TR4W (TR for Windows) is a free, lightweight contest logger inspired by the classic DOS-era TR Log. It has a minimalist interface that some operators prefer for its simplicity and speed.

**Key features:** very fast, low resource requirements, keyboard-driven interface, supports major contests, free.

**Best for:** operators who prefer a no-frills, keyboard-centric workflow.

### TLF

TLF is a free, open-source contest logger for Linux, designed for console (text-mode) operation. It runs in a terminal and is fully keyboard-driven.

**Key features:** Linux-native, very fast, works over SSH, CW keyer support, Cabrillo export, active development.

**Best for:** Linux users and operators who want a lightweight, terminal-based logger.

## Setting Up Your Logger

Regardless of which software you choose, the setup process before a contest follows the same general pattern:

1. **Select the contest.** Open the contest module for the specific event you are entering. This loads the correct exchange format, scoring rules, and multiplier definitions.

2. **Enter your station information.** Your callsign, entry category, power level, and ARRL section or CQ Zone (as applicable). This information goes into the Cabrillo header.

3. **Configure radio control.** Connect your radio via CAT (USB or serial) so the software can read and set frequencies automatically. Test the connection to ensure the software correctly tracks band changes.

4. **Set up function keys.** Assign your CQ message, exchange, and common responses to function keys. On CW, the software sends these via the radio's keying input. On phone, configure a voice keyer or sound card interface.

5. **Configure networking (multi-op).** If you are operating with a team, set up the network so all computers share a single log. Test this before the contest starts.

6. **Synchronise your clock.** Contest log times must be accurate. Use the software's built-in time sync feature to synchronise with an internet time server. Most logging programs do this automatically if you have an internet connection.

7. **Run a practice session.** Log a few test contacts to make sure everything works — radio control, function keys, exchange entry, and duplicate checking. Delete the test entries before the contest begins.

## The Cabrillo Format

**Cabrillo** is the standard electronic log format for contest submissions. It is a plain-text format that all contest logging software can export. A Cabrillo file contains:

- **A header section** with your callsign, contest name, entry category, power level, location, and other administrative details.
- **QSO records** — one line per contact, with the date, time, frequency, mode, callsigns, and exchange sent and received.

You do not need to edit Cabrillo files by hand — your logging software generates them automatically. But understanding the format helps you spot problems if a submission is rejected:

```
START-OF-LOG: 3.0
CALLSIGN: N0CALL
CONTEST: CQ-WW-SSB
CATEGORY-OPERATOR: SINGLE-OP
CATEGORY-BAND: ALL
CATEGORY-POWER: HIGH
CATEGORY-ASSISTED: NON-ASSISTED
CLAIMED-SCORE: 1234567
CLUB:
LOCATION: WMA
NAME: Your Name
QSO: 14200 PH 2025-10-25 0001 N0CALL        59  05     G4XYZ         59  14
QSO: 21300 PH 2025-10-25 0003 N0CALL        59  05     JA1ABC        59  25
END-OF-LOG:
```

Each QSO line follows a fixed column format. The fields are: frequency (in kHz), mode, date, time (UTC), your callsign, your exchange, the other station's callsign, and their exchange.

## Best Practices for Contest Logging

### Accuracy matters
Contest logs are cross-checked against each other during adjudication. If your log says you worked G4XYZ at 0001 UTC, the contest committee checks G4XYZ's log to see if they have a corresponding contact with you. Errors hurt both stations:

- **Callsign errors** are the most common and most costly mistake. If you log the callsign wrong, neither station gets credit for the contact, and you may receive a penalty.
- **Exchange errors** (wrong zone, wrong state, wrong serial number) also result in lost credit.
- **Time errors** cause problems if your clock is significantly off, making it hard to match your contacts with those in other logs.

### Enter callsigns carefully
If you are not sure you copied the callsign correctly, ask for a repeat. A moment spent confirming is far better than a penalty during log checking. Most logging software highlights unusual callsigns or warns you if a call does not match expected patterns.

### Use the check partial and super check partial features
Most contest loggers include a **check partial** function that shows possible callsign matches as you type. This helps you recognise partially copied calls and reduces errors. The **super check partial** database draws on historical contest logs to show likely calls — if you type "G4X," it might suggest G4XYZ based on that station's participation in past events.

### Log everything in real time
Enter contacts as you make them, not after the fact. Logging from memory or from paper notes after the contest introduces errors and makes it impossible to have accurate times.

### Review your log before submitting
After the contest, take a few minutes to scroll through your log and look for obvious problems: callsigns with unusual characters, exchanges that look wrong, or gaps in time that do not make sense. Most logging software includes a log-checking utility that flags potential issues.

## Submitting Your Log

The submission process varies by contest but follows a common pattern:

1. **Export to Cabrillo** from your logging software.
2. **Visit the contest sponsor's website** and find the log submission page.
3. **Upload your Cabrillo file.** Some contests also accept email submissions.
4. **Save the confirmation.** Most sponsors send an email acknowledging receipt.

**Always submit your log**, even if you only made a few contacts. Checklogs (logs submitted by operators who are not competing for a score) help the contest committee verify other operators' contacts. You can explicitly mark your log as a checklog if you prefer.

**Submission deadlines** vary from five days to thirty days after the contest. Check the rules — late logs are usually not accepted.

## Beyond the Basics

### Post-contest analysis
After the results are published (often months later), many contests provide detailed log-checking reports showing which of your contacts were confirmed, which were not found in other logs (NIL — "not in log"), and which had errors. Studying these reports helps you identify weaknesses in your operating — for example, if you have a high NIL rate, you may be logging callsigns inaccurately.

### Log archives and historical data
Many contest logging programs maintain databases of your past contests. Over time, this data lets you track your progress, compare scores year over year, and set informed goals for future events. Some operators keep a separate general [station log](/operating/logging) and import contest contacts into it after each event.

## Where to Go Next

- [Contesting Techniques](/contesting/contesting-techniques) — Strategies for improving your score
- [Contest Station Setup](/contesting/contest-station-setup) — Hardware for effective contesting
- [Getting Started with Contesting](/contesting/getting-started-contesting) — Entering your first contest
- [Major Contests](/contesting/major-contests) — The big events on the calendar
- [Logging](/operating/logging) — General station logging (non-contest)
- [Software Overview](/software/overview) — Other amateur radio software
