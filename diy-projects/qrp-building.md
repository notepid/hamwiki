---
title: QRP Building
description: Building low-power amateur radio equipment — the history, culture, techniques, and classic circuits of QRP homebrew
published: true
date: 2026-04-05T09:30:00.000Z
tags: diy, qrp, homebrew, building, low-power, cw
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# QRP Building

QRP — operating at low power, typically 5 watts or less for CW and 10 watts or less for SSB — is one of the most active and creative areas of amateur radio construction. The appeal is straightforward: at low power levels, circuits are simpler, components are cheaper, heat management is easier, and safety concerns are reduced. This makes QRP an ideal playground for learning to build, and it has produced some of the most elegant and widely replicated radio designs in the hobby.

But QRP building is more than a stepping stone — it is a discipline in its own right. Making contacts across continents with a radio you built yourself, running on a few watts or even milliwatts, is one of the most satisfying experiences in amateur radio.

## What counts as QRP?

The generally accepted QRP power limits are 5 watts output for CW (Morse code) and 10 watts PEP (peak envelope power) output for SSB (single sideband voice). Some operators push even lower into "milliwatt" territory (QRPp), where fractions of a watt are used. There is no formal regulatory definition of QRP — these are community conventions used for award programmes, contests, and general reference.

The 5-watt CW limit is a practical sweet spot: it is enough power to make reliable contacts under reasonable band conditions, while keeping circuits simple enough that a single-transistor or two-transistor output stage can deliver the power.

## A brief history of QRP homebrew

In amateur radio's earliest decades, all equipment was homebrew — there was no alternative. As commercial transceivers became available and affordable through the mid-20th century, home construction declined. But in the 1960s and 1970s, a counter-movement emerged: hams who saw value in building simple, low-power equipment and proving what could be done with it.

Doug DeMaw (W1FB) and Wes Hayward (W7ZOI) were central figures in popularising practical QRP construction, publishing designs and techniques in books and magazine articles that remain influential. Their philosophy emphasised understanding over complexity — circuits you could build, understand, modify, and repair.

The formation of QRP clubs — QRP ARCI in the United States (founded 1961), the G-QRP Club in the United Kingdom (founded 1974), and others worldwide — created communities where builders could share designs, compare results, and encourage newcomers. These clubs remain active and continue to publish original circuit designs, host construction contests, and develop kit projects.

## Building blocks of a QRP station

A QRP station is built from the same fundamental circuit blocks as any radio station, just at lower power levels. Understanding these blocks helps you read schematics, choose projects, and eventually design your own equipment.

### Oscillators

The oscillator generates the radio frequency signal. In QRP transmitters, crystal oscillators are the most common because they are stable, simple, and inexpensive. A single quartz crystal and a few components can produce a clean, stable signal on a specific frequency. Variable-frequency oscillators (VFOs) offer the ability to tune across a band but require more careful construction to maintain stability. Modern QRP designs increasingly use digital oscillator modules (Si5351 and similar synthesiser chips) controlled by microcontrollers, combining the stability of crystals with wide tuning range.

### Transmitter stages

A QRP CW transmitter can be remarkably simple. The classic progression is: crystal oscillator driving a buffer amplifier driving a power amplifier (PA), with a low-pass filter on the output to suppress harmonics. Simple single-band CW transmitters have been built with as few as two or three active components. The power amplifier in a 5-watt transmitter typically uses a single transistor (often an IRF510 MOSFET or a 2N2222/2SC1815 bipolar transistor for lower power levels), operating in class C or class E for efficiency.

### Receivers

QRP receivers range from simple to sophisticated. The **direct conversion receiver** (DCR) is a favourite of QRP builders because it is simple to construct and performs surprisingly well for CW and SSB. A DCR mixes the incoming signal directly with a local oscillator at the same frequency, producing audio output without intermediate frequency stages. The result is a receiver with fewer components than a superhet but some practical trade-offs (audio image response and susceptibility to strong-signal overload).

More ambitious builders construct **superhet (superheterodyne) receivers**, which convert the incoming signal to an intermediate frequency (IF) before detection. Superhets offer better selectivity and image rejection but require more components and careful alignment.

### Filters

Filters are essential for both transmitters and receivers. On the transmit side, **low-pass filters** remove harmonic energy that would otherwise be radiated as spurious emissions — this is not optional, it is a regulatory requirement. A typical QRP transmitter output filter uses a few inductors and capacitors in a standard filter topology (Chebyshev or Butterworth designs are common). On the receive side, **crystal filters** or **LC filters** provide selectivity, allowing you to hear the desired signal while rejecting interference.

### Keying

For CW transmitters, the keying circuit controls when the transmitter is on (key down) and off (key up). Good keying design shapes the transmitted signal to avoid clicks and splatter — a transmitter that turns on and off abruptly generates unwanted bandwidth. Simple RC shaping networks on the keying line solve this effectively.

## Classic QRP designs

Several QRP designs have achieved legendary status in the homebrew community due to their simplicity, performance, and elegance:

**The Pixie.** Perhaps the simplest complete CW transceiver ever designed — just two transistors, a crystal, and a handful of passive components. The Pixie is more of a learning exercise than a serious operating radio (selectivity is minimal and power output is well under a watt), but thousands of hams have built one as their introduction to radio construction.

**The Tuna Tin 2.** Doug DeMaw's classic single-band CW transmitter, originally built inside a tuna fish can. It produces about 1 watt and demonstrates how few components are needed for a functional transmitter. The design has been replicated and adapted countless times.

**The Micro series (Micro 40, Micro 80, etc.).** Simple direct-conversion transceivers designed for single-band CW operation. These typically deliver 1–2 watts and provide a receiver with usable (if basic) performance.

**Multi-band QRP transceivers.** More ambitious designs cover multiple bands and sometimes multiple modes. These require band-switching, wider-range VFOs or synthesisers, and more sophisticated filtering, but the principles are the same as simpler radios.

## Construction methods for QRP

QRP projects use several construction techniques, each with its own advantages:

### Printed circuit boards (PCBs)

Purpose-designed PCBs offer the neatest results and the most reliable RF performance, since trace layout is optimised for the circuit. Kits always include a PCB. Individual builders can design their own using PCB layout software and have them manufactured inexpensively by online fabrication services.

### Manhattan construction

Manhattan construction uses a copper-clad board as a ground plane, with small pads (cut from the same material) glued to the surface to serve as connection points. Components are soldered between these pads. This method is fast, requires no custom PCB, produces good RF grounding, and allows easy modification. Many classic QRP designs were built this way, and it remains popular for one-off prototypes and experimental circuits.

### Dead bug (ugly) construction

In dead bug style, the ground plane is a bare copper-clad board, and components are soldered point-to-point with their leads in the air, using the ground plane for return connections. It is faster than Manhattan construction (no pads to cut and glue) but less tidy. For simple circuits and quick experiments, it works well.

### Perfboard and stripboard

General-purpose perforated boards (perfboard) or copper-strip boards (stripboard/Veroboard) can be used for audio and low-frequency circuits. They are less ideal for RF circuits because the layout is not optimised, but careful builders can make them work at HF frequencies with attention to lead lengths and grounding.

## Test equipment for QRP builders

Building QRP equipment is more rewarding and less frustrating when you have basic test equipment. The essential instruments for QRP work are:

**Multimeter.** A digital multimeter (DMM) for measuring voltage, current, and resistance is the absolute minimum. You will use it constantly during construction and troubleshooting.

**Dummy load.** A non-inductive 50-ohm resistor rated for the power you are working with. Essential for testing transmitters without radiating a signal. A simple QRP dummy load can be built from standard resistors.

**Power meter.** A device that measures RF output power. Many QRP builders construct their own using a simple diode detector circuit. Knowing your actual output power is important for both performance evaluation and regulatory compliance.

**Frequency counter or calibrated receiver.** You need to know what frequency your transmitter is actually generating. A frequency counter is the most direct method. Alternatively, a calibrated receiver (including a general-coverage SDR receiver) can be used to verify transmit frequency.

**Oscilloscope.** Not essential for simple builds, but enormously helpful for more advanced work. An oscilloscope lets you visualise waveforms — you can see the shape of your transmitted signal, verify oscillator operation, check for parasitic oscillations, and diagnose many problems that are invisible to a multimeter.

## QRP operating

Building the radio is half the story — operating it is the other half. QRP operating requires patience, good timing, and often a good antenna to compensate for the low power. CW (Morse code) is the traditional QRP mode because it is the most efficient — a CW signal can be copied at much lower signal levels than a voice signal. Digital modes like FT8 and JS8Call have become increasingly popular in the QRP community because their weak-signal capability makes contacts easy even at very low power levels.

QRP operators learn to pick their moments — calling when band conditions are favourable, choosing clear frequencies, and being persistent. Many QRP contacts are made with no more effort than a standard-power contact when conditions cooperate. The QRP community is welcoming, and many operators specifically listen for and respond to QRP stations.

## The QRP community

QRP has one of the most active and supportive communities in amateur radio. Major QRP organisations include QRP ARCI (United States), the G-QRP Club (United Kingdom), DL-QRP-AG (Germany), QRP Club Italia (Italy), VK QRP Club (Australia), and ZL QRP Group (New Zealand), among many others. These clubs publish regular journals and newsletters packed with construction articles, operating tips, and member projects.

Annual events like the Ozark QRP Expedition, the G-QRP Convention, and numerous QRP-specific contests bring the community together. QRP frequencies — informal calling frequencies on each band — are gathering points where low-power stations can find each other.

## Where to go next

- [Kit Building](/diy-projects/kit-building) — Many popular QRP designs are available as kits
- [Soldering Basics](/diy-projects/soldering-basics) — Solid soldering is essential for reliable QRP gear
- [Antenna Projects](/diy-projects/antenna-projects) — A good antenna makes QRP operating more effective
- [Oscillators](/electronics/oscillators) — The theory behind VFOs and crystal oscillators
- [Filters & Theory](/electronics/filters-theory) — Understanding the filters in your QRP rig
- [Transmitters](/electronics/transmitters) — How transmitter circuits work at any power level
- [Receivers](/electronics/receivers) — Direct conversion and superhet receiver theory
