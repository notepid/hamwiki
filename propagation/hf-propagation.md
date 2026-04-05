---
title: HF Propagation
description: How HF signals propagate via the ionosphere for long-distance communication
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, hf, ionosphere
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# HF Propagation

The High Frequency (HF) bands — from 1.8 MHz to 30 MHz — are where amateur radio becomes truly global. Signals on these frequencies can travel thousands of kilometres by refracting off the [ionosphere](/propagation/ionosphere), a process known as skywave propagation. A modest home station running 100 watts into a wire antenna can work stations on the other side of the planet when conditions are right.

This page covers the practical side of HF propagation: how it works on each band, what determines whether a path is open, and how to use that knowledge to make contacts.

## How HF skywave propagation works

When an HF signal leaves your antenna at an angle above the horizon, it travels upward into the ionosphere. If the frequency is below the Maximum Usable Frequency (MUF) for that path and angle, the ionosphere bends the signal back toward Earth. The signal strikes the ground at some distance away, and can then bounce back up to the ionosphere for another "hop." Each hop covers roughly 2,000–4,000 km depending on the height of the reflecting layer and the takeoff angle.

The key variables are:

**Frequency:** Higher frequencies require denser ionization to be refracted. If your frequency exceeds the MUF, the signal passes through the ionosphere and is lost into space. If it's too far below the MUF, D-layer absorption may weaken it severely. The sweet spot is just below the MUF — this is why experienced operators "chase the MUF" and move between bands throughout the day.

**Takeoff angle:** Lower takeoff angles produce longer skip distances per hop and generally stronger signals at long range. This is why antenna height and type matter so much for DX — a beam antenna on a tall tower produces a lower takeoff angle than a low dipole. However, for shorter distances and [NVIS](/propagation/nvis), higher takeoff angles are actually preferred.

**Ionospheric conditions:** The electron density of the F2 layer (the primary reflecting layer for HF) varies with the time of day, season, [solar cycle](/propagation/solar-cycle), and geomagnetic activity. All of these are tracked through [band condition indices](/propagation/band-conditions).

**Path geometry:** The distance and direction between you and the other station determines which part of the ionosphere the signal must traverse. Paths over the polar regions are more susceptible to geomagnetic disturbances. Paths along the [greyline](/propagation/greyline) can produce enhanced propagation.

## Band-by-band guide

Each amateur HF band has its own character. Understanding these personalities helps you choose the right band for the contact you want to make.

### 160 metres (1.8 MHz) — "Top Band"

The lowest amateur HF band behaves more like a medium-wave broadcast frequency than a typical HF band. During the day, the D layer absorbs 160-metre signals almost completely, limiting range to ground wave (typically under 100 km). At night, when the D layer disappears, skywave propagation becomes possible, and skilled operators with good antennas can work DX across oceans.

160 metres is known as "Top Band" among enthusiasts and is considered one of the most challenging bands for DX. High atmospheric noise (especially from thunderstorms), narrow bandwidth allocations in many countries, and the need for physically large antennas make it a specialist pursuit — but the rewards are immense for those who enjoy the challenge.

**Best time:** Night, especially during winter when noise is lower and nights are longer. The hours around local midnight through pre-dawn are prime time.

### 80 metres (3.5 MHz)

Similar to 160 m but less extreme. During the day, 80 metres provides reliable regional coverage out to a few hundred kilometres via ground wave and short-skip skywave. At night, the band opens for DX, with intercontinental contacts possible.

80 metres is one of the most popular bands for local and regional nets, ragchewing (casual conversation), and [emergency communications](/emergency-communications/overview). The large antenna sizes (a full dipole is about 40 m / 130 ft long) can be accommodated with inverted-V or other shortened configurations.

**Best time:** Regional: any time. DX: nighttime, peaking in late evening through pre-dawn. Best DX season is winter.

### 60 metres (5 MHz)

A relatively new amateur allocation in many countries, 60 metres is channelized in some jurisdictions (such as the US, where operators use specific channel frequencies) and a continuous band in others (such as the UK and some European countries). It's a useful band for medium-range communication, bridging the gap between 80 m and 40 m. Propagation characteristics are intermediate between the two.

**Best time:** Variable; useful day and night with moderate D-layer absorption during the day.

### 40 metres (7 MHz)

Often called the workhorse of HF, 40 metres provides solid performance around the clock. During the day, it supports communication out to roughly 500–1,500 km with moderate D-layer absorption. At night, the band opens dramatically — DX is readily available, and 40 m is many operators' go-to band for nighttime contacts on all continents.

40 metres is heavily used for nets, digital modes, CW (Morse code), and general HF activity. Antenna sizes are manageable (a dipole is about 20 m / 66 ft long), and the band is allocated worldwide with a shared amateur/broadcast segment.

**Best time:** Regional: daytime. DX: evening through morning. The transition period around sunset can produce excellent openings. Reliable year-round.

### 30 metres (10 MHz)

A narrow band (50 kHz wide in most countries) restricted to CW and digital modes — no voice is permitted. 30 metres is an excellent propagation band that often stays open when both 40 m and 20 m are marginal. It offers a good balance of low noise and reliable ionospheric propagation, making it popular with [FT8](/digital-modes/ft8) and CW operators.

**Best time:** Often open day and night. Transitions smoothly as 20 m closes and 40 m opens, making it a reliable bridge band.

### 20 metres (14 MHz)

The most popular DX band in amateur radio. 20 metres supports long-distance propagation during daylight hours under most solar conditions, even during solar minimum. At solar maximum, it can remain open around the clock. It's typically the first band new HF operators use for intercontinental contacts.

The band supports SSB voice, CW, and digital modes across a generous 350 kHz allocation. It's well-suited to modest station setups — a simple dipole or vertical at a reasonable height will produce contacts worldwide.

**Best time:** Daytime, from shortly after sunrise to a few hours after sunset. Opens to the east first in the morning, shifts to the south around midday, and favours westward paths in the late afternoon and evening. During high solar activity, may stay open overnight.

### 17 metres (18 MHz)

One of the WARC bands (named after the World Administrative Radio Conference that allocated them), 17 metres offers DX characteristics similar to 20 m but with the advantage of being less crowded, since contests are not held on WARC bands. It requires slightly higher solar activity to open reliably than 20 m.

**Best time:** Similar to 20 m but with shorter openings. Best during moderate to high solar activity.

### 15 metres (21 MHz)

An excellent DX band during moderate to high solar activity. When open, 15 metres produces strong signals over long distances with relatively low noise. It's a favourite during the rising phase and peak of the [solar cycle](/propagation/solar-cycle). During solar minimum, openings are less frequent but can still occur, especially around the equinoxes and via [Sporadic E](/propagation/sporadic-e).

**Best time:** Midday through afternoon during moderate-to-high solar activity. Equinox months often produce the best openings.

### 12 metres (24 MHz)

Another WARC band, 12 metres behaves similarly to 10 m but opens slightly more often due to the lower frequency. It requires good solar conditions for reliable F2 propagation but can produce excellent DX with low noise when open. No contesting is permitted, so it's generally uncrowded.

**Best time:** Daytime during moderate-to-high solar activity. Sporadic E can open the band during summer.

### 10 metres (28 MHz)

The highest HF amateur band, 10 metres is the most sensitive to the solar cycle. During solar maximum, it opens for worldwide propagation — even low-power stations with simple antennas can work incredible DX. During solar minimum, F2 propagation on 10 m is rare, though Sporadic E provides exciting short-duration openings during late spring and summer.

The 10-metre band is very wide (1.7 MHz in most countries), supporting SSB, CW, FM, digital modes, and even FM repeaters. When the band is open, it has a VHF-like quality — low noise, strong signals, and wide-open spaces.

**Best time:** Daytime during solar maximum. Sporadic E during summer months. Equinox periods can be especially productive.

## Multi-hop and long-path propagation

For distances greater than about 4,000 km, signals typically require multiple ionospheric hops. Each hop incurs some signal loss, so multi-hop paths produce weaker signals than single-hop paths — but they extend your reach around the globe.

**Long path** refers to signals that travel "the long way around" the Earth. For example, from North America to India, the short path crosses the Atlantic and Europe, while the long path crosses the Pacific. Sometimes the long path produces stronger signals because it passes through more favourably ionized regions or avoids areas of absorption. Experienced DXers listen for long-path openings as a way to work difficult stations.

## Skip zone and near-skip

The skip zone (or dead zone) is the area between the farthest reach of your ground wave signal and the closest point where the skywave returns. No communication is possible in this zone on a given frequency. The skip zone is shortest on lower frequencies and longest on higher frequencies.

**Near-skip** contacts occur when signals return from the ionosphere at the shortest possible distance — typically 300–800 km on the higher HF bands. These contacts can be extremely strong because the signal has made only one short hop with minimal spreading loss. Near-skip is common on 10 and 15 metres during Sporadic E events.

## Practical tips for HF propagation

**Follow the Sun.** The ionosphere is strongest where the Sun is overhead. Think about where it's daytime along the path to your target station. Paths that are entirely in darkness work best on the lower bands; paths with daylight at both ends work best on the higher bands.

**Work the transitions.** Sunrise and sunset are among the most dynamic propagation periods. Band openings and closings happen during these transitions, and [greyline propagation](/propagation/greyline) can produce brief but remarkable signal enhancements.

**Monitor before transmitting.** Spend a few minutes listening to a band before calling CQ. You'll quickly learn whether the band is open, in which direction, and how strong the signals are. Check [PSKReporter](https://pskreporter.info) or the DX cluster for real-time intelligence.

**Use the right mode for the conditions.** When bands are marginal, digital modes like [FT8](/digital-modes/ft8) can decode signals 20 dB or more below the noise floor — far below what SSB or even CW can manage. Switching modes effectively gives you access to propagation paths that would otherwise be unusable.

**Be patient and persistent.** HF propagation is variable by nature. Bands that are dead one hour may be wide open the next. Conditions that favour one path may shift to favour another. The operators who make the most contacts are the ones who are on the air when the bands open.

## Further reading

- [Propagation Overview](/propagation/overview) — Introduction to all propagation types
- [The Ionosphere](/propagation/ionosphere) — How the ionospheric layers affect HF signals
- [Band Conditions](/propagation/band-conditions) — Reading solar indices and forecasts
- [The Solar Cycle](/propagation/solar-cycle) — Long-term propagation trends
- [NVIS](/propagation/nvis) — Regional HF communication using near-vertical skywave
- [Greyline Propagation](/propagation/greyline) — Exploiting the dawn/dusk boundary
- [Propagation Tools](/propagation/propagation-tools) — Software for predicting HF conditions
