---
title: Filters
description: RF filters for amateur radio — low-pass, high-pass, band-pass, and notch filters for interference reduction and signal selection
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, filters
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Filters

Filters are among the most important — and underappreciated — accessories in the amateur station. A filter selectively passes some frequencies while attenuating others. In amateur radio, filters serve two fundamental purposes: keeping your transmitted signal clean (suppressing harmonics and spurious emissions so you do not interfere with other services) and protecting your receiver from overload caused by strong nearby signals.

Every well-equipped station should have at least a low-pass filter on the transmitter output. As your station grows or if you encounter interference problems, additional filters become essential tools.

## Filter Basics

### Frequency response

A filter's behaviour is described by its frequency response — a plot of signal attenuation versus frequency. The key regions are the **passband** (frequencies the filter passes with minimal loss), the **stopband** (frequencies the filter strongly attenuates), and the **transition band** (the region between passband and stopband where attenuation increases). A steeper transition band means the filter can separate closely spaced signals more effectively, but steeper filters are more complex and expensive.

### Insertion loss

No filter is perfectly transparent in its passband. **Insertion loss** is the small amount of signal power absorbed or reflected by the filter even at frequencies it is designed to pass. Good filters have insertion loss below 0.5 dB in the passband — meaning less than 10% of power is lost. Poorly designed or cheaply built filters may have higher insertion loss.

### Filter order

The **order** of a filter describes its complexity (number of reactive elements — inductors and capacitors) and determines how steeply it transitions from passband to stopband. A higher-order filter has a steeper rolloff and better stopband attenuation, but also has more insertion loss and is more sensitive to component tolerances.

## Types of Filters

### Low-pass filters (LPF)

A **low-pass filter** passes all frequencies below a cutoff frequency and attenuates frequencies above it. In amateur radio, the primary application is on the transmitter output to suppress harmonics.

Every transmitter generates harmonics — signals at integer multiples of the operating frequency. If you transmit on 14 MHz, your transmitter also produces energy at 28 MHz (second harmonic), 42 MHz (third), and so on. These harmonics can interfere with other radio services, particularly broadcast FM (88–108 MHz) and television. An LPF on the transmitter output attenuates these harmonics to safe levels.

Most HF transceivers include internal low-pass filters for each band, but an external LPF provides additional attenuation — a valuable insurance policy, especially when running high power through an amplifier. Standard external LPFs for amateur use include models from ICE (now part of DX Engineering), MFJ, Palstar, and Array Solutions. A typical HF LPF has a cutoff frequency around 30–40 MHz and provides 50+ dB of attenuation at VHF and above.

**If you run an amplifier, always use a low-pass filter between the amplifier and the antenna.** Amplifiers can generate significant harmonic energy, and some amplifier designs (particularly Class C) produce stronger harmonics than the transceiver alone.

### High-pass filters (HPF)

A **high-pass filter** passes frequencies above a cutoff and attenuates those below it. In amateur radio, HPFs are most commonly used to protect consumer electronics from amateur transmissions.

The classic application: your HF transmissions are overloading your neighbour's television or stereo. Installing a high-pass filter (cutoff around 50–55 MHz) on the television's antenna input passes the TV signals (above 54 MHz) while blocking HF energy (below 30 MHz). This is a standard first step in resolving amateur-to-consumer interference complaints.

HPFs designed for this purpose are inexpensive (under 20 USD) and are available from amateur radio suppliers or can be built easily. The ARRL publishes tested designs.

### Band-pass filters (BPF)

A **band-pass filter** passes a specific range of frequencies and attenuates everything above and below that range. Band-pass filters are used for receiver front-end protection in contest and multi-transmitter stations, isolating a specific amateur band from strong out-of-band signals, multi-operator setups where multiple transmitters operate simultaneously (each radio uses a BPF to prevent its signal from desensitising the other radios' receivers), and transmitter filtering where only one specific band's signals should pass.

Commercial band-pass filter sets designed for multi-operator contesting include models from DX Engineering, 4O3A, ICE, and Array Solutions. A typical contest BPF set includes individual filters for each HF band (160 m through 10 m), each providing 30–60 dB of attenuation on the adjacent bands.

### Band-stop (notch) filters

A **band-stop filter** (also called a **notch filter**) does the opposite of a band-pass — it attenuates a narrow range of frequencies while passing everything else. Notch filters are useful for suppressing a specific interfering signal, such as a strong broadcast station near an amateur band. A notch filter tuned to the interferer's frequency removes it while leaving the rest of the band usable.

Some receivers and transceivers include built-in **DSP notch filters** that can automatically detect and suppress steady carriers and tones. These are effective against heterodyne (beat note) interference on HF.

## Filters in the Receive Path

### Preselector filters

A **preselector** is a tunable band-pass filter placed ahead of (or at the input of) the receiver. It restricts the receiver's input to the desired band, reducing overload from strong out-of-band signals. Preselectors are particularly useful with wideband receivers and SDR radios, which may have limited front-end selectivity.

Manual preselectors (like the MFJ-1040C) use variable capacitors and inductors to tune across the HF spectrum. Some modern transceivers include switched preselector filters for each band as part of their front-end design.

### IF and audio filters

Filters inside the receiver's intermediate frequency (IF) chain and audio chain provide selectivity — the ability to separate the desired signal from adjacent-channel signals. Crystal filters, ceramic filters, mechanical filters, and DSP filters are used in various receiver designs. Narrower IF bandwidth allows reception of weaker signals in the presence of strong adjacent signals, but at the cost of audio fidelity.

Most modern transceivers allow the operator to adjust IF bandwidth — wider for casual listening, narrower for crowded band conditions. CW operation typically uses very narrow filters (200–500 Hz), while SSB uses 1.8–2.7 kHz.

## Filters for Interference Reduction

### Common-mode chokes and ferrites

Strictly speaking, a **common-mode choke** is not a traditional LC filter, but it functions as a filter for common-mode RF currents — unwanted currents that flow on the outside of coax shields, power cables, and audio cables, causing radio-frequency interference (RFI). Common-mode chokes are essential for suppressing conducted interference in the station.

Ferrite chokes (snap-on ferrite cores and toroidal cores) placed on cables attenuate common-mode RF. The correct ferrite material depends on the frequency — **Mix 31** ferrite is effective across HF (1–30 MHz), **Mix 43** works well from 1–300 MHz, and **Mix 61** is suited for VHF and above. Fair-Rite and Amidon are major suppliers of ferrite materials.

A good station ground and proper common-mode choking on feedlines, power cables, and audio/USB cables can eliminate many interference problems that no amount of traditional filtering will solve.

### AC line filters

An **AC line filter** (mains filter) attenuates RF energy conducted along the AC power wiring into or out of the shack. Inexpensive AC line filters from companies like Corcom and Schaffner can reduce interference entering the station from external sources (switching power supplies elsewhere in the house, LED lighting, solar inverters) and prevent RF from the transmitter from conducted coupling onto the house wiring.

## Power Handling

Filters in the transmit path must handle the full transmitter (or amplifier) output power. Inadequate filters can overheat, saturate (losing their filtering effectiveness), or even arc at high power levels. Always check the filter's power rating and ensure it matches your station's output.

Most commercial HF low-pass filters are rated for 200–1,500 W. Contest band-pass filter sets are typically rated for 200–500 W per filter. If you run high power, verify that the filters are rated accordingly.

## Building Your Own Filters

Filters are among the most rewarding homebrew projects. Simple low-pass and high-pass filters can be constructed with standard inductors and capacitors, and designs are well-documented in the ARRL Handbook, the ARRL RFI Book, and numerous online resources. A NanoVNA or antenna analyser makes it straightforward to verify a homebrew filter's performance.

Key construction tips: use high-quality capacitors (silver mica or ceramic NPO/C0G for small filters; transmitting mica or doorknob ceramics for high-power filters), wind inductors on appropriate cores (powdered iron or air-wound for transmit filters), and keep leads short to minimise parasitic inductance and capacitance.

## See Also

- [Equipment Overview](/equipment/overview)
- [Amplifiers](/equipment/amplifiers)
- [Coaxial Cable](/equipment/coaxial-cable)
- [RF Connectors](/equipment/connectors)
- [Antenna Tuners](/equipment/antenna-tuners)
- [Test Equipment](/equipment/test-equipment)
