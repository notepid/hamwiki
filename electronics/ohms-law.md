---
title: Ohm's Law
description: The foundational equation relating voltage, current, and resistance in amateur radio circuits
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, beginner
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Ohm's Law

Ohm's Law is the single most important equation in electronics and the one you will use more than any other in amateur radio. It describes the relationship between voltage, current, and resistance in an electrical circuit, and it forms the basis for nearly every calculation you will encounter — from sizing power supply wiring to understanding receiver sensitivity.

## The law

Ohm's Law states that the current through a conductor between two points is directly proportional to the voltage across those points and inversely proportional to the resistance:

**V = I × R**

Where:
- **V** = voltage in volts (V)
- **I** = current in amperes (A)
- **R** = resistance in ohms (Ω)

This can be rearranged to solve for any of the three quantities:

**I = V / R** (to find current)
**R = V / I** (to find resistance)

### The Ohm's Law triangle

A popular memory aid is the "Ohm's Law triangle." Draw a triangle with **V** at the top and **I** and **R** at the bottom corners. Cover the quantity you want to find: if you cover V, you see I × R; cover I, you see V over R; cover R, you see V over I.

## Power formulas

By combining Ohm's Law with the basic power equation (**P = V × I**), you get a family of related formulas:

| To find | Formula | Alternative |
|---------|---------|-------------|
| Power | P = V × I | P = I² × R  or  P = V² / R |
| Voltage | V = I × R | V = P / I  or  V = √(P × R) |
| Current | I = V / R | I = P / V  or  I = √(P / R) |
| Resistance | R = V / I | R = P / I²  or  R = V² / P |

You do not need to memorise all twelve variations. If you know V = I × R and P = V × I, you can derive the rest.

## Practical examples

### Sizing a power supply

Your HF transceiver draws 22 A on transmit and requires 13.8 V. Using P = V × I:

**P = 13.8 × 22 = 303.6 W**

You need a power supply rated for at least 304 W — in practice you would choose one with some margin, perhaps 350–400 W.

### Choosing wire gauge

You are running a 3-metre cable from your power supply to your transceiver at 22 A. If the cable has a total resistance (both conductors) of 0.05 Ω, the voltage drop is:

**V = I × R = 22 × 0.05 = 1.1 V**

That means only 12.7 V arrives at the transceiver instead of 13.8 V — likely too low for reliable operation. You would need thicker wire (lower resistance) to keep the voltage drop under about 0.5 V.

### Finding current through a resistor

A 470 Ω resistor has 9 V across it. The current flowing through it is:

**I = V / R = 9 / 470 = 0.0191 A ≈ 19.1 mA**

And the power dissipated by the resistor:

**P = V × I = 9 × 0.0191 = 0.172 W**

A quarter-watt (0.25 W) resistor would be sufficient, though using a half-watt resistor gives a comfortable safety margin.

## Series circuits

In a **series circuit**, components are connected end-to-end so the same current flows through all of them. Key rules:

- **Current** is the same through every component: I_total = I₁ = I₂ = I₃
- **Voltage** divides among the components: V_total = V₁ + V₂ + V₃
- **Resistance** adds up: R_total = R₁ + R₂ + R₃

### Voltage dividers

A common application of series resistors is the **voltage divider** — two resistors in series across a voltage source where you tap the voltage at the junction between them. The output voltage is:

**V_out = V_in × R₂ / (R₁ + R₂)**

Voltage dividers appear everywhere in radio circuits: biasing transistor stages, setting reference voltages, and creating signal attenuation.

## Parallel circuits

In a **parallel circuit**, components are connected across the same two points so they share the same voltage. Key rules:

- **Voltage** is the same across every component: V_total = V₁ = V₂ = V₃
- **Current** divides among the branches: I_total = I₁ + I₂ + I₃
- **Resistance** combines by the reciprocal formula: 1/R_total = 1/R₁ + 1/R₂ + 1/R₃

For the common case of just two resistors in parallel, there is a simpler formula:

**R_total = (R₁ × R₂) / (R₁ + R₂)**

The total resistance of a parallel combination is always less than the smallest individual resistor.

### Practical application

When you connect multiple speakers or dummy loads in parallel, the total impedance drops. Two 50 Ω dummy loads in parallel present 25 Ω to the transmitter — important to know before connecting them to equipment expecting a 50 Ω load.

## Series-parallel combinations

Real circuits often combine series and parallel sections. To analyse them, simplify step by step: first combine parallel groups into their equivalent resistances, then add those in series (or vice versa) until you reduce the circuit to a single equivalent resistance. Apply Ohm's Law to the simplified circuit, then work backwards to find individual voltages and currents.

## Ohm's Law and AC circuits

Ohm's Law applies to AC circuits as well, but resistance is replaced by **impedance (Z)**, which accounts for both resistance and reactance:

**V = I × Z**

Impedance, reactance, and the behaviour of capacitors and inductors in AC circuits are covered on the [AC Circuits](/electronics/ac-circuits) page. The good news is that the structure of the calculations is identical — you are just working with more complex numbers.

## Kirchhoff's Laws

For circuits that cannot be reduced to simple series-parallel combinations, **Kirchhoff's Laws** provide additional tools:

**Kirchhoff's Current Law (KCL):** The total current entering any junction equals the total current leaving it. This is a statement of conservation of charge.

**Kirchhoff's Voltage Law (KVL):** The sum of all voltages around any closed loop in a circuit is zero. This is a statement of conservation of energy.

These laws, combined with Ohm's Law, are sufficient to analyse any linear circuit. They are especially useful when working with multi-loop circuits found in amplifier designs and filter networks.

## Common prefixes and units

Electronics uses metric prefixes extensively. The ones you will encounter most often:

| Prefix | Symbol | Multiplier | Example |
|--------|--------|-----------|---------|
| mega | M | × 1,000,000 | 3.5 MHz = 3,500,000 Hz |
| kilo | k | × 1,000 | 4.7 kΩ = 4,700 Ω |
| milli | m | × 0.001 | 50 mA = 0.050 A |
| micro | µ | × 0.000001 | 100 µV = 0.000100 V |
| nano | n | × 0.000000001 | 10 nF = 0.000000010 F |
| pico | p | × 0.000000000001 | 33 pF = 0.000000000033 F |

Being comfortable converting between these prefixes is essential for reading component values and working through calculations.

## Tips for licence exams

Ohm's Law and the related power formulas appear heavily on amateur radio licence exams worldwide. Practice these steps:

1. Identify what you are given (any two of V, I, R, P).
2. Choose the formula that uses those two known values to find the unknown.
3. Watch your units — convert milliamps to amps, kilohms to ohms, and so on before calculating.
4. Sanity-check your answer: does the magnitude make sense for the context?

## See also

- [Basic Electricity](/electronics/basic-electricity) — voltage, current, resistance, and power fundamentals
- [AC Circuits](/electronics/ac-circuits) — Ohm's Law extended to impedance
- [Filters & Theory](/electronics/filters-theory) — circuits that use resistors, capacitors, and inductors together
