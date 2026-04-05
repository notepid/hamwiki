---
title: Software Defined Radio (SDR)
description: SDR receivers and transceivers for amateur radio — how they work, popular hardware, and software options
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, sdr, software-defined-radio
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Software Defined Radio (SDR)

**Software Defined Radio** (SDR) replaces the analog filters, mixers, demodulators, and other circuits found in a traditional radio with **digital signal processing** (DSP) performed in software. Instead of hardware determining what the radio can do, software defines its capabilities — hence the name. This approach offers extraordinary flexibility: the same piece of hardware can receive AM broadcast, decode amateur SSB, demodulate FM satellites, and analyse signal spectra, all by changing the software running on a connected computer.

SDR has transformed amateur radio in two ways. First, inexpensive SDR **receivers** (dongles and standalone units) have made wideband monitoring and experimentation accessible to anyone for a few tens of dollars. Second, SDR **transceivers** now compete with and often outperform traditional superhet designs in the high-end amateur radio market, bringing features like real-time wideband spectrum displays, infinitely adjustable filters, and remote network operation.

## How SDR Works

### The basic concept

In a traditional superheterodyne receiver, the incoming RF signal passes through analog bandpass filters, is mixed down to one or more intermediate frequencies (IFs), filtered again with crystal or ceramic filters, and finally demodulated to audio. Each of these stages is built from fixed hardware.

In an SDR, the incoming RF signal is digitised as early as possible in the signal chain using an **analog-to-digital converter** (ADC). Once the signal is in digital form, all subsequent processing — filtering, mixing, demodulation, noise reduction — happens mathematically in software. This digital processing can be performed on a general-purpose computer CPU, a dedicated **FPGA** (field-programmable gate array), or a **DSP chip**.

### Direct sampling vs. superheterodyne SDR

**Direct-sampling SDR** digitises the RF signal directly (or after minimal analog preprocessing like filtering and amplification). The ADC must be fast enough to sample at or above twice the highest frequency of interest (the Nyquist rate). Modern ADCs sampling at 100+ MHz can directly digitise the entire HF spectrum. The Icom IC-7300 and FlexRadio FLEX-6000 series use this approach for HF.

**Superheterodyne SDR** uses a traditional analog front end to convert the RF signal to a lower IF, which is then digitised. This approach allows the use of slower, higher-resolution ADCs and can achieve better dynamic range. Many high-end SDR transceivers use this hybrid approach.

### IQ sampling

Most SDR receivers use **IQ (in-phase / quadrature) sampling**, where the incoming signal is mixed with two versions of a local oscillator — one shifted 90° relative to the other — producing two data streams (I and Q). These two streams together preserve the full information content of the signal, including the ability to distinguish between signals above and below the tuned frequency. IQ data is what SDR software works with to perform filtering, demodulation, and display.

## SDR Receivers

SDR receivers are receive-only devices — they cannot transmit. They are used for monitoring, scanning, signal analysis, and learning. The low cost of entry-level SDR receivers has made them enormously popular.

### RTL-SDR dongles

The most accessible SDR is the **RTL-SDR** — a USB dongle originally designed as a DVB-T (digital television) receiver, repurposed for wideband radio reception. These dongles use the Realtek RTL2832U chip paired with a tuner chip (commonly the Rafael Micro R820T2) and can receive from roughly **24 MHz to 1.7 GHz** with about 2–3 MHz of instantaneous bandwidth.

RTL-SDR dongles cost $10–35 and are an excellent way to explore the radio spectrum. They can receive FM broadcast, amateur VHF/UHF, aircraft ADS-B transponders, weather satellites, pagers, ISM-band devices, and much more. Their limitations include limited dynamic range (8-bit ADC), no HF coverage without a converter, and sensitivity to strong signals. The **RTL-SDR Blog V4** is a popular improved version with better filtering, a TCXO for frequency stability, and an HF direct-sampling mode.

### Mid-range SDR receivers

For more demanding receive applications, mid-range SDRs offer wider bandwidth, better dynamic range, and HF coverage:

**SDRplay RSP series** — the RSPdx, RSP1B, and RSPduo cover 1 kHz to 2 GHz with 14-bit ADC and up to 10 MHz instantaneous bandwidth. The RSPduo has two independent tuners for diversity reception or simultaneous monitoring of two bands. Compatible with SDRuno (manufacturer's software), SDR Console, and other applications.

**Airspy** — the Airspy HF+ Discovery covers HF and VHF with excellent dynamic range for its price. The Airspy R2 and Airspy Mini cover 24 MHz to 1.8 GHz with high sample rates. Airspy products are known for strong dynamic range and work well with SDR# (SDRSharp) software.

**KiwiSDR** — a unique SDR designed to be a web-accessible receiver. A KiwiSDR connected to an antenna and the internet allows anyone in the world to tune and listen through a web browser. Hundreds of KiwiSDRs are publicly available at kiwisdr.com, forming a global network of remote receivers.

### High-performance SDR receivers

For professional-grade receive performance:

**Elad FDM-S3** — a direct-sampling HF/VHF receiver with a 16-bit ADC, covering DC to 54 MHz and 76–108 MHz, with 24 MHz instantaneous bandwidth.

**WinRadio Excalibur** series — high-performance receivers used by both amateurs and professionals, offering wide dynamic range and advanced DSP features.

**Apache Labs ANAN series** — open-source SDR transceivers (see below) whose receive path offers outstanding performance.

## SDR Transceivers

SDR transceivers can both receive and transmit, replacing a traditional amateur transceiver with a software-defined architecture.

### Standalone SDR transceivers

Several commercial amateur transceivers use SDR architecture internally while presenting a traditional radio experience:

**Icom IC-7300** — one of the best-selling HF transceivers of the 2020s, using direct-sampling SDR for its receiver. It provides a real-time spectrum scope and waterfall, sharp DSP filters, and 100 W output, all in a traditional front-panel form factor.

**Icom IC-7610 / IC-7851** — higher-end Icom SDR transceivers with dual receivers and premium performance.

**Yaesu FTDX101 series** — uses a hybrid SDR architecture with narrow roofing filters and DSP.

**Kenwood TS-890S** — similarly combines analog roofing filters with extensive DSP processing.

See [HF Transceivers](/equipment/hf-transceivers) for more on these radios.

### Computer-hosted SDR transceivers

These SDR transceivers separate the RF hardware from the user interface, with a computer (local or networked) providing the display and controls:

**FlexRadio FLEX-6000 series** — networked SDR transceivers where the radio hardware connects to a computer (or multiple computers) over Ethernet. The operator interface (SmartSDR) runs on a PC, Mac, or iPad. Multiple operators can share a single radio simultaneously. The FLEX-6700 offers two independent SCUs (slice receivers) and 100 W output.

**Apache Labs ANAN series** — open-source hardware SDR transceivers based on the **HPSDR** (High Performance Software Defined Radio) project. These use high-performance ADCs and FPGAs, with open-source software (Thetis, piHPSDR, Quisk) providing the operator interface. The ANAN-7000DLE and ANAN-8000DLE are flagship models. The open-source nature makes them popular with experimenters.

**Hermes Lite 2** — an open-source, low-cost SDR transceiver based on HPSDR protocols. It provides 5 W output on HF bands and can be built from a kit or purchased assembled for a few hundred dollars. It is an excellent entry point into SDR transceiver experimentation.

### Portable SDR transceivers

**Icom IC-705** — a portable all-mode SDR transceiver covering HF through UHF with 10 W output (5 W on UHF), a colour touch-screen spectrum display, built-in GPS, Bluetooth, and Wi-Fi. Popular for SOTA, POTA, and portable operations.

**Xiegu X6100** — a compact HF SDR transceiver with spectrum display, designed for portable use.

## SDR Software

The software is where the "defined" in SDR happens. Different programs offer different features, interfaces, and supported hardware.

### General-purpose SDR software

**SDR# (SDRSharp)** — a popular Windows application for RTL-SDR and Airspy hardware. Provides a spectrum display, waterfall, and demodulators for AM, FM, SSB, CW, and digital modes. Free for personal use.

**SDR Console** — a feature-rich Windows application supporting a wide range of SDR hardware (SDRplay, RTL-SDR, Airspy, and others). Includes satellite tracking, frequency database integration, and recording.

**GQRX** — an open-source SDR application for Linux and macOS, based on GNU Radio. Supports RTL-SDR, Airspy, HackRF, and others.

**CubicSDR** — a cross-platform (Windows, macOS, Linux) open-source SDR application with a clean interface.

### Transceiver-specific software

**SmartSDR** — the operator interface for FlexRadio transceivers, available for Windows, macOS, and iOS.

**Thetis** — open-source software for Apache Labs ANAN transceivers, based on the PowerSDR lineage.

**SDRuno** — SDRplay's dedicated application, optimised for their hardware.

**HDSDR** — a freeware Windows application popular with many SDR receivers.

### DSP and development frameworks

**GNU Radio** — an open-source toolkit for signal processing. GNU Radio provides building blocks (signal sources, filters, demodulators, sinks) that can be connected graphically or programmatically to build custom SDR applications. It is the foundation for many SDR projects and a powerful tool for learning DSP.

**Pothos** — another open-source dataflow framework for SDR and signal processing.

## Getting Started with SDR

For someone new to SDR, a practical path is:

1. **Start with an RTL-SDR dongle** and a simple antenna. Install SDR# (Windows) or GQRX (Linux/Mac) and explore the spectrum — tune around FM broadcast, find amateur repeaters on 2 m, watch aircraft ADS-B signals, receive NOAA weather satellite images.

2. **Learn the waterfall display.** The waterfall shows signals across a band as they change over time. Learning to read a waterfall — recognising CW, SSB, FM, digital modes, and interference by their visual signatures — is a skill that transfers directly to operating modern transceivers.

3. **Experiment with decoding.** Feed audio from your SDR software into digital mode decoders — for example, decode FT8 with WSJT-X, ADS-B with dump1090, or NOAA APT weather satellite images with WXtoImg or SatDump.

4. **Upgrade hardware as interests develop.** Move to an SDRplay or Airspy for better performance, or dive into transmitting with a Hermes Lite 2 or a commercial SDR transceiver.

## Advantages of SDR

**Flexibility** — the same hardware can be updated with new features, modes, and improvements through software updates rather than hardware modifications.

**Wideband spectrum display** — SDR receivers can display activity across a wide swath of spectrum simultaneously, providing situational awareness that traditional radios cannot match.

**Sharp, adjustable filters** — DSP filters can be made arbitrarily narrow or wide, with shapes optimised for different modes. No need to buy optional filter modules.

**Recording and playback** — SDR receivers can record the raw IQ data stream, allowing you to "replay" a section of spectrum later, tune to different signals within the recorded bandwidth, and try different demodulation settings after the fact.

**Remote operation** — many SDR platforms support remote operation over a network, separating the antenna and radio hardware from the operator. This enables operating from anywhere with an internet connection.

## Limitations and Considerations

**Dynamic range** — inexpensive SDR receivers (particularly RTL-SDR dongles) can be overwhelmed by strong signals, causing intermodulation and spurious responses. This is less of an issue with higher-end SDRs but remains a factor compared to the best traditional receivers.

**Computer dependency** — most SDR setups require a computer for the user interface and signal processing. This adds complexity, power consumption, and potential RF noise. Standalone SDR transceivers like the IC-7300 handle this internally.

**Latency** — the digital processing chain introduces a small delay between the real-time signal and the audio output. For most amateur use this is imperceptible, but it can matter in certain contest or full-break-in CW situations.

**Learning curve** — SDR software can be complex, with many settings and options. New users may find it overwhelming compared to a traditional radio with a tuning knob and a few buttons.

## See Also

- [Equipment Overview](/equipment/overview)
- [HF Transceivers](/equipment/hf-transceivers)
- [VHF/UHF Transceivers](/equipment/vhf-uhf-transceivers)
- [Digital Modes Overview](/digital-modes/overview)
- [Digital Station Setup](/digital-modes/digital-station-setup)
- [Software Overview](/software/overview)
- [DIY Projects](/diy-projects/overview)
