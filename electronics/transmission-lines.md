---
title: Transmission Lines
description: Coaxial cable, ladder line, impedance matching, SWR, and how RF gets from your radio to your antenna
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, transmission-lines, feedline
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Transmission Lines

A transmission line carries radio-frequency energy from your transmitter to your antenna (and received signals back from the antenna to the receiver). Unlike ordinary wire at DC or audio frequencies, at radio frequencies the length, type, and impedance of the feedline all have a significant effect on how much power actually reaches the antenna. Understanding transmission line behaviour is essential for building an efficient station.

## Why transmission lines are different

At low frequencies (DC and audio), a wire is simply a conductor — its length does not matter much as long as the resistance is acceptably low. At radio frequencies, the wire's length becomes a significant fraction of the wavelength, and the signal travels as an electromagnetic wave along the line rather than as a simple flow of current. This wave behaviour means that voltage and current vary along the length of the line, and the line has a **characteristic impedance** that must be considered.

## Characteristic impedance

Every transmission line has a **characteristic impedance (Z₀)**, determined by its physical construction — the spacing between conductors, their diameter, and the dielectric material between them. Characteristic impedance is measured in ohms but is not the same as DC resistance (which should be very low). It describes the ratio of voltage to current for a wave travelling along the line.

Common values in amateur radio:

| Line type | Typical Z₀ | Common use |
|-----------|-----------|------------|
| RG-58 coaxial | 50 Ω | Short runs, mobile, QRP |
| RG-213 coaxial | 50 Ω | General-purpose HF station feedline |
| LMR-400 coaxial | 50 Ω | Lower-loss runs, VHF/UHF |
| RG-59 coaxial | 75 Ω | Video, some receive-only applications |
| RG-11 coaxial | 75 Ω | CATV, some antenna matching |
| 300 Ω twin-lead | 300 Ω | TV antennas, some HF dipoles |
| 450 Ω ladder line | 450 Ω | Low-loss HF balanced feedline |
| 600 Ω open wire | 600 Ω | Very low loss, homebrew balanced line |

The choice of feedline depends on the antenna impedance, the length of the run, the frequencies used, and practical considerations like weather resistance and ease of routing.

## Types of transmission lines

### Coaxial cable

**Coaxial cable** (coax) has a central conductor surrounded by a dielectric insulator, a braided or foil outer conductor (shield), and a protective jacket. The shield confines the electromagnetic field between the two conductors, preventing the feedline from radiating or picking up interference.

Coax is the most common feedline in amateur radio because it is easy to route, flexible, weather-resistant, and available in many sizes. Its 50 Ω impedance matches most amateur transmitters and many common antenna designs.

The main disadvantage of coax is **loss** — signal energy is converted to heat in the centre conductor, the shield, and the dielectric. Loss increases with frequency and cable length, and increases dramatically when SWR is high. Choosing a larger, lower-loss cable (LMR-400 instead of RG-58, for example) is the primary way to reduce feedline loss.

### Balanced feedlines

**Balanced** (parallel-conductor) lines such as ladder line, window line, and open-wire line carry the signal on two conductors with equal and opposite currents. Because the fields from the two conductors largely cancel, balanced lines have very low loss — often an order of magnitude less than coax at HF frequencies.

The trade-off is that balanced lines are more difficult to route (they must be kept away from metal objects and cannot be coiled tightly), and they typically require a balun or antenna tuner to interface with 50 Ω unbalanced equipment. Despite these inconveniences, balanced feedlines are an excellent choice for multiband dipoles and other antennas that present high impedance or significant mismatch, because the low loss means very little power is wasted even at high SWR.

### Waveguides

At microwave frequencies (above a few GHz), hollow metal tubes called **waveguides** replace coaxial cable. Waveguides have extremely low loss at their design frequency but are bulky, expensive, and work over a limited bandwidth. Amateur microwave experimenters use waveguides for high-performance applications.

## Standing waves and SWR

When a transmission line is connected to a load (antenna) whose impedance exactly matches the line's characteristic impedance, all the power travelling down the line is absorbed by the load. The line is said to be "matched" or "flat."

When the load impedance differs from the characteristic impedance, some power is **reflected** back toward the transmitter. The forward-travelling and reflected waves combine on the line, creating a pattern of voltage maximums and minimums called a **standing wave**.

### Standing wave ratio (SWR)

**Standing wave ratio (SWR)** — also called VSWR (voltage standing wave ratio) — quantifies the degree of mismatch:

**SWR = V_max / V_min**

A perfectly matched line has SWR = 1:1. Higher values indicate greater mismatch. Some reference points:

| SWR | Reflected power | Situation |
|-----|----------------|-----------|
| 1:1 | 0% | Perfect match |
| 1.5:1 | 4% | Excellent — typical well-tuned antenna |
| 2:1 | 11% | Good — acceptable for most operation |
| 3:1 | 25% | Marginal — consider tuning or matching |
| 5:1 | 44% | Poor — most transmitters will reduce power |
| ∞:1 | 100% | Open or short circuit — no power delivered |

### What high SWR really means

A common misconception is that high SWR means massive power loss. In reality, the reflected power travels back to the transmitter, where it is re-reflected and eventually delivered to the antenna (minus the loss for each round trip). The real cost of high SWR is **increased feedline loss** — every trip up and down the line dissipates some energy as heat. On a short run of low-loss cable, even fairly high SWR causes minimal total loss. On a long run of lossy cable, the extra round trips add up.

This is why balanced feedlines (with their very low loss) tolerate high SWR so well — the power simply bounces back and forth with minimal loss per trip until it reaches the antenna.

## Impedance matching

When the antenna impedance does not match the feedline characteristic impedance, an **impedance matching** device is used at one or both ends of the feedline. The goal is to present the transmitter with the 50 Ω load it expects for maximum power transfer and safe operation.

### Antenna tuners

An **antenna tuner** (more accurately, a transmatch) is an adjustable impedance matching network placed between the transmitter and the feedline. It transforms whatever impedance appears at the end of the feedline into the 50 Ω the transmitter wants to see. It does not reduce feedline loss — it simply lets the transmitter deliver full power into the feedline despite the mismatch.

Antenna tuners are essential when using multiband antennas with a single feedline, or when using balanced feedlines with unbalanced transmitters. They range from simple L-networks to elaborate roller inductors and are available in manual and automatic configurations.

### Baluns and ununs

A **balun** (balanced-to-unbalanced transformer) converts between a balanced feedline (like ladder line or the driven element of a dipole) and an unbalanced feedline (coax). Baluns are typically rated by their impedance ratio: a 1:1 balun connects equal impedances, while a 4:1 balun converts between 200 Ω and 50 Ω, for example.

An **unun** (unbalanced-to-unbalanced transformer) transforms between different unbalanced impedances — for example, matching a 200 Ω end-fed wire to 50 Ω coax.

See [Baluns and Ununs](/antennas/baluns-and-ununs) for more detail on these devices.

## Feedline loss

Loss in a feedline depends on the cable type, its length, the operating frequency, and the SWR. Cable manufacturers specify **matched loss** (loss at SWR 1:1) per unit length at various frequencies. Higher frequency means more loss — a run of RG-213 that loses 1 dB at 7 MHz might lose 3 dB at 144 MHz.

Additional loss from SWR can be estimated using published tables or online calculators. As a practical matter: use the lowest-loss cable you can afford for the run length, and keep coax runs as short as reasonable.

### Velocity factor

Radio waves travel slower in a transmission line than in free space. The **velocity factor** is the ratio of the wave's speed in the line to its speed in free space, expressed as a percentage. Solid polyethylene dielectric coax has a velocity factor around 66%, meaning waves travel at 66% of the speed of light. Foam dielectric cables are around 78–85%.

Velocity factor matters when cutting cables to specific electrical lengths — for example, when making quarter-wave matching sections or phasing harnesses. The physical length of a quarter wavelength in the cable is:

**Physical length = (λ/4) × velocity factor**

## Connectors

Common RF connectors in amateur radio include:

**PL-259/SO-239 (UHF connector):** The most widely used HF connector. Adequate for HF and reasonable at VHF, though it is not a true constant-impedance design and becomes increasingly lossy above 150 MHz.

**BNC:** A bayonet-locking connector with good 50 Ω characteristics. Popular for VHF/UHF handheld radios, test equipment, and low-power applications.

**N-type:** A precision threaded connector with excellent performance through 11 GHz. The standard choice for VHF and UHF base station installations where PL-259 performance is inadequate.

**SMA:** A small threaded connector used on handheld radios, SDR devices, and microwave equipment. Good performance to 18 GHz or higher depending on the variant.

Proper connector installation is important — a poorly soldered or assembled connector can introduce significant loss and unreliable connections, and is one of the most common causes of station problems.

## See also

- [AC Circuits](/electronics/ac-circuits) — impedance fundamentals
- [Filters & Theory](/electronics/filters-theory) — matching networks are a form of filter
- [Transmitters](/electronics/transmitters) — output impedance and SWR protection
- [RF Safety](/electronics/rf-safety) — feedline radiation and safety
- [Baluns and Ununs](/antennas/baluns-and-ununs) — impedance transformation devices
