---
title: Modulation
description: AM, FM, SSB, CW, and digital modulation techniques used in amateur radio
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, modulation, modes
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Modulation

Modulation is the process of encoding information onto a radio-frequency carrier wave so it can be transmitted through space and recovered at the receiving end. An unmodulated carrier — a pure sine wave at a single frequency — conveys no information by itself. By systematically varying one or more properties of that carrier (its amplitude, frequency, or phase), we embed the information we want to communicate.

Different modulation methods have different trade-offs in spectrum efficiency, power efficiency, noise immunity, and complexity. Amateur radio uses a wide variety of modulation types, and understanding the basics helps you choose the right mode for the situation and troubleshoot signal quality issues.

## CW — continuous wave (Morse code)

Technically the simplest form of modulation: the carrier is switched on and off in patterns corresponding to Morse code characters. The transmitter is either fully on or fully off — there is no amplitude variation to carry voice.

Despite its simplicity, CW is remarkably effective. Because a CW signal occupies very little bandwidth (typically under 200 Hz with proper keying), the receiver can use a very narrow filter, which admits much less noise than voice modes. This gives CW a significant signal-to-noise advantage — it is one of the most efficient modes for weak-signal communication. The ITU emission designator for CW is **A1A**.

### Keying waveform

Abrupt on/off switching would produce a very wide signal due to the sharp transitions (key clicks). Practical CW transmitters shape the keying waveform with controlled rise and fall times (typically 3–5 milliseconds), producing a clean, narrow signal without objectionable clicks.

## Amplitude modulation (AM)

In **amplitude modulation**, the carrier's amplitude is varied in proportion to the instantaneous value of the modulating signal (typically audio from a microphone). The result is a signal consisting of three components: the **carrier** at the centre frequency, an **upper sideband (USB)** above the carrier, and a **lower sideband (LSB)** below the carrier.

### AM bandwidth

An AM signal occupies twice the highest audio frequency: if the audio bandwidth is 3 kHz, the AM signal is 6 kHz wide (3 kHz USB + 3 kHz LSB). The ITU designator is **A3E**.

### AM efficiency

AM is inherently inefficient. At 100% modulation (the maximum before distortion), two-thirds of the transmitted power goes into the carrier (which carries no information) and only one-third into the two sidebands (which carry identical information). Despite this, AM remains popular among some amateurs on 160 m, 75/80 m, and 10 m for its natural, full-fidelity sound and the enjoyment of building and operating vintage AM equipment.

## Single sideband (SSB)

**Single sideband** is a refinement of AM that transmits only one sideband and suppresses both the carrier and the other sideband. This gives SSB two major advantages over AM:

1. **Power efficiency:** All transmitted power goes into the information-carrying sideband (no power wasted on the carrier)
2. **Spectrum efficiency:** An SSB signal occupies about 2.4 kHz instead of 6 kHz for AM

SSB is the dominant voice mode on HF amateur bands. By convention, **lower sideband (LSB)** is used on 160 m, 80 m, and 40 m, while **upper sideband (USB)** is used on 20 m and above. The ITU designator is **J3E**.

### Generating SSB

SSB is typically generated at a low intermediate frequency using a **balanced modulator** (which produces a double-sideband suppressed-carrier signal) followed by a **sideband filter** (a narrow crystal or mechanical filter that passes only the desired sideband). The resulting SSB signal is then mixed up to the operating frequency and amplified by linear amplifier stages.

An alternative method, the **phasing method**, uses phase-shift networks to cancel the unwanted sideband. This approach avoids the need for expensive crystal filters and is popular in homebrew designs and SDR implementations.

### SSB demodulation

The receiver must reinsert the missing carrier to demodulate SSB. This is done by a **beat frequency oscillator (BFO)** or product detector that generates a replacement carrier at the correct frequency. If the BFO is mistuned, voices sound unnatural (either high-pitched "Donald Duck" or low-pitched and muffled), which is why accurate tuning is important on SSB.

## Frequency modulation (FM)

In **frequency modulation**, the carrier's frequency is varied in proportion to the modulating signal while the amplitude remains constant. The amount of frequency change (the **deviation**) is proportional to the modulating audio level, and the rate of change equals the audio frequency.

### Narrowband FM (NBFM)

Amateur radio FM on VHF and UHF uses **narrowband FM** with typical maximum deviation of ±5 kHz and a channel spacing of 12.5 to 25 kHz. The ITU designator is **F3E**.

FM has excellent noise immunity compared to AM because the receiver's limiter stage strips away amplitude noise before the discriminator extracts the frequency-encoded audio. This is why FM sounds "quieter" than AM or SSB — once the signal is strong enough to engage the limiter (the **capture effect**), noise drops dramatically. Below this threshold, FM degrades rapidly — there is no gradual fade like SSB.

### FM in amateur radio practice

FM is the standard mode for VHF/UHF repeaters and simplex voice communication. Its constant-amplitude nature means the transmitter PA can operate in efficient Class C mode. FM is also used for the audio subcarrier in amateur television (ATV).

## Phase modulation (PM)

**Phase modulation** varies the carrier's phase in proportion to the modulating signal. PM is closely related to FM — in fact, PM with audio pre-emphasis produces a signal that is indistinguishable from FM. Some amateur FM transmitters actually use phase modulation of the oscillator because it is easier to implement in synthesised transmitters without pulling the oscillator frequency.

## Digital modulation

Modern digital modes encode information as discrete symbols rather than continuously varying analogue parameters. Several digital modulation techniques are used in amateur radio:

### Frequency-shift keying (FSK)

**FSK** shifts the carrier between two (or more) discrete frequencies to represent digital data. Traditional RTTY uses audio FSK with a 170 Hz shift between mark and space frequencies. Packet radio on VHF uses audio FSK at 1200 baud (Bell 202 tones) or 9600 baud (direct FSK of the transmitter).

### Phase-shift keying (PSK)

**PSK** encodes data by shifting the carrier's phase. **PSK31**, one of the most popular amateur digital modes, uses binary phase-shift keying (BPSK) with a very narrow bandwidth (about 31 Hz) to achieve keyboard-to-keyboard communication at low power. **QPSK** (quadrature PSK) encodes two bits per symbol using four phase states, doubling the data rate for the same symbol rate.

### Orthogonal frequency-division multiplexing (OFDM)

**OFDM** transmits data across many closely spaced sub-carriers simultaneously. Each sub-carrier is independently modulated, and the combination achieves high data rates with good resistance to multipath propagation. The amateur WINMOR and ARDOP modes use OFDM-like techniques, and JS8Call and FT8/FT4 incorporate elements of this approach.

### Minimum-shift keying and GMSK

**MSK** and **GMSK** (Gaussian minimum-shift keying) are special forms of FSK that maintain phase continuity, resulting in a compact spectrum. D-STAR digital voice uses GMSK at 4800 baud on its data channel.

### 4-FSK and C4FM

**4-level FSK** (4FSK) uses four frequency states to encode two bits per symbol. Yaesu's **System Fusion** uses C4FM (continuous 4-level FM) for its digital voice and data modes.

## Choosing the right modulation for the situation

| Situation | Recommended mode | Why |
|-----------|-----------------|-----|
| HF voice DX | SSB (USB/LSB) | Spectrum and power efficient |
| VHF/UHF local voice | FM | Clean audio, repeater compatible |
| Weak-signal HF | CW or FT8 | Narrow bandwidth, best S/N |
| HF digital messaging | WINMOR, ARDOP, VARA | Error correction, reasonable speed |
| Keyboard chat on HF | PSK31, JS8Call | Narrow bandwidth, readable at low power |
| Emergency/EMCOMM voice on HF | SSB | Widely available, no infrastructure needed |

The best modulation choice depends on the propagation conditions, desired communication range, available equipment, and purpose of the communication.

## Bandwidth and spectrum considerations

All modulated signals occupy bandwidth — some of the spectrum on either side of the carrier frequency. Keeping your signal within the allocated band segment and avoiding excessive bandwidth (from overmodulation, distortion, or poor keying) is both a regulatory requirement and good operating practice. Band plans designate which segments of each band are intended for which modes, helping operators coexist.

## See also

- [Transmitters](/electronics/transmitters) — how modulated signals are generated and amplified
- [Receivers](/electronics/receivers) — how modulated signals are demodulated
- [Filters & Theory](/electronics/filters-theory) — shaping modulated signal bandwidth
- [The Electromagnetic Spectrum](/electronics/electromagnetic-spectrum) — frequency allocations and band plans
