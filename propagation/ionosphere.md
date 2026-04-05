---
title: The Ionosphere
description: Understanding the ionospheric layers and their effect on radio propagation
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, ionosphere, theory
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# The Ionosphere

The ionosphere is the region of Earth's upper atmosphere where incoming solar radiation strips electrons from gas molecules, creating layers of electrically charged (ionized) particles. For amateur radio operators, the ionosphere is the mirror in the sky — it's what makes long-distance HF communication possible by bending radio waves back toward the ground.

Understanding the ionosphere's layers, how they form and fade, and how they respond to solar activity is fundamental to working HF effectively. It explains why some bands are open during the day and closed at night, why propagation improves when the Sun is more active, and why signals sometimes vanish into an "absorption zone" instead of reflecting back.

## How ionization works

The Sun continuously bombards Earth with ultraviolet (UV) radiation and X-rays. When this energy strikes gas molecules in the upper atmosphere (primarily oxygen and nitrogen), it knocks electrons free, creating a mixture of free electrons and positively charged ions — a plasma. This process is called photoionization.

The density of ionization at a given altitude depends on two competing factors: the intensity of incoming solar radiation (which is stronger higher up, where the atmosphere is thinner) and the density of gas molecules available to be ionized (which is greater lower down). The result is that ionization peaks at specific altitudes, forming distinct layers.

At night, without sunlight to sustain it, ionization gradually fades through a process called recombination — free electrons reunite with ions to form neutral atoms again. Different layers recombine at different rates, which is why the ionosphere changes dramatically between day and night.

## The ionospheric layers

The ionosphere is traditionally divided into several layers, named with letters that reflect the order in which they were discovered. From lowest to highest:

### D layer (60–90 km / 37–56 miles)

The D layer is the lowest ionospheric layer and is present only during daylight hours. It forms quickly after sunrise and disappears rapidly after sunset because the relatively dense atmosphere at this altitude promotes fast recombination.

For amateur radio, the D layer is primarily an *absorber* rather than a reflector. It absorbs energy from HF signals passing through it, particularly at lower frequencies. This is why the lower HF bands (160 m, 80 m, and 40 m) suffer heavy daytime absorption — signals on these frequencies lose much of their energy in the D layer before ever reaching the higher reflecting layers. At night, when the D layer vanishes, these bands come alive for long-distance communication.

The D layer's absorption increases with solar activity (especially during solar flares, which can cause short-wave fadeouts where all HF communication is temporarily blacked out on the sunlit side of Earth).

### E layer (90–150 km / 56–93 miles)

The E layer sits above the D layer and is also primarily a daytime phenomenon, though it persists weakly into the night. It can refract signals in the lower HF range (particularly below about 10 MHz) and plays a role in daytime propagation on the lower bands.

The E layer is most notable for amateur radio as the home of [Sporadic E](/propagation/sporadic-e) (Es) propagation. Sporadic E patches are unusually dense clumps of ionization that form unpredictably within the E layer and can reflect much higher frequencies — including 6 metres (50 MHz) and occasionally even 2 metres (144 MHz) — over distances of 1,000–2,000 km per hop. Sporadic E is most common in late spring and summer.

### F layer (150–500+ km / 93–310+ miles)

The F layer is the highest and most important layer for HF amateur radio. During the daytime, it splits into two sub-layers:

**F1 layer (150–220 km / 93–137 miles):** The lower of the two daytime F layers. It plays a secondary role in propagation and is more prominent during summer and at solar maximum. It generally has lower electron density than F2.

**F2 layer (250–500+ km / 155–310+ miles):** This is the primary reflecting layer for HF communication. It has the highest electron density of any ionospheric layer and can refract frequencies well into the HF range — up to 30 MHz or more during periods of high solar activity. Because of its great height, a single F2 hop can cover distances of 2,000–4,000 km.

At night, the F1 and F2 layers merge into a single F layer. This combined nighttime F layer persists throughout the night (unlike the D and E layers) because the low atmospheric density at this altitude means recombination is very slow. The nighttime F layer is why HF propagation continues after dark, although the maximum usable frequency generally drops.

## Key propagation concepts

### Maximum Usable Frequency (MUF)

The MUF is the highest frequency that the ionosphere will reflect for a given path at a given time. Signals above the MUF pass through the ionosphere and are lost into space. The MUF depends on the electron density (driven by solar activity and time of day) and the angle at which the signal strikes the ionosphere.

For practical operating, you generally want to operate as close to the MUF as possible without exceeding it. Higher frequencies experience less absorption in the D layer, produce stronger signals, and are less affected by atmospheric noise. A common guideline is to use the **Frequency of Optimum Traffic (FOT)**, which is roughly 85% of the MUF — high enough for good performance, but with a safety margin below the actual cutoff.

The MUF varies constantly throughout the day. It rises after sunrise as solar radiation builds up ionization, typically peaks in the early afternoon, and gradually decreases through the evening. It also varies with the [solar cycle](/propagation/solar-cycle) — during solar maximum, MUFs can exceed 30 MHz regularly, opening the 10-metre and even 6-metre bands for worldwide communication. During solar minimum, the MUF may struggle to reach 14 MHz, limiting long-distance propagation to the lower bands.

### Lowest Usable Frequency (LUF)

The LUF is the lowest frequency that can be used on a given path. Below the LUF, signals are absorbed so heavily by the D layer that they cannot reach the receiving station at usable strength. The LUF tends to be higher during the day (when the D layer is strongest) and lower at night.

### Skip distance and skip zone

When a signal is refracted by the ionosphere, it returns to Earth at some distance from the transmitter. The minimum distance at which the skywave signal returns is called the skip distance. Between the outer edge of the ground wave range and the point where the skywave first returns, there is a region called the skip zone (or dead zone) where the signal cannot be heard.

The skip distance varies with frequency — higher frequencies produce longer skip distances because they require a steeper angle to be refracted. On 10 metres, the skip distance might be 1,500 km or more, while on 40 metres it could be as short as a few hundred kilometres. Operators use [NVIS](/propagation/nvis) techniques specifically to eliminate the skip zone for regional communication.

### Critical frequency

The critical frequency (foF2 for the F2 layer) is the highest frequency that will be reflected when a signal is sent straight up (at vertical incidence). It's a direct measure of the ionization density. The MUF for an oblique path is always higher than the critical frequency — typically 3 to 4 times higher for long-distance paths, described by the "secant law" of ionospheric refraction.

## Ionospheric disturbances

Several types of solar and geomagnetic events can disrupt the ionosphere and degrade — or occasionally enhance — propagation.

### Sudden Ionospheric Disturbances (SIDs)

When a solar flare sends a burst of X-rays toward Earth, the D layer ionization increases dramatically on the sunlit side. This causes heavy absorption across the HF spectrum, sometimes blacking out all HF communication for minutes to hours. These events are called Sudden Ionospheric Disturbances or short-wave fadeouts. They affect only the daylight hemisphere and primarily impact the lower HF frequencies.

### Geomagnetic storms

When coronal mass ejections (CMEs) from the Sun reach Earth, they can trigger geomagnetic storms that disrupt the F layer, reducing its electron density and sometimes creating irregularities that scatter signals. During severe storms, HF propagation can be severely degraded for hours or days, particularly on paths crossing high latitudes (near the polar regions).

Geomagnetic storm intensity is tracked using the K-index (0–9 scale, updated every 3 hours) and the A-index (daily summary). Values of K ≥ 4 generally indicate disturbed conditions. See [Band Conditions](/propagation/band-conditions) for more on reading these indices.

### Polar Cap Absorption (PCA)

High-energy proton events from the Sun can ionize the polar atmosphere at very low altitudes, causing heavy HF absorption on paths that cross the polar regions. These events can last for days and are tracked as part of the solar weather monitoring system.

## The ionosphere and amateur bands

As a rough guide, here's how the ionospheric layers interact with the amateur HF bands:

| Band | Primary layer | Typical behaviour |
|------|--------------|-------------------|
| 160 m (1.8 MHz) | F layer at night | Night-only DX; heavy D-layer absorption by day |
| 80 m (3.5 MHz) | F layer at night | Similar to 160 m but less extreme; regional by day, DX at night |
| 40 m (7 MHz) | E and F layers | Reliable day and night; longer range at night when D layer fades |
| 30 m (10 MHz) | F layer | Transitional band; reliable for medium to long distances |
| 20 m (14 MHz) | F2 layer | The workhorse DX band; open during daylight, often into evening |
| 17 m (18 MHz) | F2 layer | Good DX band when conditions support it |
| 15 m (21 MHz) | F2 layer | Excellent DX during moderate to high solar activity |
| 12 m (24 MHz) | F2 layer | Requires good solar conditions; quiet during solar minimum |
| 10 m (28 MHz) | F2 layer / Es | Spectacular worldwide openings at solar max; Sporadic E in summer |

## Further reading

- [Propagation Overview](/propagation/overview) — Introduction to all propagation modes
- [HF Propagation](/propagation/hf-propagation) — Practical guide to working the HF bands
- [Solar Cycle](/propagation/solar-cycle) — How solar activity drives ionospheric conditions
- [Band Conditions](/propagation/band-conditions) — Reading solar indices and forecasts
- [Sporadic E](/propagation/sporadic-e) — The exciting E-layer phenomenon
- [NVIS](/propagation/nvis) — Overcoming the skip zone for regional communication
