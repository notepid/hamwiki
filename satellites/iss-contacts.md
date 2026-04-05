---
title: ISS Contacts
description: Making contact with the International Space Station — voice contacts, APRS, packet radio, and ARISS school events
published: true
date: 2026-04-05T09:30:00.000Z
tags: satellites, ISS, ARISS, space station, packet, APRS
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# ISS Contacts

The International Space Station (ISS) has carried amateur radio equipment since its earliest days of occupation. Several crew members over the years have held amateur radio licences, and the station's ham radio gear is used for casual voice contacts with operators on the ground, scheduled educational contacts with schools, packet radio digipeating, and APRS (Automatic Packet Reporting System) operations. Hearing or working the ISS is one of the most accessible and exciting space communication experiences in amateur radio.

## Amateur radio on the ISS

### ARISS — Amateur Radio on the International Space Station

ARISS (Amateur Radio on the International Space Station) is the international programme that coordinates amateur radio activities aboard the ISS. ARISS is a partnership between AMSAT, NASA, ESA, JAXA, CSA, and other space agencies. The organisation manages the radio equipment on the station, coordinates school contacts, and facilitates crew members' personal amateur radio operations.

The ISS carries amateur radio equipment in multiple modules. The radios typically operate on 2 m (144 MHz) VHF, though UHF (70 cm) capability has also been available at various times. The configuration changes depending on the equipment installed and the crew's interests.

### Crew contacts

When an ISS crew member has free time and holds an amateur radio licence (or operates under the station's own callsigns), they may make casual contacts with operators on the ground. These are unscheduled — the crew member simply turns on the radio and begins calling CQ or responding to calls. Because these opportunities depend entirely on the crew's personal time and interest, they are unpredictable. Some crew members are very active on ham radio; others rarely use it.

When a crew member is on the air, the experience is electric — operators around the world scramble to make contact during the brief window (typically 10 minutes or less) when the ISS is overhead. Given that the ISS footprint covers a very large area at any instant, dozens or hundreds of stations may be calling simultaneously.

The ISS has used several callsigns over the years, including NA1SS (US segment), RS0ISS (Russian segment), DP0ISS (Columbus module), OR4ISS, and the personal callsigns of individual crew members.

### School contacts (ARISS educational events)

One of ARISS's flagship activities is scheduling direct voice contacts between ISS crew members and students at schools and educational institutions. These events are planned months in advance and involve a school applying to ARISS, preparing curriculum-related questions, and setting up a ground station (often with help from local amateur radio clubs).

During a school contact, students take turns asking the astronaut questions — about life in space, science experiments, the view from orbit, and more — via amateur radio. The contacts typically last about 10 minutes, the length of a good overhead pass.

School contacts use either a direct approach (the school operates its own ground station) or a telebridge approach (an ARISS telebridge station in another part of the world makes the radio contact and relays audio to the school over the internet). The telebridge method allows schools without their own radio equipment to participate.

These events are often announced in advance and can be listened to by anyone with a suitable receiver, making them a great way to experience ISS ham radio even if you are not the one making the contact.

## How to hear the ISS

Listening to the ISS requires very little equipment. The station's transmitter runs about 25 watts into an omnidirectional antenna, and its VHF signals are quite strong during an overhead pass.

### Equipment for listening

- A handheld or mobile VHF radio (2 m band) or a scanner/receiver covering 145–146 MHz
- Even a rubber duck antenna on a handheld is sufficient during high-elevation passes
- An [SDR receiver](/equipment/sdr-receivers) with a simple antenna is another low-cost option

### Frequencies

The ISS voice downlink has traditionally been on **145.800 MHz** for most regions, though this can change with equipment reconfigurations. Cross-band repeater operations (when enabled) have used different frequency pairs. Always check current ARISS frequency information before attempting to listen, as the configuration evolves over time.

### Tracking the ISS

The ISS is one of the easiest objects to track because of its popularity. Dedicated ISS tracking apps, websites like Heavens-Above, and general [satellite tracking software](/satellites/satellite-tracking) all provide pass predictions. The ISS orbits at approximately 400 km (250 miles) altitude with an orbital period of about 92 minutes and an inclination of 51.6°, meaning it can be seen from locations between roughly 52°N and 52°S latitude (and somewhat beyond at lower elevations).

Passes where the ISS reaches above 30° elevation provide the best signal strength and the longest contact windows (up to about 10 minutes). You can often get 3–6 usable passes per day, though they cluster in groups separated by longer gaps as the orbital ground track shifts.

## Making voice contact with the ISS

### What you need

- A valid amateur radio licence for the bands and modes being used
- A VHF transceiver (handheld with 5 watts is sufficient) covering the 2 m band
- The current ISS uplink and downlink frequencies
- Patience — crew contacts happen on the crew's schedule, not yours

### Tips for success

The biggest challenge is timing. You need to be on the right frequency at the right time when a crew member happens to be operating. Some strategies:

- **Monitor ARISS and AMSAT news** for announcements that a crew member will be active. Sometimes crew members announce their operating plans via social media or through ARISS channels.
- **Listen during every pass** when you can. Even if no crew member is operating voice, you may hear packet or APRS activity, which confirms the radio is powered on.
- **Be ready for fast contacts.** When a crew member is active, many stations will be calling. Keep your exchange brief — callsign, location, and a signal report is usually all there is time for.
- **Use a directional antenna** if you have one. While a handheld with a whip antenna can reach the ISS, an Arrow or Elk antenna pointed at the station gives you a stronger signal in both directions and can make the difference in a pileup.

### Calling procedure

When you hear the ISS crew member calling CQ or working stations, wait for a brief gap and call with your callsign only — clearly and once. If they come back to you, give your name and location (grid square). Keep it short and friendly. The crew member may exchange a few words or simply give a signal report and move to the next caller.

## ISS packet radio and APRS

### Packet digipeater

The ISS periodically operates a packet radio digipeater on VHF. This digipeater receives packet radio signals from the ground, retransmits them, and allows two ground stations within the ISS footprint to exchange data using the station as a relay. The digipeater uses AX.25 protocol at 1200 baud.

When the digipeater is active, you can send short packet messages through the ISS using a VHF radio with a TNC (terminal node controller) or a software TNC. Because the ISS footprint at any moment covers a large area, you can make packet contacts over distances of several thousand kilometres.

### APRS digipeater

The ISS has also operated as an APRS digipeater, relaying APRS position reports and messages. By transmitting an APRS packet on the ISS uplink frequency with the ISS as the digipeater path, your position and a short message are retransmitted by the station and can be received by ground stations across a wide area.

APRS through the ISS is popular because it can be done with relatively simple equipment (a VHF radio and a small TNC or a radio with built-in APRS capability). Seeing your APRS packet show up on the ARISS website or on aprs.fi with an ISS digi path is a satisfying achievement.

### Slow Scan Television (SSTV)

The ISS periodically transmits Slow Scan Television (SSTV) images — typically during special events, commemorations, or educational activities. These transmissions send images over the amateur radio frequencies that can be decoded by anyone with a VHF receiver and SSTV decoding software (available as free smartphone apps or desktop programs).

SSTV events are announced in advance by ARISS and are a fun activity that requires only the ability to receive the ISS signal — no licence is needed to listen and decode.

## ISS contact confirmations and awards

Contacts with the ISS (both voice and digital) count for various amateur radio awards. ARISS issues special QSL cards for confirmed contacts. The ISS crew may also use special event callsigns during certain commemorations.

Contacts with the ISS count toward the AMSAT Satellite VUCC (VHF/UHF Century Club) award and may count toward other awards depending on the specific rules of each programme.

## Safety and legal notes

Making contact with the ISS follows the same rules as any other amateur radio contact — you need a valid licence for the frequency and mode in use. In most countries, Technician-class or Foundation-level licences (the entry-level licence) include 2 m VHF privileges, so ISS contacts are available to newly licensed operators.

Transmitting on ISS frequencies when the station is not overhead or when no amateur radio activity is taking place serves no purpose and can cause interference to other operators. Always confirm that the ISS is actually above your horizon before transmitting.

## See also

- [Amateur Radio Satellites](/satellites/amateur-satellites) — Other satellites you can work
- [Satellite Tracking](/satellites/satellite-tracking) — Tools for predicting ISS passes
- [Satellite Station Equipment](/satellites/satellite-equipment) — Gear for satellite and ISS contacts
- [APRS](/digital-modes/aprs) — Automatic Packet Reporting System
- [Satellites & Space Overview](/satellites/overview) — Category overview
