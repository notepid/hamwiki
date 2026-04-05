---
title: Oscillators
description: How oscillators generate radio frequencies — LC, crystal, VFO, PLL, and DDS circuits explained
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, oscillators, circuits
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Oscillators

An oscillator is a circuit that generates a repetitive electronic signal — typically a sine wave or square wave at a specific frequency. Oscillators are fundamental to amateur radio: they generate the carrier frequency in transmitters, provide the local oscillator signal in receivers, and serve as the clock source for digital circuits. Understanding oscillator types helps you appreciate how your radio selects frequencies and why stability matters.

## How oscillation works

Every oscillator relies on two principles: **positive feedback** and an **active device** that provides gain.

A portion of the output signal is fed back to the input in phase (positive feedback). If the gain of the active device (a transistor, FET, or op-amp) is sufficient to overcome circuit losses, the signal builds up and sustains itself. The frequency of oscillation is set by a **frequency-determining element** — typically a tuned LC circuit or a crystal.

### Barkhausen criteria

For oscillation to be sustained, two conditions must be met (the Barkhausen criteria):

1. The **loop gain** must be equal to or greater than 1 (the amplifier must compensate for all losses)
2. The **total phase shift** around the feedback loop must be exactly 0° (or a multiple of 360°)

If the loop gain exceeds 1, the oscillation amplitude grows until the active device reaches its limits and natural compression stabilises the output. Most practical oscillators are designed with slightly more than unity gain and rely on this self-limiting behaviour.

## LC oscillators

**LC oscillators** use an inductor (L) and capacitor (C) as the frequency-determining elements. The resonant frequency is:

**f₀ = 1 / (2π√(LC))**

Changing either L or C changes the frequency, which is how variable-frequency oscillators (VFOs) are tuned. LC oscillators are simple and can cover wide frequency ranges, but their stability depends heavily on the physical stability of the components.

### Colpitts oscillator

The **Colpitts oscillator** uses a capacitive voltage divider (two capacitors in series) with an inductor to form the resonant circuit. Feedback is taken from the junction of the two capacitors. This is one of the most common oscillator configurations in amateur radio and is found in many VFO designs. It tends to have good frequency stability and produces a clean sine wave output.

### Hartley oscillator

The **Hartley oscillator** uses an inductive voltage divider (a tapped inductor or two inductors in series) with a capacitor. Feedback is taken from the tap on the inductor. Hartley oscillators are straightforward to build and are often used in simple receiver and transmitter projects, though they can be more susceptible to stray coupling from the tapped coil.

### Clapp oscillator

The **Clapp oscillator** is a variation of the Colpitts design with an additional series capacitor in the inductor branch. This modification improves frequency stability because the oscillation frequency becomes primarily determined by the series capacitor rather than the transistor's internal capacitances. Clapp oscillators are favoured in more demanding VFO applications.

## Crystal oscillators

A **quartz crystal** is a small piece of quartz that vibrates mechanically at a precise frequency when an electric field is applied (the piezoelectric effect). Electrically, a crystal behaves like an extremely high-Q resonant circuit — typical Q values range from 10,000 to over 100,000, compared to a few hundred for a good LC circuit.

This exceptionally high Q means crystal oscillators are far more frequency-stable than LC oscillators. The frequency is determined by the crystal's physical dimensions and the way it is cut. Common crystal frequencies for amateur radio use range from a few hundred kHz to about 200 MHz for overtone crystals.

### Fundamental and overtone operation

Crystals can oscillate at their **fundamental frequency** or at odd **overtone** frequencies (approximately 3rd, 5th, 7th harmonics of the fundamental). Overtone operation allows crystals to reach higher frequencies — a 5th-overtone crystal at 100 MHz is physically the same size as a 20 MHz fundamental crystal.

### Crystal oscillator circuits

Crystal oscillators use the same basic topologies as LC oscillators (Colpitts, Hartley, Pierce), with the crystal replacing the LC resonant circuit. The **Pierce oscillator** is especially popular in digital circuits and microcontroller clock circuits because of its simplicity — it requires just a crystal and two small capacitors.

## Variable-frequency oscillators (VFOs)

A **VFO** is an oscillator whose frequency can be changed, usually by a variable capacitor or a varactor diode. VFOs give the operator the ability to tune across a band and select any operating frequency, rather than being fixed to a single crystal frequency.

### Mechanical VFOs

Traditional VFOs use a high-quality variable capacitor connected to a stable inductor. Mechanical construction must be rigid to prevent vibration-induced frequency shifts (microphonics). Temperature compensation — using components with opposing temperature coefficients — helps maintain frequency accuracy as the equipment warms up.

Legendary VFO designs from manufacturers like Collins and Drake used precision machined components and careful thermal design to achieve remarkable stability. Homebrew VFOs remain a popular construction project for amateur builders.

### Electronic tuning with varactors

Modern VFOs often replace the mechanical variable capacitor with a **varactor diode**, whose capacitance changes with applied voltage. A stable, adjustable DC voltage (from a potentiometer or digital-to-analogue converter) tunes the oscillator electronically. This allows digital control of tuning and eliminates mechanical wear.

## Phase-locked loops (PLLs)

A **phase-locked loop** is a control system that locks an oscillator's frequency and phase to a reference signal. A PLL consists of three main parts:

1. **Voltage-controlled oscillator (VCO):** An oscillator (usually LC with varactor tuning) whose frequency depends on a control voltage
2. **Phase detector:** Compares the VCO output with a reference frequency and produces an error voltage proportional to the phase difference
3. **Loop filter:** Smooths the error voltage and feeds it back to the VCO

The VCO continuously adjusts to keep its output locked to the reference. By placing a programmable frequency divider between the VCO and the phase detector, the PLL can synthesise many different output frequencies — all locked to and as stable as the single crystal reference.

PLLs are used in many older synthesised transceivers and are still found in modern radios as part of more complex frequency generation systems.

### PLL trade-offs

PLL synthesisers can exhibit **phase noise** — small, rapid fluctuations in frequency around the desired output. Phase noise can degrade receiver performance by causing reciprocal mixing (strong nearby signals mixing with the local oscillator noise to produce interference). Good PLL design minimises phase noise through careful loop filter design and high-quality VCO components.

## Direct digital synthesis (DDS)

**Direct digital synthesis** generates a waveform numerically using a digital-to-analogue converter (DAC). A DDS IC contains a phase accumulator, a sine lookup table, and a DAC. The output frequency is set by a digital control word, allowing frequency changes that are extremely fast, fine-grained, and precise.

### Advantages of DDS

- **Fine frequency resolution:** Steps of well under 1 Hz are typical
- **Fast switching:** Frequency changes in microseconds
- **Phase continuity:** Frequency changes occur without glitches
- **Digital control:** Easily interfaced with microcontrollers

### DDS in amateur radio

Popular DDS ICs like the AD9850 and AD9951 are widely used in homebrew transmitters, signal generators, and as local oscillators in homebrew receivers. Many commercial transceivers use DDS as part of a hybrid frequency synthesis system, combining DDS with PLL techniques for optimal performance.

The maximum useful output frequency of a DDS is limited to roughly 40% of its clock frequency (the Nyquist limit). DDS output also contains spurious signals (spurs) that must be filtered — typically with a good low-pass filter following the DAC output.

## Frequency stability

Frequency stability matters because a drifting oscillator makes it difficult to stay on frequency during a QSO, can cause interference to adjacent channels, and reduces the effectiveness of narrow digital modes. Several factors affect stability:

**Temperature:** Component values change with temperature. Crystal oscillators are inherently more stable than LC oscillators. Temperature-compensated crystal oscillators (TCXOs) and oven-controlled crystal oscillators (OCXOs) provide progressively better stability for demanding applications.

**Mechanical vibration:** Physical movement can shift component values. Rigid construction and shock mounting help. This is particularly important for portable and mobile installations.

**Power supply variation:** Changes in supply voltage can pull the oscillator frequency. Voltage regulation of the oscillator supply is essential.

**Warm-up drift:** Most oscillators drift during the first few minutes after power-on as components reach thermal equilibrium. Allowing a warm-up period before operating, especially in precision applications, improves stability.

## See also

- [AC Circuits](/electronics/ac-circuits) — resonance and Q factor fundamentals
- [Semiconductors](/electronics/semiconductors) — the active devices used in oscillators
- [Transmitters](/electronics/transmitters) — how oscillator signals are amplified for transmission
- [Receivers](/electronics/receivers) — local oscillators in receiver designs
- [Filters & Theory](/electronics/filters-theory) — filtering oscillator outputs for clean signals
