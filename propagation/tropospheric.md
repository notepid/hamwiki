---
title: Tropospheric Propagation
description: How weather-driven tropospheric ducting and refraction extend VHF/UHF range
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, tropospheric, vhf, uhf, weather
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Tropospheric Propagation

Tropospheric propagation — often shortened to "tropo" — occurs when conditions in the lowest layer of Earth's atmosphere bend VHF, UHF, and microwave signals beyond the normal line-of-sight range. Unlike HF skywave propagation, which relies on the [ionosphere](/propagation/ionosphere), tropo is driven entirely by weather. Temperature inversions, humidity gradients, and atmospheric pressure patterns create refractive conditions that can extend VHF/UHF range from a typical 50–80 km to several hundred or even over 1,000 km.

Tropospheric propagation is the most common form of extended-range propagation on VHF and UHF. It can occur on any frequency from about 50 MHz well into the microwave range, and it actually becomes more pronounced at higher frequencies — making it particularly important for operators on 70 cm (432 MHz), 23 cm (1296 MHz), and above.

## How tropospheric propagation works

Radio waves in the VHF/UHF range normally travel in straight lines and are limited to line-of-sight distances. However, the speed of radio waves through the atmosphere depends on the air's temperature, humidity, and pressure. When these properties change sharply with altitude, radio waves can be refracted (bent) — curving them back toward the ground and extending the range.

### Normal refraction

Under standard atmospheric conditions, temperature and humidity decrease gradually with altitude. This produces a slight downward bending of radio waves, extending the radio horizon by about 15% beyond the geometric line of sight. This "standard refraction" is already accounted for in the radio horizon formula used by most planning tools.

### Enhanced refraction (super-refraction)

When temperature decreases more slowly than normal with altitude — or actually *increases* (a temperature inversion) — the refraction becomes stronger. Radio waves bend more sharply toward the ground, and signals can travel well beyond the normal radio horizon. This is called super-refraction or enhanced tropo.

Enhanced tropo is common and can extend VHF/UHF range to 200–500 km without any dramatic weather event. Many operators notice these conditions as days when their usual repeater coverage seems a bit better than normal, or when they can hear distant repeaters they don't usually pick up.

### Tropospheric ducting

The most dramatic form of tropo occurs when a strong temperature inversion creates a "duct" — a layer of the atmosphere that traps radio waves and guides them over very long distances with relatively little signal loss. Ducting can carry signals 500–2,000 km or more, sometimes with remarkably strong signal levels.

Ducting occurs when a sharp boundary (an inversion layer) exists between warm, dry air above and cooler, more humid air below. Radio waves that enter the duct at a shallow angle are repeatedly refracted back down by the inversion and reflected back up by the ground (or lower boundary), zigzagging along inside the duct like light in a fibre optic cable.

There are two main types of tropospheric ducts:

**Surface ducts:** The duct extends from the ground up to the inversion layer. These are common along coastlines where warm air moves over cool ocean water, creating a marine inversion. Surface ducts can be remarkably effective, carrying signals over water for hundreds of kilometres.

**Elevated ducts:** The duct exists between two layers of the atmosphere, not touching the ground. Signals must be launched at the right angle to enter the elevated duct, which means elevated ducts can be selective — they may enhance propagation on one path while having no effect on another.

## Weather conditions that produce tropo

### Temperature inversions

Inversions are the primary driver of enhanced tropo. They form in several ways:

**Radiation inversions:** On calm, clear nights, the ground cools by radiating heat into space. The air near the ground cools faster than the air above, creating an inversion. These are most common in autumn and winter and are typically shallow (a few hundred metres) and short-lived (breaking up after sunrise). They can produce enhanced tropo during the evening and early morning hours.

**Subsidence inversions:** When a large high-pressure system sits over an area, air gently sinks (subsides) from aloft. As it descends, it warms and dries, creating a warm layer above the cooler surface air. Subsidence inversions can be extensive (covering hundreds of kilometres), persistent (lasting days), and strong. They are the most important type for long-range tropo.

**Frontal inversions:** Where a warm air mass overrides a cooler air mass (a warm front), the boundary between them can create tropo ducting. These tend to be temporary and geographically narrow but can produce impressive signal enhancements along the front.

**Marine inversions (advection):** When warm air moves over a cool body of water (ocean, large lake), the air near the water surface cools while the air above remains warm. This creates surface ducts that are especially common along coastlines. The California coast, the Gulf of Mexico, the North Sea, the Mediterranean, and the Japanese coast are all well-known tropo hotspots.

### High-pressure systems

Settled high-pressure weather is the single best indicator of enhanced tropo potential. When a high-pressure system stagnates over a region for several days, subsidence inversions build and strengthen. Watch for:

- Slow-moving or stationary high-pressure centres on weather maps.
- Clear, calm weather with hazy conditions (the haze is often trapped beneath the inversion).
- Warm days followed by cool nights.
- Light winds at the surface.

## Which bands benefit most?

Tropospheric propagation affects all frequencies from about 50 MHz upward, but its effect increases with frequency:

| Band | Tropo effect |
|------|-------------|
| 6 m (50 MHz) | Noticeable but modest; tropo competes with other propagation modes on this band |
| 2 m (144 MHz) | Significant; common enhanced-tropo contacts of 200–500+ km |
| 70 cm (432 MHz) | Strong; ducting events are often strongest here |
| 23 cm (1296 MHz) | Very strong; excellent ducting potential |
| 13 cm and above | Increasingly strong; ducting is a primary DX mode on microwaves |

This frequency dependence means that if you hear enhanced signals on 2 metres, it's worth checking 70 cm and 23 cm — conditions there may be even better.

## When and where tropo occurs

### Geographic hotspots

Some regions are famous for tropospheric propagation:

- **US Gulf Coast and Southeast coast:** Marine inversions and subtropical high-pressure systems create frequent tropo, particularly in summer and early autumn.
- **California coast:** Marine layer inversions are nearly constant in summer, producing consistent enhanced tropo along the coast.
- **North Sea and English Channel:** Frequent tropo between the UK and Continental Europe, particularly in summer.
- **Mediterranean:** Summer high-pressure patterns create extended tropo events across the basin.
- **Japan and East Asia:** Coastal geography and seasonal weather patterns produce regular tropo events.
- **Australia:** Tropo across the Great Australian Bight and along the eastern coast.

### Seasonal patterns

- **Late summer and early autumn (August–October in the Northern Hemisphere):** Generally the best period for tropospheric ducting. High-pressure systems are common and persistent, and the temperature contrast between warm land and cool water is strong.
- **Spring:** Another productive period as the atmosphere becomes more active.
- **Winter:** Radiation inversions are common but tend to be shallow, producing shorter-range enhancement. Major ducting events are less frequent.
- **Summer:** Mixed — very good in coastal areas with marine inversions, but convective (thunderstorm) weather inland often mixes the atmosphere and breaks up inversions.

## Detecting tropospheric propagation

### Weather maps and forecasts

Learning to read weather maps is invaluable for predicting tropo. Look for:

- High-pressure centres with tight isobars and calm conditions.
- Temperature soundings (radiosonde data) showing inversions at 500–2,000 m altitude.
- Surface dew point spreads — a large difference between temperature and dew point often indicates dry air aloft (subsidence).

### Tropo prediction tools

Several online tools are specifically designed for predicting tropospheric propagation:

- **William Hepburn's Tropospheric Ducting Forecast (weather.us/wh6p):** One of the best-known tropo prediction maps, showing forecasted ducting conditions across North America, Europe, and other regions.
- **F5LEN Tropo Forecast:** Popular European VHF tropospheric forecast.
- **DXMaps.com:** Shows real-time VHF/UHF contacts overlaid on a map, making active tropo events immediately visible.

See [Propagation Tools](/propagation/propagation-tools) for a comprehensive list.

### On-air indicators

- Distant FM broadcast stations appearing on your radio (especially in the 88–108 MHz band) are a classic sign of enhanced tropo.
- APRS stations and repeaters appearing from unusual distances.
- Stronger-than-normal signals from familiar distant stations on VHF/UHF.

## Operating during tropospheric events

### Equipment

Tropo works with standard VHF/UHF equipment, but directional antennas (Yagis) make a big difference because they focus your signal toward the duct and reduce noise from other directions. Even a small 4–5 element Yagi on 2 metres, mounted outdoors and as high as possible, significantly improves your ability to work tropo DX.

### Frequencies and modes

Weak-signal portions of the VHF/UHF bands are where tropo DX contacts take place. SSB and CW are the traditional modes, with calling frequencies at:

- 144.300 MHz (2 m SSB calling, Region 1) / 144.200 MHz (Region 2)
- 432.200 MHz (70 cm SSB calling)

FT8 and other digital modes are increasingly used during marginal tropo conditions, as they can decode weaker signals than SSB.

### Tips

- Monitor the bands regularly during settled high-pressure weather, even if conditions seem normal — tropo can develop gradually.
- If you notice enhanced conditions, call CQ and spot your activity on the DX cluster so others know the band is open.
- Try multiple bands. If 2 m is enhanced, 70 cm and 23 cm may be even better.
- Point your antenna toward the area where you expect the duct to be — often along the coast or in the direction of a high-pressure centre.

## Further reading

- [VHF/UHF Propagation](/propagation/vhf-propagation) — All propagation modes on VHF and above
- [Sporadic E](/propagation/sporadic-e) — Another major VHF propagation mode
- [Propagation Tools](/propagation/propagation-tools) — Tropo forecasting and monitoring tools
- [VHF/UHF Antennas](/antennas/vhf-uhf-antennas) — Antennas for working tropo DX
- [Propagation Overview](/propagation/overview) — Introduction to all propagation types
