---
title: The Solar Cycle
description: How the Sun's activity cycle affects radio propagation and what amateur radio operators need to know
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, solar-cycle, sun, theory
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# The Solar Cycle

The Sun is the engine that drives HF radio propagation. Its output of ultraviolet radiation and X-rays creates and sustains the [ionosphere](/propagation/ionosphere), and its level of activity determines how well — or how poorly — the ionosphere reflects radio signals. The Sun's activity rises and falls in a roughly 11-year pattern known as the solar cycle, and understanding this cycle is essential for every HF amateur radio operator.

## What is the solar cycle?

The solar cycle is a periodic variation in the Sun's magnetic activity, visible as changes in the number of sunspots, the frequency of solar flares, and the intensity of UV and X-ray emissions. Each cycle has a **solar minimum** (when the Sun is relatively quiet) and a **solar maximum** (when activity peaks).

A complete cycle — from one minimum to the next — averages about 11 years, though individual cycles have ranged from about 9 to 14 years. Cycles are numbered sequentially; Solar Cycle 25 began in December 2019 and is expected to reach its maximum around 2024–2025.

The cycle is tracked primarily by counting sunspots — dark, cooler regions on the Sun's surface that mark areas of intense magnetic activity. More sunspots generally means more UV radiation, stronger ionization, and better HF propagation conditions.

## Solar cycle phases and HF propagation

### Solar minimum

During solar minimum, the Sun has few or no sunspots for extended periods. UV output is at its lowest, and the ionosphere is weakly ionized. The practical effects for amateur radio include:

- The Maximum Usable Frequency (MUF) is often low, sometimes barely reaching 14 MHz on many paths. Bands above 20 metres (14 MHz) may be closed much of the time.
- The lower HF bands (40 m, 80 m, 160 m) become the workhorses for DX communication, particularly at night.
- 20 metres (14 MHz) often remains the best band for daytime DX, as it can still support F2 propagation even with low solar activity.
- 10 metres (28 MHz) and 12 metres (24 MHz) are mostly quiet except during occasional [Sporadic E](/propagation/sporadic-e) openings.
- Atmospheric noise tends to be the dominant signal limitation on the lower bands.

Solar minimum is a challenging but rewarding time for skilled operators. Low-power (QRP) contacts on bands like 40 metres can be very satisfying, and the quieter conditions on the higher bands make any opening especially exciting.

### Rising phase

As solar activity increases, the ionosphere becomes more strongly ionized. MUFs climb, and bands that were closed during the minimum begin to open:

- 15 metres (21 MHz) starts supporting regular DX contacts.
- 17 metres (18 MHz) and 12 metres (24 MHz) become increasingly useful.
- 20 metres becomes an even more reliable worldwide band with longer daily openings.
- Propagation paths that were difficult or impossible at minimum start becoming workable.

### Solar maximum

At solar maximum, the ionosphere is at its most densely ionized. This is the golden age for HF operators:

- 10 metres (28 MHz) opens for worldwide propagation, sometimes for many hours per day. Modest stations can work DX around the globe with low power and simple antennas.
- 12 metres and 15 metres are frequently open for long-distance contacts.
- MUFs can exceed 30 MHz, occasionally even reaching 50 MHz (6 metres) via F2 propagation — a rare and exciting event.
- 20 metres may be open virtually 24 hours a day on some paths.
- All HF bands are generally more active and lively.

However, solar maximum also brings more frequent geomagnetic storms and solar flares, which can temporarily disrupt propagation (see [Ionospheric Disturbances](/propagation/ionosphere#ionospheric-disturbances)).

### Declining phase

As activity wanes from the maximum, conditions gradually return toward minimum levels. The higher bands close first, and operators shift their attention back to the middle and lower HF bands. The declining phase can last several years and often includes periods of excellent conditions interspersed with quiet spells.

## Key solar indices

Amateur radio operators track several numbers to monitor solar activity and predict propagation. These are updated daily and are available from sources like NOAA's Space Weather Prediction Center, WWV radio broadcasts, and various [propagation tools](/propagation/propagation-tools).

### Solar Flux Index (SFI)

The Solar Flux Index measures the Sun's radio emissions at 2800 MHz (10.7 cm wavelength), recorded daily at the Dominion Radio Astrophysical Observatory in Penticton, British Columbia, Canada. It's a good proxy for UV output and ionospheric ionization.

| SFI value | Conditions |
|-----------|------------|
| 65–70 | Solar minimum; low-band propagation only |
| 80–100 | Moderate conditions; 20 m reliable, 15 m opening |
| 100–150 | Good conditions; higher bands active |
| 150–200 | Very good conditions; 10 m regularly open |
| 200+ | Excellent conditions; worldwide propagation on all HF bands |

The SFI typically ranges from about 65 (deep solar minimum) to 250 or more (strong solar maximum). Day-to-day variations of 10–20 points are normal, so it's useful to look at the smoothed (averaged) value over several months for trend analysis.

### Sunspot Number (SSN)

The Sunspot Number is the original and most traditional measure of solar activity. It counts the number and size of sunspot groups visible on the Sun's disk. The SSN correlates well with propagation conditions, though the SFI is considered a more direct indicator of ionospheric effects.

A smoothed SSN of zero indicates deep minimum; values above 100 indicate strong activity, and values above 150 indicate a very active Sun.

### K-index

The K-index measures geomagnetic field disturbance on a scale of 0 to 9, updated every three hours. It reflects the effect of the solar wind and CMEs on Earth's magnetic field. For HF propagation:

| K-index | Meaning for propagation |
|---------|------------------------|
| 0–1 | Quiet; generally good HF conditions |
| 2–3 | Unsettled; minor effects, usually still workable |
| 4 | Active; noticeable degradation, especially on polar paths |
| 5+ | Storm; significant HF degradation, higher bands may close |
| 7+ | Severe storm; HF largely disrupted |

The planetary K-index (Kp) is a global average from multiple observatories. It's the most commonly cited value in amateur radio contexts.

### A-index

The A-index is a daily summary derived from the K-index, providing a linear (rather than logarithmic) measure of geomagnetic activity over a 24-hour period. An A-index below 10 generally indicates quiet conditions; values above 30 indicate storm-level disturbances. The A-index is useful for spotting multi-day trends.

## Sunspots and magnetic fields

Sunspots appear where intense magnetic field lines break through the Sun's surface. They typically appear in pairs or groups with opposite magnetic polarity, and their positions drift from higher solar latitudes toward the equator as each cycle progresses (a pattern described by the "butterfly diagram").

At the end of each 11-year cycle, the Sun's magnetic polarity flips — north becomes south and vice versa. This means the full magnetic cycle is actually about 22 years (two sunspot cycles), though for propagation purposes the 11-year sunspot cycle is what matters most.

## Historical cycles

Solar cycles have been numbered since 1755 (Cycle 1). Some notable cycles for amateur radio:

- **Cycle 19 (1954–1964):** The strongest recorded cycle, with a peak smoothed SSN of about 201. HF propagation was extraordinary, with 10 metres open for worldwide contacts for extended periods.
- **Cycle 20 (1964–1976):** A moderate cycle; decent but unremarkable HF conditions.
- **Cycle 21 (1976–1986):** Strong cycle; excellent propagation, especially on the higher HF bands.
- **Cycle 22 (1986–1996):** Another strong cycle with a quick rise to maximum.
- **Cycle 23 (1996–2008):** Moderate cycle with a prolonged, unusually deep minimum that frustrated HF operators.
- **Cycle 24 (2008–2019):** One of the weakest cycles in a century, with a peak SSN of about 116. The higher bands were often disappointing.
- **Cycle 25 (2019–present):** Has exceeded initial predictions, showing stronger-than-expected activity through its rising phase and maximum.

## Living with the solar cycle

As an amateur radio operator, you can't control the solar cycle, but you can adapt to it:

**During solar minimum:** Focus on the lower and middle HF bands (160 m through 20 m). Use efficient antennas and digital modes like [FT8](/digital-modes/ft8), which can decode signals well below the noise floor. Explore the challenge of making contacts under tough conditions.

**During solar maximum:** Take full advantage of the higher bands. Even simple antennas and low power can produce worldwide contacts on 10 metres when the band is open. It's an excellent time for new licensees to experience HF DX.

**Year-round:** Monitor [band conditions](/propagation/band-conditions) daily. Use [propagation tools](/propagation/propagation-tools) to check forecasts and real-time maps. Pay attention to the seasonal patterns — even within a given solar cycle level, propagation changes with the seasons (equinoxes tend to produce the best conditions on many paths).

## Further reading

- [The Ionosphere](/propagation/ionosphere) — How the ionospheric layers form and behave
- [Band Conditions](/propagation/band-conditions) — Reading and interpreting propagation indices
- [HF Propagation](/propagation/hf-propagation) — Practical guide to working the HF bands
- [Propagation Tools](/propagation/propagation-tools) — Software and websites for monitoring solar activity
- [Propagation Overview](/propagation/overview) — Introduction to all propagation modes
