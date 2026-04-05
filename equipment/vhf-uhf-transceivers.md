---
title: VHF/UHF Transceivers
description: Mobile and base station transceivers for the 2 m, 70 cm, and other VHF/UHF amateur bands
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, vhf, uhf, transceivers
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# VHF/UHF Transceivers

VHF/UHF transceivers are the workhorses of local and regional amateur radio communication. Operating primarily on the **2-metre band (144 MHz)** and the **70-centimetre band (430/440 MHz)**, these radios are used for repeater access, simplex contacts, emergency communication, and increasingly for digital modes and satellite work. They are generally more affordable and simpler to set up than HF transceivers, making them a natural starting point for many newly licensed operators.

This page covers **mobile and base-station VHF/UHF transceivers** — compact units designed for vehicle installation or fixed-station use. For battery-powered portables, see [Handheld Radios](/equipment/handheld-radios).

## VHF and UHF Bands for Amateur Use

The most commonly used VHF/UHF amateur bands are:

| Band | Frequency Range | Common Name | Typical Use |
|------|----------------|-------------|-------------|
| 6 m | 50–54 MHz | "The Magic Band" | Sporadic-E and other propagation openings; SSB/CW weak-signal work |
| 2 m | 144–148 MHz | Two metres | FM repeaters, simplex, SSB/CW weak signal, digital, satellite |
| 1.25 m | 222–225 MHz | 222 | Repeaters, simplex (available in ITU Region 2 — the Americas) |
| 70 cm | 420–450 MHz | Seventy centimetres | FM repeaters, simplex, digital (DMR, D-STAR, Fusion), ATV, satellite |
| 33 cm | 902–928 MHz | 33 cm | Limited use, some repeaters and experimentation (Region 2) |
| 23 cm | 1240–1300 MHz | 23 cm | Repeaters, ATV, microwave experimentation |

Band allocations vary by country and region — always check your national frequency plan.

## How VHF/UHF Differs from HF

Communication on VHF and UHF is fundamentally different from HF. These higher frequencies travel primarily by **line-of-sight**, meaning the range between two stations depends on antenna height, terrain, and obstructions rather than ionospheric propagation. A mobile station with a rooftop antenna might reach 30–80 km to a hilltop repeater; two handheld radios on flat ground might manage only a few kilometres simplex.

This line-of-sight characteristic is why **repeaters** — automated stations on high ground that receive on one frequency and simultaneously retransmit on another — are so important on VHF/UHF. A network of repeaters can extend effective range across a city, a region, or even further when repeaters are linked together (see [Repeaters](/operating/repeaters)).

VHF/UHF also supports occasional long-distance propagation through phenomena like **tropospheric ducting**, **sporadic E** (mainly on 6 m and occasionally 2 m), **meteor scatter**, and **Earth-Moon-Earth** (EME) contacts. These modes typically use SSB or CW rather than FM.

## Modes of Operation

### FM (frequency modulation)

FM is the dominant mode on VHF/UHF for repeater and simplex voice communication. FM provides clear, noise-free audio when the signal is above the receiver's squelch threshold, but signals below that threshold drop out abruptly rather than fading gracefully as with SSB. Nearly all VHF/UHF mobile and base transceivers support FM.

### SSB and CW

SSB and CW are used for **weak-signal work** — contacts that push the limits of VHF/UHF propagation. Because SSB uses less bandwidth and is more efficient with power than FM, it is the mode of choice for DX, contests, and EME on 2 m and 70 cm. Not all VHF/UHF transceivers support SSB — it is typically found in all-mode radios rather than FM-only models.

### Digital voice

Several digital voice systems operate on VHF/UHF:

- **DMR** (Digital Mobile Radio) — a TDMA-based standard originally designed for commercial use, now widely adopted by amateurs. See [DMR](/digital-modes/dmr).
- **D-STAR** — developed by JARL (the Japan Amateur Radio League), providing digital voice, low-speed data, and internet linking. See [D-STAR](/digital-modes/dstar).
- **System Fusion / C4FM** — Yaesu's digital voice system, which can operate in both digital and analog FM modes. See [System Fusion](/digital-modes/system-fusion).

### Data modes

VHF/UHF supports a range of data modes including APRS (see [APRS](/digital-modes/aprs)), packet radio, and Winlink email. Some of these operate through the transceiver's built-in TNC (terminal node controller) or an external interface.

## Types of VHF/UHF Transceivers

### Single-band FM mobile

The simplest and most affordable option — a single-band FM transceiver covering 2 m or 70 cm. Output power is typically 25–65 watts. These are popular for vehicle installation where a single repeater band meets the operator's needs.

### Dual-band FM mobile

The most popular category. A dual-band mobile covers both **2 m and 70 cm** in a single unit, often with the ability to monitor both bands simultaneously. Many include cross-band repeat capability (receiving on one band and retransmitting on the other), which can extend the range of a handheld radio through the mobile's higher power and better antenna. Output power is typically 50 watts on 2 m and 35–50 watts on 70 cm.

### Tri-band and quad-band

Some transceivers add the 1.25 m (222 MHz) band or the 23 cm (1200 MHz) band to the standard 2 m / 70 cm combination. These serve operators who want access to less-crowded bands or specific repeater networks.

### All-mode VHF/UHF

All-mode transceivers support FM, SSB, CW, and digital modes on VHF and UHF. They are essential for weak-signal work, VHF contests, satellite operating, and EME. Output power on SSB/CW is typically 25–100 watts. These radios are more expensive and larger than FM-only models but open up an entirely different dimension of VHF/UHF operating. Examples include the Icom IC-9700 and older models like the Yaesu FT-736R and Kenwood TS-2000 (which also covers HF).

### Detachable-head / remote-mount

Many mobile transceivers offer a **detachable control head** connected to the main body by an extension cable. This allows the bulky radio body to be mounted in the boot (trunk) or under a seat while the compact control head is placed on the dashboard — especially useful in vehicles with limited dashboard space.

## Key Features and Specifications

### Power output

Most VHF/UHF mobile transceivers offer multiple power levels — typically high (50 W), medium (25 W), and low (5–10 W). Using lower power when full power is not needed saves battery drain in a vehicle and reduces heat.

### Receiver sensitivity

VHF/UHF receiver sensitivity is typically specified as the signal level needed for 12 dB SINAD (a measure combining sensitivity and audio distortion). A good VHF FM receiver achieves 0.15–0.2 µV for 12 dB SINAD. Unlike HF, where external noise dominates, VHF/UHF sensitivity matters because background noise is lower and signals may be weak.

### Squelch systems

Beyond standard carrier squelch, VHF/UHF transceivers support tone-based squelch systems used by repeaters:

- **CTCSS** (Continuous Tone-Coded Squelch System) — a sub-audible tone (67–254.1 Hz) transmitted along with the audio that the repeater checks before opening its squelch. Also known as PL (Private Line, a Motorola trademark) or simply "tone."
- **DCS** (Digital-Coded Squelch) — a low-speed digital code transmitted sub-audibly, serving the same purpose as CTCSS with more available codes.

### Memory channels

Most mobile transceivers store hundreds of memory channels, each holding a frequency, offset, tone, and label. Some support **memory banks** or groups to organise channels by region or purpose. The ability to programme memories — either from the front panel or via computer software — is a practical convenience.

### Dual receive and cross-band repeat

Many dual-band radios can **receive two frequencies simultaneously** (V+V, U+U, or V+U), displaying activity on both. **Cross-band repeat** lets the radio act as a simplex repeater — it receives on one band and retransmits on the other. This is useful for extending the range of a low-power handheld (for example, using an HT inside a building while the mobile radio in the car park retransmits with higher power and a better antenna).

### APRS capability

Some transceivers include a built-in **TNC and GPS** for [APRS](/digital-modes/aprs) operation — transmitting your position, receiving nearby stations on a display, and exchanging messages without external equipment.

## Popular VHF/UHF Mobile Transceivers

While specific model recommendations evolve over time, several categories of well-regarded radios include:

**Dual-band FM workhorses** — radios like the Icom IC-2730A, Yaesu FT-7900R/FT-8900R, and Kenwood TM-V71A are widely used, well-supported, and available new and used.

**Feature-rich dual-band** — the Yaesu FTM-400XDR and FTM-500DR include C4FM digital voice (System Fusion), GPS, APRS, and Bluetooth. The Kenwood TM-D710G includes a built-in TNC for APRS with a full GPS display.

**All-mode VHF/UHF** — the Icom IC-9700 is the current standard for all-mode 2 m / 70 cm / 23 cm base-station operating, with SDR architecture and a full spectrum scope.

**Budget options** — radios from manufacturers like TYT, Radioddity, and Anytone offer basic dual-band FM capability at very low cost, though build quality, receiver performance, and spurious emission compliance may vary.

## Installation Considerations

### Vehicle installation

Mounting a mobile transceiver in a vehicle requires attention to several details:

**Power wiring** — Run power cables directly to the vehicle battery (fused at both ends), not through the cigarette lighter socket. Most mobile transceivers draw 10–15 amps on transmit, which exceeds the rating of lighter sockets and their wiring.

**Antenna** — A **mag-mount** antenna provides a quick, non-permanent installation. For a permanent setup, a **NMO mount** drilled through the roof provides the best ground plane and performance. The antenna and [coaxial cable](/equipment/coaxial-cable) should be as short and high-quality as practical.

**Grounding** — Bond the radio chassis to the vehicle body to reduce noise and ensure proper RF grounding.

**Interference** — Vehicle electronics (alternator, ignition, LED lighting, USB chargers) can generate noise that the receiver picks up. Ferrite chokes on power and audio cables, proper grounding, and routing cables away from noise sources help manage interference.

### Base station use

A mobile transceiver makes an effective and affordable base station when paired with a [13.8 V power supply](/equipment/power-supplies) and an outdoor antenna. Many operators use a dual-band mobile on their desk connected to a vertical antenna on the roof or a mast — this provides far better performance than a handheld with its rubber duck antenna.

## VHF/UHF vs. Handheld — When to Choose What

A mobile/base transceiver offers significant advantages over a handheld: higher power (50 W vs. 5 W), a better antenna connection, superior receiver performance, and more comfortable controls. If you operate primarily from a fixed location or a vehicle, a mobile transceiver is the better choice.

A handheld is the right tool when you need portability — walking around a hamfest, hiking, or operating as a portable station. Many operators own both and use them for different situations.

For detailed handheld information, see [Handheld Radios](/equipment/handheld-radios).

## See Also

- [Equipment Overview](/equipment/overview)
- [HF Transceivers](/equipment/hf-transceivers)
- [Handheld Radios](/equipment/handheld-radios)
- [Repeaters](/operating/repeaters)
- [VHF/UHF Operating](/operating/vhf-uhf-operating)
- [DMR](/digital-modes/dmr)
- [D-STAR](/digital-modes/dstar)
- [System Fusion](/digital-modes/system-fusion)
- [APRS](/digital-modes/aprs)
