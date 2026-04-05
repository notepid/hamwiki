---
title: Repeaters
description: How amateur radio repeaters work and how to use them
published: true
date: 2026-04-05T09:30:00.000Z
tags: operating, repeaters, vhf, uhf
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Repeaters

A **repeater** is an amateur radio station that receives a signal on one frequency and simultaneously retransmits it on another, usually from an elevated location with a good antenna. This extends the range of handheld and mobile radios far beyond what direct ([simplex](/operating/simplex)) communication can achieve. Repeaters are the most common way amateur operators communicate on VHF and UHF, and they form the social backbone of many local amateur radio communities.

## How a Repeater Works

A repeater system consists of a receiver, a transmitter, a controller, a duplexer (or cavity filters), and an antenna — typically located on a hilltop, tall building, or communications tower.

The basic process:

1. **You transmit** on the repeater's **input frequency**.
2. The repeater **receives** your signal.
3. The repeater **retransmits** your audio on its **output frequency**, using higher power and a better antenna position than your radio.
4. Other stations hear the repeater's retransmission.

The difference between the input and output frequencies is called the **offset** (or shift). Standard offsets vary by band and region:

| Band | Common Offset |
|------|---------------|
| 2 metres (144 MHz) | ±600 kHz |
| 70 cm (430 MHz) | ±5 MHz |
| 1.25 metres (222 MHz) | -1.6 MHz (North America) |
| 6 metres (50 MHz) | ±500 kHz or ±1 MHz |

Whether the offset is positive (you transmit higher than you receive) or negative (you transmit lower) depends on the specific repeater and where it sits in the band. Repeater directories and your radio's programming will indicate the correct offset.

## Access Tones: CTCSS and DCS

Most modern repeaters require your transmission to include a sub-audible access tone before they will retransmit your signal. This prevents interference from other signals on the same frequency.

### CTCSS (Continuous Tone-Coded Squelch System)
A low-frequency tone (67.0–254.1 Hz) transmitted below the audible range along with your voice signal. The repeater checks for this tone and only opens when the correct tone is present. Common tones include 100.0 Hz, 88.5 Hz, 103.5 Hz, and many others. You may also see CTCSS referred to as "PL" (Private Line, a Motorola trademark) or "tone squelch."

### DCS (Digital-Coded Squelch)
Similar to CTCSS but uses a low-rate digital code instead of an analog tone. DCS codes are three-digit numbers like D023, D071, or D754. Some repeaters use DCS instead of or in addition to CTCSS.

**To use a repeater, you need to know three things:** the output frequency, the offset direction, and the access tone (CTCSS or DCS). These are published in repeater directories.

## Finding Repeaters

Several resources help you find repeaters in your area:

- **RepeaterBook** (repeaterbook.com) — A community-maintained worldwide database of repeaters, searchable by location, band, and mode.
- **Local club websites** — Amateur radio clubs often maintain repeater lists for their area.
- **National repeater directories** — Organizations like the ARRL (US), RSGB (UK), RAC (Canada), and WIA (Australia) publish directories.
- **Radio programming software** — Tools like CHIRP can import repeater databases directly into your radio's memory.

## Using a Repeater

### Making a call
To call on a repeater, key up (press the PTT button) and say your callsign, optionally followed by "listening" or "monitoring":

> "VK3ABC listening"

Wait a moment. If someone is available, they will respond with their callsign. If you want to call a specific person:

> "VK3XYZ, this is VK3ABC"

### Joining a conversation
When two or more stations are talking, wait for the **courtesy tone** (a short beep or tone between transmissions) and then say your callsign. The other stations will acknowledge you and bring you into the conversation.

### The courtesy tone
Most repeaters emit a brief tone after each transmission drops. This serves two purposes: it confirms the repeater received your signal, and it provides a gap for other stations to break in. Wait for the courtesy tone before transmitting to avoid "doubling" (transmitting at the same time as another station).

### Timing out
Repeaters have a **timeout timer** (typically 1–3 minutes) that cuts off the transmitter if someone transmits continuously for too long. This prevents the repeater from being tied up by a stuck microphone or a single long-winded transmission. Keep your transmissions under the timeout limit. If you need to talk longer, release the PTT briefly to reset the timer, then continue.

## Repeater Etiquette

- **Identify yourself** with your callsign when you begin transmitting and at regular intervals as required by your national regulations.
- **Keep transmissions reasonably short** to allow others to break in.
- **Wait for the courtesy tone** before transmitting.
- **Do not "kerchunk"** the repeater (keying up without identifying). This is both poor etiquette and a violation of regulations in most countries.
- **Use simplex when possible.** If you can hear the other station directly, consider moving to a [simplex frequency](/operating/simplex) to free up the repeater for others.
- **Yield to emergency traffic.** If someone calls with an emergency, all other traffic should stop immediately.
- **Be welcoming to new operators.** Local repeaters are where most newcomers get their first taste of amateur radio.

## Types of Repeaters

### Analog FM repeaters
The most common type. They receive and retransmit standard FM voice signals. Most handheld and mobile VHF/UHF radios work with analog FM repeaters.

### Digital voice repeaters
These use digital modulation for voice communication:

- **[DMR](/digital-modes/dmr)** (Digital Mobile Radio) — Uses time-division multiple access (TDMA) to carry two simultaneous conversations on one frequency pair. Widely deployed worldwide.
- **[D-STAR](/digital-modes/dstar)** — An open standard developed by JARL (Japan Amateur Radio League). Supports voice, low-speed data, and callsign routing.
- **[System Fusion](/digital-modes/system-fusion)** — Developed by Yaesu. Supports both analog and digital modes, making it compatible with existing FM radios.
- **[M17](/digital-modes/m17)** — A newer open-source digital voice protocol that uses the Codec2 open-source voice codec.

### Linked repeater systems
Multiple repeaters connected together via the internet or dedicated radio links to create wide-area networks. Examples include IRLP (Internet Radio Linking Project), EchoLink, AllStar, and the various DMR/D-STAR/Fusion networks. These systems allow a signal received by one repeater to be rebroadcast by all connected repeaters, potentially spanning entire countries or continents.

### Crossband repeaters
Some radios can function as a personal crossband repeater, receiving on one band (e.g., 2 metres) and retransmitting on another (e.g., 70 cm). This is sometimes used by mobile operators to extend the range of a handheld radio, with the mobile radio acting as a relay.

## Programming Your Radio

Most operators store repeater frequencies in their radio's **memory channels** rather than manually entering the frequency, offset, and tone each time. There are several approaches:

- **Manual programming** — Enter each repeater's frequency, offset, and CTCSS/DCS tone through the radio's front panel. This works but is tedious for more than a few channels.
- **Computer programming** — Use software like **CHIRP** (free and open-source) with a programming cable to load dozens or hundreds of repeater channels at once. CHIRP can import data directly from RepeaterBook and other databases.
- **Code plugs** — For DMR radios, a "code plug" is a configuration file containing repeater frequencies, talkgroups, and other settings. Many local clubs and online communities share pre-built code plugs for their area.

## Setting Up a Repeater

If you are interested in operating your own repeater, there are several considerations:

- **Licensing** — In most countries, repeaters require either a special licence, a coordination with a regional frequency coordinator, or both. Check your national regulations.
- **Frequency coordination** — To avoid interference, repeater frequencies are coordinated by regional organizations. Contact your local frequency coordination body before selecting a frequency.
- **Equipment** — A repeater requires a transceiver (or separate receiver and transmitter), a controller, cavity filters or a duplexer, and a quality antenna at a good height. Commercial-grade equipment is often used.
- **Site** — Elevated locations provide the best coverage. Many repeaters are located at communications tower sites, on hilltops, or atop tall buildings.
- **Power and connectivity** — The repeater needs reliable AC power (with battery backup if possible) and, for linked systems, an internet connection.

## Where to Go Next

- [Simplex](/operating/simplex) — Direct radio-to-radio communication without a repeater
- [VHF/UHF Operating](/operating/vhf-uhf-operating) — Overview of the VHF/UHF bands
- [DMR](/digital-modes/dmr) — Digital Mobile Radio
- [D-STAR](/digital-modes/dstar) — D-STAR digital voice
- [System Fusion](/digital-modes/system-fusion) — Yaesu's digital voice system
- [QSO Basics](/operating/qso-basics) — Making contacts step by step
