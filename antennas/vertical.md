---
title: Vertical Antennas
description: Vertical antennas for amateur radio — quarter-wave verticals, ground planes, multi-band verticals, radial systems, and ground-mounted vs elevated designs
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, vertical, hf, vhf, uhf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Vertical Antennas

Vertical antennas are among the most popular antennas in amateur radio, used from HF through UHF. Their defining feature is an **omnidirectional radiation pattern** in the horizontal plane — they radiate (and receive) equally in all compass directions. This makes them ideal when you want coverage in every direction without a rotator, and their naturally low radiation angle on HF makes them effective for DX (long-distance) communication.

## How a vertical antenna works

The most basic vertical antenna is the **quarter-wave vertical** — a conductor one-quarter wavelength tall, mounted vertically, with a ground system or counterpoise to provide the "missing" other quarter wavelength. Together, the vertical element and its ground image form the electrical equivalent of a half-wave [dipole](/antennas/dipole), with the earth (or a set of radials) acting as a mirror.

Current is maximum at the base and tapers to zero at the tip. The [feed point impedance](/antennas/antenna-fundamentals) of an ideal quarter-wave vertical over a perfect ground plane is approximately **36 ohms** — somewhat lower than 50 ohms but close enough that many installations work acceptably without a matching network. With real ground or a limited radial system, the impedance typically rises toward 50 ohms due to ground losses added to the radiation resistance.

## Radiation pattern and angle

A vertical antenna produces a radiation pattern that is **omnidirectional** in the horizontal plane and concentrated toward the horizon in the vertical plane. The low radiation angle is the vertical's greatest advantage for HF DX work — signals at low angles travel the longest distances via [ionospheric skip](/propagation/ionosphere).

However, this low-angle advantage depends heavily on the ground system and the surrounding terrain. A vertical with a poor ground system or located in hilly terrain may radiate at higher angles than expected. Over flat terrain or near salt water, verticals can produce outstanding low-angle performance.

The vertical produces **vertically polarised** signals, which is the standard for VHF/UHF FM and [repeater](/operating/repeaters) work. On HF, the polarisation is largely irrelevant for skywave communication because ionospheric reflections scramble polarisation.

## The ground system

The ground system is the most critical — and most often underappreciated — part of a vertical antenna installation. The quality of the ground system directly affects the antenna's efficiency, impedance, and radiation pattern.

### Ground-mounted verticals with radials

A ground-mounted vertical uses a set of **radial wires** laid on or just below the ground surface, extending outward from the base of the antenna. These radials collect the return current and reduce ground losses.

The classic recommendation is **120 radials, each a quarter wavelength long** — this was shown by the Brown, Lewis, and Epstein study (1937) to approach the performance of a perfect ground. In practice, few amateurs install that many. The relationship between radial count and performance is one of diminishing returns:

- **4 radials:** A dramatic improvement over no radials, but significant ground loss remains
- **16 radials:** Good performance, a practical minimum for a serious installation
- **32 radials:** Very good performance, commonly recommended as a practical optimum
- **60+ radials:** Diminishing returns, but each additional radial still helps slightly

Radial length matters less than quantity once you have enough. If space limits radial length, using more shorter radials is generally better than fewer longer ones. Radials can be laid on the ground surface — they do not need to be buried, though burying prevents damage from foot traffic and mowing.

### Elevated verticals with a counterpoise

An **elevated vertical** (ground-plane antenna) is mounted above the ground with a small number of radial wires extending horizontally or at a downward angle from the feed point. Because the radials are elevated and away from lossy ground, far fewer are needed — typically **4 radials** provide excellent performance. Each radial should be approximately a quarter wavelength long.

The elevated ground-plane antenna with four sloped radials is an extremely popular design for VHF/UHF use. The angle of the radials affects the feed point impedance: horizontal radials give about 36 ohms; radials sloping downward at 45 degrees bring the impedance close to 50 ohms, providing a natural match to standard coax.

### No-radial verticals

Some commercial vertical antennas claim to require no radials. These designs typically use an [end-fed](/antennas/end-fed-half-wave) half-wave concept (where the vertical element is a full half-wavelength, eliminating the need for a ground image) or incorporate a built-in counterpoise. They can work well but are not truly "no-ground" — the current has to return somewhere, and if no adequate counterpoise is provided, the coax shield becomes the return path, causing common-mode issues.

## Types of vertical antennas

### Quarter-wave vertical

The simplest and most fundamental vertical. One quarter wavelength tall, with a ground system. On 20 metres (14 MHz), this is about 5 metres (16.5 feet) tall — manageable. On 40 metres (7 MHz), it is about 10 metres (33 feet). On 80 metres (3.5 MHz), it reaches about 20 metres (66 feet) — a significant structure.

### Half-wave vertical

A half-wave vertical is a full half-wavelength tall and does not require a ground system (since both halves of the antenna are in the air). It is fed at the base through a matching transformer or at a current maximum point higher up. Half-wave verticals offer slightly lower radiation angles than quarter-wave verticals and eliminate the need for radials, but they are twice as tall.

### 5/8-wave vertical

The 5/8-wave vertical is popular at VHF/UHF because it produces a lower radiation angle and about 3 dB more gain toward the horizon than a quarter-wave vertical. It requires a matching network at the base (since the feed impedance is not 50 ohms) and some form of ground plane. Many commercial [VHF/UHF base station antennas](/antennas/vhf-uhf-antennas) and [mobile antennas](/antennas/mobile-antennas) use this design.

### Trapped multi-band verticals

Multi-band HF verticals use **traps** (parallel LC circuits) along the element to provide resonance on multiple bands. A trapped vertical for 10, 15, 20, and 40 metres might be about 7 metres (23 feet) tall. Some designs cover 80 metres as well, though this involves significant loading and reduced efficiency on the lowest band.

Trapped verticals are popular because they offer multi-band HF operation in a single, relatively compact antenna. The trade-offs are narrower bandwidth on each band and some loss in the traps compared to full-size monoband verticals.

### Loaded (shortened) verticals

When a full quarter-wave vertical is too tall for the available space (particularly on 80 and 160 metres), the antenna can be shortened using **loading coils** or **capacity hats**. Loading coils add inductance to electrically lengthen a physically shorter element. A capacity hat (a horizontal structure at the top) increases the antenna's capacitance to ground, improving current distribution and efficiency compared to a simple loading coil.

Shortened verticals work but with reduced bandwidth and efficiency. Centre-loading or top-loading preserves more efficiency than base-loading. For the lowest bands, some degree of shortening is often the only practical option.

### Vertical dipole

A **vertical dipole** is a full half-wave [dipole](/antennas/dipole) oriented vertically. It requires no ground system (both halves are radiating elements) and is fed at the centre with coax through a [1:1 balun](/antennas/baluns-and-ununs). The centre feed point provides a natural 50–75 ohm impedance.

The challenge is supporting the antenna — the centre feed point is at a quarter-wavelength height, and the lower half extends toward (but should not touch) the ground. Vertical dipoles are popular for [portable operation](/antennas/portable-antennas) using fibreglass masts.

## Vertical antenna myths and realities

**"Verticals radiate equally poorly in all directions."** This old joke has a grain of truth — a vertical over a poor ground system does waste power as heat in the ground. But a vertical with a good ground system or an elevated ground plane is an efficient antenna with a genuinely useful low-angle pattern. Many top DX operators and contesters use vertical arrays to great effect.

**"More radials is always better."** True, but with diminishing returns. Going from 4 to 16 radials gives a large improvement; going from 60 to 120 gives very little. Invest your time and wire up to a practical point (16–32 radials for ground-mounted, 4 for elevated), then focus on other station improvements.

**"Verticals are noisy on receive."** Verticals can pick up more man-made noise than horizontal antennas at the same site, because their omnidirectional pattern and vertical polarisation can be more susceptible to nearby noise sources (power lines, switching power supplies, LED lights). This is a real consideration, particularly on the lower HF bands in urban and suburban environments. A separate, directional receive antenna can help.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Impedance, radiation patterns, and gain
- [VHF/UHF Antennas](/antennas/vhf-uhf-antennas) — Ground-plane and collinear verticals for VHF/UHF
- [Mobile Antennas](/antennas/mobile-antennas) — Vehicle-mounted verticals
- [Portable Antennas](/antennas/portable-antennas) — Lightweight verticals for field use
- [SWR and Matching](/antennas/swr-and-matching) — Matching vertical impedances
- [Building Antennas](/antennas/building-antennas) — Construction and safety for vertical installations
