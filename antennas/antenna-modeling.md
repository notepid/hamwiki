---
title: Antenna Modeling
description: Using software to simulate antenna performance — popular modelling programs, what they can tell you, and how to get reliable results
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, modeling, software, simulation, nec
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Antenna Modeling

Antenna modelling software lets you design, analyse, and optimise antennas on your computer before building them. You can predict [radiation patterns](/antennas/antenna-fundamentals), gain, impedance, [SWR](/antennas/swr-and-matching), and bandwidth — and experiment with changes to dimensions, height, wire gauge, and surroundings without cutting a single piece of wire. For anyone serious about antenna performance, modelling is an invaluable tool.

## What antenna modelling can do

A good antenna model can tell you:

- **Resonant frequency** — where the antenna's reactance is zero and the SWR is lowest
- **Feed point impedance** — the resistance and reactance the antenna presents to the feedline at any frequency
- **SWR curve** — how the SWR varies across a range of frequencies, revealing the antenna's usable bandwidth
- **Radiation pattern** — polar plots showing where the antenna sends energy in both the horizontal (azimuth) and vertical (elevation) planes
- **Gain** — how much the antenna concentrates energy compared to an isotropic radiator or a dipole
- **Front-to-back ratio** — for directional antennas like [Yagis](/antennas/yagi), how much signal goes forward vs. backward
- **Current distribution** — how current flows along the antenna elements, useful for understanding how the antenna works
- **Near-field effects** — how nearby objects (ground, masts, other antennas) affect performance
- **Effect of changes** — what happens if you change the height, length, wire diameter, element spacing, or any other parameter

## How modelling works: NEC and MoM

Most amateur antenna modelling software is based on **NEC** (Numerical Electromagnetics Code), a computational engine originally developed by the US government. NEC uses the **Method of Moments (MoM)** to solve Maxwell's equations for a given antenna geometry.

In practice, you describe your antenna as a collection of wire segments in three-dimensional space, specify the frequency and feed point, and the software calculates the electromagnetic behaviour. The model divides each wire into small segments, computes the current on each segment, and derives all the performance parameters from those currents.

NEC-2 is freely available and is the engine behind most free amateur modelling programs. **NEC-4** is a more capable (but commercially licensed) version with better accuracy for antennas close to the ground and for buried elements.

## Popular modelling software

### Free programs

**4nec2** — A free, powerful NEC-2 based program for Windows. It provides a graphical interface for building antenna models, a geometry viewer, pattern plots, SWR sweep, and an optimiser that can automatically adjust antenna dimensions to meet performance targets. 4nec2 is extremely capable and widely used by amateur antenna designers. The learning curve is moderate but manageable with the help of online tutorials.

**MMANA-GAL** — A free antenna modelling program with a particularly user-friendly interface. It uses its own calculation engine (MoM-based) and can also export models to NEC format. MMANA-GAL is excellent for beginners because the antenna geometry editor is intuitive — you can drag wire endpoints to adjust dimensions. It includes a large library of pre-built antenna models that you can load, study, and modify.

**cocoaNEC** — A free NEC-2 based modeller for macOS. It provides a scripting interface along with a graphical editor, making it flexible for both simple and complex models.

**xnec2c** — A free, open-source NEC-2 program for Linux with a graphical interface and real-time pattern display. It updates the radiation pattern interactively as you change frequency, which is useful for quickly understanding antenna behaviour.

### Commercial programs

**EZNEC** — One of the most popular antenna modelling programs in amateur radio, developed by W7EL. EZNEC provides an intuitive interface built specifically for amateur antenna work, with features like automatic ground modelling, built-in wire tables, and comprehensive pattern and impedance displays. EZNEC is available in versions using NEC-2 and NEC-4 engines. It has been widely used and referenced in antenna literature for decades.

**AN-SOF** — A full-featured electromagnetic simulation package that goes beyond basic wire antennas to model patch antennas, horns, and other structures. More capability than most amateurs need, but available for complex projects.

## Building your first model

A good way to learn antenna modelling is to start with a simple antenna you already understand — like a half-wave [dipole](/antennas/dipole) — and verify that the model produces results consistent with what you know.

A basic dipole model requires defining:

1. **A wire** — specify the start and end coordinates in 3D space (x, y, z), the wire diameter, and the number of segments. For a dipole at 10 metres height on 20 metres (14.1 MHz), you might define a wire from (-5.07, 0, 10) to (5.07, 0, 10) — a horizontal wire about 10.14 metres long at 10 metres height.
2. **A source (feed point)** — placed at the centre segment of the wire.
3. **Ground model** — specify the ground type (perfect, real with conductivity and dielectric constant, or free space).
4. **Frequency** — the frequency (or range of frequencies) to analyse.

Run the model and examine the results: feed impedance should be close to 70 ohms resistive, the pattern should show the classic figure-eight in the horizontal plane, and the gain should be about 7.5–8 dBi (depending on height and ground model).

Once this makes sense, start modifying: change the height, adjust the length, switch the ground model, add a second element to explore [Yagi](/antennas/yagi) behaviour. Each experiment builds understanding.

## Tips for accurate models

**Use enough segments.** Each wire should be divided into enough segments for the software to calculate accurate current distribution. A common rule of thumb is at least 10 segments per half wavelength of wire, with segments roughly equal in length. Too few segments give inaccurate results; too many slow the computation without meaningful improvement.

**Model real ground.** Free-space models are useful for understanding antenna behaviour in isolation, but real performance depends on the ground. Use the "real ground" option with appropriate conductivity and dielectric constant for your soil type. Average ground (conductivity 0.005 S/m, dielectric constant 13) is a reasonable default for many locations.

**Include nearby objects.** If your antenna will be near a metal mast, tower, guttering, or other conductors, include them in the model. Nearby metal can significantly affect impedance and pattern. Most modelling programs let you add passive wire elements to represent these objects.

**Use correct wire diameters.** Wire diameter affects bandwidth and impedance. Model the actual wire or tubing size you plan to use.

**Validate against known results.** Before trusting a model of a novel design, verify that the software produces correct results for antennas with well-known characteristics (dipoles, ground planes, simple Yagis).

**Be sceptical of extreme claims.** If a model shows exceptionally high gain or unusually broadband behaviour, double-check the model setup. Errors in geometry, segmentation, or source placement can produce unrealistic results.

## What modelling cannot tell you

Antenna models have limitations:

- **Mechanical performance** — the model does not know if your antenna will survive wind, ice, or its own weight
- **Exact real-world impedance** — models use idealised ground and geometry; real installations always differ somewhat
- **Noise environment** — the model shows antenna patterns but not the noise arriving from different directions at your specific location
- **Construction losses** — connection resistance, corroded joints, and lossy insulators are not typically modelled
- **Feed system effects** — most models assume a perfect feedline; real [feedline losses](/antennas/feedlines) and [balun](/antennas/baluns-and-ununs) effects need to be accounted for separately

A model is a starting point, not the final answer. Build the antenna, measure it with an antenna analyser, and adjust as needed. The model gets you close; hands-on tuning gets you there.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — The concepts behind what the modelling software calculates
- [Yagi-Uda Antennas](/antennas/yagi) — Antenna design where modelling is most valuable
- [Dipole Antennas](/antennas/dipole) — A good first antenna to model
- [SWR and Matching](/antennas/swr-and-matching) — Interpreting the impedance and SWR results from your models
- [Building Antennas](/antennas/building-antennas) — From model to reality
