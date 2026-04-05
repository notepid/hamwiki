---
title: RF Connectors
description: Common RF connectors used in amateur radio — PL-259/SO-239, N-type, BNC, SMA, and others
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, connectors, reference
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# RF Connectors

RF connectors join coaxial cables to radios, antennas, amplifiers, and test equipment. The connector you use affects signal integrity, weatherproofing, power handling, and convenience. Amateur radio uses a handful of connector families, each with its own strengths and best-use cases. Understanding which connector to use where — and how to install them properly — prevents frustrating signal loss and intermittent problems.

## UHF Connectors (PL-259 / SO-239)

Despite the name, the **UHF connector** family is used primarily at HF and VHF frequencies. It was designed in the 1930s and pre-dates the modern concept of controlled-impedance connectors. The male plug is designated **PL-259** and the female chassis receptacle is **SO-239**. This is by far the most common connector in HF amateur radio.

### Characteristics

The UHF connector has a threaded coupling ring that provides a secure mechanical connection. It is rated for roughly 500 W at HF and handles up to about 300 MHz, though its performance degrades above 100–150 MHz because it is not a constant-impedance design — the impedance varies through the connector body, causing reflections.

At HF frequencies (below 30 MHz), the impedance discontinuity is electrically insignificant, and the PL-259/SO-239 works perfectly well. At 2 m (144 MHz), it is marginal but widely used. At 70 cm (430 MHz) and above, it is a poor choice — the loss and mismatch become meaningful.

### Installation

PL-259 connectors are available in solder-on and crimp versions. The traditional method is to solder the centre pin to the cable's centre conductor and solder the body to the braid through the connector's four holes. Adapters (reducers) are available to fit PL-259 connectors on smaller cables like RG-58 and RG-8X — the reducer slides into the connector body and sizes it down to the thinner cable.

Proper soldering technique matters: the braid must make solid contact with the connector body, and excess solder should not bridge to the centre conductor. A cold or incomplete solder joint is one of the most common sources of intermittent problems and high SWR in amateur stations.

## N-Type Connectors

The **N-type connector** (named after its inventor, Paul Neill) is a weatherproof, constant-impedance 50-ohm connector rated for use up to 11 GHz (standard version) or 18 GHz (precision versions). It uses a threaded coupling mechanism and has a gasket for weather sealing.

### Characteristics

The N-type is the preferred connector for VHF, UHF, and microwave work in amateur radio. It provides a true 50-ohm impedance match through the connector, resulting in lower loss and better SWR performance than PL-259 at higher frequencies. It handles 300–500 W at UHF frequencies and is mechanically rugged.

### When to use N-type

Use N-type connectors at 70 cm (430 MHz) and above — the difference compared to PL-259 is measurable. Many operators also use N-type on 2 m (144 MHz) feedlines, especially for long runs or when maximum performance is needed. Most commercial VHF/UHF base station antennas and repeater equipment use N-type connectors. Hardline cable terminations often use N-type as well.

### Installation

N-type connectors are available in solder, clamp, and crimp versions. Crimp connectors (using proper crimp dies for each cable type) are fast and reliable. The connector must be assembled carefully — the centre pin position is critical. A centre pin that protrudes too far or not far enough will cause a poor connection or damage the mating connector.

## BNC Connectors

The **BNC connector** (Bayonet Neill-Concelman) is a compact, quick-connect 50-ohm connector using a bayonet locking mechanism — push and twist to connect, twist and pull to disconnect. BNC is rated to about 4 GHz and handles modest power levels (up to 80–100 W at HF).

### Characteristics

BNC connectors are convenient for test equipment, low-power handheld antennas, receiver connections, and laboratory use. Their bayonet coupling is faster than threaded connectors, which is why they are standard on oscilloscopes, signal generators, and many test instruments.

### When to use BNC

BNC is common on VHF/UHF handheld radios (some models), scanners, SDR receivers, and test equipment. It is not suitable for high-power transmitting feedlines but is perfectly adequate for receive-only connections and QRP work.

### BNC adapters

BNC-to-PL-259 and BNC-to-SMA adapters are widely available and useful for connecting test equipment to station gear. Every well-equipped shack should have a few on hand.

## SMA Connectors

The **SMA connector** (SubMiniature version A) is a small, threaded 50-ohm connector rated to 18 GHz or higher. It is used extensively in modern electronics, SDR hardware, and compact amateur equipment.

### Characteristics

SMA connectors are physically small (the coupling nut is about 8 mm across) and provide excellent RF performance at high frequencies. They handle limited power (a few watts is typical for the smaller cable versions) and are somewhat fragile compared to N-type or PL-259. The threads are fine and can be cross-threaded easily — always start threading by hand before using a wrench.

### When to use SMA

SMA is the standard connector on most SDR dongles (RTL-SDR, HackRF, SDRPlay), GPS antennas, WiFi equipment, and some handheld radios (the Baofeng UV-5R uses an SMA-Female on the radio body). Many VNA instruments (NanoVNA, LiteVNA) use SMA connectors. For high-frequency and microwave amateur work (1296 MHz, 2.3 GHz, and above), SMA is commonly used.

### RP-SMA (Reverse Polarity SMA)

A variant where the gender of the centre pin is reversed from standard SMA. RP-SMA is common on WiFi equipment and some commercial products. It is physically compatible with SMA but the centre pins will not mate. Adapters are available, but be aware of the distinction when purchasing cables and adapters.

## Other Connector Types

### F-Type

A 75-ohm push-on or threaded connector standard on television coax (RG-6). Not commonly used in amateur radio for transmitting, but sometimes encountered on receive-only TV antenna feeds or FM broadcast reception setups.

### 7/16 DIN

A large, high-power 50-ohm connector rated to 7.5 GHz, used in commercial telecommunications. Some high-power amateur installations and repeater sites use 7/16 DIN connectors. They handle several kilowatts and are waterproof.

### QMA

A quick-connect version of SMA, sometimes used in commercial wireless infrastructure. Rare in amateur radio but increasingly appearing on some modern equipment.

### Binding Posts and Banana Jacks

Not RF connectors per se, but found on some older equipment and test instruments. Not suitable for RF feedlines but used for DC power, audio connections, and antenna terminals on some receivers and transmitters.

## Connector Comparison

| Connector | Impedance | Max Frequency | Power (HF) | Coupling | Weatherproof |
|-----------|-----------|---------------|-------------|----------|--------------|
| PL-259/SO-239 | Not constant | ~300 MHz | 500 W+ | Threaded | No (without sealing) |
| N-Type | 50 ohm | 11–18 GHz | 300–500 W | Threaded | Yes (gasketed) |
| BNC | 50 ohm | ~4 GHz | ~100 W | Bayonet | No |
| SMA | 50 ohm | 18+ GHz | ~10 W (small cable) | Threaded | No |
| 7/16 DIN | 50 ohm | 7.5 GHz | Several kW | Threaded | Yes |

## Adapters

Adapters convert between connector types (e.g., PL-259 to BNC, N to SMA). While adapters are convenient, every adapter introduces a small amount of loss and a potential point of failure. Use adapters for test setups and temporary connections, but for permanent installations, install the correct connector directly on the cable.

Common useful adapters to keep in the shack: PL-259 to BNC, BNC to SMA, N to PL-259, N to SMA, and barrel connectors (same type on both ends) for joining two cables.

## Installation Best Practices

**Use connectors designed for your cable type.** A PL-259 designed for RG-213 will not crimp or solder properly on RG-58 without a reducer. Crimp connectors are cable-specific — the crimp die must match both the connector and the cable.

**Prepare the cable carefully.** Strip the jacket, braid, and dielectric to the exact dimensions specified by the connector manufacturer. Use a sharp blade (a coax stripping tool makes this much easier) and avoid nicking the centre conductor or cutting braid strands.

**Solder with adequate heat.** A cold solder joint (dull, grainy, blobby) is a common source of high resistance and intermittent connections. Use a soldering iron or gun with enough thermal mass to heat the connector body quickly — a small pencil iron is usually insufficient for PL-259 connectors.

**Crimp with the correct tool.** Proper crimp tools (not pliers) produce a gas-tight mechanical joint that is as reliable as solder and faster to install. Use the die specified for your connector and cable combination.

**Weatherproof outdoor connectors.** Any connector exposed to weather should be sealed with self-amalgamating tape (such as 3M 2228), coax seal putty, or heat-shrink tubing with adhesive lining. Water inside a connector corrodes the contacts and dramatically increases loss. See [Coaxial Cable](/equipment/coaxial-cable) for more installation guidance.

**Inspect and maintain.** Periodically check connectors for corrosion (green or white deposits), loose coupling, and physical damage. A connector that worked fine when installed can degrade over time from vibration, UV exposure, or water ingress.

## See Also

- [Equipment Overview](/equipment/overview)
- [Coaxial Cable](/equipment/coaxial-cable)
- [Test Equipment](/equipment/test-equipment)
- [Filters](/equipment/filters)
- [Antenna Tuners](/equipment/antenna-tuners)
