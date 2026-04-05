---
title: Coaxial Cable
description: Types of coaxial cable and their properties for amateur radio use — RG-58, RG-8X, RG-213, LMR-400, and hardline
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, coax, feedline
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Coaxial Cable

**Coaxial cable** (coax) is the most common type of feedline used to connect an amateur radio transceiver to its antenna. It consists of a central conductor surrounded by a dielectric insulator, a metallic shield (braid, foil, or both), and an outer protective jacket. This concentric structure confines the RF fields between the inner and outer conductors, keeping the feedline from radiating and preventing external signals from coupling into it.

Choosing the right coax for your station involves balancing loss, power handling, flexibility, cost, and connector compatibility. Using an inappropriate cable — particularly one with excessive loss at your operating frequency — is one of the most common and easily avoidable mistakes in station building.

## How Coax Works

RF energy travels in the space between the centre conductor and the shield (the dielectric). The characteristic impedance of the cable is determined by the ratio of the conductor diameters and the dielectric constant of the insulating material. Nearly all amateur coaxial cable has a characteristic impedance of **50 ohms**, matching the standard impedance of amateur transceivers and most antennas.

75-ohm cable (such as RG-6 and RG-11, used in television) is occasionally used in amateur applications, particularly for receive-only antennas, specific matching schemes, and feedlines where a quarter-wave transformer is used for impedance matching.

## Key Specifications

### Loss (attenuation)

Loss is the most critical specification for most amateurs. It measures how much of the transmitter's power is absorbed by the cable and converted to heat before reaching the antenna. Loss increases with frequency and cable length, and is specified in **decibels per unit length** (dB per 100 ft or dB per 100 m) at a given frequency.

As a rule of thumb: every 3 dB of loss means half of your power is lost in the cable. A 6 dB loss means only 25% of your power reaches the antenna — the rest becomes heat. At HF frequencies (1.8–30 MHz), losses in moderate cable runs are manageable with most common cable types. At VHF (144 MHz) and especially UHF (430 MHz), loss climbs sharply and cable selection becomes critical.

### Power handling

The maximum power a cable can handle is limited by heating (which degrades the dielectric) and voltage breakdown (which can arc through the dielectric). Power ratings are specified for a given frequency at matched conditions (1:1 SWR). Under mismatched conditions, voltage peaks on the cable are higher, reducing the safe power rating.

### Velocity factor

The velocity factor is the speed of the signal in the cable relative to the speed of light in free space. Most solid-dielectric cables have a velocity factor around 0.66 (66%), while foam-dielectric cables are around 0.80–0.85. This matters when cutting cables to specific electrical lengths — for example, for phasing harnesses or quarter-wave matching sections.

### Shielding effectiveness

The quality of the shield determines how well the cable rejects external interference and prevents signal leakage. Single-braid cables provide good shielding for most amateur applications. Cables with braid plus foil (dual-shield) offer better shielding at UHF. **Solid-sheath** cables (hardline) provide the best shielding.

## Common Coaxial Cable Types

### RG-58

A thin, flexible 50-ohm cable about 5 mm (0.2 in) in diameter. RG-58 uses a single braid shield over a solid or stranded centre conductor with a solid polyethylene dielectric.

RG-58 is popular for short patch cables, QRP station feedlines, and temporary installations where flexibility matters more than loss. Its loss is relatively high — roughly 3.3 dB per 30 m (100 ft) at 30 MHz and 11 dB per 30 m at 146 MHz. It handles about 500 W at 30 MHz and 200 W at 146 MHz (at matched load). RG-58 is a poor choice for long runs or VHF/UHF feedlines.

### RG-8X (mini-8)

A medium-weight 50-ohm cable about 6.1 mm (0.24 in) in diameter — a good compromise between RG-58 and full-size RG-8/213. Loss is roughly 2.5 dB per 30 m at 30 MHz and 7.5 dB per 30 m at 146 MHz. RG-8X is a reasonable general-purpose choice for HF feedlines of moderate length (up to 30 m or so) and is easier to route and connectorize than thicker cables.

### RG-213

A full-size 50-ohm cable about 10.3 mm (0.4 in) in diameter with a single braid shield and solid polyethylene dielectric. RG-213 (and the military-spec equivalent RG-8/U) is the traditional workhorse feedline for HF stations. Loss is roughly 1.8 dB per 30 m at 30 MHz and 5.2 dB per 30 m at 146 MHz. It handles around 1,500 W at 30 MHz.

RG-213 is a solid, economical choice for HF feedlines. It is too lossy for long runs at UHF but works well on 2 m for moderate distances.

### LMR-400

A popular low-loss 50-ohm cable manufactured by Times Microwave, about 10.3 mm (0.4 in) in diameter — similar size to RG-213 but with significantly lower loss, thanks to a foam dielectric and an aluminium foil plus braided shield. Loss is roughly 1.3 dB per 30 m at 30 MHz and 3.9 dB per 30 m at 146 MHz. LMR-400 handles about 2,000 W at 30 MHz.

LMR-400 (and equivalents like Wireman CQ-series and Davis RF Bury-Flex) is an excellent choice for HF through UHF feedlines at moderate cost. An ultra-flex version (LMR-400-UF) is available with a stranded centre conductor for applications requiring tighter bends, at a slight increase in loss.

### LMR-600 and LMR-900

Larger low-loss cables (about 15 mm and 23 mm diameter respectively) for long runs or high-power UHF/microwave applications. LMR-600 has roughly half the loss of LMR-400. These are stiffer and harder to route, but are the right choice for long tower runs or high-power VHF/UHF stations.

### Hardline

**Hardline** or semi-rigid coax uses a solid copper or aluminium outer conductor instead of braid. It has the lowest loss and best shielding of any coaxial cable, making it the preferred choice for long tower runs, VHF/UHF/microwave feedlines, and high-power installations. Common types include 7/8-inch and 1-5/8-inch CATV hardline (often available as surplus from cable television operators).

Hardline is rigid and requires special connectors and careful installation — it cannot be bent sharply without kinking. Copper hardline can be soldered; aluminium hardline requires mechanical connectors. Many amateurs acquire surplus CATV hardline for tower feedlines, which is an excellent and economical low-loss option.

## Loss Comparison Table

Approximate loss in dB per 30 m (100 ft) at matched load:

| Cable Type | 3.5 MHz | 14 MHz | 30 MHz | 50 MHz | 146 MHz | 440 MHz |
|------------|---------|--------|--------|--------|---------|---------|
| RG-58 | 1.1 | 2.0 | 3.3 | 4.1 | 7.4 | 12.8 |
| RG-8X | 0.8 | 1.5 | 2.5 | 3.2 | 5.6 | 10.0 |
| RG-213 | 0.6 | 1.1 | 1.8 | 2.3 | 4.1 | 7.2 |
| LMR-400 | 0.4 | 0.8 | 1.3 | 1.6 | 2.7 | 4.8 |
| LMR-600 | 0.3 | 0.5 | 0.8 | 1.1 | 1.8 | 3.2 |
| 7/8" Hardline | 0.1 | 0.3 | 0.4 | 0.5 | 0.9 | 1.5 |

*Values are typical and vary between manufacturers. Always consult the manufacturer's published specifications for exact loss figures.*

## The Effect of SWR on Loss

Feedline loss increases when the SWR is higher than 1:1. The additional loss due to mismatch is called **mismatch loss** and can be significant when the cable itself already has high loss. The practical effect is that a high-SWR antenna connected by a low-loss cable (like LMR-400) will deliver more power to the antenna than the same antenna connected by a lossy cable (like RG-58) — the lossy cable absorbs more of the reflected power bouncing back and forth.

This is one reason why many operators observe that lossy cables appear to "improve" SWR readings at the shack end of the cable — the cable absorbs the reflected power, making the SWR look lower at the transmitter. The SWR at the antenna has not improved; you are simply losing more power.

## Choosing the Right Cable

**For HF stations (up to 30 MHz):** RG-213 or LMR-400 are the standard choices. For cable runs under 15 m with 100 W or less, RG-8X is acceptable. RG-58 should be reserved for very short patch cables.

**For VHF (144 MHz):** LMR-400 is the minimum for runs over 15 m. Hardline or LMR-600 for long tower runs.

**For UHF (430 MHz) and above:** LMR-400 for short runs, LMR-600 or hardline for anything longer. Cable loss is the dominant factor at UHF and microwave frequencies.

**For portable operation:** RG-8X or LMR-240 offer a good balance of flexibility, weight, and loss for temporary field deployments.

## Installation Tips

**Avoid sharp bends.** Every coax has a minimum bend radius — bending tighter can deform the dielectric, change the impedance, and increase loss. The minimum bend radius is typically 5–10 times the cable diameter.

**Waterproof outdoor connections.** Water in a connector or cable jacket is the most common cause of coax failure. Use self-amalgamating tape (such as 3M 2228 or Scotch 23), followed by electrical tape for UV protection, on all outdoor connectors. Alternatively, use weatherproof boots designed for the connector type. Seal the cable entry point where it enters the building.

**Support the cable properly.** Cable hanging from its own weight puts stress on connectors. Use cable ties, standoffs, or messenger wire to support long vertical runs up towers.

**Ground the shield.** At minimum, ground the coax shield where it enters the building as part of your lightning protection plan. A properly installed bulkhead connector with a ground block provides both a ground point and a clean entry through the building wall.

**Use quality cable.** There is significant variation in no-name coax from online marketplaces. Stick with known brands (Times Microwave, Belden, Davis RF, Wireman) or at least verify the cable's specifications with a VNA or antenna analyser before committing to a permanent installation.

## See Also

- [Equipment Overview](/equipment/overview)
- [RF Connectors](/equipment/connectors)
- [Antenna Tuners](/equipment/antenna-tuners)
- [Test Equipment](/equipment/test-equipment)
- [Filters](/equipment/filters)
