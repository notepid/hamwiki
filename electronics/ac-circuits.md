---
title: AC Circuits
description: Alternating current, reactance, impedance, and resonance — the theory behind radio-frequency circuits
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, ac, impedance
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# AC Circuits

While [Basic Electricity](/electronics/basic-electricity) and [Ohm's Law](/electronics/ohms-law) introduce the fundamentals using direct current, amateur radio is fundamentally about alternating current — signals that change direction many thousands or millions of times per second. Understanding how AC behaves in circuits is essential to grasping how radios, antennas, filters, and transmission lines work.

## Alternating current fundamentals

An alternating current (AC) periodically reverses direction. The most common and most important waveform is the **sine wave**, which describes the voltage or current as a smooth, repeating oscillation. A sine wave is characterised by several properties.

### Frequency and period

**Frequency (f)** is the number of complete cycles per second, measured in **hertz (Hz)**. One cycle per second is 1 Hz. Amateur radio frequencies span from about 1.8 MHz (1,800,000 cycles per second) up to 250 GHz and beyond.

The **period (T)** is the time for one complete cycle:

**T = 1 / f**

A 7 MHz signal has a period of about 143 nanoseconds — the wave completes one full cycle in that time.

### Wavelength

**Wavelength (λ)** is the physical distance a wave travels in one cycle:

**λ = c / f**

Where c is the speed of light (approximately 300,000,000 m/s). This relationship is central to antenna design and propagation. A signal at 14 MHz has a wavelength of about 21.4 metres — which is why 14 MHz is called the "20-metre band."

### Amplitude and peak values

The **amplitude** is the maximum value of the voltage or current. For a sine wave, several measurements are commonly used:

- **Peak (V_pk):** the maximum value from zero
- **Peak-to-peak (V_pp):** the total swing from negative peak to positive peak, equal to 2 × V_pk
- **RMS (V_rms):** the root-mean-square value, which represents the DC equivalent heating effect. For a sine wave: V_rms = V_pk × 0.707 (or V_pk / √2)

RMS is the most commonly used measurement because it directly relates to power. When someone says a mains outlet provides "230 V" or "120 V," they mean RMS. When you measure the output of your transmitter, the power is calculated using RMS values.

### Phase

**Phase** describes where a waveform is in its cycle at a given instant, measured in degrees (0° to 360°) or radians. Phase differences between voltage and current are the key to understanding reactance and impedance.

## Capacitors in AC circuits

A **capacitor** stores energy in an electric field between two conductive plates separated by an insulating material (the dielectric). Capacitance is measured in **farads (F)**, though practical radio values are typically in picofarads (pF) or microfarads (µF).

In a DC circuit, a capacitor charges up and then blocks further current flow. But in an AC circuit, the voltage is constantly changing, so the capacitor is constantly charging and discharging — current flows continuously.

### Capacitive reactance

The opposition a capacitor presents to AC is called **capacitive reactance (X_C)**:

**X_C = 1 / (2π × f × C)**

Key observations: reactance decreases as frequency increases (capacitors pass high frequencies more easily) and decreases as capacitance increases. This frequency-dependent behaviour is why capacitors are fundamental to filter circuits.

In a purely capacitive circuit, the current **leads** the voltage by 90°. This phase relationship is important when calculating impedance.

## Inductors in AC circuits

An **inductor** stores energy in a magnetic field created by current flowing through a coil of wire. Inductance is measured in **henrys (H)**, with typical radio values in microhenrys (µH) or millihenrys (mH).

An inductor resists changes in current — when the current through an inductor tries to change, the inductor generates a voltage that opposes the change. In an AC circuit, the current is always changing, so the inductor constantly opposes the flow.

### Inductive reactance

The opposition an inductor presents to AC is called **inductive reactance (X_L)**:

**X_L = 2π × f × L**

Key observations: reactance increases as frequency increases (inductors block high frequencies more effectively) and increases as inductance increases. This is the opposite behaviour to capacitors.

In a purely inductive circuit, the current **lags** the voltage by 90°.

### Memory aid

The mnemonic **"ELI the ICE man"** helps remember the phase relationships: in an inductor (L), voltage (E) leads current (I); in a capacitor (C), current (I) leads voltage (E).

## Impedance

**Impedance (Z)** is the total opposition to AC current flow and combines both resistance and reactance. It is measured in ohms (Ω) but is a complex quantity with both magnitude and phase.

For a series circuit containing resistance and reactance:

**Z = √(R² + X²)**

Where X is the net reactance (X_L − X_C). If inductive reactance dominates, the net reactance is positive and the impedance is inductive. If capacitive reactance dominates, it is negative and the impedance is capacitive.

The **phase angle (φ)** between voltage and current is:

**φ = arctan(X / R)**

At 0° the circuit is purely resistive; at +90° purely inductive; at −90° purely capacitive. Real circuits fall somewhere in between.

### Why impedance matters

Impedance is central to amateur radio because efficient power transfer requires impedance matching. Your transmitter, feedline, and antenna each have characteristic impedances. When these are matched (typically at 50 Ω), maximum power reaches the antenna. Mismatches cause reflected power and increased SWR — see [Transmission Lines](/electronics/transmission-lines) for more detail.

## Resonance

When a circuit contains both inductance and capacitance, there is a frequency at which the inductive reactance exactly equals the capacitive reactance. At this frequency:

**X_L = X_C** → **2πfL = 1/(2πfC)**

Solving for the resonant frequency:

**f₀ = 1 / (2π√(LC))**

At resonance, the two reactances cancel each other, and the impedance of the circuit is purely resistive. This principle is the foundation of tuned circuits, which are used in oscillators, filters, and antenna matching networks throughout amateur radio equipment.

### Series resonant circuits

In a **series resonant circuit** (inductor and capacitor in series), the impedance at resonance drops to a minimum (equal to the resistance alone). Current flow is maximum. Series resonant circuits are used where you want to pass a specific frequency — for example, in bandpass filters.

### Parallel resonant circuits

In a **parallel resonant circuit** (inductor and capacitor in parallel), the impedance at resonance rises to a maximum. Current from the source is minimum while large circulating currents flow between the inductor and capacitor. Parallel resonant circuits are used where you want to block a specific frequency or create a high-impedance point — for example, in the tuned circuits of receivers and transmitters.

### Q factor

The **quality factor (Q)** of a resonant circuit describes how sharp or selective its response is. A high-Q circuit has a narrow bandwidth and resonates strongly at one frequency; a low-Q circuit has a broader response.

**Q = X_L / R** (at resonance)

High Q is desirable for receiver selectivity and oscillator stability. Lower Q is useful when you need broader bandwidth, such as in wideband amplifiers.

**Bandwidth** of a resonant circuit is related to Q:

**BW = f₀ / Q**

A tuned circuit with a resonant frequency of 7 MHz and a Q of 100 has a bandwidth of 70 kHz.

## Transformers

A **transformer** consists of two or more inductors (windings) sharing a common magnetic core. When AC flows through the primary winding, the changing magnetic field induces a voltage in the secondary winding.

The voltage ratio equals the turns ratio:

**V_secondary / V_primary = N_secondary / N_primary**

Transformers are used in amateur radio for impedance matching (baluns, antenna tuners), voltage conversion (power supplies), and signal coupling (IF stages in receivers). A transformer can also transform impedance — the impedance ratio is the square of the turns ratio:

**Z_secondary / Z_primary = (N_secondary / N_primary)²**

A 4:1 balun uses a 2:1 turns ratio to transform a 200 Ω antenna impedance to 50 Ω for the feedline.

## Time constants

When a resistor is combined with a capacitor (RC circuit) or an inductor (RL circuit), the circuit does not respond instantly to changes. Instead, the voltage or current changes gradually according to a **time constant (τ)**:

- **RC circuit:** τ = R × C
- **RL circuit:** τ = L / R

After one time constant, the circuit has completed about 63% of the transition. After five time constants (5τ), it is effectively complete (over 99%). Time constants are relevant to understanding audio filtering, power supply smoothing, and keying waveforms in CW operation.

## Decibels

The **decibel (dB)** is a logarithmic unit used throughout amateur radio to express ratios of power, voltage, or signal levels:

**dB = 10 × log₁₀(P₂ / P₁)** (for power ratios)
**dB = 20 × log₁₀(V₂ / V₁)** (for voltage ratios)

Useful reference points to memorise:

| dB | Power ratio | Meaning |
|----|-------------|---------|
| +3 dB | 2× | double the power |
| +6 dB | 4× | double the voltage |
| +10 dB | 10× | one order of magnitude in power |
| −3 dB | 0.5× | half the power |
| −10 dB | 0.1× | one-tenth the power |

Decibels are additive, which makes them convenient for calculating gains and losses through a chain of components. If an amplifier provides +10 dB gain and the feedline loses −2 dB, the net is +8 dB.

Special decibel references include **dBm** (referenced to 1 milliwatt), **dBW** (referenced to 1 watt), and **dBd** or **dBi** (antenna gain referenced to a dipole or isotropic radiator).

## See also

- [Basic Electricity](/electronics/basic-electricity) — DC fundamentals
- [Ohm's Law](/electronics/ohms-law) — the foundation for all circuit calculations
- [Filters & Theory](/electronics/filters-theory) — how capacitors and inductors create frequency-selective circuits
- [Oscillators](/electronics/oscillators) — circuits that generate AC signals using resonance
- [Transmission Lines](/electronics/transmission-lines) — impedance and AC behaviour in feedlines
