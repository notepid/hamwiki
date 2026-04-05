---
title: Satellite Station Equipment
description: Radios, antennas, rotators, and accessories for amateur satellite communication at every level
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, equipment, antennas, rotators, full-duplex
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Satellite Station Equipment

The equipment needed for amateur satellite communication ranges from a simple handheld radio and whip antenna (enough for an FM satellite contact) to a full ground station with tracking antennas, rotators, low-noise preamplifiers, and computer-controlled Doppler correction. What you need depends on which satellites you want to work and how seriously you want to pursue satellite operating.

This page covers equipment for working LEO (low Earth orbit) satellites and the geostationary QO-100. For [EME (moonbounce)](/satellites/eme-moonbounce) equipment, which has distinct and more demanding requirements, see the dedicated EME page.

## Radios for satellite operation

### The full-duplex requirement

One of the most important concepts in satellite operation is **full-duplex** — the ability to transmit and receive simultaneously on different frequencies. When you work through a satellite, you transmit on the uplink frequency and receive on the downlink frequency at the same time. Hearing your own signal coming back through the satellite confirms that you are successfully accessing it and lets you adjust your aim, power, and frequency in real time.

There are several ways to achieve full-duplex operation:

- **A single full-duplex radio.** Some transceivers support true simultaneous transmit and receive on different bands. This is the most convenient option but is not available on all radios.
- **Two separate radios.** Many satellite operators use one radio for transmit (uplink) and another for receive (downlink). This approach offers maximum flexibility and is common for serious satellite stations.
- **A dual-band handheld with full-duplex capability.** Certain handheld transceivers can operate in full-duplex mode across VHF and UHF. This is the most popular portable satellite setup.

If you cannot operate full-duplex (for example, with a single half-duplex handheld), you can still make FM satellite contacts by transmitting blind — but you will not be able to hear whether the satellite is receiving you, making the experience much more difficult and uncertain.

### Handhelds for portable FM satellite work

For working FM satellites while portable, a dual-band VHF/UHF handheld transceiver is the most common starting point. The radio needs to cover the 2 m (144–146 MHz) and 70 cm (430–440 MHz) bands, since most FM satellites use a VHF/UHF combination for uplink and downlink.

Look for a handheld that supports full-duplex (simultaneous transmit on one band and receive on the other). Not all dual-band handhelds offer this — it is a specific feature to check for. Power output of 5 watts is typically more than adequate for FM satellite work; in many cases you will want to reduce power to avoid over-driving the satellite transponder.

### Base/mobile radios for satellite work

For a home station or a more capable portable setup, a dual-band VHF/UHF mobile or base transceiver provides higher power (useful for linear transponder satellites), better receiver performance, and CAT (Computer Aided Transceiver) control for automated Doppler correction.

Some operators use a dedicated all-mode VHF/UHF transceiver (one that supports SSB and CW in addition to FM) for working linear transponder satellites. All-mode capability is essential for SSB/CW satellite work — FM-only radios cannot access linear transponders.

For a two-radio setup, a common approach is to use one VHF all-mode radio and one UHF all-mode radio, with each connected to its own antenna. This provides complete frequency flexibility and full-duplex operation.

### Radios for QO-100

Working through QO-100 requires equipment for the 2.4 GHz uplink and the 10 GHz downlink. The downlink is typically received using a standard satellite TV LNB (low-noise block downconverter) mounted on a small dish, which converts the 10 GHz signal down to an intermediate frequency that a conventional receiver or SDR can handle.

For the uplink, operators commonly use a transverter that converts a 432 MHz or 144 MHz signal up to 2.4 GHz, or a dedicated 2.4 GHz transmitter. Power levels at 2.4 GHz are typically in the range of a few watts, fed to a helical antenna or a small dish with a feed.

## Antennas for satellite work

### Handheld directional antennas (portable)

The most popular antennas for portable FM satellite operation are lightweight, handheld directional antennas designed specifically for this purpose:

- **Arrow antenna** — a dual-band (2 m/70 cm) handheld Yagi that breaks down for transport. The Arrow II has separate VHF and UHF elements on a single boom with a handle grip. It is one of the most widely used satellite antennas among portable operators.
- **Elk antenna** — a dual-band handheld log-periodic antenna. The Elk's log-periodic design offers wider bandwidth than a Yagi, which can be an advantage when Doppler shift moves the operating frequency.
- **Homebrew Yagis** — many satellite operators build their own lightweight Yagis from materials like aluminium arrow shafts or steel tape measures. These can be highly effective and are a rewarding [DIY project](/diy-projects/overview).

With a handheld antenna, you physically point the antenna at the satellite and track it across the sky during the pass. A smartphone running a [satellite tracking app](/satellites/satellite-tracking) can help you visualise where to point.

### Fixed station antennas

For a dedicated home satellite station, fixed antennas mounted on an azimuth/elevation rotator provide consistent performance and hands-free tracking:

- **Crossed Yagis (circularly polarised)** are the standard choice for serious VHF/UHF satellite work. Satellite signals are often circularly polarised, and using a circularly polarised antenna on the ground eliminates the deep signal fades (polarisation nulls) that occur with a linearly polarised antenna. A typical setup uses a circularly polarised Yagi for 2 m and another for 70 cm, both mounted on the same rotator mast.
- **Single-polarity Yagis** — simpler and less expensive than crossed Yagis, these work well but will experience occasional polarisation fading. Many operators start with linear Yagis and upgrade to crossed Yagis later.
- **Eggbeater antennas** — omnidirectional circularly polarised antennas that do not require a rotator. Eggbeaters sacrifice gain compared to Yagis but can hear satellites in any direction, making them useful for automated stations or casual monitoring. They are typically used for receive only or for satellites with strong signals.

### Antenna considerations

**Gain vs. beamwidth:** Higher-gain antennas (longer Yagis with more elements) produce stronger signals but have a narrower beam. This means you need more precise tracking. For hand-tracking with a portable antenna, moderate gain (7–12 dBi) provides a good balance. For rotator-tracked fixed stations, higher gain (12–16 dBi) is practical.

**Separate vs. shared antennas:** Using separate antennas for transmit and receive reduces the chance of your transmitted signal desensitising your receiver. A diplexer (a filter that combines VHF and UHF onto a single feedline) can be used when space or rotator capacity limits you to a single antenna boom, but separate feedlines to separate antennas is the cleaner approach.

**Feedline loss:** At UHF frequencies (430+ MHz), coaxial cable losses are significant. Keep cable runs as short as practical, and use low-loss cable (such as LMR-400 or equivalent). For long runs, a mast-mounted preamplifier on the receive antenna can compensate for cable losses.

## Rotators

An **azimuth/elevation (az/el) rotator** holds the antenna array and automatically steers it to follow a satellite across the sky. The rotator is controlled by a computer running [tracking software](/satellites/satellite-tracking) (such as GPredict, SatPC32, or MacDoppler) that calculates the satellite's position in real time and sends pointing commands to the rotator controller.

### Rotator components

A typical az/el rotator system consists of:

- **Azimuth rotator** — turns the antenna horizontally (0–360°). Many satellite operators use standard TV-antenna rotators for the azimuth axis, though heavy-duty models are needed for larger antenna arrays.
- **Elevation rotator** — tilts the antenna vertically (0–180° or 0–90°). Some purpose-built satellite rotators integrate both az and el into a single unit.
- **Rotator controller** — the electronics that drive the rotator motors and communicate with the computer. The controller accepts commands (usually via a serial or USB connection) from tracking software and reports the current antenna position.
- **Rotator interface** — some rotator controllers speak standard protocols (like the Yaesu GS-232 protocol) natively. Others require an interface adapter to translate between the computer and the controller.

### Alternative approaches

For operators who want automated tracking without the expense of a full rotator system, several alternatives exist. Phased arrays (electronically steered antennas with no moving parts) are an emerging technology for satellite work, though not yet common in amateur use. Omnidirectional antennas like the eggbeater eliminate the need for tracking entirely, at the cost of reduced gain. Some operators also build lightweight, low-cost az/el systems from stepper motors and 3D-printed parts controlled by Arduino or Raspberry Pi boards.

## Preamplifiers

A **mast-mounted preamplifier (preamp)** is a low-noise amplifier installed at the antenna, before the signal travels down the feedline to the receiver. By amplifying the signal at the antenna where it is strongest, a preamp overcomes cable losses and improves the system's overall noise figure.

Preamplifiers are especially valuable on the UHF (70 cm) receive antenna, where cable losses are highest. A good preamplifier for satellite work has a noise figure of 0.5 dB or better and enough gain (15–20 dB) to overcome cable loss without overloading the receiver.

When using a preamp on a receive antenna that shares a feedline with a transmitter (or is physically close to a transmit antenna), you need **sequencing** — a switching arrangement that bypasses or protects the preamp during transmit and re-engages it during receive. A sequencer ensures that the preamp is never exposed to high transmit power, which would destroy it.

## Computer and software integration

A well-equipped satellite station integrates the radio, rotator, and tracking software through a computer:

- **Tracking software** ([GPredict](/satellites/satellite-tracking), SatPC32, MacDoppler, etc.) predicts satellite positions and sends real-time pointing commands to the rotator controller.
- **CAT control** — the same software sends frequency commands to the radio to correct for Doppler shift automatically. This keeps the received signal centred and the transmitted signal on the correct uplink frequency.
- **Audio recording and logging** — many operators record passes and log contacts to satellite-specific logbooks. Grid squares (Maidenhead locator) are the standard location exchange in satellite contacts.

The typical data flow: tracking software reads TLE data → calculates satellite position → sends az/el commands to rotator → sends frequency commands to radio → operator focuses on making contacts while the computer handles the mechanics.

## Building up your station over time

Satellite station equipment does not need to be acquired all at once. A practical progression:

1. **Start portable with FM:** A dual-band handheld and a handheld Arrow or Elk antenna. Total investment is modest, and you can make contacts immediately.
2. **Add a second radio for better full-duplex:** A second handheld or a mobile radio dedicated to receive improves your ability to hear your own signal and work satellites more effectively.
3. **Move to a fixed station:** Add a pair of Yagis on an az/el rotator with tracking software and CAT control. This opens up linear transponder satellites and greatly improves convenience.
4. **Optimise:** Add circularly polarised antennas, mast-mounted preamplifiers, and a sequencer. Explore QO-100 with microwave equipment or work toward an [EME station](/satellites/eme-moonbounce).

## See also

- [Amateur Radio Satellites](/satellites/amateur-satellites) — Satellite types and making your first contact
- [Satellite Tracking](/satellites/satellite-tracking) — Software and tools for predicting passes
- [EME / Moonbounce](/satellites/eme-moonbounce) — Equipment and techniques for Earth-Moon-Earth communication
- [Antennas Overview](/antennas/overview) — General antenna information
- [Satellites & Space Overview](/satellites/overview) — Category overview
