---
title: Contest Station Setup
description: How to configure and optimise your amateur radio station for contesting, from basic home setups to multi-operator stations
published: true
date: 2026-04-05T09:30:00.000Z
tags: contesting, station, equipment
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Contest Station Setup

You can contest with any amateur radio station — a basic [HF transceiver](/equipment/hf-transceivers), a simple antenna, and a computer are enough to participate and have fun. But as you become more serious about contesting, thoughtful station design can dramatically improve your results. This page covers station setup at every level, from making the most of what you already have to building a dedicated contest station.

## The Essentials

Every contest station, regardless of size, needs these core components:

### Transceiver
Any modern HF transceiver will work for contesting. Features that make a real difference in a contest environment include:

**Narrow IF filters.** Contests pack stations close together on the band. A receiver with good selectivity — particularly narrow crystal or roofing filters — lets you pull one signal out of a crowd. If your radio supports optional narrow filters, they are one of the best investments for contesting.

**Fast AGC (Automatic Gain Control).** In a contest pileup, signals of wildly varying strength appear in rapid succession. Fast AGC recovery keeps the audio level manageable and prevents strong signals from desensitising your receiver.

**Good dynamic range.** Strong signals from nearby contest stations can overload a receiver with poor dynamic range, causing distortion and spurious signals. Higher-end transceivers handle this better, but even mid-range radios perform well if you are not operating near a very large station.

**Computer control (CAT).** Computer-aided transceiver control lets your [logging software](/contesting/contest-logging) read and set frequencies automatically, track band changes, and integrate with DX cluster data. Most modern transceivers support CAT via USB or serial connection.

### Antenna System
The antenna is typically the single biggest factor in station performance. For contesting:

**Higher is better.** A dipole at 15 metres above ground will outperform the same dipole at 8 metres. Height gives you a lower radiation angle on HF, which means stronger signals at a distance.

**Directional antennas help.** A [Yagi or beam antenna](/antennas/beam-antennas) on a rotator lets you point your signal where you want it, increasing gain in one direction while reducing interference from others. Even a modest three-element tribander on a small tower is a significant advantage over a wire antenna.

**Multi-band capability matters.** Contests span multiple bands, and the ability to change bands quickly without retuning or switching antennas keeps your rate up. A tribander for 20/15/10 metres combined with wire antennas for 40/80/160 metres covers the full contest range.

**Do not let antenna limitations stop you.** Many successful contest operators work with compromise antennas — attic dipoles, end-fed wires, verticals on small lots. The bands are full of rare multipliers during big contests, and even a modest antenna will hear and work plenty of them.

### Computer and Logging Software
A computer running [contest logging software](/contesting/contest-logging) is not optional in modern contesting. The software tracks your contacts, checks for duplicates, calculates your score, and produces the Cabrillo file for submission.

**Computer requirements are minimal.** Contest logging software is not resource-intensive. Even an older laptop will work. What matters is reliability — a crash during the contest means lost contacts and lost time. Use a stable computer and keep it plugged in.

**Dual monitors are helpful.** One screen for the logging software, one for a bandmap, DX cluster, or propagation tools. This is a convenience, not a necessity, but it reduces the time spent switching between windows.

### Audio Setup
How you hear the contest makes a significant difference in your performance:

**Headphones.** Essential for serious contesting. They isolate the signal from room noise, reduce fatigue compared to a loudspeaker, and let others in the house sleep while you operate through the night. Comfortable, over-ear headphones with good bass response are ideal.

**Microphone (phone contests).** For SSB contesting, a quality microphone with a frequency response matched to voice communication makes your signal easier to copy. A boom headset (headphones with an attached microphone) is particularly convenient because it keeps both hands free.

**Audio processing.** Most HF transceivers include speech compression, which raises the average power of your voice signal without increasing peak power. Moderate compression makes your signal louder and more readable in marginal conditions. Too much compression sounds distorted — find the sweet spot.

## Station Ergonomics

Contesting can mean sitting at the radio for many hours. A comfortable, well-organised operating position makes a real difference in both performance and enjoyment.

**Chair.** A good chair with proper support is not a luxury — it is a necessity. Back pain at hour twelve will ruin the rest of your contest.

**Desk layout.** Place your radio, keyboard, and mouse so that you can reach everything without stretching. Your monitor should be at eye level. Commonly referenced items — band plan, exchange cheat sheet, multiplier list — should be visible at a glance.

**Lighting.** Adjustable lighting that illuminates your desk without creating glare on your monitor. Dim ambient lighting helps reduce eye strain during long sessions.

**Food and drink within reach.** Keep water, snacks, and meals nearby so you do not lose operating time to trips to the kitchen.

## SO2R: Single Operator, Two Radios

**SO2R** (Single Operator, Two Radios) is an advanced technique where one operator uses two transceivers and two antennas simultaneously. While transmitting a CQ on one radio, the operator listens on the second radio for new multipliers or stations to work on a different band.

SO2R requires:

- **Two transceivers** capable of independent operation.
- **Two antennas** (or more) with adequate isolation between them so that one transmitter does not overload the other receiver.
- **An SO2R controller** or switching box that routes audio from both receivers to the operator's headphones (typically left ear and right ear) and manages transmit/receive switching.
- **Logging software with SO2R support.** All major contest loggers support this.

SO2R is not for beginners — it demands the ability to listen to two signals simultaneously and make rapid decisions about which radio to prioritise. But for experienced operators, SO2R can increase scores by 20–30% by filling what would otherwise be dead time.

## Multi-Operator Station Considerations

Multi-operator contest entries — where a team shares one or more transmitters — bring additional station design challenges:

**Inband interference.** When two transmitters are active on different bands, the strong signal from one can desensitise the receiver of the other. Band-pass filters on each transmitter's output significantly reduce this problem.

**Station layout.** Each operating position needs its own radio, logging computer, headphones, and access to the antenna switching system. In a multi-multi station (multiple transmitters on different bands simultaneously), positions should be physically separated to reduce acoustic interference between operators.

**Network logging.** Multi-operator stations use networked logging software so that all contacts appear in a single shared log. This prevents duplicate contacts and allows all operators to see the team's multiplier count in real time.

**Antenna switching.** A multi-band station may have several antennas for different bands and directions. An antenna switching system — either manual switches or a remote-controlled matrix — lets operators select the best antenna for their current band and target direction.

## Antenna Considerations for Contesting

Beyond the basics of antenna choice, contesting raises some specific antenna questions:

### Band-pass filters
In any station with more than one transmitter — SO2R or multi-operator — band-pass filters are essential. These filters pass signals on the desired band and reject everything else, preventing one transmitter from overloading another receiver. A set of six filters (one for each HF contest band) is standard.

### Receive antennas
On the lower bands (80 and 160 metres), separate receive antennas can dramatically improve performance. Transmit antennas on these bands are often verticals or shortened dipoles that are effective radiators but also pick up significant local noise. A dedicated receive antenna — such as a Beverage, loop, or flag/pennant — can offer a much quieter receiving environment.

### Stacking and switching
Competitive stations often use multiple Yagi antennas stacked vertically on a tower, with a switching system that lets the operator select a single antenna or combine them for additional gain. This is well beyond what most operators need, but it illustrates how seriously the top competitors take antenna performance.

## Power and Grounding

**Power supply.** Ensure your power supply can handle sustained high-duty-cycle operation. Contesting means transmitting far more frequently than casual operating. A power supply rated for continuous duty at your radio's maximum current draw is important. If you run an amplifier, verify that your mains circuit can handle the load — a dedicated 240V circuit is common for amplifier installations.

**Grounding.** A good RF ground reduces noise, prevents RF feedback, and is important for safety. Bond all station equipment to a common ground bus, and connect that bus to an external ground rod or radial system. See [Station Grounding](/electronics/station-grounding) for details.

**Amplifiers.** Running more power helps, but the improvement is less dramatic than you might expect. Going from 100 watts to 1,000 watts (a 10 dB increase) is roughly equivalent to a one-and-a-half S-unit improvement. If your antenna is mediocre, investing in the antenna first will yield better results than adding an amplifier.

## Station Automation

As your contest station evolves, automation reduces workload and frees you to focus on operating:

**Antenna rotator control.** Software-controlled rotators let you point your beam by clicking on a map or having the logging software automatically turn the antenna toward the station you are working.

**Band decoder.** A band decoder reads your radio's current frequency and automatically selects the correct antenna, band-pass filter, and amplifier settings. This eliminates manual switching and the risk of transmitting into the wrong filter.

**Voice keyer.** A hardware or software voice keyer stores recorded messages (CQ calls, exchange elements) and plays them at the press of a button. This saves your voice and ensures consistent audio quality throughout the contest.

**CW keyer.** Your logging software can send CW messages via the radio's keying input. Combined with function key macros, this lets you run at high speed without a paddle.

## Building Up Over Time

You do not need to build the ultimate contest station on day one. A practical progression might look like:

1. **Start with what you have.** Your current radio and antenna are enough to enter contests and learn the fundamentals.
2. **Add contest logging software.** This is the single biggest improvement for a new contester.
3. **Improve your antenna.** Even modest improvements — raising a dipole, adding a vertical, putting up a tribander — make a noticeable difference.
4. **Add narrow receive filters.** If your radio supports optional filters, add them.
5. **Add an amplifier.** When your antenna and operating are solid, more power helps.
6. **Consider SO2R or multi-op.** Once you are consistently competitive, these techniques offer the next level of performance.

Each step builds on the last, and the learning you do at each stage informs your decisions for the next.

## Where to Go Next

- [Contest Logging](/contesting/contest-logging) — Software for managing contest contacts
- [Contesting Techniques](/contesting/contesting-techniques) — Operating strategies and tips
- [HF Transceivers](/equipment/hf-transceivers) — Choosing a radio
- [Beam Antennas](/antennas/beam-antennas) — Directional antennas for contesting
- [Wire Antennas](/antennas/wire-antennas) — Effective antennas on a budget
- [Getting Started with Contesting](/contesting/getting-started-contesting) — The basics of entering a contest
