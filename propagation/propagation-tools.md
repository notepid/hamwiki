---
title: Propagation Tools & Resources
description: Software, websites, and resources for predicting and monitoring radio propagation
published: true
date: 2026-04-05T09:30:00.000Z
tags: propagation, tools, software, resources
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Propagation Tools & Resources

A wide range of software tools, websites, and data sources exist to help amateur radio operators predict, monitor, and understand radio propagation. From real-time signal maps to long-range HF prediction models, these tools transform propagation from guesswork into informed decision-making. This page surveys the most useful tools available, organized by category.

## Real-time signal monitoring

These tools show you what's happening on the bands right now, based on actual reception reports from stations around the world.

### PSKReporter (pskreporter.info)

PSKReporter is one of the most valuable propagation tools available. It collects reception reports from stations running digital modes (FT8, FT4, WSPR, and others) and plots them on a world map in real time. You can filter by band, mode, and time range to see exactly which paths are open and how strong the signals are.

PSKReporter is especially useful because it provides a live, crowd-sourced propagation map with thousands of data points. If you want to know whether 20 metres is open to Japan right now, PSKReporter will show you — not based on predictions, but on actual decoded signals.

### WSPR (Weak Signal Propagation Reporter)

WSPR (pronounced "whisper") is a digital mode specifically designed for propagation monitoring. WSPR stations transmit low-power beacon signals that are decoded by receiving stations worldwide and uploaded to the WSPRnet database (wsprnet.org). Because WSPR operates at very low power (typically 1–5 watts), it reveals propagation paths that might not be apparent from normal on-air activity.

WSPRnet provides maps and data tables showing which paths are open on each band, with transmit power, received signal-to-noise ratio, and distance for each report. It's an excellent tool for understanding band conditions over time.

### DX Cluster

DX clusters are networks where operators post real-time "spots" — reports of stations they're hearing or working. While not a propagation prediction tool, the DX cluster gives you immediate intelligence about which bands are open and to where. Popular DX cluster access methods include:

- **Web-based clusters:** DXHeat.com, DXWatch.com, and DXSummit.fi provide browser-based access to cluster data with filtering and mapping.
- **Logging software integration:** Most modern [logging programs](/software/logging-software) can connect to DX clusters and display spots in real time, often colour-coded by band or overlaid on maps.
- **Telnet access:** Direct connection to cluster nodes via telnet for operators who prefer a text-based interface.

### DXMaps (dxmaps.com)

DXMaps is particularly popular with VHF/UHF operators. It displays real-time reception reports on a map, making it easy to see active [Sporadic E](/propagation/sporadic-e), [tropospheric](/propagation/tropospheric), and other VHF/UHF propagation events. It includes alerting features to notify you when specific propagation modes are detected.

## HF propagation prediction

These tools model the ionosphere and predict which HF bands will be open on specific paths at specific times.

### VOACAP (Voice of America Coverage Analysis Program)

VOACAP is the gold standard for HF propagation prediction. Originally developed by the US government for planning Voice of America shortwave broadcasts, it has been adapted for amateur radio use. VOACAP models the ionosphere based on solar activity data, time of day, season, and path geometry, and predicts the probability of communication on each amateur band.

VOACAP is available in several forms:

- **VOACAP Online (voacap.com):** A web-based interface that lets you run predictions without installing software. Enter your location, the target location, solar activity level, and power/antenna details, and it produces charts showing predicted signal strength and reliability by band and time of day.
- **HamCap:** A popular Windows-based VOACAP front end with a graphical interface and map display.
- **DX Toolbox:** A macOS and iOS application that includes VOACAP predictions, greyline maps, and other propagation tools.

### ITURHFPROP

The ITU's recommended HF propagation prediction method, similar to VOACAP but using a different ionospheric model. Some operators run both VOACAP and ITURHFPROP and compare results. Available through various software implementations.

### PropView and ACE-HF

PropView is a real-time propagation prediction tool that uses VOACAP or ICEPAC engines to show which bands are open from your location at the current moment. ACE-HF is a comprehensive HF prediction package used by both amateur and professional communicators.

## Solar and geomagnetic data

Tracking the solar indices described in [Band Conditions](/propagation/band-conditions) is essential for understanding and predicting propagation.

### NOAA Space Weather Prediction Center (swpc.noaa.gov)

The authoritative source for solar and geomagnetic data. Provides real-time solar flux, K-index, A-index, solar wind data, solar images, and multi-day forecasts. The SWPC also issues alerts for solar flares, geomagnetic storms, and radiation events that affect radio propagation.

### N0NBH Solar-Terrestrial Data Widget

The solar data widget created by Paul Herrman (N0NBH) is perhaps the most widely recognized propagation tool in amateur radio. Found at HamQSL.com/solar.html, this compact graphic displays the current SFI, sunspot number, A-index, K-index, and a band-by-band assessment of current conditions. Thousands of amateur radio websites embed this widget.

### Spaceweather.com

Provides accessible, plain-language summaries of current solar activity with images, charts, and explanations. A good resource for operators who want to understand what's happening on the Sun without diving deep into technical data.

### SolarHam (solarham.com)

A comprehensive solar monitoring website with real-time solar images, flare alerts, CME tracking, geomagnetic activity data, and educational resources. Popular with amateur radio operators who want detailed solar weather information.

### WWV/WWVH broadcasts

The US time-and-frequency stations broadcast solar and geomagnetic data at 18 minutes (WWV) and 45 minutes (WWVH) past each hour on 2.5, 5, 10, 15, and 20 MHz. This is the classic "on the radio" way to check propagation indices — no internet required.

## VHF/UHF propagation tools

### Hepburn Tropospheric Ducting Forecast

William Hepburn's tropospheric ducting forecast maps are the most widely used tropo prediction tool. Available online, these maps show forecasted ducting conditions for North America, Europe, and the Pacific for several days ahead. When the maps show enhanced tropo potential in your area, it's time to turn on the VHF/UHF station.

### F5LEN Tropo Forecast

A popular tropospheric propagation forecast specifically for European VHF operators. Shows predicted ducting conditions across Europe with daily updates.

### MMMonVHF

A European VHF/UHF/SHF activity network that provides real-time propagation reports, contest activity, and alerting for Sporadic E, tropo, and other VHF propagation events. Particularly useful for European VHF operators.

### APRS as a propagation indicator

[APRS](/digital-modes/aprs) stations on 144.390 MHz (North America) or 144.800 MHz (Europe) can serve as unintentional propagation beacons. If your APRS receiver starts picking up stations that are normally out of range, it's a sign that VHF propagation is enhanced. Some APRS monitoring websites (like aprs.fi) can help you spot anomalous reception distances.

## Beacon networks

Propagation beacons are low-power transmitters that run continuously on specific frequencies, allowing operators to check band conditions by listening for them.

### NCDXF/IARU Beacon Network

The Northern California DX Foundation (NCDXF) and the International Amateur Radio Union (IARU) operate a network of 18 beacons around the world, each transmitting sequentially on 14.100, 18.110, 21.150, 24.930, and 28.200 MHz. Each beacon transmits for 10 seconds at each of four power levels (100 W, 10 W, 1 W, 0.1 W), then the next beacon in the sequence takes over. A complete cycle takes 3 minutes.

By listening to these frequencies and noting which beacons you can hear, and at which power levels, you get an immediate real-time assessment of band conditions on specific paths.

### WSPR beacons

Many operators run dedicated WSPR beacon stations that transmit continuously on one or more bands. These contribute to the WSPRnet database and provide a persistent source of propagation data.

### VHF/UHF beacons

Many countries maintain VHF and UHF beacon transmitters that can be used to check for enhanced propagation. These typically transmit CW identification and a carrier on standard beacon frequencies. Beacon lists are maintained by national amateur radio societies and websites like beaconspot.uk.

## Greyline and map tools

### DX Atlas

A popular desktop mapping program for amateur radio that displays the [greyline](/propagation/greyline), azimuthal projections centred on your location, beam headings, and distance calculations. Useful for planning greyline DX operations and understanding path geometry.

### Google Earth with ham radio overlays

Several amateur radio operators have created Google Earth overlays showing greyline, propagation paths, and great-circle routes. These provide a visually intuitive way to understand radio geography.

### Logging software maps

Many modern logging programs ([Log4OM](/software/logging-software), N1MM+, DXKeeper, and others) include built-in maps showing greyline, beam headings, and sometimes propagation predictions. Having this integrated with your logging workflow means you can check conditions without switching applications.

## Mobile apps

Several mobile apps provide propagation data on the go:

- **HF Propagation** (iOS/Android): Displays current solar indices, band conditions, and basic propagation forecasts.
- **DX Toolbox** (iOS/macOS): Comprehensive tool with VOACAP predictions, greyline maps, DX cluster access, and more.
- **Solar Activity Monitor** (various platforms): Real-time solar data and alerts.
- **VHF Propagation** (Android): Focused on VHF/UHF propagation monitoring and alerts.

## Getting the most from propagation tools

Propagation tools are most useful when combined. A practical daily workflow might be:

1. Check the solar indices (SFI, K-index, A-index) on N0NBH's widget or NOAA SWPC.
2. Look at PSKReporter or WSPRnet to see which bands are actually open right now.
3. Check the DX cluster for recent activity.
4. If interested in VHF/UHF, check the Hepburn tropo forecast and DXMaps for current activity.
5. For specific DX targets, run a VOACAP prediction to find the best band and time.

No single tool tells the whole story, but together they give you a comprehensive picture of current and expected conditions.

## Further reading

- [Band Conditions](/propagation/band-conditions) — Understanding the indices these tools report
- [The Solar Cycle](/propagation/solar-cycle) — The long-term driver of propagation conditions
- [Software & Tools Overview](/software/overview) — Broader guide to amateur radio software
- [Online Tools](/software/online-tools) — Web-based tools for amateur radio
- [Propagation Overview](/propagation/overview) — Introduction to all propagation types
