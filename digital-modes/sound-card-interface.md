---
title: Sound Card Interfaces
description: Connecting your radio to a computer for digital modes — how sound card interfaces work and which ones to consider
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, interface, equipment, setup
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Sound Card Interfaces

A **sound card interface** is a device that connects a radio transceiver to a computer for digital mode operation. It handles the audio path (receive audio from the radio to the computer, transmit audio from the computer to the radio) and typically provides PTT (push-to-talk) control and electrical isolation between the radio and computer.

If your radio has a **built-in USB audio codec** (as most modern HF transceivers do — see [Digital Station Setup](/digital-modes/digital-station-setup)), you may not need a separate sound card interface at all. But for radios without built-in USB audio, or for situations where an external interface provides better audio quality or additional features, a sound card interface is an essential piece of the digital mode station.

## What a Sound Card Interface Does

A sound card interface performs several functions:

### Audio routing

The interface takes audio from the radio's speaker, headphone, or accessory port output and routes it to the computer as an audio input (microphone or line-in). In the other direction, it takes the computer's audio output and routes it to the radio's microphone or accessory port input for transmission.

### Isolation

**Electrical isolation** between the radio and computer is critical. Without it, ground loops can cause hum, buzz, and noise in the audio — and in some cases can damage equipment. Most sound card interfaces use **audio transformers** or **optocouplers** to electrically isolate the radio from the computer. This is one of the main reasons to use a purpose-built interface rather than a direct cable connection.

### Level matching

Radio audio levels and computer audio levels don't always match. The interface provides level adjustment (through fixed resistor networks or adjustable pots) to ensure the audio is at the right level in both directions.

### PTT control

Most interfaces include a **PTT circuit** that allows the computer to key the radio's transmitter. This is typically triggered by a serial port signal (RTS or DTR) from the computer, or by detecting audio from the computer (VOX-style). The PTT output connects to the radio's PTT input on the microphone connector or accessory port.

### USB audio codec

Many modern interfaces include a built-in USB sound card, so the computer sees the interface as a dedicated audio device. This is preferable to using the computer's built-in sound card because it provides a dedicated audio path that doesn't interfere with the computer's normal audio (system sounds, notifications, etc.).

## Popular Sound Card Interfaces

### Signalink USB

The **Tigertronics SignaLink USB** is one of the most popular and widely used sound card interfaces. It includes a built-in USB sound card, adjustable transmit and receive audio levels (via front-panel knobs), and VOX-based PTT. Radio-specific cables are available for virtually every transceiver model.

The SignaLink USB uses VOX-triggered PTT rather than a serial port signal. This simplifies setup (no COM port configuration for PTT) but means the interface needs to detect transmit audio to key the radio. In practice, this works reliably for most digital modes.

### Digirig Mobile

**Digirig Mobile** is a compact, modern interface designed by K0TX. It is very small (about the size of a USB flash drive), includes a built-in USB sound card and CAT/serial port, and connects to the radio via a single cable. Radio-specific cables are available for many popular models. The serial port provides PTT and CAT control, making it a versatile all-in-one solution.

### Masters Communications DRA series

The **DRA** (Digital Radio Adapter) series from Masters Communications offers simple, affordable interfaces. The DRA-30 and DRA-70 are small boards that connect between the radio's accessory port and the computer's USB port.

### DIY interfaces

Building your own sound card interface is a popular [homebrew project](/diy-projects/overview). A basic interface needs only a few components: audio transformers for isolation, resistors for level matching, and a transistor circuit for PTT. Many designs are available online, and building one is an excellent way to learn about the audio and control connections involved in digital modes.

### Built-in USB audio (no interface needed)

Many modern radios eliminate the need for a separate interface entirely:

- **Icom IC-7300, IC-7610, IC-705** — Built-in USB audio codec and CAT control over a single USB cable
- **Yaesu FT-991A, FTDX10, FTDX101** — Built-in USB audio and CAT
- **Kenwood TS-890S, TS-590SG** — Built-in USB audio and CAT
- **Elecraft KX3, KX2, K4** — Built-in USB audio and CAT
- **FlexRadio** — Network-connected SDR, audio handled entirely in software

If your radio is on this list (or a similar modern model), check the manual for USB audio setup before purchasing a separate interface.

## Connecting the Interface

### Radio connections

Sound card interfaces typically connect to one of these radio ports:

**Accessory port (ACC, DATA)** — A multi-pin connector on the back of the radio that provides fixed-level audio in and out, plus PTT. This is the preferred connection because audio levels from the accessory port are not affected by the radio's volume or microphone gain controls.

**Microphone connector** — The front-panel mic jack can be used for transmit audio input and PTT. Receive audio comes from the headphone or speaker jack. This works but means you need to disconnect the microphone to use digital modes (unless the radio has a separate data port).

**Headphone/speaker jack** — Provides receive audio. Level varies with the radio's volume control, so you need to set the volume to an appropriate level and leave it there during digital operation.

### Computer connections

The interface connects to the computer via **USB**, appearing as either a dedicated USB audio device (for interfaces with built-in sound cards) or connecting to the computer's existing sound card via 3.5mm audio cables.

A USB connection is strongly preferred — it provides a dedicated audio device that won't conflict with the computer's system audio.

## Troubleshooting Common Issues

**Hum or buzz in audio** — Usually a ground loop. Ensure the interface provides proper isolation. Check that the radio and computer are on the same electrical ground. A snap-on ferrite choke on the USB cable can help.

**No transmit audio** — Check that the correct audio output device is selected in your software. Verify the interface's transmit audio cable is connected to the correct radio port. Check audio levels — the computer's output level may be too low.

**ALC showing during transmit** — Transmit audio level is too high. Reduce the computer's audio output level or the interface's transmit level control until ALC reads zero.

**Receive audio too quiet or too loud** — Adjust the radio's audio output level (volume control or accessory port level setting) and/or the interface's receive level control. Software audio level indicators should show a healthy signal without clipping.

**Radio transmits continuously** — PTT is stuck on. Check the PTT wiring and software settings. If using VOX-triggered PTT, ensure the computer isn't playing system sounds through the interface.

**Software doesn't see the interface** — Make sure USB drivers are installed (if required). Check that the interface appears in the computer's sound device list. Try a different USB port or cable.

## Where to Go Next

- [Digital Station Setup](/digital-modes/digital-station-setup) — The complete station setup guide
- [FT8](/digital-modes/ft8) — Get started with the most popular digital mode
- [Fldigi](/digital-modes/fldigi) — Multi-mode digital software
- [DIY Projects](/diy-projects/overview) — Build your own interface
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
