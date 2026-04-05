---
title: Power Supplies
description: Choosing and using power supplies for your amateur radio station — AC/DC supplies, batteries, and solar
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, power, power-supply
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Power Supplies

Every amateur radio station needs a reliable source of power. Most amateur transceivers are designed to operate on **13.8 V DC** — a standard that originated from the nominal voltage of a vehicle electrical system with the engine running. A home station needs a power supply that converts mains AC to regulated 13.8 V DC. For portable and emergency operation, batteries and solar panels provide off-grid power.

A poorly chosen or inadequate power supply can cause voltage drops during transmit (reducing output power), introduce noise into the receiver (degrading sensitivity), or simply fail under load. Getting the power supply right is one of the most important and least glamorous parts of building a station.

## AC-to-DC Power Supplies

### Linear (analog) power supplies

A **linear power supply** uses a large transformer to step down mains voltage, followed by rectifier diodes, filter capacitors, and a series-pass voltage regulator to produce a clean, stable DC output.

**Advantages:** Extremely clean output — very low ripple and electrical noise. This makes linear supplies the preferred choice for sensitive receivers and weak-signal work where even small amounts of power supply noise can mask weak signals.

**Disadvantages:** Heavy and bulky due to the large transformer and heatsink. Less energy-efficient than switching supplies — typically 40–60% efficient, meaning a significant portion of the input power becomes heat. A 30-amp linear supply may weigh 15–25 kg (30–55 lbs).

Popular linear supplies include the Astron RS-35M (35 A), Astron RS-50M (50 A), and similar models. Astron linear supplies have a reputation for reliability and longevity in amateur service.

### Switching (switch-mode) power supplies

A **switching power supply** (SMPS) converts mains AC to DC using high-frequency switching circuits. The incoming AC is rectified directly, then chopped at high frequency (typically 50–200 kHz) by transistor switches, passed through a small high-frequency transformer, rectified again, and regulated by a feedback loop controlling the switching duty cycle.

**Advantages:** Much lighter and more compact than linear supplies of the same rating — a 30-amp switching supply may weigh only 2–4 kg. More energy-efficient (typically 80–90%), generating less heat.

**Disadvantages:** The high-frequency switching can generate radio-frequency interference (RFI) that appears as noise in the receiver, particularly on HF. The quality of RFI suppression varies significantly between manufacturers and models. Cheap switching supplies can be very noisy; well-designed amateur-grade switching supplies include effective filtering and shielding.

Popular switching supplies for amateur use include the Samlex SEC-1235 (30 A), MFJ-4035MV (35 A), Powerwerx SS-30DV (30 A), and various models from MeanWell (a major OEM supplier whose units are rebranded by several amateur radio vendors).

### Choosing between linear and switching

For most operators, a **quality switching supply** designed for amateur radio service works well and offers significant weight and size savings. If you operate primarily on HF with a focus on weak-signal work, CW, or are particularly sensitive to noise, a **linear supply** may be worth the extra weight and cost for its inherently cleaner output. If you notice noise from a switching supply, try adding ferrite chokes to the DC output cables and verifying the supply is properly grounded.

## Sizing Your Power Supply

### Current rating

The power supply must be able to deliver enough current for your transceiver's peak demand — which occurs during transmit at full power. A typical 100 W HF transceiver draws **20–23 amps** on transmit. Add margin for accessories (antenna tuner, desk lamp, cooling fan, computer peripherals), and a **25–30 amp supply** is a good baseline for a single-radio HF station.

If you run a VHF/UHF mobile as a base station (typically drawing 10–15 A), a **20-amp supply** is usually sufficient.

For a station with multiple radios or an amplifier requiring DC power, add up the peak draws and select a supply with at least 10–20% headroom above the total.

### Voltage regulation

The supply should hold **13.8 V ± 0.5 V** under load. A supply that sags to 12 V or below under transmit load will reduce the transceiver's output power and may trigger low-voltage protection circuits. Check that the supply's voltage regulation specification guarantees adequate voltage at your expected load.

### Duty cycle

Some supplies are rated for **continuous** current and **intermittent (ICS)** current. The ICS rating is for short bursts (like SSB voice transmission, which is intermittent). For digital modes like FT8, RTTY, or other high-duty-cycle transmissions, use the **continuous** rating. A supply rated 30 A ICS may only be rated for 25 A continuous.

## Batteries

Batteries provide power for portable operation, mobile stations, and emergency backup when mains power fails.

### Lead-acid batteries

Traditional **sealed lead-acid** (SLA) or AGM (absorbed glass mat) batteries are affordable and widely available. A 12 V, 35 Ah AGM battery can power a 100 W HF transceiver for several hours of mixed receive/transmit operation. Lead-acid batteries are heavy (roughly 10 kg for a 35 Ah unit) and should not be discharged below about 50% of capacity to preserve battery life.

Automotive starting batteries are designed for brief high-current bursts (cranking an engine) and are poor choices for radio use. **Deep-cycle** batteries — designed to be repeatedly discharged and recharged — are much more suitable.

### Lithium iron phosphate (LiFePO4)

**LiFePO4** batteries have become the preferred portable power source for amateur radio. Their nominal voltage is **12.8 V** (four cells in series at 3.2 V each), which is close enough to 13.8 V for most transceivers (output power may be slightly reduced). Key advantages include roughly one-third the weight of an equivalent lead-acid battery, flat discharge curve (voltage stays relatively constant until the battery is nearly depleted), long cycle life (2,000+ charge/discharge cycles), wide operating temperature range, and inherent safety (LiFePO4 chemistry is resistant to thermal runaway).

Popular LiFePO4 options for amateur radio include the Bioenno Power BLF series (widely used in the amateur community), Dakota Lithium, and various units from EcoFlow, Jackery, and other portable power station manufacturers.

A **20 Ah LiFePO4 battery** weighing about 2.5 kg can power a QRP transceiver for a full day of SOTA or POTA activations, or a 100 W transceiver for several hours of moderate use.

### Lithium-ion (Li-ion) and lithium polymer (LiPo)

Li-ion and LiPo batteries offer high energy density and are used in some portable power stations and as internal batteries in radios like the Icom IC-705. Their nominal voltage per cell (3.7 V) does not align as neatly with 12 V radio standards as LiFePO4, so they are typically used with a built-in voltage regulator or in pre-packaged portable power stations.

### Battery safety

All lithium batteries require proper charging — use a charger designed for the specific battery chemistry. Overcharging, over-discharging, short circuits, and physical damage can cause dangerous failures. LiFePO4 is the safest lithium chemistry, but care is still needed. Lead-acid batteries produce hydrogen gas during charging and should be charged in a ventilated area.

## Solar Power

Solar panels paired with a charge controller and battery provide indefinitely sustainable power for field and emergency stations. A practical portable solar setup for amateur radio might include a 50–100 W folding solar panel, a solar charge controller (PWM or MPPT), a LiFePO4 battery as a buffer, and the transceiver drawing from the battery.

**MPPT (Maximum Power Point Tracking)** charge controllers are more efficient than simpler PWM controllers, extracting more energy from the panel especially in suboptimal conditions (partial shade, low sun angle). For a small portable setup, even a basic PWM controller works fine.

Solar power is inherently variable — clouds, time of day, and panel orientation all affect output. The battery acts as a buffer, storing energy during good conditions and supplying the radio when solar output drops. For serious field or emergency use, size the battery to carry the station through at least a night of operation without solar input.

## Powering Your Station from a Vehicle

Running a radio from a vehicle's 12 V system is straightforward but requires attention to wiring. Run power cables directly from the battery (with appropriate fuses at both ends), not through the accessory socket (cigarette lighter). Use heavy gauge wire (10–12 AWG for runs up to a few metres) to minimise voltage drop. Install **fuses or circuit breakers** at the battery end of the run to protect against shorts.

Engine noise (alternator whine, ignition pulses) can enter the radio through the power lines. Ferrite chokes on the power cable, a good chassis ground bond, and routing power cables away from ignition wiring help suppress this interference.

## Connectors and Wiring

Most transceivers use **Anderson Powerpole** connectors or bare wire with ring terminals. Anderson Powerpoles have become a de facto standard in amateur radio — they are genderless (the same connector can be either polarity), handle high current, and are easy to assemble with a crimping tool. The **ARES/RACES standard** specifies red on the left (positive) and black on the right (negative) when looking at the mating face with the roll-out tabs on top.

**Wire gauge matters.** Under-sized wire causes voltage drop, which reduces transmitter power and can generate heat. For a 30-amp station load:

| One-Way Distance | Minimum Wire Gauge |
|------------------|--------------------|
| Up to 1 m (3 ft) | 12 AWG |
| Up to 3 m (10 ft) | 10 AWG |
| Up to 6 m (20 ft) | 8 AWG |

Always use stranded copper wire for flexibility, and crimp (rather than solder) terminals for connections that may experience vibration.

## Grounding

A station ground serves two purposes: **safety** (providing a fault path to earth) and **noise reduction** (providing a low-impedance path for RF currents and stray noise).

Connect the power supply chassis, the transceiver chassis, and any other equipment to a common ground bus. Bond this bus to an earth ground (a ground rod, cold water pipe, or building grounding system). Use short, heavy ground straps (flat braid is better than round wire at RF frequencies) and avoid creating ground loops by ensuring a single-point ground topology.

## See Also

- [Equipment Overview](/equipment/overview)
- [HF Transceivers](/equipment/hf-transceivers)
- [Amplifiers](/equipment/amplifiers)
- [Emergency Communications](/emergency-communications/overview)
- [Portable Operating](/operating/portable-operating)
