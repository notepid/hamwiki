---
title: Yagi-Uda Antennas
description: Directional Yagi antennas — how they work, design principles, practical considerations, and why the Yagi remains the king of HF and VHF directional antennas
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, yagi, directional, beam, hf, vhf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Yagi-Uda Antennas

The Yagi-Uda antenna (commonly called simply the "Yagi" or "beam") is the most widely used directional antenna in amateur radio. It provides gain, directivity, and front-to-back ratio that wire antennas cannot match, making it the antenna of choice for DX chasing, [contesting](/contesting/overview), and any situation where you want to concentrate your signal in a specific direction. If you have ever seen a rooftop TV antenna, you have seen a Yagi — and the same principles apply in amateur radio, just at different frequencies and scales.

## How a Yagi works

A Yagi antenna consists of a **driven element** (the element connected to the feedline) and one or more **parasitic elements** (elements that are not directly connected to the feedline but interact with the driven element through electromagnetic coupling). The parasitic elements are arranged in a line along a **boom**, with the driven element in the middle region.

### The three element types

**Driven element:** This is a [dipole](/antennas/dipole) (or folded dipole) at the centre of the array. It is the only element connected to the feedline. Its length is approximately one-half wavelength at the design frequency.

**Reflector:** A single element positioned behind the driven element (on the side away from the desired direction of maximum radiation). The reflector is slightly longer than the driven element — typically about 5% longer. It re-radiates energy that would otherwise go backward, redirecting it forward.

**Directors:** One or more elements positioned in front of the driven element (on the side of desired maximum radiation). Directors are slightly shorter than the driven element — typically 5–10% shorter, with each successive director slightly shorter than the one before it. Directors focus the energy into a narrower forward beam.

### How the parasitic elements work

When the driven element radiates, its electromagnetic field induces current in the parasitic elements. These parasitic elements re-radiate, and the phase and amplitude of their re-radiation depends on their length and spacing relative to the driven element. By carefully choosing these dimensions, the fields from all elements add constructively in the forward direction and cancel in the backward direction — producing a directional beam.

The reflector's slightly longer length causes it to re-radiate with a phase that reinforces forward radiation and cancels backward radiation. Each director's shorter length causes it to re-radiate with a phase that draws energy forward along the boom. The combined effect is a beam of energy concentrated in one direction.

## Performance characteristics

### Gain

A Yagi's gain increases with the number of elements and the boom length. Approximate gain figures for well-designed Yagis:

| Configuration | Approximate gain (dBd) | Approximate gain (dBi) |
|--------------|----------------------|----------------------|
| 2 elements (driven + reflector) | 4–5 | 6–7 |
| 3 elements | 6–8 | 8–10 |
| 4 elements | 7–9 | 9–11 |
| 5 elements | 8–10 | 10–12 |
| 6+ elements | 9–12 | 11–14 |

These figures assume optimal element lengths and spacing. Real-world gain depends on the specific design, height above ground, and surrounding environment. Be cautious of manufacturer claims that seem unusually high — gain is sometimes overstated by using peak free-space figures rather than realistic installed performance.

Remember that each 3 dB of gain is equivalent to doubling your transmit power. A 3-element Yagi with 7 dBd of gain makes your 100-watt transmitter perform like a 500-watt station driving a dipole — in the direction the antenna is pointed.

### Front-to-back ratio

The **front-to-back ratio (F/B)** measures how much energy goes forward compared to backward. A well-designed 3-element Yagi typically achieves 20–30 dB of F/B ratio, meaning the signal off the back is 100 to 1000 times weaker than the signal off the front. This is enormously useful for reducing interference from stations behind you while working the station in front of you.

### Beamwidth

**Beamwidth** is the angular width of the main lobe (typically measured at the -3 dB points). A typical 3-element HF Yagi has a horizontal beamwidth of about 60–70 degrees. Higher-gain Yagis with more elements have narrower beamwidths, requiring more precise aiming. For VHF long Yagis used in [satellite work](/antennas/satellite-antennas) or weak-signal operation, beamwidths can be as narrow as 20–30 degrees.

### Bandwidth

Yagi bandwidth (the frequency range over which the SWR remains acceptable) depends on the element diameter and spacing. HF Yagis using large-diameter aluminium tubing generally cover an entire amateur band with SWR below 2:1. Some designs use multi-band traps or interlaced elements to cover multiple bands.

## Feeding the Yagi

The feed point impedance of a Yagi varies with the design but is typically lower than a standalone dipole — often in the 20–35 ohm range for a standard driven element. This mismatch with 50-ohm coax must be addressed:

**Gamma match:** The most common matching method for HF Yagis. A gamma rod runs parallel to the driven element, connected at one end to the boom (ground) and capacitively coupled to the driven element at the other end. Adjusting the rod length and coupling point sets the impedance to 50 ohms. The gamma match is robust, weatherproof, and does not require a [balun](/antennas/baluns-and-ununs) because it provides an unbalanced feed point.

**Beta match (hairpin match):** A short-circuited transmission-line stub connected across the feed point that adds inductance to cancel the capacitive reactance and raise the resistive impedance. Simple and effective.

**Folded dipole driven element:** Replacing the simple driven element with a folded dipole raises the feed point impedance by approximately four times (to about 100–140 ohms), which can then be matched to 50-ohm coax with a 4:1 balun. This approach also provides wider bandwidth.

**Direct 50-ohm feed:** Some modern Yagi designs (like those optimised with computer modelling) achieve close to 50-ohm impedance through careful element dimensioning, allowing direct coax connection with just a choke balun.

## HF Yagis

HF Yagis are large antennas by any measure. A 3-element Yagi for 20 metres has a boom about 5–7 metres (16–24 feet) long, with elements spanning about 10 metres (33 feet). A 3-element 40-metre Yagi roughly doubles those dimensions. These antennas are heavy and present significant wind load, requiring substantial towers and rotators.

### Monoband vs. multi-band

**Monoband Yagis** are designed for a single band and offer the simplest design and best performance per element. Stacking monoband Yagis for different bands on the same tower (at different heights) is the approach favoured by serious contesters and DXers.

**Multi-band (tribander) Yagis** cover three or more bands — typically 20, 15, and 10 metres — using a single set of elements. They achieve this through traps (LC circuits that electrically shorten or lengthen elements for different bands), interlaced elements, or open-sleeve coupling. Tribanders are extremely popular because they offer good performance on three bands with a single antenna and rotator. The trade-off is slightly reduced performance compared to equivalent monoband designs, and greater mechanical complexity.

Common tribander configurations include 3-element designs (one reflector, one driven element, one director for each band, using traps) and larger 5–6 element designs that add extra directors for selected bands.

### Towers and rotators

An HF Yagi requires a **tower** or substantial mast to support it at a useful height (typically 12–25 metres / 40–80 feet) and a **rotator** to turn it toward the desired direction. This represents a significant investment in infrastructure, planning, and (in many areas) permits and approvals.

Tower safety is a serious matter — see [Building Antennas](/antennas/building-antennas) for information on safe tower practices, and [Antenna Restrictions](/antennas/antenna-restrictions) for regulatory and zoning considerations.

For operators who cannot install a full tower, **lower-height Yagis** on shorter masts or even roof tripods still provide meaningful gain over wire antennas, and small tribanders designed for lighter-duty installations are available.

## VHF/UHF Yagis

At VHF and UHF frequencies, Yagi elements are much shorter (a half wavelength at 144 MHz is about 1 metre / 3.3 feet), so Yagis can be much larger in terms of wavelengths — and therefore higher in gain — while remaining physically manageable.

Long VHF Yagis with 10–20 elements are commonly used for weak-signal SSB/CW work on 2 metres and 70 cm, for working [amateur satellites](/antennas/satellite-antennas), and for [moonbounce (EME)](/satellites/eme-moonbounce) communication. These antennas can provide 15 dBd or more of gain.

For [satellite work](/antennas/satellite-antennas), crossed Yagis (two Yagis mounted at right angles on the same boom) provide circular polarisation, which is preferred for satellite communication.

Portable VHF Yagis made from lightweight materials (arrow shafts, tape measures, fibreglass) are popular for satellite passes and portable operating events.

## Yagi design and modelling

Modern Yagi design relies heavily on [computer modelling](/antennas/antenna-modeling). Software like EZNEC, 4nec2, and MMANA-GAL can optimise element lengths, spacings, and diameters to maximise gain, front-to-back ratio, bandwidth, and feed point impedance — trade-offs that are difficult to manage by rule of thumb.

Several published designs by antenna engineers (such as those by W6NL/K1FO, G0KSC, WA3FET, and many others) are freely available and have been built and validated by thousands of amateurs. Building from a proven design and using modelling software to verify performance with your specific materials is the recommended approach.

## Mechanical considerations

A Yagi is a mechanical structure that must survive wind, ice, and its own weight while maintaining precise element dimensions. Key considerations:

- **Element material:** Aluminium tubing is standard for HF and VHF Yagis. Telescoping sections allow for adjustable element lengths and easy transport. Wall thickness must be adequate for the element span and expected wind load.
- **Boom material:** Aluminium or steel. The boom must be stiff enough to prevent drooping, especially on long-boom designs. Boom-to-element mounting hardware must make reliable electrical contact (or use insulated mounting, depending on the design).
- **Mounting:** The antenna connects to the mast via a boom-to-mast plate. Proper U-bolts and saddle clamps prevent the antenna from rotating in wind. The balance point should be at or near the mast attachment to minimise stress on the rotator.
- **Wind survival:** Yagis present significant wind load. Designs must account for wind forces on the elements, boom, and mounting hardware. Published wind survival ratings should be realistic, not optimistic.
- **Icing:** In cold climates, ice accumulation on elements adds weight and wind load. Some operators use element covers or accept that icing may require reduced operation during severe weather.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Gain, radiation patterns, and the theory behind directional antennas
- [VHF/UHF Antennas](/antennas/vhf-uhf-antennas) — VHF/UHF-specific antenna designs including Yagis
- [Satellite Antennas](/antennas/satellite-antennas) — Yagis and crossed Yagis for satellite work
- [Antenna Modeling](/antennas/antenna-modeling) — Software tools for designing and optimising Yagis
- [Building Antennas](/antennas/building-antennas) — Construction techniques, towers, and safety
- [Antenna Restrictions](/antennas/antenna-restrictions) — Permits, zoning, and regulations for towers and large antennas
