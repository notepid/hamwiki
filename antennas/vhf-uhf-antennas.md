---
title: VHF/UHF Antennas
description: Antennas for VHF and UHF amateur radio — ground planes, collinears, Yagis, discones, and choosing the right antenna for repeater, simplex, and weak-signal work
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, vhf, uhf, repeater, collinear
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# VHF/UHF Antennas

VHF (144 MHz) and UHF (430 MHz) are the bands most amateur radio operators encounter first — they are the home of local [repeaters](/operating/repeaters), simplex communication, [satellite passes](/satellites/overview), and weak-signal work. Because wavelengths are short (about 2 metres at 144 MHz and 70 cm at 430 MHz), antennas are physically small, relatively easy to build and install, and often quite affordable. At the same time, VHF/UHF propagation is primarily line-of-sight, which means antenna **height** and **gain** are critical. A good VHF/UHF antenna can transform a frustrating experience (barely reaching the local repeater) into a reliable one (hitting repeaters 50 km or more away).

## Key considerations at VHF/UHF

Several factors are more important at VHF/UHF than at HF:

**Feedline loss:** [Coaxial cable loss](/antennas/feedlines) increases with frequency. A cable that works fine at HF may waste a significant percentage of your signal at 430 MHz. Use the lowest-loss cable you can for any run longer than a few metres. LMR-400 or equivalent is strongly recommended for permanent VHF/UHF installations.

**Connectors:** Connector quality matters more at higher frequencies. [N-type connectors](/antennas/feedlines) are preferred for UHF and above. PL-259/SO-239 connectors are acceptable for VHF but introduce measurable loss at UHF and should be avoided for 70 cm and above.

**Height:** VHF/UHF signals travel roughly line-of-sight (with some diffraction and refraction). Getting the antenna higher extends the radio horizon dramatically. Even a few metres of additional height can make the difference between reaching a repeater or not.

**Polarisation:** [Polarisation](/antennas/antenna-fundamentals) matching matters much more at VHF/UHF than at HF because there is no ionospheric scrambling. FM and repeater operation uses **vertical polarisation**. SSB and CW weak-signal work uses **horizontal polarisation**. Satellite work uses **circular polarisation**. Using the wrong polarisation can cost 20 dB or more of signal — the difference between a strong contact and nothing at all.

## Omnidirectional antennas

### Ground-plane vertical

The **ground-plane antenna** is a quarter-wave [vertical](/antennas/vertical) element mounted above a set of radial elements. For 2 metres, the vertical element is about 48 cm (19 inches) and each of four radials is the same length. It is simple, inexpensive, and easy to build. With radials sloped downward at about 45 degrees, the feed point impedance is close to 50 ohms, providing a good match to coax.

A ground-plane antenna provides unity gain (0 dBd) with an omnidirectional pattern and is an excellent entry-level base station antenna. It is also a popular homebrew project — one can be built from a panel-mount SO-239 connector and five pieces of stiff wire.

### Collinear vertical

A **collinear antenna** stacks multiple radiating elements vertically, fed in phase, to concentrate radiation toward the horizon. This provides **gain** over a simple ground plane — typically 3–9 dBd depending on the number of elements.

Commercial collinear base station antennas are available in various gains:

| Gain (approx.) | Physical height (2 m band) | Typical use |
|----------------|--------------------------|-------------|
| 3 dBd | ~1.2 m (4 ft) | General home station |
| 6 dBd | ~2.5 m (8 ft) | Extended range, suburban |
| 9 dBd | ~4 m (13 ft) | Maximum range, rural/hilltop |

Higher gain collinears concentrate the pattern into a thinner disc around the horizon. This is beneficial for flat terrain but can be a disadvantage in hilly areas where you need to communicate with stations at significant elevation differences (above or below you). In mountainous terrain, a lower-gain antenna with broader vertical coverage may actually perform better.

### J-pole and slim jim

The **J-pole** is a half-wave vertical antenna fed at the base through a quarter-wave matching stub (shaped like the letter J). It is a popular homebrew design, often built from copper plumbing pipe or 300-ohm ladder line. The J-pole provides slightly more gain than a ground plane (about 0–1 dBd) and does not require radials.

The **slim jim** is a variant that places the matching section along the same axis as the radiating element, making it a flat, narrow design that can be rolled up for portable use. Slim jims are particularly popular as lightweight [portable antennas](/antennas/portable-antennas) — a 2-metre slim jim made from ladder line weighs almost nothing and rolls up to fit in a pocket.

### Discone antenna

The **discone** is a broadband omnidirectional antenna consisting of a disc and a cone. It covers a very wide frequency range (typically 10:1 or more, such as 25 MHz to 1300 MHz) with acceptable SWR, making it popular for scanning receivers and for operators who want a single antenna covering multiple VHF/UHF bands.

The trade-off for this wide bandwidth is that the discone offers little or no gain on any specific frequency — it is essentially a unity-gain antenna across its entire range. For serious work on a specific band, a resonant antenna will outperform a discone. But for general monitoring and casual multi-band VHF/UHF operation, a discone is a practical choice.

## Directional antennas

### Yagi-Uda

The [Yagi](/antennas/yagi) is the primary directional antenna for VHF/UHF. Because elements are small at these frequencies, Yagis with many elements and high gain are physically practical. A 9-element Yagi for 2 metres might have a boom length of about 3 metres (10 feet) and provide 11–12 dBd of gain.

VHF/UHF Yagis are used for:

- **Weak-signal SSB/CW work** — contacting distant stations via tropospheric propagation, meteor scatter, or other propagation modes
- **[Satellite communication](/antennas/satellite-antennas)** — tracking amateur satellites across the sky
- **[Moonbounce (EME)](/satellites/eme-moonbounce)** — bouncing signals off the moon (requiring very high gain, often multiple stacked Yagis)
- **Contesting** — VHF/UHF contests reward both distance and the number of contacts
- **Direction finding** — fox hunts and transmitter hunting

For horizontally polarised weak-signal work, the Yagi is mounted with elements horizontal. For FM repeater work (rarely done with a Yagi, but possible), it would be mounted vertically.

### Log-periodic dipole array (LPDA)

The **LPDA** is a broadband directional antenna that covers a wide frequency range with moderate gain (typically 5–7 dBd). Unlike a Yagi, which is optimised for a narrow bandwidth, the LPDA maintains consistent performance across its entire design range. This makes it useful for scanning, wideband monitoring, and situations where coverage of many frequencies is more important than maximum gain on one frequency.

## Dual-band and multi-band antennas

Many VHF/UHF operators want a single antenna that covers both 2 metres and 70 cm. Several approaches work:

**Dual-band collinear verticals** are the most common solution for base stations. They use multiple resonant sections to provide gain on both bands from a single antenna and feedline.

**Dual-band Yagis** are less common but exist. Some designs use interlaced elements for 2 metres and 70 cm on a single boom, though performance compromises are involved.

**Separate antennas with a diplexer** — using dedicated antennas for each band connected through a diplexer (a filter that combines/separates the two frequency ranges onto a single feedline) is the highest-performance approach. The diplexer introduces a small amount of loss but allows each antenna to be optimised for its band.

## Indoor and attic antennas

When outdoor mounting is not possible (due to [restrictions](/antennas/antenna-restrictions) or living situation), VHF/UHF antennas can often be used in attics or indoors with reasonable results. The short wavelengths mean the antennas are small enough to fit in most attic spaces. Expect some signal loss through the roof structure (typically 3–10 dB depending on materials — tiles and wood are better than metal roofing). Keep the antenna away from metal ductwork, wiring, and other conductive objects.

A simple ground-plane or J-pole in an attic can provide solid repeater access that far exceeds what a handheld with its rubber duck can manage from inside the house.

## Where to go next

- [Vertical Antennas](/antennas/vertical) — Theory behind vertical and ground-plane designs
- [Yagi-Uda Antennas](/antennas/yagi) — Detailed Yagi design and construction
- [Satellite Antennas](/antennas/satellite-antennas) — VHF/UHF antennas for satellite work
- [Mobile Antennas](/antennas/mobile-antennas) — VHF/UHF mobile installations
- [Portable Antennas](/antennas/portable-antennas) — Lightweight VHF/UHF field antennas
- [Feedlines](/antennas/feedlines) — Choosing low-loss cable for VHF/UHF
- [Antenna Restrictions](/antennas/antenna-restrictions) — Indoor and stealth options when outdoor mounting is not possible
