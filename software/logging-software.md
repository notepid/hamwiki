---
title: Logging Software
description: A comprehensive guide to amateur radio logging software — features, choosing a logger, and integration with QSL and award systems
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, logging, adif, lotw, qsl
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Logging Software

A station log is one of the most important tools in any amateur radio operator's toolkit. In many countries, keeping a log of transmissions is a regulatory requirement — but even where it is not, a well-maintained log is essential for tracking contacts, submitting confirmations for awards, and simply remembering the stations you have worked. Logging software replaces the paper logbook with a searchable, sortable database that can automate much of the bookkeeping involved in modern amateur radio operating.

## What Logging Software Does

At its core, a logging program records the details of each contact (QSO): date, time (in UTC), callsign of the other station, frequency or band, mode, and signal reports exchanged. Beyond that basic function, modern loggers offer a wide range of features:

**Callsign lookup** — When you enter a callsign, the logger queries online databases (such as QRZ.com, HamQTH, or HamCall) and returns the station's name, location, grid square, and other information. This speeds up logging and helps you know who you are talking to.

**Award tracking** — Loggers can track your progress toward popular awards like [DXCC](/awards/dxcc), [WAS](/awards/was), [WAZ](/awards/waz), [SOTA](/awards/sota), and [IOTA](/awards/iota). They show which entities, states, or zones you still need and highlight new ones when they appear on the air.

**Duplicate detection** — The logger checks incoming callsigns against your existing log and warns you if you have already worked that station on the same band and mode. This is especially useful during contests or when chasing awards.

**QSL management** — Logging software tracks which contacts have been confirmed via paper QSL cards, Logbook of The World (LoTW), eQSL, or other services. Many loggers can generate QSL card labels, print direct QSL card designs, or interface directly with the QSL Bureau system.

**Rig control (CAT)** — Many loggers can communicate with your transceiver to automatically read the current frequency and mode, eliminating the need to enter these manually for each contact.

**Integration with digital modes** — Programs like WSJT-X, fldigi, and JS8Call can send completed contacts directly to your logger, so contacts are recorded automatically without re-typing.

**Mapping and statistics** — Visualise your contacts on a world map, generate statistics by band, mode, year, or country, and produce charts showing your operating activity over time.

## Key Features to Consider

When choosing a logging program, consider the following:

### Operating system support

Most logging software was originally written for Windows, and the widest selection remains on that platform. However, cross-platform loggers that run on macOS and Linux have become increasingly capable. If you do not run Windows, check compatibility before investing time in learning a particular program.

### ADIF support

ADIF (Amateur Data Interchange Format) is the standard file format for exchanging log data between amateur radio programs. Any logger you use should support both ADIF import and export. This allows you to move your log between programs, merge logs from different sources, and upload data to online services. The current version of the standard is ADIF 3.1.4, and a good logger should support its full range of fields.

### Logbook of The World (LoTW) integration

The ARRL's Logbook of The World is the most widely used electronic QSL confirmation system. LoTW uses digital signatures (via TQSL) to authenticate each contact. Look for a logger that can sign and upload contacts to LoTW directly, and that can download and match your LoTW confirmations with your local log.

### Club Log and other aggregators

Club Log is a popular online log hosting and analysis service, especially for DX chasers. It provides DXCC league tables, DXpedition log lookups, and propagation statistics. Many loggers support direct upload to Club Log. Other services like eQSL and QRZ.com Logbook are also worth considering depending on your operating interests.

### Contest integration

If you participate in contests, consider whether your general-purpose logger can import Cabrillo files from your [contest software](/software/contest-software), or whether your contest logger can export ADIF for import into your main log. Some loggers handle both day-to-day and contest logging in a single application.

### Network and cloud operation

Some logging programs support networked multi-operator setups, where several computers share a single log in real time. This is valuable for club stations, field days, and contest multi-operator entries. A few loggers also offer cloud synchronisation, allowing you to access your log from multiple devices.

## Popular Logging Programs

The amateur radio community offers dozens of logging programs. The following are among the most widely used, spanning different platforms and approaches. This is not an endorsement of any particular program — try several and choose the one that fits your workflow.

### Desktop applications

| Program | Platforms | Licence | Notable features |
|---------|-----------|---------|-----------------|
| Log4OM | Windows, Linux (via Mono) | Free | Award tracking, LoTW/eQSL/Club Log integration, rig control, cluster |
| N1MM Logger+ | Windows | Free | Primarily a contest logger but includes a general-purpose log; very widely used in North America |
| DXKeeper (DXLab Suite) | Windows | Free | Part of the DXLab suite; deep award tracking, LoTW integration, QSL management |
| Ham Radio Deluxe (HRD) | Windows | Commercial | Integrated suite with rig control, satellite tracking, digital modes, and logging |
| Logger32 | Windows | Free | Full-featured general-purpose logger with mapping, award tracking, and cluster integration |
| MacLoggerDX | macOS | Commercial | Native Mac logger with rig control, mapping, and award tracking |
| RUMLOG | macOS | Free / paid versions | Popular among Mac users, LoTW/eQSL support |
| CQRlog | Linux | Free (open source) | GTK-based logger for Linux with rig control and Hamlib integration |
| KLog | Windows, macOS, Linux | Free (open source) | Cross-platform logger focused on award tracking and simplicity |

### Web-based and cloud loggers

Some operators prefer to keep their log online, accessible from any device with a browser. Web-based loggers include QRZ.com Logbook, Cloudlog (self-hosted, open source), and HAMRS (mobile-friendly, with optional cloud sync). These trade some of the deep integration of desktop applications for convenience and portability.

### Mobile logging

For portable operations such as [SOTA](/awards/sota) or [POTA](/awards/pota), lightweight mobile logging applications are available for iOS and Android. HAMRS, VK port-a-log, and Outd Log are examples. These typically focus on fast, simple logging and ADIF export, with optional upload to aggregator services.

## The ADIF Standard

ADIF is worth understanding in some detail, because it is the glue that holds the amateur radio software ecosystem together. An ADIF file is a plain-text file containing one record per contact. Each field is stored as a tagged value:

```
<CALL:5>W1ABC <BAND:3>20m <MODE:3>SSB <QSO_DATE:8>20260315 <TIME_ON:6>143000 <RST_SENT:2>59 <RST_RCVD:2>57 <EOR>
```

The format is designed to be forgiving: programs ignore fields they do not understand, so ADIF files can be exchanged between programs that support different feature sets. When exporting from one logger to another, always use ADIF as the transfer format.

> **Tip:** Before switching logging software or making major changes to your log, export a full ADIF backup. This is your safety net. ADIF files are plain text and can be opened in any text editor if you ever need to inspect or repair them manually.
{.is-info}

## Connecting Your Logger to Other Software

A well-integrated station has its logging software communicating with other programs in real time. The most common integration points are:

**WSJT-X and other digital mode programs** — WSJT-X can send completed FT8/FT4 contacts to your logger via UDP broadcast. Most major loggers support receiving these broadcasts. Fldigi and JS8Call offer similar integration, often via a combination of TCP/IP and shared files.

**DX cluster clients** — A DX cluster feed delivers real-time spots of stations on the air. When a spot appears in your logger, it can instantly tell you whether the spotted station is a new country, band, or mode — a powerful aid for award chasers.

**Rig control** — If your logger supports CAT (via Hamlib, OmniRig, or direct serial/network protocols), it can read your radio's frequency and mode in real time. You can also click on a DX spot in the logger and have the radio tune to that frequency automatically.

**Rotor control** — Some loggers can calculate the beam heading to a station you are about to work and aim your directional antenna automatically via a rotor interface.

**LoTW and QSL services** — Background uploading of new contacts to LoTW, eQSL, Club Log, and QRZ.com Logbook keeps your online confirmations current without manual intervention.

## Best Practices for Station Logging

**Log every contact** — Get into the habit of logging every QSO, even casual ragchews. You never know which contact will turn out to be the one that completes an award or confirms a rare grid square.

**Use UTC** — All logging should use Coordinated Universal Time (UTC), not local time. This is the universal standard in amateur radio and avoids confusion when exchanging logs with stations in different time zones.

**Back up regularly** — Keep ADIF backups on a separate drive, cloud storage, or external media. Logs represent years of operating history and are irreplaceable if lost.

**Keep your callsign database current** — Online lookup databases are updated regularly as new licences are issued and operators move. Update your local copy or check that your logger's live lookup is enabled.

**Reconcile LoTW periodically** — Download your LoTW QSL records and sync them with your local log. This ensures your award tracking is accurate and up to date.

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [Contest Software](/software/contest-software) — Specialised logging for contest operating
- [Online Tools & Resources](/software/online-tools) — Web-based callsign lookups and utilities
- [DXCC](/awards/dxcc) — The DX Century Club award
- [WAS](/awards/was) — Worked All States award
- [Digital Station Setup](/digital-modes/digital-station-setup) — Connecting radio and computer
- [FT8](/digital-modes/ft8) — The most popular digital mode
