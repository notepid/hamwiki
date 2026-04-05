---
title: SDR Software
description: Software for software-defined radio receivers and transceivers — from general-purpose SDR applications to specialised tools
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, sdr, software-defined-radio, receiver
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# SDR Software

A software-defined radio (SDR) moves most of the signal processing that traditionally happens in analogue circuits — filtering, demodulation, noise reduction, and more — into software running on a computer. The hardware captures a wide swath of radio spectrum and digitises it; the software then does everything else. This means the "radio" you interact with is largely a program on your screen, and upgrading your receiver can be as simple as updating the software.

SDR software ranges from general-purpose applications that work with many different hardware devices to manufacturer-specific programs tightly integrated with a particular receiver or transceiver. This page covers the major categories, what to look for when choosing SDR software, and how SDR applications fit into the wider amateur radio station.

## How SDR Software Works

In a traditional superhet receiver, the incoming signal passes through physical bandpass filters, is mixed down to an intermediate frequency, filtered again, and demodulated — all in hardware. In an SDR, the hardware front end converts the radio signal to a digital data stream (typically via an analogue-to-digital converter, or ADC). That stream is sent to the computer, where software performs:

**Spectrum display and waterfall** — The software computes a Fast Fourier Transform (FFT) to show the entire received bandwidth as a real-time spectrum and scrolling waterfall display. You can see every signal in the passband at once, which is a dramatic improvement over tuning across a band one signal at a time.

**Filtering** — Digital filters can be made extremely sharp and are adjustable on the fly. You can narrow a CW filter to 50 Hz, widen an SSB filter to 3.5 kHz, or set any arbitrary bandwidth — all in software.

**Demodulation** — The software demodulates AM, FM, SSB (USB and LSB), CW, and various digital modes. Some SDR applications include built-in decoders for modes like FT8, RTTY, and PSK31.

**Noise reduction** — Digital noise reduction algorithms (spectral subtraction, adaptive filtering, neural-network-based NR) can be applied in real time to clean up received audio.

**Recording** — SDR software can record the entire received bandwidth as an IQ (in-phase and quadrature) file. You can play back this recording later and tune through it as if you were listening live — a powerful feature for reviewing contest activity, catching stations you missed, or documenting interference.

## Types of SDR Hardware

SDR software is closely linked to the hardware it drives. Understanding the main hardware categories helps in choosing the right software:

### Low-cost USB dongles

RTL-SDR dongles, based on the Realtek RTL2832U chip, are inexpensive (often under $30 USD) and cover roughly 24 MHz to 1.7 GHz. They are receive-only, with 8-bit resolution and up to about 2.4 MHz of instantaneous bandwidth. These are excellent for getting started, monitoring FM repeaters, receiving weather satellites, tracking aircraft (ADS-B), and experimenting with VHF/UHF signals.

### Mid-range receivers

Devices in this category offer wider bandwidth, higher bit depth (typically 12–16 bits), and better dynamic range. Examples include receivers covering HF through VHF/UHF with 10–50 MHz of instantaneous bandwidth. Many connect via USB 3.0 or Ethernet and are designed specifically for amateur radio use.

### High-performance SDR transceivers

At the top end are SDR transceivers that can both receive and transmit, with performance comparable to or exceeding conventional transceivers. These units often include high-speed ADCs and DACs with 16-bit or higher resolution, direct-sampling architectures covering HF through 6 metres, and Ethernet or USB 3.0 interfaces. Some are standalone units with optional displays, while others are entirely computer-controlled.

### Network-attached SDRs

Some SDR receivers are designed to be accessed over a network, either on the local LAN or over the internet. This allows you to place the receiver at a remote location with good antennas and operate it from anywhere with a network connection. The KiwiSDR project, for example, has deployed hundreds of web-accessible HF receivers around the world that anyone can tune via a browser.

## Popular SDR Software Applications

The following table lists widely used SDR software. No endorsement is implied — this is a representative sample of the options available across different platforms.

### General-purpose SDR applications

| Program | Platforms | Licence | Notable features |
|---------|-----------|---------|-----------------|
| SDR# (SDRSharp) | Windows | Free | Widely used with RTL-SDR and Airspy devices; plugin system for frequency scanning, digital decoding, and more |
| HDSDR | Windows | Free | Supports many SDR hardware devices via ExtIO plugins; dual-VFO, recording, and playback |
| SDR++ | Windows, macOS, Linux | Free (open source) | Modern, cross-platform, modular design; supports many hardware devices and demodulator plugins |
| CubicSDR | Windows, macOS, Linux | Free (open source) | Cross-platform with a clean interface; supports SoapySDR for broad hardware compatibility |
| GQRX | Linux, macOS | Free (open source) | Popular on Linux; built on GNU Radio; supports many devices via OsmoSDR |
| GNU Radio | Windows, macOS, Linux | Free (open source) | Signal processing framework rather than a standalone application; build custom signal processing chains with a graphical flowgraph editor |
| LinHPSDR | Linux | Free (open source) | Client for high-performance SDR transceivers using the openHPSDR protocol |

### Manufacturer-specific software

Many SDR hardware manufacturers provide dedicated software optimised for their products. These programs are typically the most polished option for a given device and often support advanced features like transmit capability, hardware-specific controls, and tight integration with the device firmware. Check your hardware manufacturer's website for the recommended software.

### Web-based SDR software

WebSDR and OpenWebRX are server applications that make an SDR receiver accessible through a web browser. Station owners run the server software on a computer connected to an SDR receiver and antenna; remote users tune and listen through their browser with no software installation needed. This approach has created a global network of publicly accessible receivers that are invaluable for propagation monitoring and remote listening.

## Choosing SDR Software

### Hardware compatibility

The first consideration is whether the software supports your SDR hardware. Some programs work only with specific devices, while others use abstraction layers like SoapySDR, ExtIO, or Hamlib to support a wide range of hardware. If you are buying hardware and software together, check that they are a supported combination.

### Operating system

Windows has the widest selection of SDR software. Linux is well-served by GQRX, SDR++, CubicSDR, and GNU Radio. macOS support has improved but is still more limited, with SDR++, CubicSDR, and GQRX being the main options.

### Performance requirements

SDR software performs continuous FFT calculations on large data streams, which can be CPU-intensive. Wider bandwidths and higher FFT resolutions require more processing power. A modern multi-core processor and a dedicated GPU (for waterfall rendering) help with smooth performance. If you are using a low-powered laptop, you may need to reduce bandwidth or FFT size.

### Integration with other software

If you plan to use your SDR for digital modes, check how the SDR software routes audio to programs like WSJT-X or fldigi. Some SDR applications have built-in virtual audio cable support, while others require a separate virtual audio cable program. On Linux, PulseAudio or PipeWire typically handle this routing natively.

## Common SDR Concepts

### IQ data

SDR hardware delivers data as pairs of in-phase (I) and quadrature (Q) samples. This IQ format preserves both the amplitude and phase of the received signal, which is necessary for the software to distinguish between signals above and below the tuned frequency. You will encounter IQ when recording or streaming SDR data.

### Sample rate and bandwidth

The sample rate of the ADC determines the instantaneous bandwidth the SDR can receive. A sample rate of 2.4 MHz (common with RTL-SDR) means you can see 2.4 MHz of spectrum at once. Higher-end devices with sample rates of 50 MHz or more allow you to view an entire amateur band simultaneously.

### FFT size and resolution

The FFT (Fast Fourier Transform) converts the time-domain IQ data into a frequency-domain spectrum display. A larger FFT size gives finer frequency resolution (you can distinguish signals closer together) but requires more computation and introduces more latency. Most SDR programs let you adjust the FFT size to balance resolution and performance.

### Dynamic range and bit depth

The bit depth of the ADC determines the dynamic range of the receiver — its ability to receive weak signals in the presence of strong ones. An 8-bit ADC (RTL-SDR) provides roughly 48 dB of dynamic range; a 16-bit ADC provides roughly 96 dB. For crowded HF bands with strong broadcast signals, higher dynamic range is important.

> **Tip:** If you are new to SDR, start with an inexpensive RTL-SDR dongle and a free program like SDR# or SDR++. This lets you explore the technology and learn the concepts at minimal cost before investing in higher-end hardware.
{.is-info}

## Using SDR Software in Your Station

### SDR as a panadapter

Even if your main receiver is a conventional transceiver, an SDR receiver connected to the same antenna (or a tap from the IF stage) can serve as a panadapter — a wideband visual display of activity on the band. Many operators use this setup to spot signals visually on a waterfall while tuning their main radio by ear.

### SDR for digital modes

SDR software can feed audio directly to digital mode programs. The typical setup routes the SDR's demodulated audio through a virtual audio cable to WSJT-X, fldigi, or another decoder. On receive, this works well and gives you the added benefit of the wideband waterfall display. For transmitting, you still need a conventional transceiver or an SDR transceiver.

### Remote operation

SDR's digital nature makes it well-suited for remote operation. You can run the SDR server at a remote site with good antennas and control it over the internet from home. Latency and bandwidth are the main considerations — IQ streaming requires a stable connection with sufficient throughput.

### Recording and playback

Recording the raw IQ stream captures everything within the SDR's bandwidth at that moment. You can play back the recording days or weeks later and tune through it as if listening live. This is valuable for post-contest review, identifying intermittent interference, or simply capturing a band opening that you did not have time to fully explore in real time.

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [Digital Mode Software](/software/digital-mode-software) — Programs for FT8, PSK31, RTTY, and more
- [Antenna Modelling Software](/software/antenna-modeling-software) — Simulate antenna designs on screen
- [Equipment Overview](/equipment/overview) — Radio hardware including SDR transceivers
- [Digital Station Setup](/digital-modes/digital-station-setup) — Connecting radio and computer
- [FT8](/digital-modes/ft8) — The most popular digital mode, often used with SDR
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — Operating on bands where RTL-SDR excels
