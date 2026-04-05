---
title: Loop Antennas
description: Loop antenna designs for amateur radio — small magnetic loops, full-wave horizontal loops, delta loops, and quad loops
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, loop, magnetic-loop, delta, quad
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Loop Antennas

Loop antennas come in a remarkable range of forms — from tiny magnetic loops that sit on a desktop to full-wave horizontal loops strung around the perimeter of a garden. What they share is a continuous conductor formed into a closed loop. Beyond that, their behaviour, performance, and applications vary enormously depending on the loop's size relative to the operating wavelength.

This page covers the major categories of loop antennas used in amateur radio, with practical guidance on when each type makes sense.

## Two families of loops

Loop antennas divide naturally into two groups based on their size:

**Small loops (magnetic loops):** The loop circumference is a small fraction of the operating wavelength — typically one-tenth of a wavelength or less. These antennas are dominated by magnetic field coupling and behave very differently from wire antennas. They are compact, can be very effective despite their small size, and are popular for restricted-space and portable operation.

**Large loops (full-wave and larger):** The loop circumference is one full wavelength or more. These are full-size antennas that behave more like bent [dipoles](/antennas/dipole) or arrays. They offer excellent performance and can rival or exceed a dipole in many situations. Full-wave horizontal loops, delta loops, and quad loops fall into this category.

## Small magnetic loops

The small transmitting magnetic loop (often called a "mag loop") has gained tremendous popularity among operators who face antenna restrictions, have limited space, or operate portable. A well-built magnetic loop can be surprisingly effective — many operators work DX regularly with these antennas from apartments, patios, and hotel rooms.

### How a magnetic loop works

A small magnetic loop consists of a single-turn loop of large-diameter conductor (copper or aluminium tubing, typically 12–25 mm / 0.5–1 inch in diameter) formed into a circle or octagon, with a tuning capacitor connected across a gap in the loop. The loop diameter is typically 0.5 to 1.5 metres (1.5 to 5 feet).

The loop is tuned to resonance by the variable capacitor. At resonance, very high circulating current flows in the loop — far higher than the current delivered by the transmitter. This high current produces a strong magnetic field that radiates. The tuning is extremely sharp (narrow bandwidth), and the antenna must be retuned every time you move more than a few kilohertz.

The feedline is coupled to the loop via a smaller coupling loop (typically one-fifth the diameter of the main loop) positioned inside the main loop and connected to the coax.

### Performance and trade-offs

**Advantages:**
- Very compact — a loop for 40 metres can be just 1 metre (3 feet) in diameter
- Can be used indoors (with appropriate RF exposure precautions)
- Inherently quiet on receive — the small capture area and deep nulls reject local electrical noise
- Directional pattern with deep nulls broadside to the loop plane, useful for nulling interference sources
- No ground system or radials needed
- Can be rotated easily for direction finding or noise rejection

**Disadvantages:**
- Very narrow bandwidth — typically only 5–30 kHz of usable bandwidth before retuning is required
- Reduced efficiency compared to full-size antennas, especially on lower bands. Efficiency depends heavily on conductor size, frequency, and construction quality. On 20 metres, a well-built magnetic loop can be quite efficient (50–80%). On 80 metres with the same loop, efficiency may drop to single digits.
- High voltage across the tuning capacitor — at 100 watts, the voltage can reach several thousand volts, requiring a high-quality vacuum or butterfly variable capacitor
- High circulating current requires excellent conductor joints with minimum resistance — every milliohm of loss reduces efficiency

### Tuning capacitor options

The tuning capacitor is the most critical and often most expensive component. Requirements include high voltage rating (1 kV to 10 kV depending on power and band), low loss (air-spaced or vacuum), and smooth adjustment for precise tuning.

**Vacuum variable capacitors** offer the best performance — very high voltage rating, low loss, and wide capacitance range in a compact package. They are available as surplus components from commercial and military sources.

**Butterfly capacitors** use specially shaped vanes that eliminate the sliding contact of conventional variable capacitors. This is important because even small contact resistance in the capacitor can dominate losses in the system.

**Split-stator capacitors** (two sections in series) double the voltage rating for a given capacitor size.

**Motor-driven tuning** is popular because the loop must be retuned frequently and manual adjustment requires approaching the antenna (which changes the tuning due to body proximity). A small stepper motor or gear motor driving the capacitor, controlled from the operating position, makes operation much more practical.

### Building a magnetic loop

Magnetic loops are popular homebrew projects. Key construction guidelines:

- Use the **fattest conductor you can** — larger diameter tubing has lower resistance and higher efficiency. Copper tubing of 22 mm (7/8 inch) or larger is excellent. Aluminium tubing works well too, especially in larger sizes.
- **Minimise joints** and ensure any joints are soldered (copper) or clamped with maximum contact area (aluminium). Every joint adds resistance.
- Keep the loop shape as close to **circular** as practical — a circle encloses the maximum area for a given perimeter. Octagonal shapes are common because they are easier to build from straight tubing sections.
- Position the **coupling loop** at the bottom of the main loop, opposite the tuning capacitor, for the smoothest impedance match.
- Mount the loop **clear of nearby metal** objects, which can couple to the loop and increase losses.

> **Safety warning:** Magnetic loops generate very high voltages across the tuning capacitor and strong electromagnetic fields close to the antenna. Maintain safe distance from the antenna during transmission. Do not touch the antenna while transmitting. Follow your country's RF exposure guidelines, and be especially cautious when operating indoors or at higher power levels.
{.is-danger}

## Full-wave horizontal loop (sky loop)

The **full-wave horizontal loop** — sometimes called a "sky loop" or "loop skywire" — is a loop of wire with a circumference of one full wavelength at the design frequency, supported horizontally above the ground. The loop can be any shape (square, rectangular, triangular, irregular) as long as the total wire length is approximately one wavelength.

### How it works

At one wavelength circumference, the loop is resonant and the current distribution produces useful radiation. The feed point impedance depends on the loop shape and where the feedline is attached, but is typically around 100–130 ohms for a square loop fed at one corner. A [4:1 balun](/antennas/baluns-and-ununs) brings this to approximately 50 ohms, or the loop can be fed with ladder line and a tuner for multi-band use.

### Radiation pattern

A horizontal full-wave loop at modest height (less than one-half wavelength above ground) radiates primarily **straight up** — a high-angle pattern that is excellent for [NVIS communication](/propagation/nvis) and medium-distance contacts on 80 and 40 metres. As the antenna is raised higher, the pattern breaks into lower-angle lobes suitable for DX.

The horizontal loop is quieter on receive than a dipole at the same height, partly because its closed shape tends to reject some types of local noise, and partly because its high-angle pattern does not pick up as much distant noise from low angles.

### Multi-band operation

A full-wave loop for 80 metres (approximately 86 metres / 282 feet of wire) also works on higher bands as a multi-wavelength antenna. Fed with ladder line and a tuner, it can operate on 80 through 10 metres. The radiation pattern changes significantly on each band — on higher bands the pattern develops multiple lobes — but overall it performs well as a general-purpose multi-band antenna.

### Practical considerations

The main challenge with a horizontal loop is the **space required** — you need supports at multiple points around the loop perimeter, typically trees, masts, or building attachment points. The loop does not need to be a perfect shape; irregular loops draped around available supports work well. Performance is remarkably tolerant of shape distortion.

A full-wave 80-metre loop requires roughly 86 metres (282 feet) of wire, which can fit in a garden of approximately 21 metres (70 feet) per side if arranged as a square. A 40-metre loop at about 43 metres (140 feet) is more manageable.

## Delta loop

The **delta loop** is a full-wave loop arranged in a vertical triangle (delta shape). One side is typically horizontal at the top, with the apex pointing downward, though the opposite orientation (apex up) is also used.

### Performance

A vertically oriented delta loop produces a different radiation pattern than a horizontal loop. Fed at the bottom apex, it radiates with predominantly **vertical polarisation** and a low radiation angle — excellent for DX on HF. Fed at one of the top corners or at the midpoint of the bottom side, the polarisation shifts toward horizontal.

The delta loop offers about 1–2 dB of gain over a dipole at the same height, with a useful omnidirectional pattern (slightly directional broadside to the plane of the loop). This gain advantage, combined with the low-angle radiation when vertically oriented and bottom-fed, makes the delta loop popular for DX-oriented stations that cannot install a [Yagi](/antennas/yagi).

### Construction

A delta loop for 40 metres requires about 43 metres (140 feet) of wire and a vertical dimension of roughly 12 metres (40 feet). This usually means the top wire is supported between two high points (trees, masts, or buildings) and the bottom apex is anchored near or just above the ground.

A delta loop for 20 metres is half that size and more practical for many installations. Multi-band operation is possible with a tuner, though dedicated single-band delta loops are simpler to optimise.

## Quad loop

The **cubical quad** antenna uses one or more full-wave square loops arranged on a boom, analogous to a [Yagi](/antennas/yagi). A single quad loop (one element) is a full-wave loop antenna that can be oriented horizontally or vertically. A multi-element quad array (with reflector and director loops) provides gain and directivity similar to a Yagi.

### Quad vs. Yagi

The quad has some theoretical advantages over a Yagi of equivalent boom length — slightly higher gain (about 1–2 dB), a broader frequency response, and better performance at lower heights. In practice, these advantages are debated and depend on the specific designs being compared.

The main disadvantage of the quad is mechanical complexity. Each element is a loop rather than a straight rod, requiring a support structure (spreaders) at each corner. This makes the quad heavier, more wind-resistant, and more difficult to maintain than a Yagi of similar gain. Spider-style spreaders made from fibreglass are common.

Quad antennas have a dedicated following, particularly for 2-element and 3-element designs on 20, 15, and 10 metres. Multi-band quads (with concentric loops for different bands on the same spreaders) are available commercially and as homebrew designs.

## Choosing a loop antenna

The right loop antenna depends on your situation:

- **Very limited space or antenna restrictions:** Small magnetic loop — compact, no ground system, can be used indoors
- **Moderate space, want multi-band HF:** Full-wave horizontal loop with ladder line and tuner — excellent all-around performer
- **DX focus, vertical installation possible:** Delta loop, bottom-fed — low-angle radiation with useful gain
- **Want directional gain, accept mechanical complexity:** Quad array — Yagi-class performance with loop elements
- **NVIS/regional communication on the low bands:** Full-wave horizontal loop at modest height — ideal high-angle radiator

## Where to go next

- [Dipole Antennas](/antennas/dipole) — The half-wave dipole for comparison
- [Wire Antennas](/antennas/wire-antennas) — Other wire antenna designs
- [Yagi-Uda Antennas](/antennas/yagi) — Directional antennas for comparison with the quad
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Radiation patterns, gain, and polarisation
- [Portable Antennas](/antennas/portable-antennas) — Magnetic loops and other portable options
- [Antenna Restrictions](/antennas/antenna-restrictions) — When a magnetic loop is your best option
- [Building Antennas](/antennas/building-antennas) — Construction techniques and safety
