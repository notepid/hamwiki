---
title: Logging Contacts
description: Keeping a log of your amateur radio contacts — why, how, and what software to use
published: true
date: 2026-04-05T09:30:00.000Z
tags: operating, logging
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Logging Contacts

A **log** is a record of your amateur radio contacts. Logging has been part of amateur radio since its earliest days, and while regulations around mandatory logging have relaxed in many countries, keeping a log remains one of the most valuable habits an operator can develop.

## Why Keep a Log?

**Regulatory requirements** — In some countries, maintaining a station log is still a legal requirement. Even where it is not mandatory, having a log available demonstrates good operating practice and is useful if questions about interference or band usage arise.

**Awards and contests** — All [award programs](/awards/overview) and [contests](/contesting/overview) require log submissions. You need an accurate log to claim awards like [DXCC](/awards/dxcc), [WAS](/awards/was), and [POTA](/awards/pota), and to submit scores for contests.

**QSL management** — A log is essential for managing incoming and outgoing [QSL cards](/operating/qsl-cards) and electronic confirmations. Without a log, you cannot verify whether a reported contact actually took place.

**Personal record** — Your log is a diary of your amateur radio journey. Looking back through years of logs, you can see your progress, remember memorable contacts, and track your station's growth.

**Station analysis** — Logs help you understand your station's performance. You can analyse which bands and times produce the most contacts, track how propagation changes with the solar cycle, and measure the effect of antenna improvements.

## What to Log

At minimum, each contact entry should record:

| Field | Description | Example |
|-------|-------------|---------|
| **Date** | Date of the contact in UTC | 2026-04-05 |
| **Time** | Time of the contact in UTC | 14:32 |
| **Callsign** | The other station's callsign | VK3ABC |
| **Band** | The frequency band | 20m |
| **Frequency** | The exact frequency (optional but useful) | 14.225 MHz |
| **Mode** | The communication mode | SSB, CW, FT8, FM, etc. |
| **RST sent** | Signal report you gave | 59 |
| **RST received** | Signal report you received | 57 |

Additional fields that many operators record:

- **Name** of the other operator
- **QTH** (location) of the other station
- **Grid square** (Maidenhead locator)
- **Power** used
- **Antenna** used
- **Notes** about the contact, propagation conditions, or anything memorable
- **Contest exchange** (for contest contacts)
- **POTA/SOTA reference** (for portable activations)

## UTC Time

Amateur radio universally uses **UTC** (Coordinated Universal Time) for logging. This ensures that when two stations in different time zones log the same contact, the time entries match. UTC does not observe daylight saving time.

Set your computer's clock accurately and configure your logging software to use UTC. Many operators use internet time synchronization (NTP) to keep their clocks accurate to within a second — this is especially important for digital modes like [FT8](/digital-modes/ft8), which require precise timing.

## Paper Logging

A paper logbook works perfectly well and has the advantage of never crashing, losing data, or requiring electricity. Many operators, particularly those who operate [portable](/operating/portable-operating), prefer a small notebook for field logging and then transfer contacts to a computer log later.

Paper logs should use the same fields listed above, recorded in UTC. Pre-printed amateur radio logbook sheets are available commercially, or you can create your own.

## Logging Software

Most operators today use computer logging software, which automates many tasks and integrates with online services. Here is an overview of popular options:

### General-purpose logging programs

**N1MM Logger+** (Windows, free) — The most popular contest logging software, but also excellent for general logging. Integrates with DX clusters, LoTW, eQSL, and Club Log. Widely used and well-documented.

**Log4OM** (Windows, free) — A full-featured general-purpose logger with award tracking, DX cluster integration, QSL management, and a clean interface.

**Logger32** (Windows, free) — A comprehensive logging program with extensive features for DXers, including award tracking, QSL management, and cluster integration.

**Ham Radio Deluxe (HRD)** (Windows, paid) — A suite of programs including a logger, digital mode software, and rig control. Popular but commercial.

**MacLoggerDX** (macOS, paid) — A feature-rich logger for Mac users with DX cluster, rig control, and award tracking.

**CQRLOG** (Linux, free) — An open-source logger for Linux with rig control, DX cluster, and LoTW integration.

**CloudLog** (web-based, free/open-source) — A self-hosted web application for logging. Useful for operators who want access from multiple devices or locations.

### Mobile and field logging

**HAMRS** (cross-platform, free) — A simple, clean logging app designed for portable operations (POTA, SOTA, Field Day). Available for Windows, macOS, Linux, iOS, and Android.

**VK port-a-log** — A simple Android app for portable logging.

**Paper + ADIF conversion** — Some operators log on paper in the field and use tools to enter contacts into ADIF format later.

### Specialised loggers

**WSJT-X** — The standard software for [FT8](/digital-modes/ft8) and other weak-signal digital modes. It includes built-in logging and can export to ADIF for import into your main logger.

**fldigi** — Software for many [digital modes](/digital-modes/fldigi) with built-in logging.

**N1MM+, TR4W** — Primarily contest loggers with features specifically designed for contest operating.

## ADIF: The Standard Log Format

**ADIF** (Amateur Data Interchange Format) is the standard file format for exchanging amateur radio log data between software programs and online services. Almost all logging software can import and export ADIF files, making it easy to move data between programs, upload to LoTW, submit to contest sponsors, and share with award programs.

An ADIF file is a text file containing records with tagged fields. You do not normally need to edit ADIF files by hand, but it is useful to know the format exists for troubleshooting.

A related format is **Cabrillo**, which is the standard for contest log submissions. Most contest loggers can export in Cabrillo format directly.

## Integrating with Online Services

Modern logging software typically integrates with several online services:

- **[LoTW](/operating/qsl-cards)** — Upload contacts for electronic QSL confirmation. Many loggers can upload automatically in real time or in batches.
- **[eQSL](/operating/qsl-cards)** — Electronic QSL card exchange.
- **[Club Log](https://clublog.org)** — Online log hosting and DX analysis.
- **[QRZ.com Logbook](/operating/qsl-cards)** — Online logbook and QSL system.
- **[POTA](/awards/pota)** — Upload logs for Parks on the Air activations.
- **[SOTA](/awards/sota)** — Log contacts for Summits on the Air.
- **DX clusters** — Many loggers display real-time DX spots and highlight stations you need for awards.

## Rig Control and Automatic Logging

Many logging programs can connect to your radio via a serial or USB interface to:

- **Automatically record the frequency and mode** for each contact, eliminating manual entry errors.
- **Control the radio** from the logging software — change bands, frequencies, and modes.
- **Interface with antenna rotators** to point the antenna toward the station being worked.

This is called **CAT (Computer Aided Transceiver) control** and uses protocols like CI-V (Icom), CAT (Yaesu), or Kenwood's serial protocol. Many modern radios also support network-based control.

## Tips for Good Logging Practice

- **Log every contact.** Even casual repeater QSOs can be worth recording.
- **Use UTC for all times.** Set your computer clock accurately.
- **Log in real time.** Enter contacts as they happen rather than trying to remember them later.
- **Back up your log.** Keep regular backups of your log file. A hard drive failure that destroys years of logging data is a painful loss.
- **Upload to LoTW regularly.** The sooner you upload, the sooner your contacts are confirmed.
- **Verify your data.** Periodically review your log for errors — wrong bands, modes, or times can prevent QSL matches.

## Where to Go Next

- [QSL Cards](/operating/qsl-cards) — Confirming contacts with paper and electronic QSLs
- [Awards Overview](/awards/overview) — Awards that require log submissions
- [Contesting Overview](/contesting/overview) — Contest logging requirements
- [QSO Basics](/operating/qso-basics) — What information to record during a contact
- [Software Overview](/software/overview) — Amateur radio software
