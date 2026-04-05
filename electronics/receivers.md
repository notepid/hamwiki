---
title: Radio Receivers
description: How radio receivers work — from crystal sets to superheterodyne to modern SDR architectures
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, receivers
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Radio Receivers

A radio receiver takes the weak electromagnetic signals captured by an antenna and converts them into audio or data that a human or computer can use. Receiver design has evolved enormously since the earliest days of radio, but the fundamental challenge remains the same: pick out one desired signal from among thousands on the air while rejecting noise, interference, and signals on nearby frequencies.

## What a receiver must do

Every receiver, regardless of architecture, must perform several jobs: **select** the desired frequency from all others present at the antenna, **amplify** the tiny received signal (often measured in microvolts) to a usable level, and **demodulate** it — recover the original information (voice, CW, data) from the modulated RF carrier. How well a receiver does these jobs, and how it handles strong unwanted signals while doing them, defines its performance.

## Receiver architectures

### The crystal set

The earliest receivers used no amplification at all. A **crystal set** consists of a tuned LC circuit connected to the antenna, with a diode (originally a galena crystal with a "cat's whisker" wire contact) to detect the AM envelope. The detected audio drives high-impedance headphones directly.

Crystal sets are instructive because they clearly show the basic functions — tuning, detection, and audio output — without any complexity. They remain a popular first construction project for new amateurs and electronics learners.

### Tuned radio frequency (TRF) receiver

The **TRF receiver** adds amplification stages before the detector. Multiple tuned amplifier stages provide gain and selectivity, but every stage must be tuned to the same frequency, which makes tuning across a band cumbersome (multiple capacitors must track together). TRF receivers were largely superseded by the superheterodyne in the 1930s but the concept helps understand why frequency conversion is so valuable.

### The superheterodyne receiver

The **superheterodyne** ("superhet") has been the dominant receiver architecture since its invention and remains the basis for most amateur transceivers today. Its key innovation is **frequency conversion**: the incoming signal is mixed with a local oscillator (LO) to produce an **intermediate frequency (IF)** signal that is always at the same fixed frequency, regardless of what frequency the receiver is tuned to.

#### How it works

1. **RF amplifier (optional):** A low-noise amplifier boosts the antenna signal and provides some initial selectivity through a band-pass filter. Not all receivers include a separate RF amplifier.

2. **Mixer:** The mixer combines the received signal with the local oscillator signal. The output contains signals at the sum and difference of the two input frequencies. One of these (typically the difference) is the desired IF.

3. **IF filter and amplifier:** The IF signal passes through a narrow band-pass filter that provides the receiver's main selectivity — this is where the receiver separates the desired station from adjacent signals. The filtered IF signal is then amplified. Using a fixed IF frequency means this filter can be optimised for one frequency, achieving excellent selectivity.

4. **Demodulator (detector):** The demodulator recovers the audio or data from the IF signal. Different demodulator types are used for different modes: an envelope detector for AM, a product detector for SSB and CW, and a discriminator or quadrature detector for FM.

5. **Audio amplifier:** The recovered audio is amplified to drive headphones or a speaker.

#### Intermediate frequency choices

Common IF frequencies in amateur equipment include 455 kHz, 9 MHz, 10.7 MHz, and 45 MHz. Some high-performance receivers use multiple conversions — for example, a first IF at 45 MHz for good image rejection, then a second conversion down to 9 MHz where crystal filters provide sharp selectivity, and sometimes a third conversion to a low frequency for DSP processing.

#### Image frequency

A potential weakness of the superhet is the **image frequency** — an unwanted signal that is spaced from the desired signal by twice the IF frequency and would also convert to the IF. For example, if the IF is 9 MHz and you are tuned to 14.2 MHz with the LO at 23.2 MHz, a signal at 32.2 MHz would also produce a 9 MHz difference. Front-end filtering before the mixer must suppress the image frequency adequately. Higher first IF frequencies make image rejection easier because the image is farther from the desired signal.

### Direct conversion receivers

A **direct conversion** (DC) receiver mixes the incoming signal directly to audio — the IF is 0 Hz (baseband). The local oscillator runs at the same frequency as the received signal. The mixer output is the audio-frequency difference between the signal and the LO.

Direct conversion receivers are simple and popular for homebrew projects. They avoid the image problem entirely but have their own challenges: audio images (both sidebands are heard simultaneously unless a phasing method is used), LO radiation from the antenna, and susceptibility to strong-signal effects. Many SDR receiver designs use a form of direct conversion with I/Q (in-phase and quadrature) processing to resolve the sideband ambiguity.

### Software-defined radio (SDR)

A **software-defined radio** digitises the RF signal as early as possible and performs most or all of the receiver functions — filtering, frequency conversion, demodulation, and audio processing — in software (DSP). In the most direct approach, an analogue-to-digital converter (ADC) samples the antenna signal directly. More commonly, the signal is first down-converted to a lower frequency before digitisation.

SDR advantages include: infinitely flexible filtering (change bandwidth and shape with a mouse click), ability to display a wide spectrum simultaneously (panadapter/waterfall), easy implementation of multiple modes, and the ability to upgrade performance through software updates.

Popular SDR platforms in amateur radio range from inexpensive USB dongles (RTL-SDR for receive only) to high-performance transceivers like the Flex Radio series, Apache Labs ANAN, and Hermes Lite.

## Key receiver performance specifications

### Sensitivity

**Sensitivity** measures the weakest signal a receiver can usefully detect. It is typically specified as the minimum signal level required to produce a certain signal-to-noise ratio (SNR) at the audio output — for example, 0.15 µV for 10 dB S+N/N. Better sensitivity means you can hear weaker, more distant stations.

Sensitivity is primarily determined by the **noise figure** of the receiver's front end. A low-noise amplifier (LNA) at the front of the receiver minimises the noise added by the receiver itself. On the lower HF bands (below about 10 MHz), atmospheric and man-made noise typically exceeds the receiver's own noise floor, so extreme sensitivity is less important than good dynamic range. At VHF and above, receiver sensitivity becomes more critical because external noise levels are much lower.

### Selectivity

**Selectivity** is the ability to separate the desired signal from adjacent signals. It is determined primarily by the IF filter bandwidth and shape factor. A receiver with good selectivity lets you hear one SSB station while rejecting another only 3 kHz away.

Selectivity and bandwidth are trade-offs: narrower bandwidth improves rejection of adjacent signals but can also cut off parts of the desired signal or make tuning more critical. Operators typically choose bandwidth to match the mode — about 2.4 kHz for SSB, 500 Hz or less for CW, and 12–15 kHz for FM.

### Dynamic range

**Dynamic range** describes the receiver's ability to handle both very weak and very strong signals simultaneously without overloading or producing spurious responses. On a crowded amateur band, the desired signal might be barely detectable while a contest station a few kHz away is enormously strong.

**Blocking dynamic range** measures how strong a nearby signal can be before it compresses (reduces) the receiver's response to the desired signal.

**Intermodulation dynamic range (IMD DR)** measures how strong nearby signals can be before the receiver generates spurious mixing products (intermodulation distortion) that can sound like real signals.

A receiver with excellent dynamic range allows comfortable operation on crowded bands without having to constantly readjust the RF gain or attenuator.

### AGC — automatic gain control

**AGC** automatically adjusts the receiver's gain so that weak signals are amplified to a comfortable listening level while strong signals are attenuated to prevent overloading. Good AGC responds quickly enough to handle rapid signal changes (as in contest pile-ups) without excessive "pumping" or distortion. Most transceivers offer selectable AGC time constants (fast, medium, slow) and an AGC-off mode.

## Receiver controls relevant to operators

**RF gain:** Adjusts the amplification of the front-end and IF stages. Reducing RF gain can improve the receiver's handling of strong signals on a busy band.

**IF shift / passband tuning:** Moves the IF filter passband relative to the displayed frequency, helping to avoid interference on one side of the desired signal.

**Notch filter:** Attenuates a narrow slice of the audio or IF spectrum to eliminate a single interfering carrier.

**Noise blanker (NB):** Mutes the receiver for the brief duration of impulse noise (such as ignition noise or electrical switch clicks). Effective against repetitive pulse-type interference.

**Noise reduction (NR):** A DSP function that estimates and subtracts background noise from the audio output, improving readability of weak signals.

**Attenuator:** Inserts a fixed amount of signal reduction (typically 6, 12, or 20 dB) before the first amplifier stage. Useful when very strong signals are overloading the front end.

**Preamplifier:** Adds extra gain at the front end for improved sensitivity. Useful on VHF/UHF or on the higher HF bands where atmospheric noise is low. On the lower HF bands, a preamp often degrades performance by amplifying atmospheric noise along with the signal.

## See also

- [Transmitters](/electronics/transmitters) — the other half of the transceiver
- [Modulation](/electronics/modulation) — how information is encoded for transmission and decoded by the receiver
- [Filters & Theory](/electronics/filters-theory) — the filters that create receiver selectivity
- [Oscillators](/electronics/oscillators) — local oscillators in receiver designs
- [Semiconductors](/electronics/semiconductors) — the active devices in receiver circuits
