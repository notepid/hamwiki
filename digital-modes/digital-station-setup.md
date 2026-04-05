---
title: Digital Station Setup
description: How to set up a complete digital modes station — connecting your radio, computer, and software for HF and VHF digital operation
published: true
date: 2026-04-05T09:30:00.000Z
tags: digital, setup, beginner
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Digital Station Setup

Setting up a station for digital modes involves connecting a radio to a computer so that software can generate transmitted audio and decode received audio. The good news is that the same basic setup works for almost all HF digital modes — [FT8](/digital-modes/ft8), [FT4](/digital-modes/ft4), [PSK31](/digital-modes/psk31), [RTTY](/digital-modes/rtty), [JS8Call](/digital-modes/js8call), [Winlink](/digital-modes/winlink), and more. Once your station is configured, switching between modes is usually just a matter of opening different software.

This guide covers the typical HF digital station. For VHF/UHF digital voice modes ([DMR](/digital-modes/dmr), [D-STAR](/digital-modes/dstar), [System Fusion](/digital-modes/system-fusion)), the radio usually handles everything internally and no computer connection is needed during normal operation (though programming software may require a USB connection).

## The Three Connections

A digital mode station has three logical connections between the radio and computer:

### 1. Audio: Radio ↔ Computer

The computer needs to hear what the radio receives (receive audio) and feed audio into the radio for transmission (transmit audio). This audio path is the core of any digital mode setup.

**Modern radios with built-in USB audio** — Many current HF transceivers (Icom IC-7300, Yaesu FT-991A, Yaesu FTDX10, Kenwood TS-890S, Elecraft KX3, FlexRadio, and others) include a built-in USB audio codec. When you connect the radio to the computer with a USB cable, it appears as a sound card. No external interface is needed.

**External sound card interface** — For radios without built-in USB audio, you need a [sound card interface](/digital-modes/sound-card-interface) — a device that connects between the radio's audio jacks (or accessory port) and the computer's USB port. See the [Sound Card Interface](/digital-modes/sound-card-interface) page for details on popular interfaces and how they work.

### 2. PTT: Computer → Radio

The computer needs a way to tell the radio to start and stop transmitting (push-to-talk). Several methods exist:

**CAT PTT** — The computer sends a "transmit" command through the CAT (Computer Aided Transceiver) control connection. This is the cleanest method and is supported by all modern radios with CAT capability.

**Serial port RTS/DTR** — The computer asserts a serial port signal (RTS or DTR) to key the transmitter. The sound card interface typically includes a circuit to convert this signal to the radio's PTT input.

**VOX** — The radio's voice-activated transmit triggers when it detects audio from the computer. This works but is the least reliable method — timing delays and false triggers can cause problems, especially with time-critical modes like FT8.

**Hardware PTT via interface** — Many sound card interfaces include a built-in PTT circuit triggered by the same serial port or USB connection.

For most setups, **CAT PTT** is recommended. It is reliable, has no timing delays, and does not require additional wiring.

### 3. CAT Control: Computer ↔ Radio

**CAT (Computer Aided Transceiver)** control allows the computer to read and set the radio's frequency, mode, and other settings. While not strictly required for digital modes, CAT control is highly recommended because it allows software to:

- Set the radio to the correct frequency and mode automatically
- Control PTT (as described above)
- Read the radio's frequency for accurate logging
- Monitor transmit power and other status information

CAT connections are typically made via USB (for modern radios) or a serial cable (for older radios). Each radio manufacturer uses their own protocol (Icom CI-V, Yaesu CAT, Kenwood command set), but software like WSJT-X and Fldigi support most radios through the **Hamlib** library.

## Typical Setup Scenarios

### Scenario 1: Modern radio with USB (easiest)

If your radio has a built-in USB audio codec and CAT control via USB (e.g., Icom IC-7300):

1. Connect a **single USB cable** from the radio to the computer
2. Install the radio's **USB driver** if required (some need it, others are class-compliant)
3. In your digital mode software, select the radio's USB audio device for input and output
4. Configure CAT control with the correct radio model, COM port, and baud rate
5. Set PTT method to CAT

That's it. One cable handles audio, PTT, and CAT control.

### Scenario 2: Radio + external sound card interface

If your radio has a traditional audio output (speaker/headphone jack, accessory port, or data port) and no USB audio:

1. Connect the [sound card interface](/digital-modes/sound-card-interface) between the radio and computer
2. Connect a **CAT cable** (USB or serial) from the radio to the computer for CAT control
3. In your digital mode software, select the interface's USB audio device for input and output
4. Configure CAT control with the correct radio model and COM port
5. Set PTT method to CAT or to the serial port signal used by your interface

### Scenario 3: Older radio with no CAT control

For radios without CAT control:

1. Connect a sound card interface for audio
2. Use VOX or a serial port PTT circuit for transmit control
3. Set the radio's frequency and mode manually
4. In your software, select the interface's audio device and configure PTT

This works but requires more manual intervention. You will need to tune the radio by hand and may need to adjust settings manually when changing bands.

## Audio Level Setup

Correct audio levels are **critical** for clean digital mode operation. Incorrect levels cause distortion, splatter (interfering with other stations), and poor decode performance.

### Transmit audio

The goal is to produce a clean, undistorted signal from your radio with **zero ALC activity**. ALC (Automatic Level Control) in a radio is designed for voice peaks, not the constant-level signals of digital modes. When ALC activates on a digital signal, it distorts the signal.

To set transmit audio:

1. Set your radio to a low power level (5–10 watts)
2. Start a test transmission in your digital mode software (use a dummy load or a clear frequency)
3. **Watch the ALC meter** — it should show no deflection
4. Adjust the computer's audio output level (or the interface's drive control) until the radio produces some power output but ALC remains at zero
5. Once audio drive is set, increase radio power to your desired operating level using the radio's power control (not by increasing audio drive)

### Receive audio

The radio's receive audio needs to reach the computer at an appropriate level — not too quiet (poor decoding) and not too loud (clipping/distortion). Most digital mode software includes an audio level indicator:

- In **WSJT-X**, the level meter in the lower left should read approximately 30–60 dB
- In **Fldigi**, the input level should be in the green zone, not red

Adjust the radio's audio output level (or the interface's receive gain) until the software shows a healthy level. If using a radio with USB audio, the audio level may be controlled through a menu setting on the radio.

## Time Synchronisation

Many digital modes — especially [FT8](/digital-modes/ft8), [FT4](/digital-modes/ft4), and [JS8Call](/digital-modes/js8call) — require your computer's clock to be accurate within **±1 second of UTC**. If your clock is off, you won't decode signals properly and other stations won't decode you.

**Windows:** Use an NTP (Network Time Protocol) client. Windows' built-in time synchronisation is often not accurate enough. Free tools like **Meinberg NTP**, **BktTimeSync**, or **Dimension 4** provide more accurate synchronisation.

**macOS and Linux:** The built-in NTP client is usually sufficient if configured to sync frequently.

**Without internet:** A GPS-disciplined clock or GPS receiver with a PPS (pulse per second) output can provide sub-microsecond time accuracy. This is the gold standard but only necessary if you operate without internet access.

## Software Overview

Once your station is connected, the software you use depends on the mode:

| Mode(s) | Software |
|---------|----------|
| FT8, FT4 | WSJT-X (free) |
| JS8Call | JS8Call (free) |
| PSK31, RTTY, and many others | [Fldigi](/digital-modes/fldigi) (free) |
| RTTY (contest) | MMTTY, 2Tone, or N1MM Logger+ |
| Winlink email | Winlink Express (Windows), Pat (cross-platform) |
| VARA modem | VARA HF / VARA FM |
| APRS | Dire Wolf, pinpoint, Xastir |
| Logging | WSJT-X (built-in), Log4OM, N3FJP, HRD |

Most operators end up with several programs installed, launching whichever one they need for the current mode.

## Where to Go Next

- [Sound Card Interface](/digital-modes/sound-card-interface) — Detailed guide to audio interfaces
- [FT8](/digital-modes/ft8) — Get started with the most popular digital mode
- [Fldigi](/digital-modes/fldigi) — Multi-mode software for PSK31, RTTY, and more
- [HF Transceivers](/equipment/hf-transceivers) — Choosing a radio
- [Digital Modes Overview](/digital-modes/overview) — All digital modes at a glance
