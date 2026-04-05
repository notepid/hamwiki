---
title: EME / Moonbounce
description: Earth-Moon-Earth communication — bouncing radio signals off the Moon for long-distance contacts
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, EME, moonbounce, VHF, UHF, microwave, JT65, Q65
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# EME / Moonbounce

Earth-Moon-Earth (EME) communication — commonly called moonbounce — is one of the most technically challenging and rewarding activities in amateur radio. The concept is straightforward: transmit a signal toward the Moon, let it reflect off the lunar surface, and receive the faint echo approximately 2.5 seconds later. In practice, the extreme path loss (over 250 dB on 144 MHz) and the weak, fading nature of the reflected signal make EME a demanding pursuit that pushes station capabilities to their limits.

Despite these challenges, EME contacts are made regularly by amateur operators around the world, on frequencies from 50 MHz up through the microwave bands. The development of digital modes like JT65 and Q65 has dramatically lowered the entry barrier, allowing stations with modest antennas to complete EME contacts that would have been impossible using CW or SSB.

## How EME works

### The Moon as a reflector

The Moon is roughly 384,400 km (238,855 miles) from Earth on average, though this distance varies due to the Moon's elliptical orbit. A radio signal travelling at the speed of light takes about 1.28 seconds to reach the Moon, resulting in a round-trip delay of approximately 2.5 seconds. This delay is immediately noticeable in operation — you hear your own echo (or another station's signal) returning noticeably after transmission.

The Moon is not a smooth reflector. Its surface is rough and irregular, which means it scatters the incoming signal in many directions rather than reflecting it cleanly like a mirror. Only a small fraction of the transmitted energy is reflected back toward Earth. The Moon's radar cross-section is roughly equivalent to a flat disc about 500 km in diameter — much smaller than the Moon's actual diameter of 3,474 km.

### Path loss

The total path loss for an EME signal is enormous. On 144 MHz, the two-way path loss is approximately 252 dB. On 432 MHz, it rises to about 261 dB, and it increases further at higher frequencies. To put this in perspective, 252 dB of loss means that for every watt transmitted, only about 6 × 10⁻²⁶ watts arrive back at the receiving antenna. Overcoming this requires a combination of high transmit power, high-gain antennas, and extremely sensitive receivers.

### Libration fading

Because the Moon has a slight wobble (libration) and its surface is irregular, the reflected signal arrives via multiple slightly different paths. These multipath reflections cause the signal to fade in and out — sometimes rapidly, sometimes slowly. This **libration fading** can cause deep signal dropouts lasting fractions of a second to several seconds, making it difficult to copy weak signals even when the overall signal level is theoretically adequate.

On the lower frequencies (144 MHz), libration fading tends to be slower and deeper. At higher frequencies (1296 MHz and above), the fading becomes more rapid but shallower. The characteristics of libration fading influence the choice of operating mode and data rate.

### Faraday rotation

On the lower VHF frequencies (notably 144 MHz), the signal polarisation rotates as it passes through the Earth's ionosphere — an effect known as Faraday rotation. This can cause the received signal to shift between horizontal and vertical polarisation, creating additional fading at the receiver. Operators on 144 MHz often use circular polarisation or switchable polarisation antennas to mitigate this effect. At 432 MHz and above, Faraday rotation is generally negligible.

## Operating modes for EME

### CW (Morse code) — the traditional mode

Before the advent of digital modes, CW was the primary mode for EME communication. CW's narrow bandwidth and the human ear's ability to detect signals close to the noise floor made it the best choice for weak-signal work. EME CW contacts follow a structured exchange procedure because signals are often right at the threshold of audibility:

A typical CW EME contact involves exchanging callsigns, signal reports (using a simplified TMO system: T = both callsigns copied, M = partial copy, O = nothing copied), and acknowledgements in a standardised sequence of transmission periods (usually 2.5 minutes each, synchronised to the minute clock).

CW EME requires large antennas and high power — typically a multi-Yagi array or a large dish antenna and a kilowatt-class amplifier on 144 MHz. As a result, CW EME has traditionally been limited to well-equipped stations.

### JT65 — the digital EME revolution

The introduction of JT65 (developed by Joe Taylor, K1JT, as part of the WSJT software suite) transformed EME operating. JT65 uses structured messages, deep error-correction coding, and synchronised transmission periods to detect signals far below the noise floor — signals that are completely inaudible to the human ear.

JT65 reduced the antenna and power requirements for EME significantly. On 144 MHz, a single long Yagi (or a pair of Yagis) and a few hundred watts can be sufficient for JT65 EME contacts, compared to the large arrays previously needed for CW. This opened EME to many more operators.

### Q65 — the next generation

Q65 is a newer mode, also from the WSJT-X software suite, designed specifically for weak and fading signals. It is particularly well suited to EME on the higher bands (432 MHz and above) where libration fading is rapid. Q65 offers better performance than JT65 under fast-fading conditions and has become increasingly popular for microwave EME.

### SSB (voice)

SSB EME is possible on 144 MHz but requires very large stations — typically an array of four or more long-boom Yagis (or a large dish) and full legal power. SSB EME is a prestigious achievement because of the raw signal strength required. On higher bands, SSB EME becomes progressively more difficult due to increasing path loss.

## Equipment for EME

EME places extreme demands on station performance. Every decibel matters — there is very little margin between a successful contact and hearing nothing at all.

### Antennas

On **144 MHz**, the most common EME antenna is an array of long-boom Yagis. A typical moderate station might use two to four Yagis with 10–15 dBd of gain each, combined with a power combiner/splitter. Larger stations use arrays of eight, sixteen, or more Yagis. Alternatively, a parabolic dish antenna of 3 m (10 ft) diameter or larger can provide equivalent or superior gain.

On **432 MHz**, long-boom Yagis are again common, either individually or in arrays. Dish antennas become more practical at this frequency because the wavelength is shorter — a 3 m dish provides roughly 24 dBi of gain at 432 MHz.

On **1296 MHz and higher**, parabolic dish antennas dominate. At microwave frequencies, a modest dish (1.5–3 m / 5–10 ft) provides very high gain. Many EME operators on 1296 MHz and above use surplus commercial or TVRO (satellite TV) dishes repurposed with appropriate feeds.

All EME antennas require precise pointing capability, typically an azimuth/elevation rotator and tracking software that can follow the Moon's position across the sky.

### Transmitters and amplifiers

High power is a significant advantage in EME. On 144 MHz, most serious EME stations run 400 watts to 1.5 kW. On 432 MHz, power levels are similar where legal. On microwave bands, lower power levels are often used (50–200 W is common) because the available antenna gain is higher.

Amplifier technology varies by band — solid-state amplifiers are increasingly common on VHF and UHF, while travelling wave tube amplifiers (TWTAs) have been used on microwave bands. Power amplifier reliability is important because EME sessions can last hours.

### Receivers and preamplifiers

Receiver sensitivity is critical. A high-quality mast-mounted preamplifier with a very low noise figure (0.3–0.5 dB or better on 144/432 MHz) is essential. On microwave bands, preamplifiers using GaAs FET or HEMT devices achieve noise figures below 0.3 dB.

The system noise temperature — which accounts for the preamplifier noise, cable losses, antenna noise, and sky background temperature — determines the weakest signals you can detect. EME operators work hard to minimize every source of noise in the receiving chain.

### Software

WSJT-X is the essential software package for digital EME. It includes JT65, Q65, and other modes optimised for weak-signal communication. WSJT-X handles the timing, encoding, decoding, and Doppler correction needed for EME contacts. The software is free and open source, available for Windows, macOS, and Linux.

Moon tracking software (integrated into many satellite tracking programs or standalone lunar tracking applications) is needed to point the antennas at the Moon.

## EME activity and operating practices

### Activity periods and conventions

EME activity is concentrated during specific windows to maximise the chance of finding other stations to work. The international EME community has established activity weekends (often called "activity time windows" or ATWs) on various bands, typically one weekend per month. Major EME contests, such as the ARRL EME Contest, also concentrate activity.

On 144 MHz, random EME operation (calling CQ and listening for replies) is possible throughout the month, with activity peaking around weekends and when the Moon is in a favourable position (high declination and close to perigee, which reduces path loss slightly).

### Scheduling and coordination

Because EME signals are so weak and finding other stations can be difficult, many EME contacts are pre-arranged (scheduled). Operators use online tools, email reflectors, and dedicated chat platforms to coordinate schedules — agreeing on a time, frequency, and mode before going on the air.

Loggers and chat tools (such as the HB9Q EME logger and various online chatrooms) allow real-time coordination during EME sessions, helping operators find each other on the band.

### Moonrise, moonset, and sky temperature

The Moon must be above the horizon at both the transmitting and receiving stations simultaneously for an EME contact to occur. This limits the available operating windows. Additionally, when the Moon passes through or near the galactic plane (the Milky Way), background sky noise increases significantly, degrading receiver sensitivity. EME operators learn to be aware of the sky temperature in the Moon's direction and preferentially operate when the lunar sky background is coolest.

## Getting started with EME

EME is not a beginner activity, but it is more accessible today than ever before, thanks to digital modes. A practical path to getting started:

1. **Start with digital modes.** JT65 on 144 MHz is the most accessible entry point. You need a single high-performance Yagi (or a pair), 200–500 watts, a low-noise preamplifier, and WSJT-X software.
2. **Build up antenna capability.** More antenna gain is always beneficial. Adding a second Yagi or upgrading to a longer boom antenna significantly improves your signal.
3. **Optimise your receive system.** A top-quality preamplifier at the antenna, with the shortest possible cable run, maximises your ability to hear weak signals.
4. **Try during high-activity periods.** Join EME contests and activity weekends to find the most stations on the band.
5. **Connect with the EME community.** The EME community is welcoming and supportive. Online reflectors, email lists, and regional EME groups share schedules, technical advice, and encouragement.

## See also

- [Satellite Station Equipment](/satellites/satellite-equipment) — Related equipment topics including rotators and preamplifiers
- [Propagation Overview](/propagation/overview) — How radio signals travel
- [Amateur Radio Satellites](/satellites/amateur-satellites) — Other space-based communication
- [Satellites & Space Overview](/satellites/overview) — Category overview
