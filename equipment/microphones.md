---
title: Microphones
description: Choosing and using microphones for amateur radio — hand mics, desk mics, and audio best practices
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, microphones, audio
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Microphones

The microphone is your voice's entry point into the radio. A good microphone, properly used, produces clear and intelligible audio that is pleasant to listen to and easy to copy — especially under poor conditions. A poor microphone, or a good one used incorrectly, produces muffled, distorted, or noisy audio that makes contacts harder and annoys other operators.

Most transceivers ship with a basic **hand microphone** that is perfectly functional. But upgrading the microphone or simply understanding how to get the best audio from what you have can meaningfully improve your on-air presence.

## Microphone Types

### Dynamic microphones

A **dynamic microphone** uses a diaphragm attached to a coil of wire suspended in a magnetic field. Sound waves move the diaphragm, the coil moves in the field, and a small electrical signal is generated. Dynamic microphones require no power supply (no phantom power, no batteries), are rugged, and tolerate rough handling and temperature extremes well.

Most **hand microphones** shipped with transceivers are dynamic. They have a frequency response tailored for communications intelligibility — emphasising the 300–3,000 Hz range that carries the most speech information while rolling off the deep bass and high treble that waste bandwidth and add nothing to intelligibility on SSB.

Dynamic desk microphones are also popular. The **Heil Sound GM series** (GM-4, GM-5) and classic models like the **Shure SM58** (with appropriate adapter) are widely used in amateur radio.

### Electret condenser microphones

An **electret condenser** microphone uses a permanently charged capacitor element. These are small, lightweight, and inexpensive to produce. Electret elements are found in many headset microphones, clip-on (lavalier) microphones, and some desk microphones. They require a small bias voltage (usually supplied by the radio through the microphone connector), offer wider frequency response than most dynamic microphones, and can have excellent sensitivity.

The trade-off is that electret microphones are more sensitive to handling noise and breath pops, and their wider frequency response can pick up more room noise.

### Studio / USB microphones

Some operators use **studio-quality condenser microphones** or USB microphones designed for podcasting and streaming. These can produce superb audio quality, but they require attention to setup: their wide frequency response and high sensitivity can capture room echo, keyboard clicks, fan noise, and other background sounds that degrade on-air audio. They also require an audio interface or the radio's USB audio input rather than the standard microphone connector.

Using a studio microphone effectively on amateur radio usually means applying equalisation (EQ) and compression to shape the audio for the communications channel — cutting frequencies below 200 Hz and above 2,800 Hz (for SSB), and adding mild compression to keep transmit levels consistent.

## Microphone Form Factors

### Hand microphone (hand mic)

The most common microphone in amateur radio — a small handheld unit with a PTT (push-to-talk) button built in. The standard hand mic that ships with a transceiver is adequate for general operating. Upgraded hand mics with better elements, noise-cancelling features, or more comfortable ergonomics are available from manufacturers like Heil Sound, Yaesu, Icom, and Kenwood.

### Desk microphone

A desk microphone sits on a stand and frees both hands for logging, tuning, and adjusting the radio. Desk mics often have a larger element that produces fuller audio, and many include a PTT bar or switch at the base. Some have built-in EQ or selectable frequency response modes.

Popular desk microphones include the Heil Sound Pro 7 and Pro Set Elite (which combine a desk stand with the same element used in their headsets), the Yaesu MD-200, and the Kenwood MC-60A.

### Boom microphone (headset)

A microphone mounted on a boom arm attached to a headset. This keeps the mic at a consistent distance from the mouth (important for consistent audio levels) and provides hands-free operation. Boom microphones are the standard for serious contesters and operators who spend long hours on the air. See [Headsets](/equipment/headsets) for more detail.

### Clip-on / lavalier

A small microphone clipped to a collar or lapel. Rarely used in traditional amateur radio but useful in some portable and emergency communication setups where a hand mic is inconvenient.

## Microphone Connectors

Different transceiver brands use different microphone connectors, and even within a brand, connectors may vary between model lines. Common types include:

- **8-pin round** — used by many Icom and Kenwood HF transceivers. Pin assignments differ between brands, so an Icom mic and a Kenwood mic with the same connector are not interchangeable without rewiring.
- **8-pin modular (RJ-45)** — used by Yaesu on many current models and by some other brands. Again, pin assignments are brand-specific.
- **4-pin round** — used on some mobile and handheld radios.
- **3.5 mm / 2.5 mm jacks** — used on handheld radios, typically with a combined mic/speaker jack or separate jacks.

When purchasing a third-party microphone, verify that it is wired for your specific radio. Many microphone manufacturers offer model-specific cables or adapters (for example, Heil Sound sells adapter cables for Icom, Yaesu, Kenwood, Elecraft, and FlexRadio).

## Audio Quality on SSB

SSB (single sideband) transmits only the audio frequencies within the transmitter's passband — typically **300 Hz to 2,700 Hz** (standard) or **100 Hz to 2,900 Hz** (extended, sometimes called "hi-fi SSB" in amateur circles). Everything outside this range is wasted energy or actively harmful (low-frequency rumble wastes transmitter power, and high-frequency hiss adds no intelligibility).

For the best SSB audio:

**Speak across the microphone, not into it.** Positioning the mic slightly to the side of your mouth (about 2–5 cm away, at a 45° angle) reduces breath pops and plosives (the "P" and "B" sounds that produce bursts of low-frequency noise).

**Maintain a consistent distance.** Moving closer and farther from the microphone causes fluctuating audio levels. A boom mic on a headset naturally maintains a fixed distance. If using a desk mic, discipline yourself to stay at a consistent position.

**Set the mic gain correctly.** The transceiver's mic gain control (or the ALC — automatic level control) should be set so that normal speech peaks just reach the ALC threshold without exceeding it. Over-driving the mic gain causes flat-topping (clipping the peaks of the audio waveform), which produces distorted audio and splatter on adjacent frequencies. Under-driving results in a weak, quiet signal.

**Use compression judiciously.** Many transceivers include a built-in **speech compressor** (or speech processor) that boosts the average power of the transmitted audio by reducing the dynamic range. A moderate amount of compression (6–10 dB) can make your signal noticeably more effective — louder average power without increasing peak power. Too much compression makes the audio harsh and fatiguing to listen to.

**Use EQ if available.** Some transceivers offer adjustable transmit equalisation. Boosting the midrange (around 1.5–2.5 kHz) and cutting the low end can improve intelligibility, especially with deeper voices.

## Audio Quality on FM

FM has a wider audio bandwidth than SSB (typically up to 5 kHz for narrowband FM used on VHF/UHF). Audio quality on FM is generally good with stock microphones. The main concern is **deviation** — the amount of frequency swing caused by audio input. Over-deviation (too much mic gain) causes distorted audio and may exceed the channel bandwidth. Under-deviation produces a quiet signal. Set mic gain so that your signal fills the deviation meter (if your radio has one) without exceeding the limit.

## Microphone Maintenance

Keep microphone elements clean and dry. Wind screens (foam covers) protect the element from moisture, breath, and dust. If audio quality degrades over time, check the cable for broken conductors (flex points near the connector are common failure points), clean the connector pins, and verify that the element has not been damaged by moisture or impact.

## See Also

- [Equipment Overview](/equipment/overview)
- [Headsets](/equipment/headsets)
- [HF Transceivers](/equipment/hf-transceivers)
- [VHF/UHF Transceivers](/equipment/vhf-uhf-transceivers)
- [HF Operating](/operating/hf-operating)
