---
title: Dipole Antennas
description: The classic dipole antenna — theory, construction, variations, and practical tips for one of amateur radio's most versatile antennas
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, dipole, wire, hf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Dipole Antennas

The half-wave dipole is the most fundamental antenna in amateur radio. It is the reference against which other antennas are measured, the starting point for understanding [antenna theory](/antennas/antenna-fundamentals), and — importantly — a genuinely excellent performer. Many experienced operators have worked stations around the world with nothing more than a dipole strung between two trees. If you are putting up your first HF antenna, a dipole is an outstanding choice.

## What is a dipole?

A dipole is an antenna consisting of two conductive elements (usually wire) arranged in a straight line, fed at the centre. Each element is approximately one-quarter wavelength long, making the total antenna approximately one-half wavelength at the design frequency. The feedline connects at the centre point between the two elements.

The name "dipole" simply means "two poles" — referring to the two halves of the antenna.

## How it works

When the transmitter drives the centre feed point, current flows outward along both halves of the dipole. The current is maximum at the centre and tapers to zero at the tips. The voltage follows the opposite pattern — zero at the centre and maximum at the tips. This current distribution creates the characteristic radiation pattern.

At its resonant frequency, a half-wave dipole presents a purely resistive impedance at the feed point, making it straightforward to match to [coaxial feedline](/antennas/feedlines). The theoretical free-space impedance is about 73 ohms, but in practice the impedance varies with height above ground, typically ranging from about 50 to 75 ohms — conveniently close to the 50-ohm standard of most amateur equipment.

## Radiation pattern

A horizontal dipole produces a **figure-eight** pattern in the horizontal plane. Maximum radiation is broadside to the wire (perpendicular to it), with deep nulls off the ends. If you hang a dipole running north-south, it will radiate best to the east and west.

In the vertical plane, the pattern depends heavily on height above ground. At low heights (below about a quarter wavelength), most energy goes straight up — good for [NVIS](/propagation/nvis) communication within a few hundred kilometres. As the antenna is raised higher, the radiation angle drops, favouring longer-distance contacts. At a height of one-half wavelength, the dipole produces a useful low-angle lobe for DX work.

This makes height one of the most important factors in dipole performance. Even a modest increase in height can meaningfully improve DX capability.

## Calculating dipole length

The standard formula for a half-wave dipole in metres:

**Total length (metres) ≈ 143 / f (MHz)**

Or in feet:

**Total length (feet) ≈ 468 / f (MHz)**

Each half of the dipole is half of this total length. For example, a dipole for the 20-metre band (14.1 MHz):

- Total length ≈ 143 / 14.1 ≈ 10.14 metres (33.3 feet)
- Each leg ≈ 5.07 metres (16.6 feet)

These formulas include an approximate correction for the velocity factor of wire (about 95% of free-space wavelength). The actual resonant length depends on wire diameter, height above ground, and proximity to other objects, so always **cut slightly long and trim to tune**. An [antenna analyser](/antennas/swr-and-matching) makes this process quick and precise.

### Quick reference: dipole lengths for popular HF bands

| Band | Frequency (MHz) | Approx. total length |
|------|-----------------|---------------------|
| 80 m | 3.6 | 39.7 m (130.0 ft) |
| 40 m | 7.1 | 20.1 m (66.0 ft) |
| 30 m | 10.125 | 14.1 m (46.2 ft) |
| 20 m | 14.1 | 10.1 m (33.2 ft) |
| 17 m | 18.1 | 7.9 m (25.9 ft) |
| 15 m | 21.1 | 6.8 m (22.2 ft) |
| 12 m | 24.9 | 5.7 m (18.8 ft) |
| 10 m | 28.3 | 5.1 m (16.5 ft) |

## Building a simple dipole

A basic single-band dipole requires very few materials:

- **Wire** — stranded copper wire is the most common choice. Sizes from 18 AWG (1.0 mm) for lightweight portable use to 12 AWG (2.0 mm) or 14 AWG (1.6 mm) for permanent installations work well. Insulated wire is fine and slightly affects the velocity factor (requiring the antenna to be a bit shorter). Bare wire works too. Copper-clad steel ("Copperweld") wire is stronger and better for long spans but harder to solder.
- **Centre insulator/feed point** — a commercial centre insulator with an SO-239 connector, or a homebrew solution using a piece of Perspex/Plexiglas or other insulating material. The feedline connects here.
- **End insulators** — small insulators (ceramic egg insulators, dog-bone insulators, or even short lengths of PVC pipe) at each tip to isolate the wire from the support ropes.
- **Support rope** — UV-resistant synthetic rope (Dacron/polyester is preferred; nylon stretches significantly in wet weather). Avoid metal wire for support, as it can interact with the antenna.
- **Feedline** — [coaxial cable](/antennas/feedlines), typically RG-213 or RG-8X for HF use.
- **Balun** — a [1:1 choke balun](/antennas/baluns-and-ununs) at the feed point is recommended to suppress common-mode current on the coax shield.

The construction is straightforward: cut two lengths of wire to the calculated length (plus a small extra for attachment), attach them to the centre insulator, add end insulators, connect the feedline through the balun, and hoist the antenna into position. Trim the wire tips equally on each side to bring the resonant frequency to your target.

## Dipole variations

The basic half-wave dipole is just the starting point. Many popular antenna designs are variations on the dipole concept.

### Inverted-V dipole

The **inverted-V** is a dipole with the centre supported at a single high point (mast, tree, or house peak) and the two legs sloping downward at an angle. This is one of the most popular configurations because it requires only **one** high support point rather than two.

The inverted-V has a slightly different radiation pattern than a flat-top dipole — the pattern is more omnidirectional (less figure-eight), which can be an advantage when you want coverage in all directions. The feed point impedance drops somewhat (typically to around 50 ohms, a near-perfect match to coax), and the resonant frequency shifts slightly, requiring minor length adjustment.

For best results, keep the included angle between the legs at 90 degrees or greater. Steeper angles (legs hanging nearly straight down) reduce performance.

### Fan dipole

A **fan dipole** (or multi-band dipole) uses multiple pairs of dipole elements connected at a common centre feed point, with each pair cut for a different band. The elements fan out slightly to avoid contact with each other. On any given band, the resonant pair of elements carries most of the current while the other pairs have relatively little effect.

Fan dipoles are a practical way to cover three or four bands with a single feedline and feed point. They work best when the bands are not harmonically related (for example, 40/20/15 works well; 80/40 can interact and require careful adjustment).

### Trapped dipole

A **trapped dipole** uses LC (inductor-capacitor) traps inserted along each element. Each trap is resonant at a specific frequency — at that frequency, it presents high impedance and electrically isolates the outer portion of the wire. At lower frequencies, the trap looks like a loading coil, and the current flows through to the full length of wire beyond the trap.

This allows a single dipole to operate on multiple bands using a single pair of elements. The trade-off is that the traps introduce some loss, narrow the bandwidth on each band, and add weight and complexity. Commercial trapped dipoles are widely available and popular for multi-band operation with limited space.

### Off-centre fed dipole (OCF / Windom)

An **off-centre fed dipole** is fed at a point approximately one-third of the way from one end rather than at the centre. This feed point presents an impedance of roughly 200–300 ohms, which can be matched using a [4:1 or 6:1 balun/unun](/antennas/baluns-and-ununs) to 50-ohm coax.

The advantage of off-centre feeding is multi-band operation — because the asymmetric feed point encounters different impedances on harmonically related bands, an OCF cut for 80 metres can often be used on 40, 20, and 10 metres (with a tuner on some bands). The disadvantage is that the feedline sees high SWR on some bands, and the unbalanced feed point can cause more common-mode current issues than a centre-fed design.

### Folded dipole

A **folded dipole** is made by connecting two parallel conductors at both ends, with one of them split at the centre and fed. The folded structure multiplies the feed point impedance by approximately four times (to about 300 ohms for a standard two-wire version), which is useful for matching 300-ohm feedline or with specific matching networks. Folded dipoles also have wider bandwidth than a simple dipole of the same wire size, because the effective conductor diameter is larger.

### Shortened (loaded) dipole

When space does not permit a full-size dipole, the antenna can be **shortened** by adding loading coils or capacitance hats. Loading coils (inductors) are inserted partway along each element to electrically lengthen a physically shorter wire. Centre-loaded, base-loaded, and linear-loaded dipoles are all common approaches.

Shortened dipoles work — many hams use them successfully — but the trade-offs include narrower bandwidth, lower radiation resistance (making the antenna more sensitive to losses), and reduced efficiency compared to a full-size dipole. The closer the loading coil is to the centre, the greater the efficiency penalty; coils placed closer to the tips preserve more efficiency.

## Dipole orientation and placement

### Height matters

As mentioned earlier, height above ground has a profound effect on a dipole's radiation pattern and performance. The general guidance is to get the antenna as high as you can. For DX (long-distance) work on HF, a height of at least a half wavelength above ground is desirable (about 10 metres / 33 feet on 20 metres). For NVIS work on the lower bands, lower heights (a quarter wavelength or less) are actually beneficial.

### Orientation for your target area

Since a dipole radiates best broadside to the wire, orient it perpendicular to the direction of the stations you most want to work. If you primarily work stations in a specific direction, this is worth considering. If you want all-around coverage, an inverted-V is a better choice, or you can accept the figure-eight pattern and orient the wire based on your most common operating direction.

### Sloping, bending, and drooping

Real-world antenna installations rarely achieve textbook geometry. Dipole legs that slope, bend around corners, or droop due to trees and structures still work well. The pattern will be modified and the resonant frequency may shift, but practical performance is often surprisingly close to the ideal. Do not let imperfect geometry discourage you from putting up a dipole — an imperfect dipole in the air beats a perfect dipole on the workbench.

## Feeding the dipole

The most common approach is to feed the dipole with 50-ohm coaxial cable connected through a [1:1 choke balun](/antennas/baluns-and-ununs) at the centre. This provides a good match on the design band, easy installation, and straightforward coax routing.

Alternatively, a dipole can be fed with [ladder line](/antennas/feedlines), transforming it into a **doublet** — a multi-band antenna system. A centre-fed doublet with ladder line and a tuner in the shack is one of the most efficient and versatile HF antenna systems. The doublet does not need to be resonant on any particular band because the tuner handles the matching. See the [Wire Antennas](/antennas/wire-antennas) page for more on the doublet.

## Where to go next

- [Wire Antennas](/antennas/wire-antennas) — Doublets, random wires, G5RV, and other wire antenna designs
- [End-Fed Half-Wave](/antennas/end-fed-half-wave) — A popular alternative to the dipole requiring only one support point
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — The theory behind dipole behaviour
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Why you need a balun on your dipole
- [SWR and Matching](/antennas/swr-and-matching) — Tuning your dipole and understanding SWR readings
- [Building Antennas](/antennas/building-antennas) — Construction techniques and safety
