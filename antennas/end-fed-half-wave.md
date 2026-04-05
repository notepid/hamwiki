---
title: End-Fed Half-Wave (EFHW)
description: End-fed half-wave antennas — theory, transformer design, multi-band operation, and why the EFHW has become one of the most popular portable and stealth antennas
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, efhw, wire, portable, hf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# End-Fed Half-Wave (EFHW)

The end-fed half-wave antenna has become one of the most popular antenna designs in amateur radio over the past decade, driven largely by the growth of portable operations like [Parks on the Air (POTA)](/awards/pota) and [Summits on the Air (SOTA)](/awards/sota). Its appeal is straightforward: it needs only a **single elevated support point**, is lightweight and easy to deploy, and can cover multiple HF bands with one wire. Whether you are setting up in a park, operating from a hotel room, or installing a stealth antenna at home, the EFHW is worth understanding.

## How it works

An end-fed half-wave antenna is exactly what the name says — a half-wave wire fed at one end rather than at the centre. This differs from a [dipole](/antennas/dipole), which is the same length of wire fed at the midpoint.

The challenge with end-feeding is **impedance**. At the centre of a half-wave antenna, the impedance is moderate (around 50–75 ohms) — easy to match. At the end, the impedance is very high — theoretically several thousand ohms. This high impedance must be transformed down to 50 ohms for connection to standard coaxial cable and radio equipment.

This transformation is accomplished by an **impedance-matching transformer** (an [unun](/antennas/baluns-and-ununs)), typically with a turns ratio that produces an impedance ratio of 49:1 (for approximately 2450-ohm to 50-ohm transformation) or 64:1 (for approximately 3200-ohm to 50-ohm). The transformer is a compact device — often small enough to fit in one hand — consisting of a ferrite toroid core with two windings.

## Multi-band operation

One of the EFHW's key advantages is inherent multi-band capability. A half-wave antenna is also resonant at its harmonic frequencies — the even and odd multiples of the fundamental frequency. This means a wire cut as a half-wave for **40 metres** (7 MHz) is also approximately resonant on **20 metres** (14 MHz), **15 metres** (21 MHz), and **10 metres** (28 MHz) — four popular HF bands from a single wire.

Similarly, a wire cut for **80 metres** (3.5 MHz) covers 80, 40, 20, 15, and 10 metres — though the 80-metre version is approximately 40 metres (130 feet) long, which requires more space.

In practice, the impedance at the harmonics is not identical to the fundamental, and the [SWR](/antennas/swr-and-matching) varies across bands. Most EFHW antennas provide a direct match (SWR below 2:1) on two or three bands and may need a tuner for others. The transformer design and wire length can be optimised to favour specific bands.

### Common EFHW lengths

| Target bands | Approx. wire length | Notes |
|-------------|-------------------|-------|
| 40/20/15/10 m | 20 m (66 ft) | Most popular portable length |
| 80/40/20/15/10 m | 40 m (130 ft) | Full 80-through-10 coverage |
| 20/15/10 m | 10 m (33 ft) | Compact, higher bands only |
| 30/17/12 m | 14.2 m (46.5 ft) | WARC bands (non-harmonic — tuner usually needed) |

The 40-through-10-metre version at roughly 20 metres of wire is the most common configuration, offering a practical balance between coverage and portability.

## The matching transformer

The heart of an EFHW system is the matching transformer. Most designs use a **toroidal ferrite core** with a primary winding of 2–3 turns and a secondary winding of 14–24 turns (depending on the desired impedance ratio and ferrite material).

### Key design considerations

**Ferrite core selection:** The core must handle the power level without saturating and should provide good performance across the target frequency range. Common choices include FT-140-43 (Fair-Rite type 43 material, suitable for 1–30 MHz, adequate for 100 watts) and larger cores like FT-240-43 for higher power. Type 43 material is the most popular for EFHW transformers, though type 52 material is sometimes used for lower HF frequencies.

**Turns ratio:** A 49:1 transformer (7:1 turns ratio, such as 2:14 or 3:21) is the most common. Some builders prefer a 64:1 ratio (8:1 turns ratio). The "correct" ratio depends on the actual end impedance, which varies with installation — there is no single perfect value.

**Compensation capacitor:** Many EFHW transformer designs include a small capacitor (typically 100–150 pF) across the primary winding. This compensates for parasitic inductance and improves performance at the higher frequency bands.

**Enclosure and weatherproofing:** For permanent installations, house the transformer in a waterproof enclosure. For portable use, many builders use small plastic project boxes. Seal all cable entry points against moisture.

Building an EFHW transformer is one of the most popular [homebrew projects](/diy-projects/overview) in modern amateur radio — the components are inexpensive, the construction is simple, and the satisfaction of building your own multi-band antenna system is considerable.

## Counterpoise

A frequently debated topic with EFHW antennas is the **counterpoise** — a short wire connected to the ground side of the transformer that provides a return path for RF current.

In theory, a perfectly resonant half-wave antenna should have a high-impedance end that does not require a ground reference. In practice, the impedance transformation is imperfect, the wire may not be exactly resonant, and some current does flow on the "ground" side of the transformer. Without a counterpoise, this current flows on the outside of the coax shield, causing the feedline to radiate and potentially bringing RF back into the operating position.

A counterpoise of approximately **0.05 wavelength** (about 1–2 metres for a 40-metre band EFHW) connected to the ground terminal of the transformer is the common recommendation. Some operators experiment with different counterpoise lengths or use multiple counterpoises. The counterpoise should generally be routed away from the main radiating wire, often along the ground or at an angle.

Getting the counterpoise right can make the difference between a clean, quiet station and one plagued by RF feedback and common-mode issues. A [choke balun](/antennas/baluns-and-ununs) on the coax near the transformer can also help suppress common-mode current.

## Deployment configurations

One of the EFHW's great strengths is deployment flexibility. Common configurations include:

**Sloper:** The transformer at the bottom (near the operator), with the wire sloping up to a single high point and the far end tied off. This is the most common portable setup — throw a rope over a tree branch, hoist the far end, and you are on the air.

**Inverted-V:** The wire goes up from the transformer to a central high point, then back down to a far anchor. Similar to an inverted-V dipole but fed at one end.

**Horizontal:** The wire runs horizontally between two supports, with the transformer at one end. Works well for permanent home installations.

**Inverted-L:** The wire goes up vertically from the transformer (attached near the ground) and then runs horizontally at the top. This produces a mix of vertical and horizontal radiation and can be effective for all-around coverage.

**Indoor:** EFHW antennas can be run indoors — along walls, through attic spaces, or around room perimeters. Performance will be reduced compared to outdoor mounting, and RF exposure must be considered (keep the antenna away from occupied areas, especially at higher power levels). Indoor EFHWs are a last resort but can still make contacts, especially with [digital modes like FT8](/digital-modes/ft8).

## EFHW vs. dipole

The EFHW and the centre-fed [dipole](/antennas/dipole) are both half-wave antennas using the same length of wire. The fundamental performance — gain, radiation pattern, efficiency — is very similar. The differences are practical rather than theoretical:

**Advantages of the EFHW:** Only one elevated support point needed (the far end). The feedline connects at one end, which is often more convenient for routing coax. Easier to deploy for portable operations. Multi-band operation without traps.

**Advantages of the dipole:** Simpler feed system (no transformer needed, just a balun). More symmetrical current distribution (less common-mode current tendency). No counterpoise needed. Slightly more predictable behaviour across bands. The centre-fed dipole with ladder line (doublet) is arguably an even more versatile multi-band system.

Neither antenna is "better" in absolute terms — the best choice depends on your specific situation, supports, and operating style.

## Common EFHW issues and solutions

**High SWR on some bands:** The EFHW may not present a good match on all harmonic bands simultaneously. An antenna tuner (internal or external) resolves this. Adjusting the wire length by small amounts can shift the SWR curve to favour your preferred bands.

**RF in the shack:** This usually indicates common-mode current on the coax. Solutions include adding a choke balun on the coax (several ferrite toroids or a coiled-coax choke), adjusting the counterpoise length, and ensuring the wire is truly resonant.

**Transformer heating:** If the ferrite core gets hot during transmission, the core may be too small for the power level, the SWR may be excessively high, or the ferrite material may not be appropriate for the operating frequency. Reduce power, check SWR, and consider a larger core.

**Interaction with surroundings:** Because the wire runs from the feed point in a single direction, the radiation pattern is influenced by how the wire is routed. Bends, slopes, and proximity to structures all affect performance. Experiment with different configurations to find what works best at your location.

## Where to go next

- [Dipole Antennas](/antennas/dipole) — The centre-fed alternative and comparison point
- [Wire Antennas](/antennas/wire-antennas) — Other wire antenna designs including doublets and random wires
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Understanding the matching transformer
- [Portable Antennas](/antennas/portable-antennas) — Antennas for POTA, SOTA, and field operations
- [SWR and Matching](/antennas/swr-and-matching) — Tuning and troubleshooting your EFHW
- [Building Antennas](/antennas/building-antennas) — Construction techniques for wire antennas
