---
title: Baluns and Ununs
description: Understanding baluns and ununs — managing balanced and unbalanced transitions, choking common-mode current, and impedance transformation in antenna systems
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, balun, unun, matching, impedance
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Baluns and Ununs

If you have ever connected a coaxial cable directly to a dipole, you have unknowingly created a problem that baluns are designed to solve. Baluns and ununs are devices used in antenna systems to manage the transition between different types of transmission lines and antennas, and to transform impedances. They are among the most misunderstood components in amateur radio, but understanding what they do and when you need one will improve your station's performance and help you avoid frustrating problems.

## Balanced vs. unbalanced

The terms "balanced" and "unbalanced" refer to how current flows in a transmission line or antenna relative to ground:

An **unbalanced** line has one conductor at ground potential (or connected to a shield) and the other carrying the signal. **Coaxial cable** is the most common unbalanced transmission line — the outer shield is typically grounded, and the centre conductor carries the signal.

A **balanced** line has two conductors that carry equal but opposite currents, with neither conductor at ground potential. **Ladder line** (open-wire line) is a balanced transmission line. A **dipole** is a balanced antenna — the two halves are mirror images, and current flows equally in each half.

The issue arises when you connect an unbalanced line (coax) directly to a balanced antenna (dipole). The connection creates an imbalance that can cause current to flow on the outside of the coax shield. This **common-mode current** radiates from the feedline, distorting the antenna's radiation pattern, causing RF to flow back into the shack (leading to RF interference with other equipment), and making the SWR reading unreliable.

## What is a balun?

A **balun** (from "**bal**anced to **un**balanced") is a device that provides a proper transition between a balanced system and an unbalanced system. When placed at the feed point of a dipole that is fed with coax, a balun prevents common-mode current from flowing on the outside of the coax shield.

Baluns can also provide **impedance transformation**. A 1:1 balun provides a balanced-to-unbalanced transition without changing the impedance. A 4:1 balun transforms the impedance by a factor of four (for example, converting 200 ohms balanced to 50 ohms unbalanced) while also providing the balanced/unbalanced transition.

## What is an unun?

An **unun** (from "**un**balanced to **un**balanced") transforms impedance between two unbalanced systems without changing the balance mode. For example, a 9:1 unun can transform a high-impedance unbalanced feed point (such as an end-fed wire antenna) down to approximately 50 ohms for connection to standard coax.

The key distinction: a **balun** changes the balance mode (and may also transform impedance), while an **unun** changes impedance only without altering the balance mode.

## Common-mode current: the real problem

Common-mode current is current that flows on the outside of the coax shield (or equally on both conductors of a balanced line, rather than differentially). It is the primary issue that choke baluns are designed to suppress.

Common-mode current causes several problems:

- **Feedline radiation** — the coax shield becomes part of the antenna, distorting the intended radiation pattern
- **RF in the shack** — common-mode current flows back to the radio and radiates inside the operating area, causing interference with computers, audio equipment, and other electronics
- **Unpredictable SWR** — the feedline contributes to the antenna system impedance, making SWR readings unreliable and varying with cable length
- **Receive noise pick-up** — the feedline picks up electrical noise from sources near the cable run, degrading reception

A good **choke balun** (also called a common-mode choke or current balun) presents high impedance to common-mode current while having minimal effect on the desired differential-mode signal. This forces the current to flow only in the intended paths — inside the coax and in the antenna elements.

## Types of baluns

### Choke balun (current balun)

The choke balun works by presenting high impedance to common-mode current. It does not use transformer action and therefore does not saturate under high power. This is the most recommended type for most amateur applications.

**Ferrite choke balun:** Coax is wound through or around ferrite cores (toroids or clamp-on cores). The ferrite provides impedance to common-mode current flowing on the outer shield while the signal inside the coax passes through unaffected. Mix 31 ferrite is popular for HF use, while Mix 43 works well at higher frequencies.

**Air-wound choke balun (ugly balun):** Several turns of coax are wound into a coil, typically 15–20 cm (6–8 inches) in diameter. The inductance of the coil presents impedance to common-mode current. This is the simplest and cheapest balun to build — it works, though not as effectively as ferrite designs, especially at lower HF frequencies. It is sometimes called an "ugly balun" because it looks like a coil of leftover coax.

**Stacked ferrite bead choke:** Multiple ferrite beads (or snap-on chokes) are placed over the coax near the feed point. Effective and simple, though it requires enough beads to develop sufficient choking impedance.

### Voltage balun (flux-coupled / transformer balun)

The voltage balun uses transformer action to force equal and opposite voltages at the balanced output. Traditional designs wind separate windings on a ferrite core. While voltage baluns provide the balanced-to-unbalanced transition, they are less effective at suppressing common-mode current than choke baluns and can saturate at high power levels when the load is reactive (high SWR).

For most amateur applications, a **choke balun is the better choice** because it handles high SWR gracefully and directly addresses the common-mode current problem.

### Guanella and Ruthroff transmission-line transformers

For impedance-transforming baluns and ununs, two design approaches are widely used:

**Guanella balun:** Uses parallel transmission-line segments wound on ferrite cores. These segments are connected in parallel on one side and in series on the other to achieve the desired impedance ratio. Guanella designs have wider bandwidth and handle higher SWR better than Ruthroff designs. A Guanella 4:1 balun is an excellent choice for feeding a folded dipole or a doublet antenna system.

**Ruthroff unun/balun:** Uses a single transmission-line winding on a ferrite core with a specific connection arrangement to achieve impedance transformation. Ruthroff designs are simpler to build but have narrower bandwidth and are more sensitive to reactive loads. A Ruthroff 9:1 unun is commonly used with [end-fed half-wave antennas](/antennas/end-fed-half-wave).

## Common ratios and applications

| Ratio | Type | Typical application |
|-------|------|-------------------|
| 1:1 | Balun (choke) | Dipole fed with coax — the most common use. Suppresses common-mode current without impedance transformation. |
| 1:1 | Balun (choke) | At the point where ladder line transitions to coax entering the shack. |
| 4:1 | Balun | Folded dipole (300 Ω) to coax (75 Ω). Doublet antenna with ladder line to a tuner with balanced input. |
| 9:1 | Unun | End-fed half-wave or random wire antenna to coax. Transforms roughly 450 Ω (or higher) to 50 Ω. |
| 49:1 | Unun | End-fed half-wave antenna (high impedance feed point of ~2500 Ω) to 50 Ω coax. |
| 6:1 | Unun | Off-centre fed dipole (OCF) to coax, where the feed point impedance is roughly 300 Ω. |

## Building vs. buying

Both commercial and homebrew baluns and ununs can work well. For hams who enjoy building, these are satisfying projects that require only ferrite cores, wire or coax, and an enclosure. Key considerations:

- **Ferrite material matters.** Different ferrite mixes work best at different frequency ranges. Mix 31 is excellent for the HF bands (1.8–30 MHz). Mix 43 is better for higher frequencies. Using the wrong mix results in poor choking performance.
- **Enough turns/beads.** A choke balun needs sufficient choking impedance — generally at least 500 ohms of common-mode impedance at the lowest operating frequency, and ideally over 1000 ohms. Too few turns or beads gives inadequate choking.
- **Power handling.** At high power levels with reactive loads, ferrite cores can heat up. Choose cores and designs rated for your power level. If in doubt, oversize the core.
- **Weatherproofing.** Baluns mounted at the antenna feed point must be weather-sealed. Use a waterproof enclosure and seal all cable entry points.

For purchased baluns, look for units that specify the ferrite material used, the choking impedance across the frequency range, and the power rating under mismatched (high SWR) conditions — not just matched-load ratings.

## Where should you use a balun?

**At the feed point of any balanced antenna fed with coax.** This means any dipole, doublet, loop, or Yagi fed with coaxial cable should have a 1:1 choke balun at the feed point. This is the single most impactful place to use a balun and addresses the most common source of common-mode problems.

**At the transition from ladder line to coax.** If you use ladder line from the antenna and then transition to a short run of coax into the shack, place a 1:1 choke balun at (or near) that transition point.

**At the entry to the shack.** An additional choke on the coax where it enters the building can further reduce common-mode current and help with RF interference inside the station.

**On receive antennas.** Common-mode current on receive feedlines picks up noise from electrical sources near the cable run. A choke balun can significantly improve the signal-to-noise ratio on receive-only antennas.

## Common mistakes

- **Omitting the balun entirely.** Many hams connect coax directly to a dipole and it "works." But the feedline is radiating, the pattern is distorted, and RF problems in the shack are likely. A 1:1 choke balun is inexpensive and almost always worthwhile.
- **Using a voltage balun where a choke balun is needed.** If your primary goal is common-mode suppression (which it usually is), a choke/current balun is the right choice.
- **Wrong ferrite mix.** A balun wound on the wrong ferrite material will not provide adequate choking impedance at your operating frequencies.
- **Insufficient choking impedance.** A few turns of coax in the air (the "ugly balun") may not provide enough impedance at lower HF frequencies. Ferrite-loaded designs are more effective, especially on 160 and 80 metres.
- **Confusing impedance ratio with voltage/current ratio.** A 4:1 balun has a 4:1 impedance ratio but a 2:1 voltage/current ratio. Make sure you are applying the correct transformation for your system.

## Where to go next

- [SWR and Matching](/antennas/swr-and-matching) — How SWR relates to impedance matching and why it matters
- [Feedlines](/antennas/feedlines) — Choosing and installing coax and ladder line
- [Dipole Antennas](/antennas/dipole) — The classic balanced antenna and a prime candidate for a balun
- [End-Fed Half-Wave](/antennas/end-fed-half-wave) — An antenna type that commonly uses ununs
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Core concepts including impedance
