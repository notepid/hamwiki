---
title: HF Transceivers
description: Transceivers for the HF bands — features, options, and popular models for 1.8–54 MHz operation
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, hf, transceivers
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# HF Transceivers

An HF transceiver is the centrepiece of any station built for long-distance communication. These radios operate on the **high-frequency bands** from **1.8 MHz (160 m) to 30 MHz (10 m)**, with most modern models also covering **50 MHz (6 m)**. Thanks to skywave propagation — signals bouncing off the ionosphere — an HF station with modest power and a reasonable antenna can reach across continents, making HF the backbone of worldwide amateur communication.

## How an HF Transceiver Works

At its core, an HF transceiver is two devices in one: a **receiver** that converts incoming radio signals into audio or data, and a **transmitter** that converts audio or data into a radio signal. Modern transceivers share most of their circuitry between transmit and receive, switching between the two functions with a push-to-talk button (for voice) or automatic keying (for CW and digital modes).

### Superheterodyne architecture

Most HF transceivers use a **superheterodyne** receiver design. The incoming signal is mixed with a local oscillator to convert it to one or more **intermediate frequencies** (IFs) where filtering and amplification are easier to implement. Traditional designs use multiple conversions (double or triple conversion) with crystal or ceramic filters at each IF stage. This architecture has been refined over decades and is well understood.

### Direct-sampling SDR architecture

A growing number of modern transceivers use **direct-sampling software-defined radio** (SDR) architecture. Instead of converting the signal through analog IF stages, the receiver digitises the incoming RF directly (or after a single down-conversion) using a high-speed analog-to-digital converter (ADC). All filtering, demodulation, and noise reduction then happens in digital signal processing (DSP). This approach offers extremely sharp filters, real-time spectrum displays, and flexibility that would be impractical in analog circuits.

## Key Features to Consider

### Output power

Most full-size HF transceivers produce **100 watts** of RF output, which is the standard for general amateur use. Some entry-level models output 50 or 75 watts. At the other end, **QRP transceivers** intentionally limit output to **5–10 watts** for lightweight, portable, and low-power operating.

The 100-watt standard is a good starting point — it provides enough signal for reliable contacts on most bands without requiring an external amplifier, and it can drive an [amplifier](/equipment/amplifiers) if you later decide you want more power.

### Frequency coverage and bands

At minimum, an HF transceiver should cover the amateur bands from 80 m (3.5 MHz) through 10 m (28 MHz). Most current models cover all amateur bands from 160 m through 6 m. Some also include general-coverage receive (0.5–30 MHz or wider), which is useful for listening to shortwave broadcasts, aviation, marine, and utility stations.

### Modes

The standard voice mode on HF is **SSB** (single sideband) — specifically LSB on 160, 80, and 40 m, and USB on 20 m and above. All HF transceivers support SSB. Beyond that, look for:

- **CW** (Morse code) — supported by virtually all HF rigs, with varying levels of built-in CW features (keyer, adjustable speed, CW filters)
- **AM** (amplitude modulation) — used on certain frequencies and by vintage radio enthusiasts
- **FM** — useful on 10 m and 6 m repeaters, sometimes included
- **Digital modes** — modern transceivers include USB or built-in sound card interfaces for modes like FT8, JS8Call, PSK31, and RTTY (see [Digital Modes](/digital-modes/overview))

### Receiver performance

The quality of the receiver is what separates a capable transceiver from a frustrating one. Key specifications include:

**Sensitivity** — how well the receiver hears weak signals. On HF, external noise usually dominates, so extreme sensitivity is less important than on VHF/UHF. A typical HF receiver has a sensitivity of around 0.2–0.5 µV for 10 dB signal-to-noise ratio.

**Dynamic range** — the receiver's ability to handle strong signals without overloading or creating spurious responses. A receiver with good dynamic range lets you hear a weak station right next to a very strong one without the strong signal swamping the weak one. This matters most on crowded bands during contests or on the low bands where strong broadcast signals are nearby.

**Selectivity** — how well the receiver separates the desired signal from adjacent signals. This is determined by the IF filters (analog or DSP). A narrow filter (250–500 Hz) for CW, a medium filter (1.8–2.4 kHz) for SSB, and broader filters for AM give the operator flexibility to match conditions.

**Phase noise** — a measure of the local oscillator's spectral purity. Low phase noise means the receiver does not "spread" strong signals into adjacent frequencies. This spec matters most for serious contesters and DXers.

### DSP and filtering

All current-production HF transceivers include some level of **digital signal processing**. At minimum, DSP provides adjustable IF bandwidth, noise reduction, notch filtering (to remove an interfering carrier), and noise blanking (to suppress pulse-type interference like ignition noise). Higher-end models offer continuously adjustable filter bandwidth, filter shape, and multiple layers of noise management.

In SDR-based transceivers, all filtering is done in DSP, giving the operator extraordinary control over passband width and shape with no need for expensive optional crystal filters.

### Spectrum display and waterfall

Many modern HF transceivers include a **real-time spectrum display** or **waterfall** that shows activity across a portion of the band. This is enormously useful — you can see signals, gauge band conditions, and spot activity at a glance without tuning across the band. SDR-based transceivers typically offer wider and higher-resolution displays than traditional superheterodyne designs.

### Built-in antenna tuner

Some HF transceivers include a **built-in automatic antenna tuner** (ATU) that can match a range of antenna impedances. These tuners typically handle SWR up to about 3:1, which is sufficient for a resonant antenna that is slightly off-frequency but not enough for a random wire or severely mismatched antenna. An external tuner provides wider matching range if needed (see [Antenna Tuners](/equipment/antenna-tuners)).

## Categories of HF Transceivers

### Flagship / contest-grade

These are the top-of-the-line models from each manufacturer, built for the most demanding operating scenarios — serious contesting, DXing, and weak-signal work. They feature the best receiver performance, large high-resolution displays, extensive DSP, dual receivers for listening on two frequencies simultaneously, and heavy-duty construction. Price typically ranges from $5,000 to $15,000+. Examples include the Icom IC-7851, Yaesu FTDX101MP, Kenwood TS-890S, and Elecraft K4.

### Mid-range

The sweet spot for most active operators, mid-range transceivers offer excellent receiver performance, good DSP, and solid build quality at a more accessible price. Most include 100 watts output, a built-in ATU, and a spectrum scope. Prices generally fall between $1,500 and $4,000. Examples include the Icom IC-7300, Yaesu FTDX10, and Kenwood TS-590SG.

### Entry-level

Designed for newcomers and operators on a budget, entry-level HF transceivers cover the essential bands and modes with adequate performance for casual operating. They may omit features like built-in ATUs or spectrum scopes. Prices start around $500–$1,200. The Yaesu FT-891, Icom IC-7100, and Xiegu G90 are popular choices in this segment.

### QRP and portable

QRP transceivers are designed for low-power operation, usually 5–10 watts. They prioritise compact size, low weight, and low current draw, making them ideal for portable, backpack, and field operation (activities like SOTA — Summits on the Air — and POTA — Parks on the Air). Popular QRP rigs include the Elecraft KX2 and KX3, Icom IC-705, Lab599 TX-500, and Xiegu X6100.

### Kit transceivers

For those who enjoy building their own equipment, kit transceivers offer a hands-on path to HF operating. Kits range from simple single-band CW transmitters to full-featured multi-band multi-mode transceivers. Building a kit teaches electronics fundamentals and gives you a deep understanding of how your radio works. See [DIY Projects](/diy-projects/overview) for more on homebrewing.

## Major Manufacturers

The HF transceiver market is served by several well-established manufacturers:

**Icom** — A Japanese manufacturer known for the IC-7300 (one of the best-selling HF transceivers of the SDR era), the IC-705 (a popular portable all-mode radio), and the flagship IC-7851.

**Yaesu (Vertex Standard)** — Another Japanese manufacturer with a long history in amateur radio. The FTDX101 series, FTDX10, and FT-891 are widely used.

**Kenwood (JVCKENWOOD)** — Produces the TS-890S (flagship) and TS-590SG (mid-range), both well-regarded for receiver performance.

**Elecraft** — An American company specialising in high-performance transceivers, including the K4 (flagship), K3S, and the KX-series portable radios. Elecraft has a strong following among contesters and QRP operators.

**FlexRadio** — An American company pioneering networked SDR transceivers. The FLEX-6000 series allows remote operation over a network, with the radio hardware separated from the operator interface.

**Xiegu** — A Chinese manufacturer offering affordable HF transceivers such as the G90 and X6100, expanding access to HF for budget-conscious operators.

## Connecting an HF Transceiver

A basic HF station setup involves:

1. **Power supply** — Connect a [13.8 V DC power supply](/equipment/power-supplies) rated for the transceiver's current draw (typically 20–25 A for a 100 W rig).
2. **Antenna** — Run [coaxial cable](/equipment/coaxial-cable) from the transceiver's antenna jack (usually SO-239 / PL-259 or N-type) to your [antenna](/antennas/overview).
3. **Antenna tuner** — Optionally, insert an [antenna tuner](/equipment/antenna-tuners) between the transceiver and the feedline.
4. **Microphone / key** — Plug in a [microphone](/equipment/microphones) for voice or a [key/paddle](/equipment/keyers-and-paddles) for CW.
5. **Computer interface** — For digital modes, connect the transceiver to a computer via USB or a sound card interface. Many modern transceivers handle this through a single USB cable.
6. **Grounding** — Connect the transceiver's ground terminal to a station ground for safety and to reduce noise.

## Tips for Choosing an HF Transceiver

**Match the radio to your operating style.** If you plan to operate mainly from home on SSB and CW, a mid-range base station is a solid choice. If you want to do portable SOTA/POTA activations, a QRP rig makes more sense.

**Receiver quality matters more than output power.** You can always add an amplifier later, but you cannot bolt a better receiver onto a mediocre radio. Prioritise dynamic range and selectivity.

**Consider the ecosystem.** Some manufacturers offer matching accessories (tuners, amplifiers, power supplies) designed to integrate seamlessly with their transceivers.

**Try before you buy if possible.** Visit a local radio club, attend a hamfest, or find an operator who will let you try their rig. Operating feel — the ergonomics of the controls, the audio quality, and the user interface — is personal and hard to judge from specifications alone.

**Used gear can be excellent value.** The ham radio market has a strong second-hand culture, and well-maintained transceivers hold their value. See [Used Equipment](/equipment/used-equipment) for buying tips.

## See Also

- [Equipment Overview](/equipment/overview)
- [VHF/UHF Transceivers](/equipment/vhf-uhf-transceivers)
- [Handheld Radios](/equipment/handheld-radios)
- [SDR Receivers](/equipment/sdr-receivers)
- [Amplifiers](/equipment/amplifiers)
- [Antenna Tuners](/equipment/antenna-tuners)
- [Buying Guide](/equipment/buying-guide)
- [HF Operating](/operating/hf-operating)
