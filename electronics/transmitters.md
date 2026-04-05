---
title: Radio Transmitters
description: How radio transmitters generate, modulate, and amplify RF signals for amateur radio communication
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, transmitters
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Radio Transmitters

A radio transmitter converts information — your voice, a digital data stream, or a Morse code key press — into a radio-frequency signal and delivers it to the antenna at sufficient power to communicate. Every transmitter, from a simple QRP kit putting out a few watts to a kilowatt amplifier station, performs the same basic functions: generate a stable frequency, modulate it with information, amplify it to the desired power level, and filter the output to keep the signal clean.

## Basic transmitter block diagram

A typical transmitter consists of these stages, roughly in order from signal generation to the antenna:

**Oscillator** → **Buffer/driver** → **Modulator** → **Power amplifier (PA)** → **Output filter** → **Antenna**

Some transmitters rearrange or combine stages, but these functions are always present. Modern transceivers that share circuitry between transmit and receive may implement these stages differently from a standalone transmitter, but the underlying principles are the same.

## The oscillator stage

The oscillator generates the radio-frequency carrier signal. In a simple CW transmitter, this might be a single crystal oscillator on the desired operating frequency. In a full-featured transceiver, the oscillator system is typically a synthesiser (PLL, DDS, or a combination) that can generate any frequency across the amateur bands.

The oscillator must be **frequency-stable** — drift causes your signal to wander, making it difficult for others to receive and potentially causing interference. See [Oscillators](/electronics/oscillators) for a detailed look at how different oscillator types achieve stability.

## Buffer and driver stages

The oscillator output is typically very low power — milliwatts at most. Before it can drive the power amplifier, it must be amplified by one or more **buffer** and **driver** stages.

The **buffer** serves a dual purpose: it amplifies the signal and isolates the oscillator from the stages that follow. Without a buffer, changes in the load (such as antenna SWR variations) could pull the oscillator frequency. The buffer presents a constant, light load to the oscillator regardless of what happens downstream.

The **driver** stage further amplifies the signal to the level needed to drive the power amplifier's input — typically from tens of milliwatts to a few watts, depending on the PA design.

## Modulation

**Modulation** is the process of encoding information onto the carrier signal. The type of modulation determines the mode of operation. Modulation is covered in detail on the [Modulation](/electronics/modulation) page, but here is how it fits into the transmitter chain:

**CW (Morse code):** The simplest form — the carrier is simply switched on and off (keyed). Keying can happen at the oscillator, buffer, or PA stage. Good keying waveform shaping (controlled rise and fall times) prevents key clicks that would cause wideband interference.

**AM (amplitude modulation):** The carrier amplitude is varied in proportion to the audio signal. In a traditional AM transmitter, the modulator (essentially a high-power audio amplifier) varies the PA's supply voltage.

**SSB (single sideband):** Only one sideband of the AM signal is transmitted, with the carrier suppressed. SSB is generated at a low power level using a **balanced modulator** and sideband filter, then amplified by linear stages. SSB is the dominant voice mode on HF because it uses spectrum and power far more efficiently than AM.

**FM (frequency modulation):** The carrier frequency is varied in proportion to the audio signal while the amplitude stays constant. FM is the standard voice mode on VHF and UHF. Modulation is typically applied at the oscillator or synthesiser stage by varying the control voltage.

## Power amplifiers

The **power amplifier (PA)** is the final stage that brings the signal up to the desired output power. PAs range from a fraction of a watt in QRP rigs to 1,500 W (the legal limit in many countries) in high-power stations.

### Amplifier classes

PA stages are categorised by how much of each RF cycle the active device conducts:

**Class A:** The device conducts for the full 360° of each cycle. This produces the most linear (faithful) amplification but is the least efficient — theoretical maximum efficiency is 50%, practical efficiency around 25–35%. Class A is used in low-power driver stages where linearity matters more than efficiency.

**Class AB:** The device conducts for more than 180° but less than 360° of each cycle. This is the standard operating class for linear SSB power amplifiers, offering a good compromise between linearity and efficiency (typically 50–65%). Most amateur HF transceivers operate their PA in Class AB.

**Class B:** The device conducts for exactly 180° of each cycle. Two Class B devices in a push-pull arrangement can produce a full sine wave with higher efficiency than Class A. Used in some audio amplifiers and RF stages.

**Class C:** The device conducts for less than 180° of each cycle. Very efficient (up to 70–80%) but highly nonlinear — suitable only for CW and FM where the signal amplitude does not carry information. A Class C amplifier would severely distort an SSB signal.

**Class D, E, and F:** Switching amplifier classes where the device acts as a switch rather than a linear amplifier. These can achieve very high efficiency (90%+) and are used in some modern solid-state amplifier designs, particularly for CW and digital modes.

### Tube vs. solid-state PAs

**Vacuum tube** amplifiers dominated amateur radio for decades and remain popular in homebrew and high-power applications. Tubes are naturally suited to high-power RF because a single tube can handle hundreds or even thousands of watts. Common amateur tubes include the 6146, 572B, 3-500Z, and 8877.

**Solid-state** amplifiers use power transistors, most commonly **LDMOS MOSFETs** for HF through VHF. Modern LDMOS devices can deliver 500+ watts from a single transistor package. Solid-state amplifiers offer instant-on operation (no warm-up), lower operating voltages, greater reliability, and lighter weight. However, they are less tolerant of high SWR and require robust protection circuits.

### Amplifier protection

Power amplifiers are expensive and easily damaged. Common protection circuits include SWR protection (reducing power when reflected power is too high), over-temperature shutdown, over-current limiting, and sequencing circuits that ensure the antenna relay switches before RF is applied.

## Output filtering

The PA output contains not just the desired signal but also **harmonics** (multiples of the operating frequency) and potentially other **spurious emissions** generated by nonlinearities in the amplifier. Regulations require these to be suppressed, typically to at least 43 dB below the fundamental for amateur transmitters.

A **low-pass filter** at the transmitter output is the primary means of harmonic suppression. Modern transceivers use a bank of switched low-pass filters, automatically selecting the correct filter for the band in use. See [Filters & Theory](/electronics/filters-theory) for details on filter design.

## Transmitter performance specifications

### Output power

Measured in watts, this is the RF power delivered to a matched load (typically 50 Ω). Licence regulations specify maximum permissible power, which varies by country and licence class. Many countries allow up to 1,500 W PEP (peak envelope power) for the highest licence class.

### Frequency accuracy and stability

How closely the transmitter output matches the intended frequency, and how little it drifts over time and temperature. Modern synthesised transmitters are accurate to within a few Hz. This is critical for digital modes where frequency offsets of even 10–20 Hz can prevent decoding.

### Spectral purity

A clean transmitter output should contain only the desired signal with harmonics and spurious emissions well suppressed. The transmitter should not generate excessive broadband phase noise that might interfere with receivers on nearby frequencies.

### Linearity

For SSB and some digital modes, the amplifier chain must faithfully reproduce the amplitude variations of the modulated signal. Nonlinearity causes **intermodulation distortion (IMD)** products — unwanted signals that splatter into adjacent frequencies. A transmitter's IMD performance is specified as the level of third-order and higher distortion products relative to the desired signal, typically −25 dB to −40 dB or better.

## Transceiver integration

Most modern amateur stations use a **transceiver** — a combined transmitter and receiver sharing the same oscillator, display, and control systems. When you switch from receive to transmit, the T/R (transmit-receive) switching circuit disconnects the receiver, activates the transmitter chain, and keys the antenna relay. This happens in milliseconds and is coordinated by sequencing logic to prevent hot-switching (applying RF before the antenna relay has settled).

## See also

- [Oscillators](/electronics/oscillators) — generating the carrier frequency
- [Modulation](/electronics/modulation) — encoding information onto the carrier
- [Filters & Theory](/electronics/filters-theory) — output filtering for clean signals
- [Receivers](/electronics/receivers) — the other half of the transceiver
- [Semiconductors](/electronics/semiconductors) — transistors used in transmitter stages
- [RF Safety](/electronics/rf-safety) — safe operating practices for transmitter power levels
