---
title: Antenna Modeling Software
description: Software for designing and simulating amateur radio antennas — NEC-based modelling, popular programs, and practical tips
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, antennas, modeling, nec, simulation
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Antenna Modeling Software

Building an antenna without first modelling it is a bit like navigating without a map — you might get where you want to go, but you will waste time and materials on wrong turns. Antenna modelling software lets you describe an antenna's geometry on screen, simulate its electromagnetic behaviour, and see the predicted gain, radiation pattern, impedance, and bandwidth before you cut a single piece of wire. This makes the design process faster, cheaper, and far more educational.

## How Antenna Modelling Works

Most antenna modelling software for amateur radio is based on the **Numerical Electromagnetics Code (NEC)**, originally developed by Lawrence Livermore National Laboratory in the 1970s and 1980s. NEC uses the **Method of Moments (MoM)** to solve Maxwell's equations numerically for an antenna structure described as a collection of wire segments.

The basic process is:

1. **Define the geometry** — You describe the antenna as a set of wires in three-dimensional space, specifying each wire's start point, end point, diameter, and the number of segments it is divided into.
2. **Set the excitation** — You define where the antenna is fed (typically the centre of a driven element) and at what frequency or range of frequencies.
3. **Specify the ground** — You choose a ground model: free space (no ground), perfect ground, or a real ground with specific conductivity and dielectric constant.
4. **Run the simulation** — The software divides each wire into segments, sets up a system of linear equations representing the currents on those segments, and solves them. From the current distribution, it calculates the antenna's properties.
5. **Examine the results** — The output includes feed-point impedance (resistance and reactance), SWR, gain, front-to-back ratio, radiation pattern plots (azimuth and elevation), and current distribution along the wires.

### NEC-2 versus NEC-4

NEC-2 is the version most commonly used in amateur radio software. Its source code was released into the public domain, which is why so many free programs are built on it. NEC-2 handles wire antennas well but has limitations with buried wires and certain geometries near ground.

NEC-4 improves on NEC-2 in several areas, particularly ground interaction modelling and the handling of wires that cross the air-ground interface. However, NEC-4 is not public domain — a licence is required. Some commercial antenna modelling programs include or offer NEC-4 as an option.

### What NEC models well — and what it does not

NEC excels at wire antennas: dipoles, verticals, Yagis, loops, delta loops, log-periodics, phased arrays, and similar structures made from straight wire elements. It models these very accurately when the model is set up correctly.

NEC is less suited for antennas with solid surfaces (like parabolic dishes or patch antennas) or complex dielectric structures. For those, full-wave 3D electromagnetic solvers using finite element or finite difference methods are needed, and these are typically outside the scope of amateur radio modelling.

> **Important:** A model is only as good as its inputs. Small errors in wire placement, segment count, or ground parameters can produce misleading results. Always validate your models against known antenna designs before trusting results for a new design.
{.is-warning}

## Popular Antenna Modelling Programs

| Program | Platforms | Licence | Notable features |
|---------|-----------|---------|-----------------|
| EZNEC | Windows | Commercial (free demo with element limits) | The most widely used antenna modelling program in amateur radio; intuitive interface built on NEC-2 (NEC-4 available in Pro version); excellent documentation |
| 4nec2 | Windows | Free | Full-featured NEC-2 modelling with graphical geometry editor, optimiser, and 3D pattern display; steep learning curve but very capable |
| MMANA-GAL | Windows | Free | Moment-method modelling with a user-friendly interface; includes antenna optimiser and a large library of pre-built antenna models; not NEC-based (uses its own MoM engine) |
| cocoaNEC | macOS | Free | NEC-2 modelling for Mac; includes both graphical and script-based model input |
| xnec2c | Linux | Free (open source) | GTK-based NEC-2 front end for Linux; real-time pattern display as you adjust geometry |
| OpenFDTD | Windows, Linux | Free (open source) | Finite Difference Time Domain solver; useful for antennas NEC cannot model (patch, horn, etc.) |
| AN-SOF | Windows | Commercial (free limited version) | Full-wave antenna simulation using its own MoM engine; includes wire, patch, and surface modelling |

### Which program to start with

If you are new to antenna modelling and run Windows, EZNEC (even the demo version) is the most approachable starting point — it has the clearest interface and the best documentation for beginners. MMANA-GAL is also beginner-friendly and comes with a large antenna model library that you can study and modify. For free full-featured modelling, 4nec2 is extremely capable but requires more time to learn.

Mac users should look at cocoaNEC, and Linux users at xnec2c. Both are solid NEC-2 implementations.

## Understanding the Results

### Feed-point impedance and SWR

The model calculates the complex impedance (R + jX) at the feed point. From this, you can compute the SWR for a given feed line impedance (typically 50 ohms). A purely resistive impedance close to 50 ohms means a good match; significant reactance means you may need to adjust element lengths or add a matching network.

Most programs can sweep the frequency across a range and plot impedance, SWR, and other parameters versus frequency. This shows you the antenna's bandwidth — the range over which SWR remains acceptable.

### Radiation pattern

The radiation pattern shows the antenna's gain as a function of direction, usually displayed as two plots: azimuth (top view) and elevation (side view). From the pattern you can see the antenna's directivity, front-to-back ratio, and whether there are unwanted sidelobes.

Patterns are shown in dBi (gain relative to an isotropic radiator) or dBd (gain relative to a dipole). The maximum gain and the direction of maximum radiation tell you how effective the antenna will be for your intended purpose.

### Current distribution

Visualising the current on each wire segment helps you understand how the antenna works and can reveal modelling errors. If the current distribution looks unexpected — for example, high current at a wire end — there may be a segmentation error or geometry problem.

## Practical Tips for Antenna Modelling

**Start with known designs** — Before modelling a new antenna, model a simple half-wave dipole and verify that the results match published values. This confirms your software is working correctly and that you understand how to set up a model.

**Use adequate segmentation** — Each wire should be divided into enough segments for the model to converge. A common rule of thumb is at least 10 segments per half wavelength of wire, with odd numbers preferred so that the feed point falls at the centre of a segment. Too few segments produce inaccurate results; too many waste computation time and can introduce numerical errors.

**Model the real ground** — Free-space models are useful for understanding an antenna's inherent pattern, but real antennas operate over real ground. Use a ground model appropriate to your location. Average ground (conductivity of about 5 mS/m and dielectric constant of 13) is a reasonable starting point for many locations, but ground quality varies widely.

**Model the support structures** — Metal masts, towers, and guy wires near the antenna can affect its performance significantly. If your antenna will be mounted on a metal structure, include it in the model.

**Use the optimiser** — Several modelling programs include built-in optimisers that can automatically adjust element lengths, spacing, or other parameters to meet your performance goals (maximum gain, minimum SWR, target impedance, etc.). This saves time compared to manual trial-and-error adjustment.

**Verify with measurements** — After building the antenna, measure the real SWR and compare it to the model's predictions. If they disagree significantly, review your model and your build for discrepancies. Over time, this feedback loop will make you a better modeller and a better antenna builder.

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — The principles behind antenna design
- [Wire Antennas](/antennas/wire-antennas) — Simple and effective HF antennas
- [Directional Antennas](/antennas/directional-antennas) — Yagis, quads, and beam antennas
- [Antenna Matching](/antennas/antenna-matching) — Impedance matching and feed systems
- [DIY Antenna Projects](/diy-projects/antenna-projects) — Build your own antennas
- [Online Tools & Resources](/software/online-tools) — Web-based calculators and utilities
