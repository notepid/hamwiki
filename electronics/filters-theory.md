---
title: Filter Theory
description: Low-pass, high-pass, band-pass, and notch filters — how frequency-selective circuits work in amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, filters, circuits
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Filter Theory

Filters are circuits that pass certain frequencies while attenuating others. They are everywhere in amateur radio — in your transmitter to ensure a clean signal, in your receiver to select one station from thousands, in your power supply to smooth rectified AC, and in your antenna system to suppress harmonics. Understanding the four basic filter types and how they are built gives you practical insight into how your equipment works and how to solve interference problems.

## Why filters matter

Without filters, a transmitter would radiate harmonics and spurious signals across the spectrum, causing interference to other services. A receiver without filters would hear every signal at once, making communication impossible. Filters make selective, clean radio communication possible.

## The four basic filter types

### Low-pass filter (LPF)

A **low-pass filter** passes frequencies below a specified **cutoff frequency** and attenuates frequencies above it. The cutoff frequency is conventionally defined as the point where the output power drops to half (−3 dB) of the passband level.

In amateur radio, low-pass filters are commonly used at the output of transmitters to suppress harmonics. A transmitter operating on 14 MHz will generate harmonics at 28 MHz, 42 MHz, 56 MHz, and so on. A low-pass filter with a cutoff around 30 MHz will pass the desired 14 MHz signal while strongly attenuating the harmonics — preventing interference to services on higher frequencies.

The simplest low-pass filter is a single resistor and capacitor (RC), but practical radio filters use networks of inductors and capacitors (LC) for sharper cutoff and lower loss.

### High-pass filter (HPF)

A **high-pass filter** passes frequencies above its cutoff frequency and attenuates those below it. High-pass filters are useful for preventing strong broadcast signals (AM, FM, or TV) from overloading an amateur receiver. If a powerful broadcast station near your home is causing interference, a high-pass filter at the receiver input can help.

### Band-pass filter (BPF)

A **band-pass filter** passes a specific range of frequencies (the passband) and attenuates frequencies both above and below. The width of the passband is called the **bandwidth**.

Band-pass filters are fundamental to receiver design. In a superheterodyne receiver, band-pass filters at the intermediate frequency (IF) stage determine the receiver's selectivity — how well it separates the desired signal from adjacent signals. A narrow CW filter might have a bandwidth of 250–500 Hz, while an SSB filter typically passes about 2.4 kHz, and an FM filter might be 12–15 kHz wide.

### Band-stop (notch) filter

A **band-stop filter** (also called a notch filter or band-reject filter) attenuates a specific range of frequencies while passing everything else. Notch filters are invaluable for removing a single interfering signal — for example, a persistent carrier on a frequency near your desired station.

Many modern transceivers include adjustable notch filters (sometimes implemented digitally as DSP notch filters) that the operator can tune to eliminate a specific interferer in real time.

## Filter components

### Passive filters

Passive filters use only **resistors (R)**, **capacitors (C)**, and **inductors (L)** — no active devices or power supply needed. LC filters are the standard for RF applications because they can handle significant power levels and introduce minimal noise.

A capacitor in a filter passes high frequencies (its reactance decreases with frequency) while blocking low frequencies. An inductor does the opposite — it passes low frequencies and blocks high frequencies. By combining these elements in various arrangements, you create the four filter types described above.

### Active filters

Active filters use an **operational amplifier** (op-amp) or other active device along with resistors and capacitors. They are primarily used at audio frequencies — for example, in the audio output stage of a receiver to shape the audio response, or in CW audio peaking filters.

Active filters can provide gain (unlike passive filters, which can only attenuate) and can achieve filter characteristics that would be difficult with passive components alone at audio frequencies. They are generally not used at RF because op-amps cannot operate at radio frequencies.

### Crystal and ceramic filters

For very sharp selectivity at IF frequencies, **crystal filters** and **ceramic filters** use the mechanical resonance of quartz crystals or ceramic resonators. These filters can achieve very narrow bandwidths with steep skirts (rapid transition from passband to stopband).

Crystal filters are the traditional technology for high-performance IF selectivity in amateur transceivers. A typical 9 MHz crystal filter for SSB reception has a bandwidth of 2.4 kHz with shape factors (the ratio of bandwidth at −60 dB to bandwidth at −6 dB) of 2:1 or better.

### Mechanical filters

**Mechanical filters** use small metal resonators coupled by wires to achieve extremely selective filtering, typically at 455 kHz IF frequencies. Originally developed by Collins Radio, mechanical filters are prized for their exceptional shape factor and stability. While no longer in production, they remain sought after by enthusiasts building high-performance receivers.

### DSP filters

Modern transceivers increasingly use **digital signal processing (DSP)** to implement filters in software. The analogue signal is converted to digital samples by an analogue-to-digital converter (ADC), processed mathematically, and then converted back to analogue.

DSP filters offer tremendous flexibility — the same hardware can provide variable bandwidths, adjustable notch filters, noise reduction, and other features that would require many separate physical filters. Software-defined radios (SDRs) rely almost entirely on DSP filtering.

## Filter design parameters

### Cutoff frequency

The frequency at which the filter's response has fallen by 3 dB from the passband level. For band-pass filters, there are two cutoff frequencies defining the lower and upper edges of the passband.

### Rolloff rate

How quickly the filter attenuates signals beyond the cutoff frequency, measured in **decibels per octave** (dB/octave) or **decibels per decade**. A single-element (first-order) filter rolls off at 6 dB per octave (20 dB per decade). Each additional filter element adds another 6 dB per octave. A 5-element low-pass filter rolls off at 30 dB per octave — much sharper.

### Insertion loss

The amount of signal lost passing through the filter in the passband. Good LC filters have very low insertion loss (fractions of a dB). Crystal filters typically have 2–6 dB of insertion loss. Minimising insertion loss is important in receiver front ends where every fraction of a dB affects sensitivity.

### Shape factor

For band-pass filters, the **shape factor** describes the steepness of the filter skirts. It is the ratio of bandwidth at a deep attenuation level (typically −60 dB) to bandwidth at a shallow level (typically −6 dB). A perfect rectangular filter would have a shape factor of 1:1. Practical crystal filters achieve shape factors around 1.5:1 to 2:1. LC filters are broader, with shape factors around 4:1 to 10:1.

### Ripple

Some filter designs allow small variations in response within the passband (ripple) in exchange for a sharper cutoff. **Chebyshev** filters exhibit passband ripple; **Butterworth** filters have a maximally flat passband with no ripple but a gentler rolloff.

## Filter design families

Different mathematical approaches to filter design yield different performance trade-offs:

**Butterworth** — maximally flat passband, moderate rolloff. A good general-purpose choice when uniform passband response matters.

**Chebyshev** — steeper rolloff than Butterworth for the same order, at the cost of ripple in the passband. Useful when sharp cutoff is more important than flat passband response.

**Elliptic (Cauer)** — the steepest rolloff for a given filter order, but with ripple in both the passband and stopband. Used where maximum rejection near the cutoff is critical.

**Bessel** — maximally flat group delay, meaning signals passing through maintain their waveform shape. Useful for data transmission where waveform distortion must be minimised.

## Practical filter applications in amateur radio

### Transmitter output filtering

Regulations require that harmonic and spurious emissions be suppressed well below the fundamental signal level. A multi-section low-pass filter at the transmitter output is standard practice. Commercial transceivers typically switch between multiple LPFs, selecting the appropriate filter for the band in use.

### Receiver front-end filtering

Band-pass filters in the receiver front end prevent strong out-of-band signals from overloading the first mixer or amplifier stage. This improves resistance to intermodulation distortion and blocking.

### IF filtering and selectivity

The IF filter determines what you hear. Choosing the right bandwidth for the mode — wide for FM, medium for SSB, narrow for CW — is a key operator skill. Many radios allow you to select between multiple IF filter bandwidths.

### Audio filtering

After the signal is demodulated to audio, additional filtering can improve readability. Audio band-pass filters, CW peaking filters, and DSP noise reduction all work at the audio stage.

### Power supply filtering

Rectified AC must be smoothed by filter capacitors (and sometimes inductors) before it can power sensitive radio equipment. Inadequate power supply filtering produces ripple that can modulate your transmitted signal (hum) or degrade receiver performance.

## See also

- [AC Circuits](/electronics/ac-circuits) — reactance, impedance, and resonance fundamentals
- [Receivers](/electronics/receivers) — how filters create receiver selectivity
- [Transmitters](/electronics/transmitters) — output filtering for clean signals
- [Oscillators](/electronics/oscillators) — filters clean up oscillator output
