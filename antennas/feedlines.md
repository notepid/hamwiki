---
title: Feedlines & Transmission Lines
description: Coaxial cable, ladder line, and other transmission lines — how they work, how to choose, and how to install them properly
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, feedline, coax, ladder-line, transmission-line
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Feedlines & Transmission Lines

The feedline is the link between your radio and your antenna. Its job is simple in concept — carry RF energy from the transmitter to the antenna, and from the antenna to the receiver — but the choice of feedline, how it is installed, and how well it is matched to the rest of the system can have a significant impact on station performance. A poor feedline installation can waste more of your signal than a mediocre antenna.

## What is a transmission line?

A **transmission line** is any conductor system designed to carry electromagnetic energy from one point to another with controlled characteristics. In amateur radio, the term **feedline** is used interchangeably with transmission line when referring to the cable between the radio and the antenna.

All transmission lines have a **characteristic impedance** (Z₀) — the impedance the line presents to a signal travelling along it. This impedance is determined by the physical construction of the line (conductor size, spacing, and dielectric material) and is constant along the line's length regardless of how long the line is. The most common characteristic impedances in amateur radio are **50 ohms** (coaxial cable) and **300–600 ohms** (open-wire and ladder line).

## Types of feedline

### Coaxial cable

Coaxial cable ("coax") is by far the most widely used feedline in amateur radio. It consists of a central conductor surrounded by a dielectric insulator, which is surrounded by a braided or foil shield conductor, all enclosed in a protective outer jacket.

Coax is popular because it is self-shielding — the outer conductor contains the electromagnetic field inside the cable, so it can be routed near metal objects, run through conduits, and buried without significantly affecting its performance. It is also relatively easy to work with and available with a wide range of standard connectors.

**Common coaxial cables for amateur radio:**

| Cable type | Z₀ (ohms) | Outer diameter | Loss at 30 MHz (per 30 m / 100 ft) | Loss at 150 MHz (per 30 m / 100 ft) | Typical use |
|-----------|-----------|---------------|-------------------------------------|--------------------------------------|-------------|
| RG-174 | 50 | 2.8 mm (0.11 in) | ~3.3 dB | ~7.5 dB | Short jumpers only |
| RG-58 | 50 | 5 mm (0.20 in) | ~1.8 dB | ~4.2 dB | Short runs, QRP, receive |
| RG-8X | 50 | 6.1 mm (0.24 in) | ~1.5 dB | ~3.5 dB | Portable operations, moderate runs |
| RG-213 / RG-8 | 50 | 10.3 mm (0.41 in) | ~0.9 dB | ~2.1 dB | General HF/VHF station use |
| LMR-400 | 50 | 10.3 mm (0.41 in) | ~0.6 dB | ~1.4 dB | Lower-loss general purpose |
| LMR-600 | 50 | 14.9 mm (0.59 in) | ~0.4 dB | ~1.0 dB | Long runs, VHF/UHF |
| RG-62 | 93 | 6.1 mm (0.24 in) | ~1.2 dB | ~2.9 dB | Specialised matching |
| RG-11 | 75 | 10.3 mm (0.41 in) | ~0.7 dB | ~1.7 dB | CATV, some antenna matching |

*Loss figures are approximate and vary by manufacturer. Always consult the specific cable's datasheet for accurate values.*

**Key points about coax:**

The most important consideration when choosing coax is **loss**. Loss increases with frequency and cable length, and it increases significantly when the [SWR](/antennas/swr-and-matching) on the line is high. For HF use with reasonable SWR, RG-213 or LMR-400 are excellent choices for typical run lengths. For VHF/UHF, where losses are higher, lower-loss cable like LMR-400 or LMR-600 becomes more important, especially for longer runs.

Thin cables like RG-58 and RG-174 are suitable for short jumper cables and portable use, but should be avoided for permanent station feedlines longer than a few metres, particularly at VHF and above.

### Open-wire and ladder line

**Open-wire line** (also called parallel wire, window line, or ladder line) consists of two parallel conductors held at a fixed spacing by periodic insulating spacers. It has a much higher characteristic impedance than coax — typically 300 to 600 ohms depending on conductor spacing and diameter.

The great advantage of open-wire line is its **extremely low loss**, even when operating at high SWR. This makes it an excellent choice for multi-band antenna systems where a single antenna is used on many bands with an antenna tuner. A centre-fed doublet fed with ladder line and a tuner is one of the most versatile and efficient antenna systems possible.

The disadvantage is that open-wire line is **not self-shielding**. It radiates if it runs near metal objects, if the spacing between conductors varies, or if it is not kept clear of the ground and other structures. It cannot be run through metal conduit, and routing it into the house typically requires more care than coax.

**Common open-wire line types:**

- **300-ohm twinlead** — flat ribbon cable commonly used for FM radio and TV antennas. Lightweight and inexpensive but fragile, and its loss increases dramatically when wet. Not recommended for transmitting use.
- **450-ohm window line (ladder line)** — two conductors held apart by a plastic web with rectangular windows punched out to reduce dielectric losses. Widely available and an excellent general-purpose choice for open-wire feedlines.
- **600-ohm open-wire line** — two conductors with wider spacing, sometimes home-built using wire and periodic spacers. The lowest loss option available, but requires more care in routing.

### Hardline

**Hardline** is coaxial cable with a solid or corrugated outer conductor (usually copper or aluminium) rather than a braided shield. It offers significantly lower loss than flexible coax of the same diameter but is rigid or semi-rigid and more difficult to install. Hardline is used in commercial installations and by amateurs who need the lowest possible loss for long runs or at VHF/UHF/microwave frequencies. Surplus commercial hardline can sometimes be obtained at reasonable cost.

## Characteristic impedance and matching

For maximum power transfer and minimum loss, the feedline's characteristic impedance should match both the radio's output impedance and the antenna's feed point impedance. Most amateur equipment is designed for **50 ohms**, so 50-ohm coax is the standard choice.

When the impedances do not match, some of the power is reflected back from the mismatch point, creating **standing waves** on the feedline. The severity of this mismatch is measured by the [Standing Wave Ratio (SWR)](/antennas/swr-and-matching). A 1:1 SWR means a perfect match; higher values indicate increasing mismatch.

A moderate SWR (up to about 2:1 or 3:1) on coax causes relatively little additional loss at HF with quality cable. But high SWR on coax at VHF/UHF, or on long runs, can result in significant additional power lost as heat in the cable. This is where open-wire line shines — its inherently low loss means that even very high SWR values cause only modest additional loss.

[Baluns and ununs](/antennas/baluns-and-ununs) are used to transform impedances and to transition between balanced lines (like ladder line and dipoles) and unbalanced lines (like coax).

## Connectors

The feedline must be terminated with connectors to attach to the radio and antenna. Common RF connectors in amateur radio include:

- **PL-259 / SO-239 (UHF connector)** — the most common connector in amateur radio, despite its name being misleading (it was designed in the 1930s when UHF meant something different). Adequate for HF use and acceptable for VHF, but not ideal above 150 MHz due to impedance discontinuities. Easy to install and universally compatible with amateur equipment.
- **BNC** — a compact bayonet-style connector with better RF performance than PL-259. Common on handheld radios and test equipment. Rated for use up to several GHz.
- **N-type** — a precision 50-ohm connector designed for use well into the GHz range. Preferred for UHF, microwave, and any application where connector quality matters. Larger and more expensive than BNC.
- **SMA** — a small threaded connector used on many modern handheld radios and on SDR dongles. Good performance at high frequencies but fragile and not intended for frequent connection/disconnection cycles.

**Connector installation quality matters.** A poorly installed connector with exposed shield braid, a cold solder joint, or moisture inside is a source of loss and intermittent problems. Take the time to learn proper connector installation for your chosen cable types, and consider using weatherproofing (self-amalgamating tape or heat-shrink with sealant) on any outdoor connections.

## Feedline loss in practice

Feedline loss is measured in **decibels (dB)**. Every 3 dB of loss means half your power is being lost as heat in the feedline. Here is what that means in practice:

| Feedline loss | Power reaching antenna | Equivalent effect |
|--------------|----------------------|-------------------|
| 0.5 dB | 89% | Barely noticeable |
| 1 dB | 79% | Minimal impact |
| 2 dB | 63% | Noticeable but acceptable |
| 3 dB | 50% | Half your power is wasted |
| 6 dB | 25% | Three-quarters wasted — serious problem |
| 10 dB | 10% | Most power lost — feedline needs attention |

Loss increases with frequency, cable length, and SWR. The combination of these factors means that a feedline that works fine for HF may be unacceptable for the same length at UHF.

When calculating total system loss, remember that feedline loss affects both transmit and receive. A 3 dB feedline loss costs you 3 dB on transmit (half the power reaches the antenna) and 3 dB on receive (half the received signal reaches the radio) — a total of 6 dB effective loss in the communication link.

## Installation best practices

Proper feedline installation protects performance and extends the life of your cable:

- **Keep coax runs as short as practical.** Route directly between the radio and antenna rather than leaving excess cable coiled up. A coil of extra coax adds loss and can create unwanted inductance.
- **Protect outdoor connections from moisture.** Water inside coax dramatically increases loss and will eventually corrode the conductors. Seal outdoor connections with self-amalgamating tape, coax seal, or heat-shrink with adhesive lining.
- **Support the cable to prevent strain.** The cable's weight should not hang from the connector or the antenna feed point. Use cable ties, clamps, or a drip loop to manage weight and prevent water from running down into connectors.
- **Avoid sharp bends.** Each cable type has a minimum bend radius (typically 5–10 times the cable diameter for coax). Bending tighter than this can damage the dielectric or deform the centre conductor, creating an impedance bump and increased loss.
- **Keep ladder line clear of metal.** Open-wire line should be routed at least several centimetres away from metal gutters, downspouts, tower legs, and similar objects. Use standoff insulators where the line passes near the house or tower.
- **Ground the feedline entry point.** Where the feedline enters the building, provide a proper ground connection to protect against static build-up and lightning-induced surges. This is both a safety measure and a regulatory requirement in many countries.
- **Label your cables.** If you have multiple feedlines, label both ends. It saves considerable frustration later.

## Choosing the right feedline

The best feedline for your station depends on your specific situation:

- **Single-band coax-fed antenna (HF):** RG-213 or LMR-400 is an excellent choice for most run lengths.
- **Multi-band antenna with tuner:** 450-ohm ladder line offers the lowest loss and greatest flexibility. The tuner handles the impedance transformation.
- **VHF/UHF station:** Use the lowest-loss coax you can afford, especially for runs over 10 metres (30 feet). LMR-400 or better is recommended.
- **Portable or temporary setup:** RG-8X offers a good compromise between loss, flexibility, and weight.
- **Short jumper cables:** RG-58 or RG-8X is fine for patch cables of a metre or two.

In most cases, spending money on better feedline gives more performance improvement than spending the same money on a more expensive antenna. The feedline is the part of your station that literally throws power away as heat — minimising that waste is always a good investment.

## Where to go next

- [SWR and Matching](/antennas/swr-and-matching) — Understanding standing wave ratio and impedance matching
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Transforming impedances and managing balanced/unbalanced transitions
- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Core antenna concepts including impedance and resonance
- [Building Antennas](/antennas/building-antennas) — Practical construction including feedline installation
