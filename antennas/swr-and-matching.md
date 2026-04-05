---
title: SWR and Impedance Matching
description: Understanding standing wave ratio, impedance matching, antenna tuners, and what SWR really tells you about your antenna system
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, swr, matching, theory, tuner
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# SWR and Impedance Matching

Standing Wave Ratio (SWR) is one of the most discussed — and most misunderstood — measurements in amateur radio. New hams often worry excessively about achieving a perfect 1:1 SWR, while experienced operators know that a moderate SWR is perfectly acceptable and that the number on the SWR meter does not tell the whole story about antenna performance. This page explains what SWR actually is, what it means for your station, and how to manage impedance matching in practice.

## What is SWR?

When a transmitter sends RF energy down a feedline to an antenna, the antenna absorbs most of that energy and radiates it. But if the antenna's impedance does not perfectly match the feedline's characteristic impedance, some energy is **reflected** back toward the transmitter. The interaction between the forward-travelling wave and the reflected wave creates a pattern of voltage and current peaks and valleys along the feedline — **standing waves**.

**SWR** (or more precisely, VSWR — Voltage Standing Wave Ratio) is the ratio of the maximum voltage to the minimum voltage along the feedline:

**SWR = V_max / V_min**

A perfect match produces no reflections, no standing waves, and an SWR of **1:1**. As the mismatch increases, more power is reflected and the SWR rises. An open circuit or short circuit at the end of the feedline produces complete reflection and an infinite SWR.

## SWR and reflected power

SWR is directly related to the fraction of power reflected at the mismatch point:

| SWR | Power reflected | Power delivered to antenna |
|-----|----------------|--------------------------|
| 1.0:1 | 0% | 100% |
| 1.5:1 | 4% | 96% |
| 2.0:1 | 11% | 89% |
| 3.0:1 | 25% | 75% |
| 5.0:1 | 44% | 56% |
| 10:1 | 67% | 33% |

These numbers might suggest that SWR below about 2:1 is almost irrelevant — and for the mismatch loss alone, that is true. Only 11% of your power is reflected at 2:1 SWR, which is less than half a decibel. The more important concern is what high SWR does to **feedline losses**, which is covered below.

## The real cost: additional feedline loss

When SWR is high, the standing waves on the feedline increase the peak voltage and current. This causes additional power to be lost as heat in the feedline — on top of the feedline's normal "matched loss." The additional loss depends on both the SWR and the inherent loss of the feedline.

This is the critical insight: **high SWR is most damaging when the feedline already has significant loss.** A 3:1 SWR on a low-loss feedline (say, LMR-400 on HF) adds very little extra loss. The same 3:1 SWR on a long run of RG-58 at VHF could waste a substantial amount of power.

Conversely, if you use a very low-loss feedline like ladder line (which has inherently tiny matched loss), you can tolerate very high SWR with minimal additional loss. This is exactly why ladder line works so well for multi-band antenna systems — even though the SWR on the line may be 10:1 or higher on some bands, the actual power lost in the feedline remains small.

## What your SWR meter actually shows

Most SWR meters are installed in the shack between the radio and the feedline. It is important to understand what the meter is reading and what it is not:

**What the meter shows:** The SWR at the point where the meter is installed — typically at the radio end of the feedline.

**What the meter does not show:** The SWR at the antenna feed point. Due to feedline loss, the SWR measured at the shack end of the feedline is always lower than the actual SWR at the antenna. The lossier the feedline, the greater this difference. In extreme cases, a lossy feedline can show a low SWR at the shack simply because most of the reflected power is being absorbed as heat in the cable before it reaches the meter.

This means that a low SWR reading is not always good news. If your SWR is low because the feedline is absorbing most of the power (both forward and reflected), the antenna system is inefficient even though the meter looks reassuring.

## Measuring SWR

### SWR meters and bridges

The most common way to measure SWR is with a dedicated SWR meter (also called an SWR bridge) inserted in the feedline. These are available as standalone instruments or are built into many modern transceivers. To measure SWR, you transmit a carrier at the frequency of interest and read the SWR value.

Most modern HF transceivers include a built-in SWR meter and will display the reading on the front panel during transmission. Many also include automatic SWR protection that reduces output power when the SWR exceeds a threshold (typically around 2:1 to 3:1).

### Antenna analysers

An **antenna analyser** (such as the popular NanoVNA or similar vector network analysers) provides much more detailed information than a simple SWR meter. It can sweep across a range of frequencies, showing you the SWR curve and revealing the antenna's resonant frequency, bandwidth, and impedance (both resistance and reactance). This information is invaluable for tuning and troubleshooting antennas.

Antenna analysers operate at very low power levels and do not require you to transmit, making them safe and convenient to use during antenna adjustment.

### Interpreting SWR readings

When adjusting an antenna, you typically want to achieve the lowest SWR at your desired operating frequency. Here are some practical guidelines:

- **1.0:1 to 1.5:1** — Excellent. No action needed.
- **1.5:1 to 2.0:1** — Very good. Entirely acceptable for most purposes.
- **2.0:1 to 3.0:1** — Acceptable on HF with good feedline. Your radio may reduce power slightly. Consider matching if you want to operate in this range regularly.
- **Above 3.0:1** — Your radio's internal protection may limit power significantly. An antenna tuner will likely be needed. Investigate the cause if you expect better performance.

Remember that SWR varies across a band. An antenna that shows 1.5:1 at the centre of a band might be 2.5:1 at the edges. This is normal behaviour and the bandwidth over which SWR stays below your threshold depends on the antenna design.

## Antenna tuners

An **antenna tuner** (more accurately called a **transmatch** or **matching unit**) is a variable impedance-matching network placed between the radio and the feedline. It transforms whatever impedance appears at the shack end of the feedline into the 50 ohms the radio expects to see.

### What a tuner does — and does not do

A tuner makes the **radio** happy by presenting it with a 50-ohm load. This allows the radio to deliver its full rated power. However, the tuner does **not** change the SWR on the feedline between the tuner and the antenna. If the SWR on the feedline was 5:1 before you engaged the tuner, it is still 5:1 after. The tuner simply absorbs the mismatch at the shack end.

This means that if you have a lossy feedline with high SWR, a tuner does not solve the efficiency problem — it masks it. The feedline still wastes the same amount of power. The tuner is most effective when used with a **low-loss feedline** (such as open-wire line), where the high SWR on the line does not cause significant additional loss.

### Types of antenna tuners

**Manual tuners** have variable capacitors and inductors that the operator adjusts to find the best match. T-network and L-network designs are common. Manual tuners give the operator full control and can match a wide range of impedances.

**Automatic tuners** sense the SWR and adjust internal switching components (switched capacitors and inductors) to find a match. Most modern automatic tuners can find a match in a few seconds. Many HF transceivers include a built-in automatic tuner, though these typically handle only moderate mismatches (up to about 3:1). External automatic tuners can handle much wider ranges.

**Remote tuners** are mounted at the antenna feed point rather than in the shack. This approach is ideal because it eliminates the SWR on the feedline entirely — the tuner matches the antenna impedance directly, and the coax between the remote tuner and the radio sees a 1:1 SWR. This gives the best of both worlds: multi-band operation with minimal feedline loss.

### When do you need a tuner?

A tuner is useful in several situations:

- **Multi-band antennas** — When operating an antenna on bands where it is not resonant. A dipole cut for 40 metres can be tuned to work on 20 or 15 metres with a tuner (though the radiation pattern changes).
- **Wide-band operation** — When you want to operate across an entire band but the antenna's SWR exceeds 2:1 at the band edges.
- **Ladder-line fed systems** — A doublet or loop fed with ladder line and a tuner is one of the most versatile and efficient multi-band antenna systems. The tuner handles the widely varying impedance presented by the ladder line on different bands.
- **Non-resonant antennas** — Random wire antennas and other non-resonant designs require a tuner (and often a [9:1 or 49:1 unun](/antennas/baluns-and-ununs)) to present an acceptable impedance to the radio.

## Matching at the antenna

In addition to tuners, impedance matching can be done at the antenna itself using several techniques:

### Matching networks

An **L-network**, **gamma match**, **beta match (hairpin match)**, or **delta match** can be built into the antenna feed point to transform the antenna's impedance to 50 ohms. Yagi antennas commonly use gamma or beta matches. These are fixed-frequency matching systems — they work well over the antenna's natural bandwidth but do not adapt to different bands.

### Feed point adjustment

Some antenna impedance problems can be solved by adjusting where and how the feedline connects to the antenna:

- Moving the feed point of a dipole off-centre (creating an off-centre fed dipole or OCF) changes the feed point impedance.
- Adjusting the spacing and length of a matching section (such as a quarter-wave transformer) can match unusual impedances.
- Using a folded element increases the feed point impedance by approximately four times, which can be useful for matching specific feedline impedances.

### Practical example: quarter-wave transformer

A quarter-wave section of transmission line with the right characteristic impedance can transform one impedance to another. The relationship is:

**Z_transformer = √(Z_source × Z_load)**

For example, to match a 75-ohm antenna to a 50-ohm feedline, you would need a quarter-wave section of cable with a characteristic impedance of √(75 × 50) ≈ 61 ohms. This is close to the impedance of some 75-ohm coax types when used in parallel, or it can be approximated with specific cable configurations. This technique is commonly used to match stacked Yagi arrays and other specific antenna configurations.

## Common SWR myths

**Myth: "SWR must be 1:1 or the antenna is bad."**
Reality: An SWR below 2:1 is excellent. Even 3:1 on HF with good feedline wastes very little power. The difference between 1:1 and 1.5:1 is undetectable in practice.

**Myth: "High SWR will damage my radio."**
Reality: Modern transceivers have protective circuits that reduce power when SWR is high. Older radios with valve (tube) finals are quite tolerant of high SWR. Damage from SWR alone is rare with modern equipment, though sustained high SWR at full power can stress the radio's output stage over time.

**Myth: "An antenna tuner fixes a bad antenna."**
Reality: A tuner makes the radio happy but does not improve the antenna or reduce feedline loss. It is a tool for matching, not for making a bad system good. With low-loss feedline, however, a tuner enables excellent multi-band performance from a single antenna.

**Myth: "The SWR meter shows how much power reaches the antenna."**
Reality: The SWR meter shows the impedance match at the measurement point. A low SWR at the shack does not guarantee low feedline loss — it might just mean the feedline is absorbing everything. Conversely, a 3:1 SWR on a low-loss line wastes very little power.

**Myth: "Reflected power is lost."**
Reality: Reflected power bounces back toward the transmitter, where most of it is re-reflected and sent back toward the antenna again. The power sloshes back and forth on the line until it is either radiated or lost as heat. In a low-loss system, most of the reflected power eventually gets radiated — the main cost of high SWR is increased feedline heating, not "lost" reflected power.

## Troubleshooting SWR problems

If your SWR is higher than expected, check these common causes in order:

1. **Antenna dimensions** — Is the antenna cut to the correct length for your target frequency? Use an antenna analyser to find the actual resonant frequency and trim or extend as needed.
2. **Feedline and connectors** — Check for damaged coax, corroded connectors, or water ingress. A damaged feedline can cause SWR readings that change unpredictably.
3. **Height and surroundings** — An antenna too close to the ground, a metal roof, or other large objects will have its impedance shifted from the expected value.
4. **Balun issues** — A missing or defective [balun](/antennas/baluns-and-ununs) can cause common-mode current on the feedline, giving misleading SWR readings.
5. **Antenna analyser check** — Measure the antenna impedance at the feed point (with the shortest possible feedline) to isolate whether the issue is in the antenna or the feedline.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — Core concepts including impedance and resonance
- [Feedlines](/antennas/feedlines) — How feedline choice and loss interact with SWR
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Impedance transformation and common-mode current management
- [Building Antennas](/antennas/building-antennas) — Practical construction and tuning tips
- [Antenna Modeling](/antennas/antenna-modeling) — Predicting antenna impedance before you build
