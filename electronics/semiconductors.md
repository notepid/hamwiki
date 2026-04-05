---
title: Semiconductors
description: Diodes, transistors, and integrated circuits — the active components that make radio possible
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, semiconductors, components
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Semiconductors

Semiconductor devices are the building blocks of every modern radio. From the diodes that detect signals to the transistors that amplify them to the integrated circuits that process digital modes, understanding these components gives you a practical foundation for working with amateur radio equipment, building kits, and troubleshooting problems.

## What is a semiconductor?

A **semiconductor** is a material whose electrical conductivity falls between that of a conductor (like copper) and an insulator (like glass). Silicon is by far the most commonly used semiconductor material; germanium was common in early transistor designs and is still found in some specialised applications.

Pure semiconductor material is not particularly useful on its own. What makes semiconductors powerful is **doping** — intentionally adding tiny amounts of impurity atoms to change the material's electrical properties.

### N-type and P-type material

When silicon is doped with atoms that have one extra electron in their outer shell (such as phosphorus or arsenic), those extra electrons are free to move, creating **N-type** material — it has an abundance of negative charge carriers.

When silicon is doped with atoms that have one fewer electron (such as boron or gallium), this creates "holes" — places where an electron is missing. These holes behave as positive charge carriers, creating **P-type** material.

The magic happens when N-type and P-type materials are joined together.

## The PN junction

When P-type and N-type materials are placed in contact, a **PN junction** forms. At the boundary, electrons from the N side fill holes on the P side, creating a thin **depletion region** with no free charge carriers. This region acts as a barrier to further current flow.

Applying a voltage in the **forward** direction (positive to P, negative to N) reduces the barrier and allows current to flow — the junction conducts. Applying voltage in the **reverse** direction widens the barrier and blocks current flow. This one-way behaviour is the basis of all semiconductor devices.

## Diodes

A **diode** is the simplest semiconductor device — a single PN junction with two terminals (anode and cathode). It allows current to flow in one direction and blocks it in the other.

### Forward voltage drop

When forward-biased, a silicon diode drops approximately 0.6–0.7 V across it. Germanium diodes drop about 0.2–0.3 V. This voltage drop is essentially constant regardless of the current flowing (within the diode's ratings).

### Common diode types in amateur radio

**Signal diodes** (such as 1N4148) are small, fast diodes used for switching and signal detection. They appear in receiver detector stages, mixer circuits, and protection circuits.

**Rectifier diodes** (such as 1N4001 through 1N4007) are designed to handle larger currents and are used in power supplies to convert AC to DC.

**Zener diodes** are designed to conduct in reverse at a specific, controlled voltage. They are used as voltage regulators and references — a 12 V Zener will maintain approximately 12 V across its terminals regardless of current variations. You will find them protecting sensitive circuits and providing stable reference voltages.

**Schottky diodes** use a metal-semiconductor junction instead of a PN junction, giving them a lower forward voltage drop (around 0.2–0.3 V) and very fast switching. They are used in high-frequency mixers, RF detectors, and efficient power supply rectifiers.

**Varactor diodes** (also called varicap diodes) are designed so their junction capacitance changes with applied reverse voltage. They are used in voltage-controlled oscillators (VCOs) and electronic tuning circuits — many modern transceivers use varactors to tune across a band without mechanical variable capacitors.

**LEDs** (light-emitting diodes) convert electrical energy directly into light. Beyond front-panel indicators, LEDs are used in optocouplers for electrical isolation between circuits.

## Transistors

A **transistor** is a semiconductor device with three terminals that can amplify signals or act as an electronic switch. Transistors revolutionised electronics and are the reason modern transceivers can be small, reliable, and affordable.

### Bipolar junction transistors (BJTs)

A BJT consists of three layers of semiconductor material forming two PN junctions. The three terminals are the **base (B)**, **collector (C)**, and **emitter (E)**.

**NPN transistors** have an N-P-N structure. A small current flowing into the base allows a much larger current to flow from collector to emitter. NPN types are the most common in amateur radio circuits.

**PNP transistors** have a P-N-P structure. A small current flowing out of the base allows a larger current to flow from emitter to collector. PNP transistors are used where the circuit requires a device that controls current flow in the opposite sense to an NPN.

The key property of a BJT is **current gain (β or h_FE)** — the ratio of collector current to base current. Typical values range from 50 to 300. A transistor with β = 100 allows 100 mA of collector current for every 1 mA of base current.

BJTs are used as small-signal amplifiers in receiver front ends, audio amplifiers, and switching circuits. They are also found in some lower-power transmitter stages.

### Field-effect transistors (FETs)

FETs use an electric field (voltage) to control current flow, rather than a current as in BJTs. This gives them very high input impedance — they draw almost no current from the signal source.

**JFETs** (junction FETs) have three terminals: **gate (G)**, **drain (D)**, and **source (S)**. The voltage on the gate controls the current flowing from drain to source. JFETs are commonly used in the front-end amplifiers of receivers because their high input impedance and low noise make them excellent for amplifying weak signals.

**MOSFETs** (metal-oxide-semiconductor FETs) use an insulated gate, giving them even higher input impedance than JFETs. They come in two varieties: **enhancement mode** (normally off, turned on by gate voltage) and **depletion mode** (normally on, turned off by gate voltage).

Power MOSFETs are widely used in modern amateur radio transmitter final amplifier stages. The popular LDMOS (laterally diffused MOSFET) transistors can deliver hundreds of watts at HF frequencies with good linearity. Many modern solid-state HF amplifiers use LDMOS devices.

### Comparing BJTs and FETs

| Property | BJT | FET |
|----------|-----|-----|
| Input impedance | Moderate (kΩ) | Very high (MΩ to GΩ) |
| Controlled by | Base current | Gate voltage |
| Noise at RF | Moderate | Low (especially JFETs) |
| High-power RF | Limited | Excellent (LDMOS) |
| Switching speed | Fast | Very fast (MOSFETs) |

Both types are found throughout amateur radio equipment, each chosen for the properties that best suit the specific circuit application.

## Integrated circuits

An **integrated circuit (IC)** combines many transistors, diodes, resistors, and capacitors on a single chip of silicon. ICs range from simple operational amplifiers containing a few dozen transistors to complex microprocessors containing billions.

### Common ICs in amateur radio

**Operational amplifiers (op-amps)** are versatile building blocks used for audio amplification, active filtering, signal conditioning, and voltage regulation. A single op-amp IC like the LM358 or NE5532 can replace many discrete components.

**Voltage regulators** (such as the 78xx series for positive voltages or LM317 adjustable regulators) provide stable DC output voltage from a higher, varying input. They are essential in power supplies.

**Mixer ICs** (such as the NE602/SA612) combine two signals to produce sum and difference frequencies, a fundamental operation in superheterodyne receivers.

**Digital signal processors (DSPs)** and **microcontrollers** handle the digital processing in modern software-defined radios (SDRs), digital mode interfaces, and transceiver control systems.

**Direct digital synthesis (DDS) ICs** (such as the AD9850 or AD9951) generate precise, digitally controlled frequencies and are used in the local oscillators of many modern transceivers and homebrew projects.

## Semiconductor handling and safety

MOSFETs and some ICs are sensitive to **electrostatic discharge (ESD)**. Static electricity from your body can permanently damage the thin gate oxide layer. When handling sensitive components, use an ESD wrist strap, work on an antistatic mat, and avoid touching the pins directly. Store sensitive components in antistatic bags.

Transistors and diodes can also be damaged by excessive heat during soldering. Use a suitable soldering iron temperature, work quickly, and consider using a heat sink clip on the leads when soldering near the component body.

## Identifying semiconductor packages

Semiconductors come in a variety of physical packages. Through-hole packages like TO-92 (small transistors), TO-220 (power transistors and regulators), and DIP (dual in-line package for ICs) are common in hobbyist projects and kits. Surface-mount packages like SOT-23, SOIC, and QFN are used in commercial equipment and increasingly in homebrew construction as builders gain surface-mount soldering skills.

## See also

- [Basic Electricity](/electronics/basic-electricity) — voltage, current, and resistance fundamentals
- [Oscillators](/electronics/oscillators) — circuits that use transistors to generate signals
- [Transmitters](/electronics/transmitters) — how transistors amplify RF to transmission power levels
- [Receivers](/electronics/receivers) — how semiconductor devices detect and amplify weak signals
