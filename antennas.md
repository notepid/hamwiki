---
title: Antennas
description: An introduction to antennas for amateur radio — what they do, how they work, and how to choose the right one
published: true
date: 2026-04-05T17:42:09.871Z
tags: 
editor: markdown
dateCreated: 2026-04-05T17:42:09.871Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Antennas Overview

The antenna is arguably the most important part of any amateur radio station. It is the point where electrical energy from your transmitter becomes radio waves, and where incoming radio waves are converted back into electrical signals for your receiver. No matter how powerful or expensive your radio equipment is, a poor antenna will limit what you can do — and a good antenna can make a modest station perform remarkably well.

## What does an antenna do?

At its simplest, an antenna is a conductor (usually wire or metal tubing) that **radiates electromagnetic energy** when driven by a transmitter and **captures electromagnetic energy** when connected to a receiver. The antenna converts between two forms of energy: the alternating current flowing in the feedline and the electromagnetic waves travelling through space.

Every antenna has characteristics that determine how well it performs and in which directions it sends or receives signals. The most important of these are covered on the [Antenna Fundamentals](/antennas/antenna-fundamentals) page, but the key concepts to understand early on are **resonance**, **impedance**, **radiation pattern**, **gain**, and **polarisation**.

## Types of antennas

Amateur radio operators use a tremendous variety of antenna designs. Each type has trade-offs in size, performance, cost, complexity, and suitability for different frequency bands. Here are the broad categories:

### Wire antennas

Wire antennas are the workhorses of HF amateur radio. They are inexpensive, effective, and relatively simple to build and install. The [dipole](/antennas/dipole) is the most fundamental wire antenna and a natural starting point for any new ham. Other popular wire antennas include the [end-fed half-wave (EFHW)](/antennas/end-fed-half-wave), random wire antennas, doublets, and various multi-band designs. See [Wire Antennas](/antennas/wire-antennas) for a broader survey.

### Vertical antennas

[Vertical antennas](/antennas/vertical) are popular for both HF and VHF/UHF use. They radiate equally in all horizontal directions (omnidirectional pattern), which is useful when you want to communicate in every direction without rotating the antenna. Ground-mounted verticals, ground-plane antennas, and vertical dipoles are all common configurations.

### Directional antennas

When you want to focus your signal toward a particular direction — for example, when working DX (long-distance) stations or during contests — directional antennas like the [Yagi-Uda (Yagi)](/antennas/yagi) offer significant advantages. These antennas concentrate transmitted energy in one direction and improve reception from that same direction, providing **gain** over simpler antennas.

### Loop antennas

[Loop antennas](/antennas/loop-antennas) come in many forms, from full-wavelength horizontal loops to compact magnetic loops that fit on a desktop. Small magnetic loops are particularly popular in situations where space is limited or outdoor antennas are restricted, since they can be effective despite their small size.

### VHF/UHF antennas

The shorter wavelengths at [VHF and UHF frequencies](/antennas/vhf-uhf-antennas) mean antennas are physically smaller and often easier to install. Common designs include ground-plane verticals, collinear arrays, and Yagi beams. Many VHF/UHF antennas are designed to work with [repeaters](/operating/repeaters) for local communication.

### Satellite antennas

Working amateur [satellites](/satellites/overview) requires antennas that can be pointed at a satellite as it passes overhead. [Satellite antennas](/antennas/satellite-antennas) range from simple handheld Yagis to fully tracked crossed-Yagi arrays.

### Mobile and portable antennas

Operators who work from vehicles use [mobile antennas](/antennas/mobile-antennas) — typically shortened verticals mounted on the vehicle body. Those who operate from parks, summits, or while travelling use lightweight [portable antennas](/antennas/portable-antennas) designed for quick setup and takedown.

## The antenna system

An antenna does not work in isolation. The complete **antenna system** includes several components that work together:

- **The antenna itself** — the radiating element(s)
- **The feedline** — the cable (usually [coaxial cable](/antennas/feedlines)) that carries RF energy between the radio and the antenna
- **Matching devices** — components like [baluns, ununs](/antennas/baluns-and-ununs), and antenna tuners that help ensure efficient power transfer between the radio, feedline, and antenna
- **Supports** — masts, towers, trees, or other structures that hold the antenna in position
- **Grounding and bonding** — electrical connections to earth ground for safety and, in some antennas, performance

Understanding how all these pieces work together is important. A great antenna connected with lossy feedline, or a mismatched antenna without proper [SWR management](/antennas/swr-and-matching), will not perform to its potential.

## Choosing your first antenna

If you are new to amateur radio and wondering where to start, here are some practical guidelines:

**For VHF/UHF (local communication and repeaters):** Most new hams start with a handheld radio, which comes with a short "rubber duck" antenna. Upgrading to a simple external antenna — even a basic ground-plane or slim-jim — makes a dramatic difference. For a home station, a modest VHF/UHF vertical on the roof is an excellent investment.

**For HF (long-distance communication):** A half-wave [dipole](/antennas/dipole) for your favourite band is the classic first HF antenna. It is inexpensive, easy to build, and performs well. If you have limited space, an [end-fed half-wave](/antennas/end-fed-half-wave) or a small [magnetic loop](/antennas/loop-antennas) may be better options. Multi-band wire antennas like fan dipoles or trapped dipoles let you work several bands with a single antenna.

**General advice:** Put your antenna as high as you reasonably can, use good quality [feedline](/antennas/feedlines) with appropriate connectors, and keep the antenna clear of nearby metal objects. Height and a clear location matter more than antenna complexity for most operating situations.

## Safety

Antenna work involves some real hazards. Before installing or working on antennas, be aware of these critical safety concerns:

- **Electrical hazard** — Contact with overhead power lines is the single greatest danger in antenna work. Always ensure that no part of your antenna, mast, feedline, or support ropes can come into contact with power lines, even if something falls. Maintain a safe distance at all times.
- **Falling hazard** — Tower and mast climbing should only be done with proper training, equipment, and a ground crew. Falls from height are a leading cause of serious injury in the hobby.
- **RF exposure** — Transmitting antennas produce electromagnetic fields. Keep antennas at a safe distance from people, especially high-gain antennas at high power levels. Follow your country's RF exposure guidelines.
- **Structural loads** — Antennas, masts, and towers must withstand wind, ice, and their own weight. Ensure all installations are structurally sound and properly guyed or bracketed.

See [Building Antennas](/antennas/building-antennas) for construction safety practices and [Antenna Restrictions](/antennas/antenna-restrictions) for regulatory and zoning considerations.

## Antenna modelling

Before building an antenna, many hams use [antenna modelling software](/antennas/antenna-modeling) to simulate how a design will perform. Modelling can predict radiation patterns, gain, impedance, and the effects of nearby objects — saving time and materials in the design process.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Learn the core concepts: resonance, impedance, gain, and radiation patterns
- [Dipole Antennas](/antennas/dipole) — The classic first antenna and a foundation for understanding all others
- [Feedlines](/antennas/feedlines) — How RF energy gets from the radio to the antenna
- [SWR and Matching](/antennas/swr-and-matching) — Understanding and managing standing wave ratio
- [Building Antennas](/antennas/building-antennas) — Practical construction tips and safety
