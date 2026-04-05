---
title: Voice Modes (SSB, FM, AM)
description: Operating using voice modes including SSB, FM, and AM on amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: operating, ssb, fm, am, voice
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Voice Modes (SSB, FM, AM)

Voice communication is the most common mode of operation in amateur radio. When people think of "talking on the radio," they are thinking of voice modes. Amateur operators use three main analog voice modes — **SSB**, **FM**, and **AM** — each with different characteristics suited to different bands and situations.

## FM (Frequency Modulation)

FM is the voice mode most new operators encounter first, because it is the standard mode on VHF/UHF [repeaters](/operating/repeaters) and handheld radios.

### How FM works
In FM, the voice signal modulates (varies) the **frequency** of the radio carrier, rather than its amplitude. The result is a signal that is resistant to amplitude noise and interference, producing clean, clear audio.

### Characteristics
- **Audio quality** — FM produces the best audio quality of the three modes, with crisp, natural-sounding voice.
- **Bandwidth** — An FM signal occupies about 16 kHz (for wideband FM) or 11 kHz (for narrowband FM). This is much wider than SSB, which means fewer stations can fit on a band segment.
- **Capture effect** — FM receivers tend to "capture" the strongest signal on a frequency, suppressing weaker ones. This means the strongest station wins, which can be a disadvantage for weaker stations.
- **Squelch** — FM radios use a squelch circuit to silence the receiver when no signal is present, eliminating the constant background hiss.

### Where FM is used
- **VHF/UHF** — FM is the dominant voice mode on 2 metres, 70 centimetres, and higher bands, both through repeaters and on simplex.
- **10 metres** — There is a small FM segment around 29.6 MHz, including FM repeaters.
- **FM is not commonly used on most HF bands** because its wide bandwidth would use too much spectrum in the already-crowded HF allocations.

### Operating FM
FM operation is straightforward: tune to a frequency, press the PTT (push-to-talk) button, and speak. On a repeater, you need the correct offset and [CTCSS/DCS tone](/operating/repeaters). On simplex, both stations use the same frequency.

Speak at a normal conversational level, holding the microphone a few centimetres from your mouth. Over-modulating (speaking too loudly or too close) causes distorted audio on FM.

## SSB (Single Sideband)

SSB is the primary voice mode on the HF bands and is also used for weak-signal work on VHF/UHF.

### How SSB works
SSB is a refined form of AM. A normal AM signal consists of a carrier and two sidebands (upper and lower), each containing a copy of the voice information. SSB removes the carrier and one sideband, transmitting only the remaining sideband. This makes SSB much more efficient than AM — all the transmitter power goes into the voice signal rather than being wasted on a carrier.

The two variants are:
- **USB (Upper Sideband)** — Used on frequencies above 10 MHz (including 20, 17, 15, 12, and 10 metres), and on VHF/UHF.
- **LSB (Lower Sideband)** — Used on frequencies below 10 MHz (including 80, 60, and 40 metres).

This convention is a long-standing tradition, not a technical requirement. Most radios automatically select the correct sideband based on the band, but it is important to be on the right one.

### Characteristics
- **Bandwidth** — An SSB signal occupies about 2.4 kHz, roughly one-seventh of an FM signal. This efficient use of spectrum is why SSB is the standard on the crowded HF bands.
- **Power efficiency** — Because there is no carrier to waste power on, all transmitted power goes into the intelligence-carrying sideband.
- **Audio quality** — SSB audio is narrower and less natural than FM. It sounds somewhat "tinny" or "nasal" compared to FM, but is perfectly intelligible.
- **Tuning sensitivity** — SSB signals must be tuned precisely. Being off by even a few hundred hertz changes the pitch of the received audio, making voices sound too high or too low. Modern radios with stable synthesizers make this straightforward, but it is something to be aware of.
- **No squelch** — SSB receivers do not have a capture effect or automatic squelch like FM. The background noise is always present, and operators rely on their ears to detect signals.

### Where SSB is used
- **All HF bands** — SSB is the standard voice mode on HF. The phone (voice) portions of each band are predominantly SSB.
- **VHF/UHF weak-signal** — SSB is used in the lower segments of the 6-metre, 2-metre, and 70 cm bands for long-distance weak-signal communication, satellite work, and contests.

### Operating SSB
Operating SSB requires a bit more attention than FM:

- **Tune carefully.** Adjust the VFO until the other station's voice sounds natural. If it sounds too high-pitched or like chipmunks, you are tuned too low. If it sounds too deep, you are tuned too high.
- **Speak close to the microphone** but do not shout. SSB benefits from consistent audio levels. Many experienced operators use speech processing (compression) to increase their average transmitted power.
- **Watch your ALC (Automatic Level Control).** Over-driving the transmitter causes a wide, distorted signal that interferes with adjacent frequencies. The ALC meter on your radio should show only occasional deflection on voice peaks.
- **Use headphones.** On noisy HF bands, headphones make a significant difference in your ability to copy weak signals.

## AM (Amplitude Modulation)

AM was the original voice mode in amateur radio and in broadcast radio. While it has been largely replaced by SSB for general HF communication, AM retains a dedicated and enthusiastic following.

### How AM works
In AM, the voice signal modulates the **amplitude** (power level) of the carrier wave. The transmitted signal contains the carrier and two sidebands.

### Characteristics
- **Audio quality** — AM can produce rich, warm, full-fidelity audio. Many AM enthusiasts transmit wider audio than standard SSB, and vintage AM transmitters are prized for their audio character.
- **Bandwidth** — An AM signal occupies about 6 kHz (double sideband), which is wider than SSB but narrower than FM.
- **Power efficiency** — AM is the least power-efficient voice mode. At least two-thirds of the transmitter power goes into the carrier, which carries no voice information. A 100-watt AM transmitter has the effective voice power of a roughly 25-watt SSB transmitter.
- **Compatibility** — AM can be received on any general-coverage receiver without special demodulation, which is one reason it was the original broadcast standard.

### Where AM is used
- **75 metres (3.885 MHz area)** — The most active AM frequency in the US.
- **40 metres (7.290 MHz area)** — Another popular AM gathering spot.
- **10 metres (29.0–29.2 MHz area)** — Some AM activity.
- **160 metres** — AM activity exists, often using vintage equipment.
- **6 metres** — Some AM activity, particularly among enthusiasts.

AM frequencies are informal gathering spots rather than officially designated segments, though band plans may indicate suggested AM windows.

### The AM community
The AM community tends to emphasize audio quality, vintage equipment, and the art of transmitter design. Many AM operators use classic or homebrew transmitters and enjoy discussing and modifying equipment. The round-table style of AM conversations — where groups of operators take turns in extended, friendly exchanges — is characteristic of the mode.

## Digital Voice Modes

In addition to the three analog modes, amateur radio also uses digital voice modes where voice is digitized, compressed, and transmitted as digital data. These include [DMR](/digital-modes/dmr), [D-STAR](/digital-modes/dstar), [System Fusion](/digital-modes/system-fusion), and [M17](/digital-modes/m17). Digital voice modes are covered in the [Digital Modes](/digital-modes/overview) section of this wiki.

## Choosing a Voice Mode

| Factor | FM | SSB | AM |
|--------|----|----|-----|
| Typical use | VHF/UHF repeaters, local communication | HF voice, VHF/UHF weak signal | HF enthusiast groups |
| Audio quality | Excellent | Good (narrower bandwidth) | Excellent (wide audio possible) |
| Bandwidth | ~16 kHz (wide) / ~11 kHz (narrow) | ~2.4 kHz | ~6 kHz |
| Power efficiency | Good | Excellent | Poor |
| Equipment needed | FM transceiver (HT, mobile, base) | SSB-capable transceiver | AM-capable transceiver |
| Ease of use | Very easy | Requires careful tuning | Moderate |

## Where to Go Next

- [QSO Basics](/operating/qso-basics) — How to make contacts on any mode
- [Repeaters](/operating/repeaters) — FM operating on repeaters
- [HF Operating](/operating/hf-operating) — SSB and AM on the HF bands
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — FM and SSB on VHF/UHF
- [Digital Modes Overview](/digital-modes/overview) — Digital voice and data modes
