---
title: VHF/UHF Propagation
description: Propagation modes for VHF and UHF frequencies including line-of-sight, tropo, sporadic E, and more
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, vhf, uhf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# VHF/UHF Propagation

For many amateur radio operators, VHF and UHF are the bands of everyday local communication — handheld radios, repeaters, and simplex contacts within the line of sight. But these bands also offer some of the most exciting and unpredictable propagation in all of amateur radio. Under the right conditions, signals on 6 metres, 2 metres, 70 centimetres, and even higher bands can travel hundreds or thousands of kilometres using propagation modes that are entirely different from HF skywave.

This page covers the main propagation modes available on VHF (30–300 MHz) and UHF (300 MHz–3 GHz) and explains when and how to take advantage of them.

## Line-of-sight propagation

The default propagation mode for VHF/UHF is line-of-sight. Radio waves at these frequencies travel in essentially straight lines, like light. The maximum range is determined by the curvature of the Earth and any obstructions (hills, buildings, trees) between the two stations.

### Radio horizon

The radio horizon is slightly farther than the optical horizon because radio waves in the VHF/UHF range experience some refraction (bending) in the lower atmosphere. A common approximation for the radio horizon distance is:

**Distance (km) ≈ 4.12 × (√h₁ + √h₂)**

Where h₁ and h₂ are the antenna heights of the two stations in metres. For example, two stations with antennas at 10 metres height have a radio horizon of about 26 km between them.

This formula shows why antenna height is the single most important factor for VHF/UHF range. Doubling the height doesn't double the range, but it does increase it significantly. Stations on hilltops or tall buildings can communicate over much greater distances than those in valleys.

### Practical line-of-sight range

Under typical conditions, simplex contacts between ground-level stations on 2 metres or 70 cm range from about 10 to 80 km depending on antenna height, power, terrain, and whether directional antennas are used. [Repeaters](/operating/repeaters) on elevated sites can extend coverage to 50–150 km or more.

## Beyond line-of-sight: enhanced propagation modes

The excitement of VHF/UHF propagation comes from the modes that carry signals beyond the normal line-of-sight range. These include:

### Tropospheric propagation

[Tropospheric propagation](/propagation/tropospheric) occurs when weather conditions in the lower atmosphere bend VHF/UHF signals beyond the horizon. Temperature inversions — layers where warm air sits above cooler air — refract radio waves downward, extending range to several hundred kilometres or more. In extreme cases, tropospheric ducting can carry signals over 1,000 km on 2 metres.

Tropospheric propagation is the most common form of VHF/UHF enhancement and can occur on any band from 6 metres through the microwave region. It's most frequent along coastlines, in river valleys, and during settled high-pressure weather systems. See the [Tropospheric Propagation](/propagation/tropospheric) page for details.

### Sporadic E

[Sporadic E](/propagation/sporadic-e) (Es) occurs when dense patches of ionization form in the E layer of the [ionosphere](/propagation/ionosphere). These patches can reflect VHF signals over distances of 1,000–2,000 km per hop. Sporadic E is most common on 6 metres (50 MHz), where it can produce strong, wide-open band openings lasting minutes to hours. It occasionally affects 2 metres (144 MHz) and, rarely, even 70 cm (432 MHz).

Sporadic E is most frequent during late spring and summer (May–July in the Northern Hemisphere, November–January in the Southern Hemisphere), with a secondary peak in December–January in the north. It's unpredictable but tremendously exciting when it occurs.

### Meteor scatter

When meteors enter Earth's atmosphere, they burn up at altitudes of 80–120 km, leaving brief trails of ionized gas. These trails can reflect VHF signals for durations ranging from a fraction of a second to several seconds. By using high-speed digital modes (such as [MSK144](https://wsjt.sourceforge.io/) from the WSJT-X suite) or high-speed CW, operators can complete contacts by exchanging information during these brief reflections.

Meteor scatter works best on 6 metres and 2 metres. It's most productive during major annual meteor showers (Perseids in August, Geminids in December, Quadrantids in January, and others), but random ("sporadic") meteors provide a baseline level of activity at all times. Typical contact distances are 500–2,200 km.

### Auroral propagation

During geomagnetic storms, the aurora (northern and southern lights) creates a curtain of ionization in the E-region of the ionosphere at high latitudes. VHF signals (primarily on 6 m and 2 m) can be reflected off this ionization, enabling contacts over 500–2,000 km. However, because the ionization is turbulent, reflected signals have a distinctive rough, hissing quality on SSB and a raspy tone on CW. SSB voice is often difficult to copy through auroral flutter, so CW is the preferred mode.

Auroral propagation is most common at higher latitudes (above about 45° N or S) and occurs most often around the equinoxes during periods of elevated geomagnetic activity. Stations aim their antennas toward the aurora (generally north in the Northern Hemisphere) rather than directly at the station they want to contact.

### EME (Moonbounce)

[EME (Earth-Moon-Earth)](/satellites/eme-moonbounce) is the ultimate in VHF/UHF DX — bouncing signals off the surface of the Moon and receiving the reflected signal back on Earth. Because the Moon is visible from an entire hemisphere at a time, EME allows contacts over any distance where both stations can see the Moon simultaneously.

EME requires significant station capability: high-gain antennas (large Yagis or dish antennas), low-noise receivers, and moderate to high power on transmit. Path loss is enormous (about 250 dB round-trip on 2 metres). Digital modes like JT65 and Q65 have made EME more accessible by allowing contacts at much lower signal levels than SSB or CW.

EME is practical on all VHF and UHF bands from 6 metres through the microwave region, with 2 metres (144 MHz) and 70 cm (432 MHz) being the most popular.

### Aircraft scatter

VHF signals can be reflected by aircraft fuselages, producing brief signal enhancements over distances of 300–800 km. This is most noticeable along busy air corridors. While not reliable enough for planned contacts, aircraft scatter reflections are regularly observed on 2 metres and can occasionally complete contacts when combined with digital modes.

### Rain scatter

At UHF and microwave frequencies (particularly above 3 GHz), heavy rain can scatter signals beyond the horizon. Heavy thunderstorms and rain cells act as reflectors, and operators point their antennas toward the storm rather than directly at the distant station. Rain scatter is most useful on the 10 GHz band and above, where contacts of 200–500 km are possible through intense precipitation.

## The 6-metre band — "The Magic Band"

The 6-metre band (50–54 MHz) deserves special mention because it sits at the boundary between HF and VHF and benefits from an extraordinary range of propagation modes. Amateur operators call it "The Magic Band" because of the variety and unpredictability of its openings:

- **Sporadic E:** The most common enhanced mode on 6 m. Summer Sporadic E openings can produce strong signals over 1,000–2,000 km, and double-hop Es can reach 4,000+ km.
- **F2 propagation:** During solar maximum, the MUF can occasionally reach 50 MHz, opening 6 m for true worldwide F2 skywave propagation — a rare and exciting event.
- **Tropospheric:** Enhanced tropo can extend 6 m range to several hundred kilometres.
- **Meteor scatter:** Highly effective on 6 m due to the relatively low frequency.
- **TEP (Trans-Equatorial Propagation):** A specialized F-layer mode that carries signals across the geomagnetic equator between stations at roughly equal distances north and south of it. TEP on 6 m can cover 3,000–6,000 km.
- **Auroral and auroral-E:** Both modes work well on 6 m at higher latitudes.

The combination of these modes means that 6 m can go from completely dead to wide open with little warning, rewarding patient and attentive operators with contacts that would be impossible on any other band.

## Getting started with VHF/UHF weak-signal work

Most amateur VHF/UHF activity uses FM through repeaters, but the propagation modes described above are primarily exploited using SSB, CW, and digital modes on the weak-signal portions of the bands. If you want to explore extended-range VHF/UHF propagation:

**Equipment:** An SSB-capable VHF transceiver (many modern all-mode radios cover 6 m and 2 m) and a directional antenna (Yagi) are the basic requirements. Even a modest 3–5 element Yagi on 2 metres, mounted as high as possible, will open up a new world of contacts.

**Frequencies:** Weak-signal activity concentrates on the lower portions of each band (e.g., 50.000–50.300 MHz on 6 m, 144.000–144.300 MHz on 2 m in Region 1). SSB calling frequencies and FT8 frequencies are standardized — check your region's bandplan.

**Software:** [WSJT-X](/software/digital-mode-software) is essential for meteor scatter (MSK144), EME (JT65, Q65), and general weak-signal digital work (FT8). [PSKReporter](https://pskreporter.info) provides real-time maps showing where your signals are being decoded.

**Monitoring:** Watch for propagation alerts from sources like DXMaps.com, which shows real-time VHF/UHF propagation data, and the MMMonVHF website for European VHF activity.

## Further reading

- [Sporadic E](/propagation/sporadic-e) — Detailed guide to Sporadic E propagation
- [Tropospheric Propagation](/propagation/tropospheric) — Weather-related VHF/UHF enhancement
- [EME (Moonbounce)](/satellites/eme-moonbounce) — Earth-Moon-Earth communication
- [Propagation Tools](/propagation/propagation-tools) — Software for monitoring VHF/UHF conditions
- [VHF/UHF Antennas](/antennas/vhf-uhf-antennas) — Antennas for the bands above HF
- [Propagation Overview](/propagation/overview) — Introduction to all propagation types
