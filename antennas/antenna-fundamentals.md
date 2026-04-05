---
title: Antenna Fundamentals
description: Core antenna concepts every ham should understand — resonance, impedance, gain, radiation patterns, polarisation, and bandwidth
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, theory, fundamentals
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Antenna Fundamentals

Before diving into specific antenna designs, it helps to understand the core principles that govern how all antennas work. These concepts will come up repeatedly as you explore different antenna types, evaluate designs, and troubleshoot performance issues. You do not need to master all of this at once — many hams develop their understanding gradually through hands-on experience — but having a foundation in these ideas will make everything else about antennas much clearer.

## How antennas radiate

An antenna radiates electromagnetic waves when an alternating current flows through it. As the current oscillates back and forth in the conductor, it creates changing electric and magnetic fields around the antenna. These fields detach from the antenna and propagate outward through space as electromagnetic waves — radio waves.

The reverse happens on receive: passing radio waves induce a small alternating current in the antenna conductor, which the receiver amplifies and processes.

The key insight is that an antenna is a **transducer** — it converts between conducted electrical energy and radiated electromagnetic energy. The same antenna properties that make it a good transmitting antenna also make it a good receiving antenna. This principle, known as **reciprocity**, means that you can analyse antenna performance in either direction and the results apply to both.

## Resonance

An antenna is **resonant** at a frequency where its electrical length is a specific fraction of the wavelength — most commonly one-half wavelength (λ/2) for a dipole. At resonance, the antenna naturally presents a purely resistive impedance to the feedline, which simplifies matching and maximises efficient power transfer.

### Wavelength and physical length

The relationship between frequency and wavelength is:

**λ = c / f**

Where λ is wavelength in metres, c is the speed of light (approximately 300,000,000 m/s), and f is frequency in hertz. For practical antenna calculations in metres:

**λ (metres) = 300 / f (MHz)**

A half-wave dipole for the 20-metre band (14.1 MHz) would theoretically be 300 / 14.1 / 2 ≈ 10.64 metres long. In practice, the antenna will be slightly shorter because radio waves travel a bit slower along a wire than in free space. A common shortcut for a half-wave dipole in metres is:

**Length (metres) ≈ 143 / f (MHz)**

This gives approximately 10.14 metres for 14.1 MHz — about 5% shorter than the free-space calculation. The exact shortening depends on the wire diameter, height above ground, and nearby objects, which is why antenna builders typically cut slightly long and trim to tune.

### Off-resonance operation

You can use an antenna away from its resonant frequency, but the impedance will become complex (containing a reactive component), and the [SWR](/antennas/swr-and-matching) will rise. An [antenna tuner](/antennas/swr-and-matching) or matching network can compensate for this, allowing an antenna to be used across a wider range of frequencies — though with trade-offs in efficiency depending on the severity of the mismatch and feedline losses.

## Impedance

**Impedance** is the opposition that the antenna presents to the flow of alternating current, measured in ohms (Ω). It has two components:

- **Resistance (R)** — the part that dissipates energy, either as radiation (radiation resistance) or as heat (loss resistance)
- **Reactance (X)** — the part that stores and returns energy without radiating it, caused by the antenna's capacitive or inductive properties

At resonance, the reactance is zero (or very nearly so), leaving only the resistive component. The **feed point impedance** — the impedance at the point where the feedline connects — is what matters most in practice because it determines how well the antenna matches the feedline and transmitter.

### Common impedance values

A half-wave dipole in free space has a theoretical feed point impedance of about **73 ohms**. In practice, the impedance of a real dipole varies with height above ground and proximity to other objects, typically ranging from about 50 to 75 ohms. This is conveniently close to the 50-ohm standard impedance used by most amateur radio equipment and coaxial cable, which is one reason the dipole is such a practical antenna.

A quarter-wave vertical over a perfect ground plane has a theoretical feed point impedance of about **36 ohms**. A folded dipole presents about **300 ohms**. Different antenna designs have different characteristic impedances, and part of antenna system design is matching these to your feedline and radio — a topic covered in detail on the [SWR and Matching](/antennas/swr-and-matching) and [Baluns and Ununs](/antennas/baluns-and-ununs) pages.

## Radiation patterns

An antenna's **radiation pattern** describes how it distributes energy in different directions. No practical antenna radiates equally in all directions — every design favours some directions over others. Understanding the radiation pattern helps you choose and orient an antenna for your operating needs.

### Isotropic and real antennas

An **isotropic radiator** is a theoretical point source that radiates equally in every direction — a perfect sphere of radiation. No physical antenna can achieve this, but the isotropic radiator is a useful reference against which real antennas are compared.

### The dipole pattern

A half-wave dipole has a classic **figure-eight** (toroidal) pattern in the horizontal plane when mounted horizontally. Maximum radiation occurs broadside to the wire (at right angles to it), while very little energy is radiated off the ends. If you string a dipole running east-west, it will radiate primarily to the north and south.

When a dipole is mounted vertically, its pattern becomes **omnidirectional** in the horizontal plane (equal radiation in all compass directions) but concentrated toward the horizon rather than straight up or down.

### Elevation angle

For HF communication, the **elevation angle** (the angle above the horizon at which most energy is radiated) matters greatly. Lower radiation angles are generally better for long-distance (DX) communication, while higher angles favour shorter-distance contacts via [Near Vertical Incidence Skywave (NVIS)](/propagation/nvis). Antenna height above ground is the primary factor controlling elevation angle for most antenna types.

### Reading pattern plots

Radiation patterns are usually shown as **polar plots** — circular diagrams with the antenna at the centre. The distance from the centre to the pattern boundary at any angle indicates the relative strength in that direction. Patterns are typically shown for both the horizontal plane (azimuth) and vertical plane (elevation). These plots can be generated using [antenna modelling software](/antennas/antenna-modeling).

## Gain

**Gain** describes how much an antenna concentrates energy in its preferred direction(s) compared to a reference antenna. Gain does not mean the antenna creates extra power — it simply redirects energy that would otherwise go in less useful directions.

### Units of gain

Gain is expressed in decibels (dB) relative to a reference:

- **dBi** — gain relative to an isotropic radiator. A half-wave dipole has a gain of approximately 2.15 dBi.
- **dBd** — gain relative to a half-wave dipole. By definition, a dipole has 0 dBd.

The two scales differ by a constant: **dBi = dBd + 2.15**. When comparing antenna specifications, always check which reference is being used. A "7 dBd" antenna and a "9.15 dBi" antenna have identical performance — but the dBi number looks more impressive, which is why some manufacturers prefer it.

### What gain means in practice

Every 3 dB of gain is equivalent to doubling your effective transmit power in the favoured direction. A Yagi antenna with 10 dBd of gain (12.15 dBi) effectively multiplies your transmit power by about ten times in the direction the antenna is pointed — without any increase in actual transmitter output.

The trade-off is that this extra gain comes from narrowing the pattern. Higher-gain antennas have narrower beamwidths, meaning they must be aimed more precisely at the station you want to work.

## Polarisation

**Polarisation** describes the orientation of the electric field in the radio wave. The three most common types are:

- **Horizontal** — the electric field oscillates parallel to the ground (e.g., a horizontal dipole)
- **Vertical** — the electric field oscillates perpendicular to the ground (e.g., a vertical antenna)
- **Circular** — the electric field rotates as the wave travels (used for [satellite communications](/antennas/satellite-antennas))

When two stations use the same polarisation, signals are strongest. A mismatch between horizontal and vertical polarisation can cause a signal loss of 20 dB or more on line-of-sight VHF/UHF paths. On HF, signals bouncing off the [ionosphere](/propagation/ionosphere) have their polarisation scrambled, so the polarisation mismatch penalty is usually small on HF skywave paths.

For VHF/UHF FM and repeater work, **vertical polarisation** is the convention. For HF, **horizontal polarisation** is more common, largely because horizontal antennas tend to produce lower radiation angles and are easier to install at effective heights. For satellite work, **circular polarisation** (usually right-hand circular, RHCP) is preferred to avoid polarisation fading as the satellite tumbles or the geometry changes.

## Bandwidth

An antenna's **bandwidth** is the range of frequencies over which it performs acceptably — typically defined as the range where the SWR stays below a specified limit (commonly 2:1). Bandwidth depends on the antenna design and, importantly, on the conductor thickness: fatter conductors (or cage/fan arrangements) produce wider bandwidth.

Some antenna types are inherently broadband (covering a wide frequency range), while others are narrowband (optimised for a small slice of spectrum). For example, a simple dipole made from thin wire might cover only a portion of an amateur band, while a fan dipole or folded dipole using thicker elements can cover the entire band.

Multi-band antennas — those designed to operate on several amateur bands — achieve this through various techniques including traps, multiple driven elements, and off-centre feeding. These are covered in the individual antenna type pages.

## Efficiency

Not all power delivered to an antenna is radiated. Some energy is lost as heat in the antenna conductor, in loading coils, in ground resistance, and in nearby lossy objects. **Antenna efficiency** is the ratio of radiated power to total input power.

Full-size antennas (those close to a half wavelength or larger) are generally very efficient — losses in the antenna wire itself are small. Shortened or loaded antennas, such as compact mobile whips or small magnetic loops, must use loading elements that introduce additional losses, reducing efficiency. This does not make them bad antennas — they can still be very effective — but it is a trade-off to be aware of, especially at lower power levels where every decibel counts.

## Near field and far field

Close to the antenna (the **near field**), the electric and magnetic fields are complex and do not behave like a travelling wave. The radiation pattern only forms in the **far field**, which begins at a distance roughly proportional to the antenna size and wavelength. Antenna measurements and pattern plots are always based on far-field behaviour.

The near field is relevant for safety (RF exposure is highest close to the antenna) and for understanding why nearby objects can affect antenna performance — anything in the near field interacts strongly with the antenna.

## Putting it all together

These fundamentals interact with each other. A higher antenna generally produces a lower radiation angle. A larger antenna can offer more gain but with a narrower beamwidth. A shortened antenna trades efficiency for compactness. Understanding these trade-offs is what lets you make informed choices about antenna designs for your particular situation, location, and operating goals.

The best approach for most hams is to start simple — a basic [dipole](/antennas/dipole) or [vertical](/antennas/vertical) — and learn from direct experience. As you operate and observe how your antenna performs under different conditions, the concepts on this page will become increasingly intuitive.

## Where to go next

- [Dipole Antennas](/antennas/dipole) — The most fundamental antenna design and a great place to start
- [Feedlines](/antennas/feedlines) — Transmission lines that connect your radio to the antenna
- [SWR and Matching](/antennas/swr-and-matching) — Measuring and managing impedance matching
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Impedance transformation and balanced/unbalanced transitions
- [Antenna Modeling](/antennas/antenna-modeling) — Simulating antenna performance before you build
