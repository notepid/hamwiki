---
title: Emergency Nets
description: How emergency communication nets are organized, operated, and managed — net control, directed nets, message handling, and best practices
published: true
date: 2026-04-05T09:30:00.000Z
tags: emergency, nets, net-control, operating, emcomm
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Emergency Nets

An emergency net is a structured, on-air meeting of amateur radio operators organized to support communication during an emergency, disaster, or public service event. Unlike casual on-air conversations, an emergency net operates under strict discipline with defined roles, procedures, and protocols designed to move critical information efficiently and accurately.

Emergency nets are the backbone of amateur radio emergency communication. When [ARES](/emergency-communications/ares), [RACES](/emergency-communications/races), or similar organizations activate, the first step is almost always establishing a net on a designated frequency.

## Types of emergency nets

### Tactical nets
Tactical nets handle real-time operational communication within a specific area or function. They are the most common type of emergency net and typically operate on VHF/UHF repeaters or simplex frequencies.

Characteristics of tactical nets:
- Communication is immediate and conversational (within net discipline)
- Stations identify by location or function rather than callsign alone (e.g., "Shelter 3," "EOC," "Red Cross HQ")
- Messages are generally informal — spoken rather than written
- Used for coordination, situational awareness, and resource requests
- Typically cover a city, county, or specific operational area

### Formal traffic nets
Traffic nets handle formal written messages (radiograms or ICS-213 forms) that must be transmitted word-for-word. These nets move slower than tactical nets because accuracy is paramount.

Characteristics:
- Messages are read exactly as written — no paraphrasing
- The receiving station reads the message back for verification
- Standard message formats are used (ARRL radiogram, ICS-213)
- Used for health-and-welfare messages, resource orders, situation reports, and other official communications
- May operate on HF for long-distance relay

### Resource nets
Resource nets manage personnel and equipment deployment. During large activations, a separate net may be established to track operator availability, assign personnel to locations, and manage logistics without tying up the tactical net.

### Liaison nets
Liaison nets connect different operational levels — for example, linking county-level nets to the state-level emergency management network, or connecting multiple tactical nets through a central hub. These typically operate on HF or digital modes.

### SKYWARN nets
[SKYWARN](/emergency-communications/skywarn) nets are specialized weather-reporting nets activated during severe weather events. They follow the general directed net format but are specifically structured to collect and relay weather observations to the National Weather Service.

## Net control station (NCS)

The net control station is the operator who manages the net. NCS is arguably the most important role in emergency communication, and it requires skill, practice, and composure.

### NCS responsibilities

**Opening the net.** The NCS announces the net, states its purpose, identifies the frequency, and calls for check-ins.

**Managing traffic flow.** All communication on a directed net goes through or is authorized by the NCS. Stations do not talk to each other without NCS permission. This prevents chaos when many stations need to communicate.

**Prioritizing.** The NCS decides the order in which stations are heard, prioritizing emergency and priority traffic over routine messages.

**Timekeeping.** The NCS tracks how long the net has been active, calls for periodic check-ins, and manages shift changes for long-running nets.

**Record keeping.** The NCS (or an assigned logger) maintains a written log of all stations checked in, messages handled, and significant events. This log becomes part of the after-action documentation.

**Closing the net.** When the net is no longer needed, the NCS formally closes it and releases all stations.

### Qualities of a good NCS
- Clear, concise voice communication
- Ability to remain calm under pressure
- Strong organizational skills — tracking multiple stations and messages simultaneously
- Knowledge of net procedures and proper prowords
- Willingness to maintain firm but courteous control of the net
- Experience — this skill improves dramatically with practice

## Directed net procedures

During an emergency, nets operate in **directed** mode, meaning all communication is controlled by the NCS. This is fundamentally different from an open repeater where anyone can talk at any time.

### Opening the net

A typical net opening sounds like:

> "Attention all stations, this is [callsign], net control for the [County Name] Emergency Net. This net is being activated at the request of [served agency] in response to [event]. This is a directed net. All stations wishing to check in, please call net control now."

### Checking in

Stations check in by transmitting their callsign, name, location, and status:

> "[Callsign], [Name], located at [location], available for assignment."

Or, for a station already at a served agency location:

> "[Callsign], [Name], stationed at [location], operational."

The NCS acknowledges each check-in and notes it on the station log.

### Requesting to pass traffic

If a station has a message, they request permission:

> "Net control, [Callsign], I have [priority] traffic for [destination]."

Priorities follow a standard scale:
- **Emergency** — Immediate threat to life or property
- **Priority** — Important to the response, time-sensitive
- **Welfare** — Health and welfare inquiries
- **Routine** — General information, non-urgent

The NCS directs the station to pass the traffic, either to a specific receiving station or to NCS directly.

### Passing formal messages

When passing a formal written message (ICS-213 or radiogram), the procedure is:

1. NCS directs the sending and receiving stations to move to an alternate frequency if needed (to keep the main net clear)
2. The sending station reads the message clearly and slowly
3. The receiving station reads the message back
4. The sending station confirms accuracy or makes corrections
5. Both stations return to the main net and confirm the message was passed

### Standard prowords

Emergency nets use standard prowords to keep communication clear and efficient:

| Proword | Meaning |
|---------|---------|
| **Roger** | I have received and understand your last transmission |
| **Copy** | I have received and copied your message |
| **Say again** | Please repeat your last transmission |
| **Affirmative** | Yes |
| **Negative** | No |
| **Stand by** | Wait — I will respond shortly |
| **Break** | Pause in a message (used to separate sections) |
| **Break break** | I need to interrupt for emergency traffic |
| **Go ahead** | Proceed with your transmission |
| **Nothing heard** | I did not receive a response from the station called |
| **Clear** | This station is leaving the net |
| **Net clear** | The net is closed (NCS only) |

### Tactical callsigns

During emergency operations, stations are often assigned tactical callsigns based on their location or function. This makes traffic handling more intuitive — "Shelter 3" is immediately meaningful, while a callsign alone requires checking a roster.

FCC regulations in the United States require that the operator's FCC-assigned callsign be given at least every ten minutes and at the end of a communication. In practice, operators use the tactical callsign for most exchanges and append their FCC callsign periodically. Other countries have similar identification requirements.

## Digital emergency nets

While voice nets remain the primary mode for real-time emergency communication, digital modes are increasingly important:

**[Winlink](/digital-modes/winlink)** — Provides email-like message handling over radio. Particularly valuable for transmitting ICS forms, situation reports, and documents. Winlink sessions operate alongside voice nets, often on a separate frequency.

**[APRS](/digital-modes/aprs)** — Provides automatic position reporting, which helps track the location of deployed operators and resources. APRS also supports short text messaging.

**Packet radio** — Used for data transfer and bulletin board-style messaging in some emergency operations.

## Setting up an emergency net

When establishing an emergency net, several decisions must be made quickly:

**Frequency selection.** Choose a frequency appropriate to the coverage needed. Local operations typically use a VHF/UHF repeater. If the repeater is down, have a designated simplex backup frequency. Regional or long-distance nets use HF frequencies.

**Backup frequencies.** Always designate at least one backup frequency in case the primary is unusable. Document this in advance.

**Net schedule.** Determine whether the net will be continuous or periodic. During active emergencies, nets typically run continuously. As the situation stabilizes, nets may shift to scheduled check-in times.

**NCS rotation.** Plan for NCS rotation — running a net for more than two to three hours is exhausting. Designate backup NCS operators and plan shift changes.

**Logging.** Designate a logger (or have the NCS log) to maintain a record of check-ins, messages, and events. This documentation is essential for after-action reviews and may be needed for government reporting.

## Best practices

**Keep transmissions short.** Brevity is essential on a busy emergency net. Say what needs to be said and release the frequency.

**Listen before transmitting.** Wait for the NCS to direct you before speaking, unless you have emergency traffic that cannot wait.

**Speak clearly and slowly.** Under stress, people tend to talk faster. Consciously slow down, enunciate, and use the [phonetic alphabet](/getting-started/phonetic-alphabet) for critical information.

**Write it down before transmitting.** For anything beyond a brief status update, write your message before keying up. This reduces errors and keeps transmissions concise.

**Use plain language.** Avoid jargon, abbreviations, and codes that the receiving station or served agency may not understand. Emergency communication should be clear to anyone listening.

**Don't editorialize.** Report facts. "Water is approximately one metre deep at the intersection of Main and Oak" is useful. Commentary and speculation are not.

**Maintain net discipline.** This means following the NCS's direction, waiting your turn, not transmitting over other stations, and keeping non-essential communication off the net.

## Practising net operations

The best way to become proficient at emergency net operations is regular practice:

- Check into weekly ARES/RACES training nets
- Volunteer to serve as NCS during practice nets
- Participate in [Simulated Emergency Tests](/emergency-communications/emcomm-training) (SETs)
- Support [public service events](/emergency-communications/overview) that use net-style communication
- Practice formal message handling — send and receive ICS-213 messages and radiograms

## See also

- [Emergency Communications Overview](/emergency-communications/overview)
- [ARES](/emergency-communications/ares) — Amateur Radio Emergency Service
- [SKYWARN](/emergency-communications/skywarn) — Severe weather nets
- [EmComm Training](/emergency-communications/emcomm-training) — Training for net participants and NCS operators
- [Net Operations](/operating/net-operations) — General net operating practices
- [Winlink](/digital-modes/winlink) — Digital message handling
- [APRS](/digital-modes/aprs) — Automatic position reporting
- [Phonetic Alphabet](/getting-started/phonetic-alphabet) — NATO phonetic alphabet reference
