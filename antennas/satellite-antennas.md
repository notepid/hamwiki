---
title: Satellite Antennas
description: Antennas for working amateur radio satellites — from handheld Yagis to fully tracked crossed-Yagi arrays and eggbeater antennas
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, satellite, yagi, circular-polarisation, eme
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Satellite Antennas

Working [amateur radio satellites](/satellites/overview) is one of the most exciting aspects of the hobby — making contacts through a spacecraft passing overhead, often with modest equipment. The antenna requirements for satellite work differ from terrestrial communication because the satellite moves across the sky during a pass, the signal path goes through the atmosphere at varying angles, and polarisation effects (Faraday rotation) are significant. This page covers the antenna options for satellite communication, from simple setups that cost almost nothing to high-performance tracking stations.

## What satellite antennas need to do

Amateur satellites are typically in low Earth orbit (LEO), passing overhead in a window of roughly 5–15 minutes. During a pass, the satellite moves from one horizon, across the sky, to the opposite horizon. An antenna for satellite work must:

- **Cover the sky** — either by having a broad enough pattern to cover the pass without moving, or by being steerable to track the satellite as it moves
- **Handle dual-band operation** — most FM satellites use different uplink and downlink frequencies, typically on 2 metres (144 MHz) and 70 cm (430 MHz)
- **Manage polarisation** — signals passing through the ionosphere experience Faraday rotation, which randomly shifts polarisation. Circularly polarised antennas are less affected by this than linearly polarised ones

## Simple approaches: getting started

### Handheld radio with a better antenna

The easiest way to hear (and even work) FM satellites like SO-50 or the [ISS](/satellites/iss-contacts) is with a dual-band handheld radio and an upgraded antenna. Replacing the stock rubber duck with a **half-wave whip** or a **dual-band telescoping antenna** provides a significant improvement. You can hear many satellite passes and make contacts on the strongest FM satellites with nothing more than this.

The technique is straightforward: stand outdoors with a clear view of the sky, point the handheld toward the satellite (using a tracking app on your phone), and work the pass. This is how many operators get their first satellite contact.

### Arrow-style portable Yagi

The **Arrow antenna** (and similar designs) is a lightweight, handheld dual-band [Yagi](/antennas/yagi) with elements for both 2 metres and 70 cm on a single boom. It is the most popular entry-level directional satellite antenna and can be used handheld — the operator physically points it at the satellite during the pass while holding it overhead.

A typical Arrow-style antenna has 3 elements on 2 metres and 7 elements on 70 cm, providing moderate gain on both bands. It connects to the radio via a short feedline with a duplexer that combines the two bands onto a single port (useful for full-duplex operation with radios that have separate VHF and UHF connectors, or for use with a single-port radio).

Arrow antennas are effective, portable, and relatively affordable. Many satellite operators have made hundreds or thousands of contacts with one.

### Tape-measure Yagi

A **tape-measure Yagi** for 2 metres is a popular homebrew project — the elements are made from steel tape measure blades that can flex and fold for transport. With 3 elements, it provides useful gain for satellite work and costs very little to build. While it only covers one band, it is a great first satellite antenna project.

## Omnidirectional satellite antennas

For operators who want to work satellites without physically tracking them (hands-free operation), omnidirectional antennas with **circular polarisation** are available:

### Eggbeater antenna

The **eggbeater** antenna consists of two loops arranged at right angles to each other (like an eggbeater) and fed 90 degrees out of phase to produce circular polarisation. The eggbeater has a broad upward-facing pattern that covers most of the sky without the need for a rotator. Separate eggbeaters are used for VHF and UHF.

The eggbeater is a good choice for an unattended satellite ground station or for operators who want to work FM satellites without hand-tracking. Its gain is modest (a few dB over a dipole), so it is best suited for stronger satellites.

### Turnstile antenna

The **turnstile** is two dipoles arranged at right angles and fed 90 degrees out of phase, producing circular polarisation. Like the eggbeater, it has a broad upward pattern. It is simpler to build than the eggbeater but has less gain. Adding a ground-plane reflector below the turnstile improves the upward gain.

### Quadrifilar helix antenna (QFH)

The **QFH** is a compact, self-phasing circularly polarised antenna that produces a broad overhead pattern. It is popular for receiving weather satellite imagery (NOAA APT and Meteor-M LRPT) and works for amateur satellites as well. The QFH can be built from coaxial cable or copper tubing and is an interesting homebrew project.

## Tracking antenna systems

For maximum satellite performance — especially for SSB/CW linear transponder satellites, higher-orbit satellites, or [moonbounce (EME)](/satellites/eme-moonbounce) — a steerable antenna system with higher gain is needed.

### Crossed Yagis

**Crossed Yagis** are two [Yagi antennas](/antennas/yagi) mounted on the same boom at right angles to each other, fed 90 degrees out of phase to produce circular polarisation. This is the standard high-performance satellite antenna. Separate crossed-Yagi pairs are used for VHF and UHF, mounted on an azimuth-elevation (az-el) rotator that tracks the satellite across the sky.

A typical satellite station might use 2x 9-element crossed Yagis for 70 cm and 2x 5-element crossed Yagis for 2 metres on an az-el rotator controlled by tracking software (such as GPredict, SatPC32, or MacDoppler) interfaced to the rotator controller.

### Azimuth-elevation rotators

An **az-el rotator** allows the antenna to point in any direction in the sky — both horizontally (azimuth) and vertically (elevation). This is essential for tracking LEO satellites. The rotator is typically controlled by a computer running satellite tracking software, which calculates the satellite's position in real time and sends commands to the rotator.

Commercial az-el rotators designed for amateur satellite work are available from several manufacturers. Some operators build their own az-el systems using modified TV antenna rotators or stepper motors.

### EME (moonbounce) antennas

[EME communication](/satellites/eme-moonbounce) requires extremely high gain — the round-trip path loss to the moon and back is enormous. EME stations on 2 metres typically use arrays of 4, 8, or even 16 long-boom Yagis (each 6–10 metres long) stacked together on a large az-el mount. On 70 cm, similar arrays with more elements per Yagi are used.

EME is the most demanding amateur antenna application and represents the pinnacle of VHF/UHF antenna technology. Stations capable of EME represent a serious investment in hardware, but the experience of bouncing a signal off the moon is unlike anything else in the hobby.

## Polarisation for satellite work

**Right-hand circular polarisation (RHCP)** is the most common convention for amateur satellite antennas. Using circular polarisation avoids the deep fading that occurs when a linearly polarised antenna receives a signal whose polarisation has been rotated by Faraday rotation or by the satellite's tumbling.

With a handheld linearly polarised antenna (like the Arrow), you will experience periodic signal fading as the polarisation alignment shifts during a pass. This is manageable for FM satellites (where the signal is either there or not) but more problematic for SSB/CW work where signal strength variations matter.

Switching between RHCP and LHCP (left-hand circular polarisation) can sometimes recover a signal that has undergone 90 degrees of Faraday rotation. Some stations use a relay to switch polarisation sense.

## Feedline and station considerations

Satellite antennas are often mounted high (for a clear view of the sky), which means potentially long feedline runs. At VHF and especially UHF, feedline loss is a significant concern. Use the lowest-loss [coaxial cable](/antennas/feedlines) practical — LMR-400 or better for runs over a few metres.

A **preamplifier** (low-noise amplifier, LNA) mounted at the antenna reduces the impact of feedline loss on receive. Many satellite operators use a mast-mounted preamp on the downlink antenna, with a relay to bypass it during transmit.

## Where to go next

- [Satellites Overview](/satellites/overview) — Getting started with amateur satellites
- [ISS Contacts](/satellites/iss-contacts) — Contacting the International Space Station
- [EME/Moonbounce](/satellites/eme-moonbounce) — The ultimate antenna challenge
- [Yagi-Uda Antennas](/antennas/yagi) — Yagi design principles
- [VHF/UHF Antennas](/antennas/vhf-uhf-antennas) — Other VHF/UHF antenna options
- [Portable Antennas](/antennas/portable-antennas) — Lightweight satellite antennas for field use
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Polarisation and gain concepts
