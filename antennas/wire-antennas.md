---
title: Wire Antennas
description: A survey of wire antenna designs beyond the dipole — doublets, long wires, G5RV, Windom, random wires, and other popular HF wire antennas
published: true
date: 2026-04-05T09:30:00.000Z
tags: antennas, wire, hf, doublet, g5rv, longwire
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Wire Antennas

Wire antennas are the backbone of HF amateur radio. They are inexpensive, effective, and can be installed in a vast range of locations and configurations. While the [dipole](/antennas/dipole) and [end-fed half-wave](/antennas/end-fed-half-wave) each have their own dedicated pages, this page covers the broader family of wire antenna designs — from simple random wires to time-tested classics like the G5RV and doublet.

The common thread uniting wire antennas is their construction: they are made primarily from wire (copper, copper-clad steel, or aluminium), supported by rope, insulators, and whatever structures are available — trees, masts, buildings, or purpose-built supports. They have no moving parts, require minimal maintenance, and can deliver performance that competes with far more complex (and expensive) antenna systems.

## The doublet (centre-fed wire with ladder line)

The **doublet** is a centre-fed wire antenna — essentially a [dipole](/antennas/dipole) — but instead of being fed with coax and used on a single band, it is fed with [ladder line (open-wire feedline)](/antennas/feedlines) and used with a tuner on multiple bands. This is one of the most versatile and efficient HF antenna systems available.

### How it works

A doublet does not need to be resonant on any particular band. The ladder line carries RF energy between the antenna and a tuner in the shack, and the tuner transforms whatever impedance appears at its input into the 50 ohms the radio expects. Because ladder line has extremely low loss even at high [SWR](/antennas/swr-and-matching), the power wasted in the feedline remains small across all bands.

### Sizing the doublet

A good general-purpose doublet for covering 80 through 10 metres is approximately 40 metres (130 feet) long — long enough to be at least a half wavelength on 80 metres. However, a doublet does not have to be any specific length, and shorter versions work well if you do not need the lowest bands. The key consideration is to **avoid lengths that are exact multiples of a half wavelength on multiple bands**, as this can create very high impedance at the feed point that some tuners struggle with. Common recommended lengths include approximately 40 m (132 ft), 33 m (108 ft), or 26 m (85 ft).

### Practical considerations

The main challenge with a doublet is routing the ladder line into the house and transitioning to coax for the short run to the tuner. Ladder line cannot be run through metal conduit or close to metal objects without degrading performance. A common approach is to bring the ladder line to a [1:1 balun](/antennas/baluns-and-ununs) mounted on the outside wall near the entry point, then transition to a short run of coax to the tuner. Alternatively, some operators route the ladder line directly to a balanced tuner inside the shack.

Despite the feedline routing challenges, a doublet with ladder line is hard to beat for all-around HF performance. Many experienced operators consider it the best compromise between simplicity, cost, and multi-band capability.

## Random wire antenna

The **random wire** (sometimes called a long wire, though technically these are different things) is the simplest of all antennas — a single length of wire, run out from the shack to a far support, and fed at one end. The name "random" reflects the fact that the wire is not cut to any specific resonant length.

### Feeding a random wire

Because the wire is not resonant and the impedance at the end can vary wildly across bands, a random wire **always requires a matching device**. This is typically an [unun](/antennas/baluns-and-ununs) (commonly 9:1 or 49:1) followed by an antenna tuner. Some operators use just a tuner with a built-in wire connection (many manual tuners have a "random wire" terminal).

A good **RF ground** or counterpoise is essential with a random wire because the antenna is unbalanced and the return current path must go somewhere. Without an adequate ground, the coax shield and station equipment become part of the antenna, causing RF interference in the shack.

### Performance

A random wire will get you on the air on multiple bands with minimal investment, but its performance is less predictable than a resonant or purpose-designed antenna. The radiation pattern changes with frequency, and efficiency depends on the wire length relative to the wavelength on each band. Longer is generally better — at least a quarter wavelength on the lowest band you want to use.

Certain wire lengths should be avoided because they present very high or very low impedances that are difficult for tuners to match. The traditional list of "bad" lengths includes exact multiples and half-multiples of a half wavelength on any of your target bands. In practice, getting the wire as long and as high as possible matters more than obsessing over exact length.

## The G5RV antenna

The **G5RV**, designed by Louis Varney (G5RV) in the 1940s, is one of the most well-known multi-band wire antennas. It consists of a 31.1 metre (102 foot) flat-top wire, centre-fed with a specific length of open-wire matching section, which then transitions to coax for the run to the shack.

### How it works

The G5RV was originally designed as a 3-half-wavelength antenna for 20 metres (14 MHz), where the matching section transforms the antenna impedance to approximately 50 ohms. On other bands, the matching section does not produce a 50-ohm match, and an antenna tuner is required for multi-band use.

The matching section is typically 10.36 metres (34 feet) of 300-ohm or 450-ohm ladder line. The total system — flat-top wire, matching section, and coax — works on 80 through 10 metres with a tuner, though performance varies by band.

### The G5RV in practice

The G5RV has been enormously popular for decades, largely because it offers reasonable multi-band performance in a simple, affordable package. However, it is important to understand that it is **not a magical multi-band antenna** — on most bands, it is simply a centre-fed wire that requires a tuner, similar to a doublet. The matching section provides a good match on 20 metres but not necessarily on other bands.

Some operators prefer a plain doublet fed with full-length ladder line (no coax transition in the middle) as a simpler and more flexible alternative. Others swear by the G5RV as a proven design that just works. Both approaches are valid.

### The ZS6BKW variant

The **ZS6BKW** (designed by Brian Austin, ZS6BKW) is a modified version of the G5RV with different flat-top and matching section lengths (approximately 27.5 metres / 90.2 feet of flat-top and 12.2 metres / 40.0 feet of 450-ohm matching section). These dimensions are optimised to provide a better match on more bands without a tuner, though a tuner is still useful for full band coverage.

## The Windom and off-centre fed dipole (OCF)

The **Windom** antenna, named after Loren Windom (W8GZ) who described it in 1929, was originally a half-wave wire fed with a single wire at a point about 36% from one end. The modern **off-centre fed dipole (OCF)** is a related concept — a half-wave antenna fed off-centre using a [balun or unun](/antennas/baluns-and-ununs) and coaxial cable.

The feed point impedance at approximately the one-third point is roughly 200–300 ohms, which can be matched to 50-ohm coax with a 4:1 or 6:1 balun. The advantage is that an OCF cut for 80 metres (about 40 metres / 132 feet long) can operate on multiple harmonically related bands — often 80, 40, 20, and 10 metres — with acceptable SWR on several of those bands.

The OCF is popular for multi-band operation, but it can be more sensitive to installation details than a centre-fed dipole, and common-mode current on the feedline is more of a concern due to the asymmetric feed. A good quality choke balun at the feed point is especially important.

## Long wire antennas

A **true long wire** antenna is a wire that is at least one wavelength long at the operating frequency, running in a single direction from the feed point. It differs from a "random wire" in that its length is specifically chosen to be multiple wavelengths long on the target band.

Long wires produce **directional radiation patterns** with main lobes that sharpen and point closer to the wire axis as the antenna becomes longer. A long wire of several wavelengths can provide useful gain toward its far end. This property is exploited in more advanced designs like the Beverage antenna (a receive-only long wire laid close to the ground, used for low-noise directional reception on the low bands) and the rhombic antenna (four long wires arranged in a diamond shape for high gain).

In practice, few amateur stations have enough space for a true long wire, but the term is frequently (if technically incorrectly) applied to any single long wire used as an antenna.

## Extended double Zepp (EDZ)

The **extended double Zepp** is a collinear wire antenna approximately 1.28 wavelengths long, centre-fed. It provides about 3 dB of gain over a half-wave dipole, with a narrower broadside pattern. The feed point impedance is roughly 130–140 ohms, which requires a matching solution — typically a 4:1 balun or a ladder line and tuner combination.

The EDZ is most commonly used on a single band (often 20 metres) where its gain advantage is worthwhile. It is a simple and effective way to get extra performance from a wire antenna when you have the space to accommodate the extra length.

## Inverted-L

The **inverted-L** antenna consists of a vertical section of wire going up from a feed point near the ground, transitioning to a horizontal section running along at the top. The shape forms an "L" rotated 90 degrees. The inverted-L combines properties of both vertical and horizontal antennas — it radiates with a mix of vertical and horizontal polarisation and produces a radiation pattern that is somewhat omnidirectional.

The inverted-L is particularly popular on the **160-metre and 80-metre bands**, where full-size horizontal antennas are impractically large. A quarter-wave inverted-L for 160 metres requires about 40 metres (130 feet) of wire, with as much of that as possible in the vertical section. It requires a good ground system or counterpoise, similar to a [vertical antenna](/antennas/vertical).

## Practical wire antenna tips

**Wire choice:** Stranded copper wire (12–14 AWG / 1.6–2.0 mm for permanent installations, 18–22 AWG / 0.6–1.0 mm for portable use) is the standard. Copper-clad steel is stronger for long spans but less flexible. Avoid aluminium wire for soldered connections (it cannot be easily soldered) and bare steel (high RF resistance).

**Supports:** Trees are free antenna supports, but they move in the wind. Use a pulley or a weight-and-rope arrangement to allow the antenna to move with the tree without breaking. Fibreglass masts, push-up poles, and guyed metal masts are all popular options. See [Building Antennas](/antennas/building-antennas) for construction and safety details.

**Insulators:** End insulators prevent RF current from flowing into support ropes. Ceramic egg insulators are traditional and effective. Dog-bone insulators are cheap and durable. In a pinch, a short piece of PVC pipe or even a zip-tie loop works on receive-only antennas or low power.

**Centre connectors:** Commercial centre insulators with built-in SO-239 connectors are convenient and weatherproof. Homebrew feed points work well too — use a piece of weather-resistant plastic or fibreglass board and seal all connections against moisture.

**Height:** For most HF wire antennas, getting the wire higher improves performance. Even a few extra metres of height can lower the radiation angle and improve DX capability. Prioritise height over perfect geometry.

**Stealth:** If your antenna must be invisible (due to [restrictions](/antennas/antenna-restrictions) or personal preference), thin wire is nearly invisible at a distance. Dark-coloured wire against trees and sky is very hard to spot. End-fed designs are particularly well suited to stealth installation since the feedline only connects at one end.

## Where to go next

- [Dipole Antennas](/antennas/dipole) — Detailed coverage of the half-wave dipole and its variants
- [End-Fed Half-Wave](/antennas/end-fed-half-wave) — The popular EFHW antenna for portable and stealth use
- [Feedlines](/antennas/feedlines) — Coax vs. ladder line for wire antennas
- [Baluns and Ununs](/antennas/baluns-and-ununs) — Matching and feeding wire antennas
- [Antenna Restrictions](/antennas/antenna-restrictions) — Dealing with HOAs, zoning, and landlords
- [Building Antennas](/antennas/building-antennas) — Construction safety and techniques
