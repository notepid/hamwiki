---
title: Test Equipment
description: Essential test equipment for the amateur radio station — multimeters, SWR meters, antenna analysers, oscilloscopes, and more
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, test, measurement
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Test Equipment

Test equipment allows you to build, maintain, troubleshoot, and optimise your station. You do not need a fully equipped laboratory to enjoy amateur radio, but even a few basic instruments save enormous time when something is not working or when you want to squeeze the best performance out of your antenna system. As your station grows, so will your collection of test gear.

## The Essentials: Where to Start

If you are building your first station, three instruments cover the vast majority of day-to-day measurement needs: a digital multimeter, an SWR/power meter, and an antenna analyser. Everything else on this page is useful but can be added over time.

## Digital Multimeter (DMM)

A digital multimeter measures voltage, current, and resistance — the three fundamental electrical quantities. In the shack, you will use a DMM to check power supply voltage under load, verify fuse continuity, measure DC current draw, test cables for shorts or opens, and check battery condition.

Any reputable DMM in the 20–50 USD range from manufacturers like Fluke, Klein, or even budget brands like AstroAI is more than adequate for station work. Key features to look for include auto-ranging, a DC current range of at least 10 A (for checking transceiver draw), a continuity buzzer, and safety-rated probes (CAT III or better if you work near mains wiring).

For RF work, keep in mind that a standard DMM cannot accurately measure radio-frequency voltages or currents — its frequency response is far too low. RF measurements require dedicated instruments.

## SWR and Power Meters

An **SWR meter** (standing wave ratio meter) measures the ratio of forward to reflected power in a feedline, giving you a direct indication of how well your antenna is matched to the transmission line. An SWR of 1:1 means a perfect match (all power goes to the antenna); 3:1 means a significant mismatch that will reduce radiated power and stress your transmitter's output stage.

Most SWR meters also display **forward power** and **reflected power** directly, making them power meters as well.

### In-line (cross-needle) meters

Traditional cross-needle SWR meters use two meter movements — one for forward power, one for reflected — crossed on the same dial so you can read SWR at a glance. The Daiwa CN-801 series and Diamond SX-series are popular examples. These are inserted permanently in the feedline between the transceiver and the antenna (or antenna tuner) and give continuous monitoring.

### Digital SWR/power meters

Digital meters provide a numeric readout and often include peak-hold, average power measurement, and data logging. Some measure power at multiple points simultaneously. The LP-100A from Telepost is a well-regarded digital wattmeter for HF through 6 m. Many modern transceivers include a built-in SWR and power display, which is convenient but not a substitute for an external meter when troubleshooting feedline or antenna problems.

### Directional couplers

A directional coupler is the sensing element inside an SWR/power meter. Standalone couplers (like the Bird 43 Thruline) use plug-in elements rated for specific frequency ranges and power levels. The Bird 43 has been an industry standard for decades and is widely available used. Its slug-based system covers HF through UHF at power levels from milliwatts to kilowatts, depending on the slug.

## Antenna Analysers

An **antenna analyser** is arguably the single most useful test instrument for the station operator. It sweeps across a range of frequencies and measures the impedance (resistance and reactance) of whatever is connected to it — typically your antenna and feedline. From this data, it calculates and displays SWR, impedance magnitude and phase, resistance, and reactance across the band, letting you see at a glance whether your antenna is resonant where you want it and how it behaves across its bandwidth.

### Standalone analysers

Standalone analysers are self-contained, battery-powered instruments with their own display. Popular models include the RigExpert AA-55 ZOOM and AA-230 ZOOM, the MFJ-259C and MFJ-269D, and the Comet CAA-500 Mark II. These are convenient for field use — you can walk up to the antenna feedpoint and make measurements without running back to the shack.

### NanoVNA and low-cost vector network analysers

The **NanoVNA** is a small, inexpensive (typically 30–60 USD) vector network analyser that has revolutionised antenna measurement for amateurs. It measures both magnitude and phase of the reflected signal, providing full impedance data, Smith chart plots, and SWR curves. The NanoVNA-H4 and its derivatives cover frequencies from around 50 kHz to 1.5 GHz (depending on the version), making them useful for HF through UHF work.

The small screen on the NanoVNA can be limiting, but PC and smartphone software (NanoVNA Saver, NanoVNA App) connects via USB or Bluetooth and provides much more detailed plots and analysis.

For more advanced work, the **NanoVNA-F V2** and **LiteVNA** offer wider frequency ranges and improved dynamic range.

### What to measure with an antenna analyser

Typical measurements include finding the resonant frequency of an antenna (the frequency where reactance crosses zero), checking SWR across a band to see where the antenna performs best, measuring feedline loss by comparing impedance at both ends, verifying that a balun or transformer is working correctly, and checking antenna components for faults (open or shorted elements, water-damaged connections).

## Dummy Loads

A **dummy load** is a non-radiating resistive load that substitutes for an antenna during testing and tune-up. It absorbs RF power and converts it to heat, presenting a near-perfect 50-ohm impedance to the transmitter. This allows you to test transmitter output, adjust power levels, and check modulation without radiating a signal over the air.

Dummy loads are rated by power and duty cycle. A small QRP dummy load might handle 5–15 watts continuously. Oil-cooled dummy loads (like the Heathkit Cantenna or modern equivalents) handle 1,000–1,500 watts for short periods. MFJ, Palstar, and Bird all make dummy loads in various power ratings.

**Always use a dummy load when testing your transmitter** — transmitting into an antenna during prolonged tune-up wastes airtime, causes QRM (interference to other stations), and in some cases violates regulations regarding unidentified transmissions.

## Oscilloscopes

An **oscilloscope** displays the waveform of an electrical signal over time. In amateur radio, an oscilloscope is useful for checking modulation quality on SSB and AM (looking for flat-topping, distortion, or over-modulation), examining CW keying waveform shape (rise and fall times), troubleshooting audio stages and digital interfaces, measuring signal levels and timing, and examining digital mode waveforms.

For amateur use, a basic digital storage oscilloscope (DSO) with at least 50 MHz bandwidth and two channels covers most needs. Budget instruments like the Rigol DS1054Z (which can be unlocked to 100 MHz) and the Siglent SDS1104X-E offer excellent value. Vintage analog oscilloscopes from Tektronix and HP (often available at hamfests for very low prices) are also perfectly serviceable for audio and low-frequency RF work.

An oscilloscope with FFT (fast Fourier transform) capability can also serve as a basic spectrum display, showing frequency-domain content of a signal.

## Spectrum Analysers

A **spectrum analyser** displays signal amplitude across a range of frequencies — the frequency-domain complement of an oscilloscope's time-domain display. In the amateur station, a spectrum analyser is useful for checking transmitter spectral purity (harmonic levels, spurious emissions), examining the RF environment for interference sources, measuring filter performance, and verifying that amplifier output is clean.

Dedicated spectrum analysers (like those from Rigol, Siglent, or older HP/Agilent models) can be expensive, but several affordable options exist for amateurs. The **TinySA** (and its Ultra variant) is a pocket-sized spectrum analyser covering roughly 100 kHz to 5.3 GHz that costs under 100 USD. Like the NanoVNA, it has brought spectrum analysis within reach of every amateur. SDR receivers with appropriate software (like SDR# or GQRX) can also serve as a wideband spectrum display.

## Signal Generators

A **signal generator** produces a known RF signal at a specified frequency and amplitude. Uses include testing receiver sensitivity, aligning filters and tuned circuits, calibrating other test equipment, and testing antenna systems. A basic RF signal generator covering HF through UHF with adjustable output level is a useful bench tool, though not essential for casual station operation.

The NanoVNA can serve as a basic signal generator in a pinch, as can many SDR transmitters. Dedicated signal generators from the surplus market (HP 8640B, Marconi 2022, etc.) are powerful instruments often available at hamfests for reasonable prices.

## Frequency Counters

A **frequency counter** measures the frequency of a signal with high precision. Modern transceivers have synthesised oscillators with crystal-referenced accuracy, reducing the need for an external counter in day-to-day operation. However, a frequency counter is useful for calibrating older equipment, verifying crystal frequencies, measuring repeater offsets, and checking oscillator drift.

GPS-disciplined frequency references (like the Leo Bodnar GPS reference) provide extremely accurate 10 MHz standards for calibrating other instruments.

## Time Domain Reflectometers (TDR)

A **time domain reflectometer** sends a pulse down a cable and measures the reflected signal to locate faults — opens, shorts, kinks, water ingress, and connector problems. TDR functions are built into some antenna analysers and can also be performed with a NanoVNA using appropriate software. A TDR is invaluable when you suspect a fault somewhere in a long feedline run or a buried cable.

## Building Your Test Bench

You do not need to buy everything at once. A sensible progression for building up a test bench might follow this order:

**Start with (essential):** digital multimeter, SWR/power meter, dummy load.

**Add next (highly recommended):** antenna analyser or NanoVNA.

**Expand as needed:** oscilloscope, spectrum analyser or TinySA, signal generator.

**Advanced or specialized:** frequency counter, GPS reference, TDR, network analyser.

Hamfests and estate sales are excellent sources for quality used test equipment at a fraction of retail price. Older instruments from HP, Tektronix, and Bird are often built to military standards and will outlast their owners with minimal maintenance. See [Buying Used Equipment](/equipment/used-equipment) for tips on evaluating used gear.

## See Also

- [Equipment Overview](/equipment/overview)
- [Coaxial Cable](/equipment/coaxial-cable)
- [RF Connectors](/equipment/connectors)
- [Filters](/equipment/filters)
- [Antenna Tuners](/equipment/antenna-tuners)
- [Equipment Buying Guide](/equipment/buying-guide)
- [Buying Used Equipment](/equipment/used-equipment)
