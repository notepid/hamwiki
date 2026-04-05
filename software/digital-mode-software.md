---
title: Digital Mode Software
description: Software for encoding and decoding amateur radio digital modes — from FT8 and PSK31 to RTTY, Winlink, and beyond
published: true
date: 2026-04-05T09:30:00.000Z
tags: software, digital-modes, ft8, psk31, rtty, fldigi, wsjt-x
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Digital Mode Software

Digital mode software is the bridge between your transceiver's audio and the digital signals that travel over the air. These programs take audio from your radio, decode it into text or data, and — on transmit — generate the precisely timed audio tones your radio broadcasts. Without them, modes like [FT8](/digital-modes/ft8), [PSK31](/digital-modes/psk31), and [RTTY](/digital-modes/rtty) would not exist.

This page covers the major categories of digital mode software, what each program does well, and how they connect to your radio and the rest of your station.

## How Digital Mode Software Works

The basic signal chain is the same for nearly all digital mode programs:

**On receive:** Radio audio → sound card interface or USB audio → computer → software decodes the audio into text, callsigns, or data.

**On transmit:** Software generates audio tones → sound card interface or USB audio → radio transmits the tones as an SSB signal (or in some cases, FSK).

The computer's sound card (or the radio's built-in USB audio codec) is the critical link. A [sound card interface](/digital-modes/sound-card-interface) handles level matching, isolation, and PTT (push-to-talk) switching between the radio and computer. Modern transceivers with built-in USB audio (such as those from Icom, Yaesu, Kenwood, Elecraft, and others) eliminate the need for a separate interface — you connect a single USB cable and the radio appears as an audio device and serial port on the computer.

The software must also control the radio's PTT to switch between receive and transmit. This is done via CAT command, a serial port signal (RTS or DTR), or VOX (though VOX is not recommended for most digital modes due to timing delays).

## Major Digital Mode Programs

### WSJT-X

WSJT-X is the home of the **FT8**, **FT4**, **JT65**, **JT9**, **WSPR**, **MSK144**, **FST4**, and **Q65** modes. Developed by Joe Taylor (K1JT) and a team of contributors, WSJT-X is designed specifically for weak-signal communication. It runs on Windows, macOS, and Linux.

FT8 is by far the most popular digital mode in amateur radio, and WSJT-X is the primary program that implements it. If you plan to operate FT8, you will use WSJT-X. See the [FT8 page](/digital-modes/ft8) for a detailed setup guide.

WSJT-X includes a built-in waterfall display, automatic sequencing for standard exchanges, integration with callsign databases, and the ability to send logged contacts to external loggers via UDP. It does not include a general-purpose log — you will want a separate [logging program](/software/logging-software) to receive contacts from WSJT-X.

### JTDX

JTDX is a third-party fork of WSJT-X that focuses on enhanced decoding performance for JT65, JT9, and FT8 modes. Some operators prefer JTDX for its multi-pass decoding algorithms, which can pull additional signals out of the noise. It shares the same configuration approach as WSJT-X and is available for Windows, macOS, and Linux.

### JS8Call

JS8Call extends FT8 technology into a keyboard-to-keyboard messaging system. Where FT8 is limited to short, structured exchanges, JS8Call allows freeform text messaging over weak-signal paths. It supports directed messages, group calls, relay networks, and store-and-forward messaging. JS8Call is particularly popular among operators interested in [emergency communications](/emergency-communications/overview) and off-grid messaging. See the [JS8Call page](/digital-modes/js8call) for details.

### Fldigi

Fldigi (Fast Light Digital) is a versatile, open-source program that supports a wide range of digital modes — over 80, including PSK31, PSK63, RTTY, OLIVIA, MT63, MFSK, Contestia, Thor, DominoEX, and many more. It runs on Windows, macOS, and Linux.

Fldigi is the go-to program for modes that WSJT-X does not cover. Its interface includes a waterfall display, a text input/output window for keyboard-to-keyboard operation, built-in macros for common exchanges, and a simple built-in logger. Fldigi can also interface with external loggers and with flrig (a companion rig control program) or Hamlib for CAT control.

For operators interested in the broad range of traditional digital modes, fldigi is an essential tool. See the [PSK31](/digital-modes/psk31) and [RTTY](/digital-modes/rtty) pages for mode-specific information.

### Winlink Express

Winlink Express is the primary client for the [Winlink](/digital-modes/winlink) global radio email system. It sends and receives email over amateur radio using VARA (HF and FM), ARDOP, Pactor, or packet radio connections. Winlink is widely used in emergency communications and by operators in remote locations without internet access.

Winlink Express handles the email composition, address book, attachment handling, and connection management. The underlying modem (VARA, ARDOP, etc.) runs as a separate program that Winlink Express controls. The system currently runs on Windows, though some components are available on Linux via Wine or native ports.

### VARA

VARA is a high-performance HF and VHF/FM modem used primarily with Winlink and peer-to-peer connections. It offers significantly higher throughput than older protocols like ARDOP. VARA comes in HF and FM versions and runs on Windows. A free version is available with reduced speed; the full-speed version requires a paid licence.

### MMTTY and similar RTTY programs

MMTTY is a dedicated RTTY (radioteletype) program for Windows. While fldigi also handles RTTY well, MMTTY is widely used in contest environments because it integrates tightly with [contest software](/software/contest-software) — many contest loggers can control MMTTY directly as an external modem. MMTTY focuses purely on RTTY and does it well, with excellent decode performance and tuning indicators.

### Digital mode decoders for SDR

If you use an [SDR receiver](/software/sdr-software), you can pipe the SDR's audio output to a digital mode decoder via a virtual audio cable. Some SDR applications include built-in digital mode decoding — for example, decoding FT8 signals directly within the SDR waterfall. This creates a fully software-defined digital receive station with no traditional radio hardware in the chain.

## Connecting Digital Mode Software to Your Radio

The most important technical step in getting started with digital modes is establishing the audio and PTT connection between your computer and transceiver. There are three common approaches:

### Built-in USB audio (modern radios)

Many current transceivers include a USB port that presents both an audio codec (sound card) and a serial port (CAT control) to the computer. You connect a single USB cable and the radio appears as audio input/output and a COM port. This is the simplest and cleanest approach.

### External sound card interface

For older radios without USB audio, a sound card interface sits between the radio's audio connections (microphone, speaker, or accessory port) and the computer's sound card. The interface handles level matching, ground isolation (to prevent ground loops and hum), and often provides PTT switching via a serial port signal. Commercially available interfaces are plug-and-play; homebrew designs are also popular among amateur builders.

### Virtual audio cables

When running multiple programs that need to share audio — for example, an SDR application feeding audio to WSJT-X — virtual audio cable software creates internal audio connections between programs. On Windows, VB-Cable and Virtual Audio Cable (VAC) are commonly used. Linux handles this natively with PulseAudio or PipeWire. macOS users can use BlackHole or Loopback.

> **Important:** Digital modes require your radio to be set to the correct sideband. Most HF digital modes use **USB** (upper sideband). Some programs and modes use the radio's dedicated **DATA** or **DIGI** mode if available, which may apply different filtering or ALC behaviour. Consult your radio's manual and the software's documentation.
{.is-info}

## Audio Levels and ALC

Proper audio levels are critical for clean digital transmissions. The single most common mistake new digital mode operators make is overdriving the audio, which produces splatter — unwanted signals that interfere with nearby stations.

**Set power via the radio's power control, not the audio level.** Your audio drive level should be set just high enough that the radio reaches your desired output power. The ALC meter on your radio should show **little or no ALC activity** during digital mode transmission. If the ALC is deflecting, reduce the audio drive level from the software or the sound card output level.

**Do not use speech processing or compression** on digital modes. These features are designed for voice and will distort digital signals.

## Integration with Logging Software

Most digital mode programs can send completed contacts to your [logging software](/software/logging-software) automatically:

- **WSJT-X and JTDX** send contacts via UDP broadcast. Most major loggers can receive these broadcasts.
- **JS8Call** supports UDP logging output similar to WSJT-X.
- **Fldigi** can log contacts to its built-in log and export ADIF, or interface with external loggers via TCP/IP.
- **Contest loggers** often have built-in digital mode interfaces that control MMTTY, fldigi, or WSJT-X directly from within the contest logging environment.

## Choosing Digital Mode Software

Your choice of software depends primarily on which modes you want to operate:

| If you want to operate... | Use... |
|--------------------------|--------|
| FT8, FT4, JT65, JT9, WSPR, MSK144 | WSJT-X or JTDX |
| Keyboard-to-keyboard weak-signal messaging | JS8Call |
| PSK31, OLIVIA, MT63, and other traditional modes | Fldigi |
| RTTY (especially for contests) | Fldigi or MMTTY |
| Radio email (Winlink) | Winlink Express + VARA or ARDOP |

Many operators run multiple programs, switching between them depending on their current operating activity. Since they all use the same sound card interface and CAT connection, switching is usually a matter of closing one program and opening another (or running them in parallel if your audio routing supports it).

## Where to Go Next

- [Software & Tools Overview](/software/overview) — All software categories at a glance
- [FT8](/digital-modes/ft8) — Detailed guide to the most popular digital mode
- [PSK31](/digital-modes/psk31) — Keyboard-to-keyboard HF communication
- [RTTY](/digital-modes/rtty) — Radioteletype operation
- [JS8Call](/digital-modes/js8call) — Weak-signal messaging
- [Winlink](/digital-modes/winlink) — Radio email system
- [Digital Station Setup](/digital-modes/digital-station-setup) — Connecting radio and computer
- [Sound Card Interface](/digital-modes/sound-card-interface) — The hardware link
- [Logging Software](/software/logging-software) — Recording and managing contacts
- [Contest Software](/software/contest-software) — Logging for contest operating
