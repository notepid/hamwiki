---
title: Amplifiers
description: RF power amplifiers for amateur radio — how they work, types, selection, and safe operation
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, amplifiers, power
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Amplifiers

A **linear amplifier** (often simply called an "amp" or "linear") boosts the RF output of a transceiver to a higher power level. A typical HF station runs 100 watts from the transceiver; adding an amplifier can raise that to 500–1,500 watts PEP (peak envelope power), the legal limit in many countries. More power means stronger signals at the receiving end, which can make the difference between a solid contact and one lost in the noise — particularly when chasing DX, operating in contests, or pushing through poor propagation.

Amplifiers are not a substitute for a good antenna — improving the antenna system is almost always a better investment per decibel — but they are a valuable tool when the antenna is already optimised and more signal is needed.

## How a Linear Amplifier Works

A linear amplifier takes a relatively low-power RF signal from the transceiver (the "drive" or "exciter") and amplifies it while preserving the characteristics of the original signal — its modulation, frequency, and waveform shape. The term "linear" means the amplifier's output is a faithful, proportionally larger copy of the input. This is essential for SSB and other modes where the signal's amplitude carries information; a non-linear amplifier would distort the signal and generate unwanted spurious emissions (splatter) on adjacent frequencies.

The basic amplifier chain is:

1. **Transceiver** outputs 50–100 watts
2. **Amplifier input** — the drive signal enters through an input matching network
3. **Active device** (tube or transistor) amplifies the signal
4. **Output network** — a tuned circuit (pi-network or pi-L network) matches the amplifier's output to the 50-ohm feedline
5. **Feedline** carries the amplified signal to the antenna

A **T/R (transmit/receive) relay** or electronic switching system routes the antenna between the amplifier output on transmit and the transceiver's receiver on receive. Most amplifiers handle this switching automatically using a keying line from the transceiver.

## Tube vs. Solid-State Amplifiers

### Tube (valve) amplifiers

Vacuum tubes have been used in RF power amplifiers since the earliest days of radio and remain popular in amateur amplifiers today. Common power tubes used in amateur amplifiers include the 3CX800A7, 3CX1200A7, 3CX1500A7 (triodes), 4CX800A, 4CX1000A, 4CX1500B (tetrodes), and the GU-74B and GU-84B (Russian-made tetrodes widely used in amateur equipment).

**Advantages of tubes:**
Tubes are inherently rugged when it comes to load mismatch — they tolerate high SWR better than transistors without immediate damage. They can produce high power from a single device, keeping the circuit relatively simple. Tube amplifiers are often easier to repair because individual tubes can be replaced.

**Disadvantages of tubes:**
Tubes require high-voltage plate supplies (typically 1,500–4,000 V DC), which presents a serious safety hazard. They generate substantial heat and require forced-air cooling. Tubes have a finite lifespan and eventually need replacement. Tube amplifiers are physically large and heavy. Warm-up time is needed before the amplifier is ready to operate.

### Solid-state amplifiers

Modern solid-state amplifiers use **LDMOS** (laterally diffused metal oxide semiconductor) transistors or, less commonly, **GaN** (gallium nitride) transistors to achieve high RF power output. LDMOS devices like the NXP MRF1K50H can produce over 1,000 watts from a single transistor package.

**Advantages of solid-state:**
No warm-up time — instant on. No high-voltage plate supply (solid-state amps typically run on 48–50 V DC). Lighter weight and more compact. No tubes to wear out or replace. Many solid-state amplifiers include automatic band switching and require no manual tuning.

**Disadvantages of solid-state:**
Less tolerant of high SWR — transistors can be damaged by severe mismatch, so solid-state amps include protective circuits that reduce power or shut down if SWR exceeds a safe level. Typically more expensive than tube amplifiers for the same power output, though the gap is narrowing. Heat management requires large heatsinks and fans.

## Classes of Amplifier Operation

Amateur linear amplifiers operate in specific bias classes that balance efficiency against linearity:

**Class AB** — the most common class for amateur HF amplifiers. The active device conducts for more than half but less than the full RF cycle. Class AB provides a good compromise between linearity (important for SSB) and efficiency (typically 50–65%). Nearly all amateur voice/SSB amplifiers operate in Class AB.

**Class A** — the device conducts for the full RF cycle. Extremely linear but inefficient (typically 25–35%), generating a lot of heat. Rarely used in high-power amateur amplifiers.

**Class C** — the device conducts for less than half the cycle. Efficient (up to 70–80%) but non-linear, making it suitable only for FM and CW — not SSB. Some VHF/UHF FM amplifiers use Class C.

**Class D/E/F** — switching-mode classes used in some modern designs, particularly for digital modes like FT8 where the signal has a constant envelope. These achieve very high efficiency (80–95%) but are not suitable for all modes.

## Types of Amateur Amplifiers

### HF amplifiers

The most common category. HF amplifiers cover some or all of the amateur bands from 160 m (1.8 MHz) through 6 m (54 MHz). Output power ranges from 500 watts to the legal limit (typically 1,500 W PEP in the US, 400 W in some European countries, 1,000 W in Canada — always check your national regulations and licence class).

**Desktop HF amplifiers** are the standard for home stations. Examples include the Ameritron ALS-1306 (solid-state, 1,200 W), Elecraft KPA1500 (solid-state, 1,500 W, auto-band-switching), Acom 1200S (tube, 1,200 W), and the Palstar HF-AUTO-1800 (tube, 1,800 W PEP).

### VHF/UHF amplifiers

Amplifiers for 2 m (144 MHz) and 70 cm (430 MHz) are used for weak-signal work, EME (Earth-Moon-Earth), meteor scatter, and contesting. Power levels typically range from 100 W to 1,500 W. VHF/UHF amplifiers use either tubes (like the 3CX800A7 or GS-35B) or LDMOS transistors. Examples include the TE Systems line and the RF Concepts/Mirage amplifiers.

### QRP amplifiers

Small amplifiers that boost a QRP transceiver's 5–10 W output to 50–100 W. These are useful for portable operators who want more power than their QRP rig provides without carrying a full-size amplifier. The Elecraft KXPA100 (designed to pair with the KX2/KX3) and HardRock-50 (open-source kit) are examples.

## Drive Power and Gain

An amplifier's **gain** describes how much it multiplies the input signal. Gain is expressed in decibels (dB):

| Input (Drive) | Output | Gain |
|---------------|--------|------|
| 5 W | 500 W | 20 dB |
| 50 W | 500 W | 10 dB |
| 100 W | 1,000 W | 10 dB |
| 100 W | 1,500 W | ~12 dB |

Most HF amplifiers are designed for **50–100 W of drive** to produce full output. Some solid-state amplifiers accept lower drive levels (25–50 W), which is useful with transceivers that have reduced power output on certain bands.

**Do not over-drive the amplifier.** Applying more drive than the amplifier is designed for causes distortion (flat-topping on SSB), generates splatter on adjacent frequencies, and can damage the amplifier. Set your transceiver output to the level specified in the amplifier's manual.

## Important Specifications

**Power output (PEP)** — the peak envelope power on SSB. This is the headline number for most amplifiers. Continuous output (key-down CW or digital modes) is often lower because of thermal limits.

**Duty cycle** — how long the amplifier can sustain full power. SSB has a low average duty cycle (you are only transmitting during voice peaks), while CW is higher, and digital modes like FT8 and RTTY approach 100% duty cycle. Many amplifiers must be derated (operated at reduced power) for continuous-duty modes.

**Input SWR** — the amplifier should present a good match (low SWR) to the transceiver's output. Most amplifiers include input matching networks for each band.

**Harmonic suppression** — how well the amplifier suppresses harmonics and spurious emissions. Good amplifiers provide at least 40–50 dB of harmonic suppression. An external [low-pass filter](/equipment/filters) adds additional harmonic attenuation.

## Safety

Amplifiers — especially tube amplifiers — involve **lethal voltages**. A tube amplifier's plate supply typically operates at 1,500–4,000 V DC with enough stored energy in the filter capacitors to kill. Even after the amplifier is turned off, capacitors can retain a charge for minutes or longer.

**Never work inside an amplifier with power applied.** Always unplug the amplifier, wait for capacitors to discharge (many amplifiers have bleeder resistors, but verify with a high-voltage meter), and short the capacitor terminals with an insulated discharge stick before touching anything inside.

Solid-state amplifiers operate at lower voltages (48–50 V DC) and are less dangerous from a shock standpoint, but the currents involved (30–40 amps) can cause burns or fire if wiring fails.

**RF safety** is also a consideration at high power. Ensure your antenna is properly installed with adequate distance from people, and be aware of RF exposure limits set by your national regulator. See [RF Safety](/electronics/rf-safety) for more information.

## Amplifiers and Your Licence

Power limits vary by country and licence class. In the United States, the maximum power for most licence classes is 1,500 W PEP output (Novice/Technician are limited to lower power on certain bands). In the United Kingdom, a Full licence allows 400 W PEP. In Canada, the limit is 1,000 W PEP for Advanced holders. Always verify the legal power limit for your licence class and country before operating with an amplifier.

Some licence classes do not permit amplifier use at all, or only on certain bands. See [Licensing & Regulations](/licensing/overview) for details.

## Tips for Amplifier Use

**Tune up at reduced power.** When adjusting a manual-tune amplifier, start at low drive and work up. This protects the tubes and avoids transmitting a mistuned signal.

**Watch the SWR.** An amplifier does not fix a poorly matched antenna — it amplifies the mismatch problem. Use an [antenna tuner](/equipment/antenna-tuners) between the amplifier and the feedline if necessary, or better yet, tune the antenna itself.

**Mind the duty cycle with digital modes.** FT8 and similar modes transmit for 15 seconds at full power, repeatedly. This is much harder on an amplifier than SSB voice. Reduce power for high-duty-cycle modes, or use an amplifier rated for continuous duty.

**Use a sequencer if needed.** A sequencer ensures that the amplifier's T/R relay, the antenna relay, and the transceiver key in the correct order — preventing hot-switching (keying the transmitter before the relays have switched) which can damage relays and cause RF arcing.

## See Also

- [Equipment Overview](/equipment/overview)
- [HF Transceivers](/equipment/hf-transceivers)
- [Power Supplies](/equipment/power-supplies)
- [Filters](/equipment/filters)
- [Antenna Tuners](/equipment/antenna-tuners)
- [Contesting](/contesting/overview)
- [DX Operating](/operating/dx-operating)
