---
title: Basic Electricity
description: Voltage, current, resistance, and power — the foundations of electronics for amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, beginner
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Basic Electricity

Everything in amateur radio depends on electricity — from the current flowing through your transceiver's circuits to the electromagnetic waves radiating from your antenna. Understanding a few fundamental concepts will make the rest of electronics and radio theory far easier to grasp, whether you are studying for a licence exam or troubleshooting a station problem.

## Electric charge

All matter is made up of atoms, and atoms contain particles that carry **electric charge**. Protons carry a positive charge and electrons carry a negative charge. When electrons are free to move through a material — as they are in metals like copper — we have the basis for electric current.

Charge is measured in **coulombs (C)**. A single electron carries an incredibly tiny charge (about 1.6 × 10⁻¹⁹ coulombs), so in practical electronics we are always dealing with enormous numbers of electrons moving together.

## Voltage

**Voltage** (symbol **V** or **E**) is the electrical "pressure" that pushes charge through a circuit. More formally, it is the difference in electric potential energy between two points. Voltage is measured in **volts (V)**.

A helpful analogy is water pressure in a pipe: the higher the pressure, the more forcefully water flows. Similarly, a higher voltage drives more current through a circuit, all else being equal.

Common voltage sources in amateur radio include batteries (typically 12 V for mobile and portable operation), mains-powered supplies (13.8 V is the standard for most HF transceivers), and solar panels used for off-grid portable setups.

### Voltage sources in series and parallel

When you connect batteries **in series** (positive terminal to negative terminal), their voltages add up. Two 6 V batteries in series provide 12 V. When you connect them **in parallel** (positive to positive, negative to negative), the voltage stays the same but the available current capacity increases.

## Current

**Current** (symbol **I**) is the rate at which electric charge flows through a conductor. It is measured in **amperes** or **amps (A)**.

One ampere equals one coulomb of charge flowing past a point each second. In amateur radio, typical current levels range from microamps in sensitive receiver stages to tens of amps in a high-power HF transmitter's final amplifier.

### Conventional current vs. electron flow

There are two conventions. **Conventional current** flows from positive to negative — this is the direction used in most circuit diagrams and engineering analysis. **Electron flow** describes the actual movement of electrons from negative to positive. Both conventions are valid and give the same results in circuit calculations; most amateur radio references use conventional current.

## Resistance

**Resistance** (symbol **R**) is the opposition a material presents to the flow of current. It is measured in **ohms (Ω)**.

Materials with very low resistance (metals like copper, silver, and aluminium) are called **conductors**. Materials with very high resistance (glass, rubber, dry air) are called **insulators**. In between are **semiconductors** like silicon and germanium, which form the basis of modern electronic components (see [Semiconductors](/electronics/semiconductors)).

### Factors affecting resistance

The resistance of a conductor depends on four things: the material it is made of (its **resistivity**), its **length** (longer means more resistance), its **cross-sectional area** (thicker means less resistance), and its **temperature** (for most metals, resistance increases with temperature).

This is why antenna wire gauge matters — thinner wire has more resistance, which means more of your transmitted power is lost as heat rather than radiated as radio waves.

## Power

**Power** (symbol **P**) is the rate at which electrical energy is converted into another form — heat, light, radio waves, or mechanical motion. It is measured in **watts (W)**.

The basic power formula is:

**P = V × I**

Power equals voltage multiplied by current. A transceiver drawing 20 A from a 13.8 V supply is consuming 276 W of electrical power. By combining this formula with Ohm's Law (see [Ohm's Law](/electronics/ohms-law)), you can derive two additional useful forms:

**P = I² × R** and **P = V² / R**

### Power in amateur radio context

Licence classes typically specify maximum transmitter output power in watts. Understanding the relationship between power supply voltage, current draw, and output power helps you choose appropriate power supplies, fuses, and wiring for your station. It also matters for calculating RF exposure safety limits (see [RF Safety](/electronics/rf-safety)).

## Direct current (DC)

**Direct current** flows in one direction only. Batteries produce DC, and most electronic circuits inside a transceiver operate on DC. The voltage and current may be steady (like a battery) or they may vary over time (like the output of a rectifier before filtering), but the current always flows the same way.

## Alternating current (AC)

**Alternating current** periodically reverses direction. The mains electricity in your home is AC — in most countries it alternates at either 50 Hz or 60 Hz. More importantly for radio, the signals we transmit and receive are AC at radio frequencies, ranging from a few kilohertz to many gigahertz.

AC introduces additional concepts like frequency, period, wavelength, and phase that are covered in detail on the [AC Circuits](/electronics/ac-circuits) page.

## Energy and work

**Energy** is the capacity to do work. In electrical terms, energy is power multiplied by time:

**Energy (watt-hours) = P × t**

A transceiver consuming 100 W for 2 hours uses 200 watt-hours (Wh) of energy. This concept is essential when planning battery capacity for portable and emergency operation — a 100 amp-hour (Ah) battery at 12 V stores 1,200 Wh of energy.

## Conductors, insulators, and grounds

In station wiring, choosing the right conductor size and type is a practical application of basic electricity. The wire must carry the required current without excessive voltage drop or dangerous heating. The American Wire Gauge (AWG) system and metric millimetre-squared ratings specify wire sizes.

**Grounding** is critically important in amateur radio for safety, lightning protection, and RF performance. A good electrical ground provides a low-resistance path for fault currents and helps reduce unwanted RF interference. Station grounding practice is covered in more detail in the equipment and safety sections of this wiki.

## Putting it together

These four quantities — voltage, current, resistance, and power — are the building blocks for everything else in electronics. The mathematical relationships between them are formalised in [Ohm's Law](/electronics/ohms-law), which is the single most used equation in amateur radio electronics. From there, you can move on to [AC Circuits](/electronics/ac-circuits) to understand how these concepts extend to the alternating signals that make radio communication possible.

## See also

- [Ohm's Law](/electronics/ohms-law) — the fundamental circuit equation
- [AC Circuits](/electronics/ac-circuits) — extending these concepts to alternating current
- [Semiconductors](/electronics/semiconductors) — components built from semiconductor materials
- [RF Safety](/electronics/rf-safety) — understanding power and exposure limits
