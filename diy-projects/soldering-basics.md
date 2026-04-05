---
title: Soldering Basics
description: A practical guide to soldering for amateur radio projects — equipment, techniques, safety, and troubleshooting
published: true
date: 2026-04-05T09:30:00.000Z
tags: diy, soldering, tools, skills, homebrew
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Soldering Basics

Soldering is the most fundamental skill in amateur radio construction. Nearly every kit, homebrew project, antenna connector, and repair job involves joining components together with molten solder. The good news is that soldering is not difficult to learn — with a modest investment in equipment and a little practice, most people can produce reliable solder joints within their first session.

This page covers the equipment you need, the techniques that produce good joints, common mistakes and how to avoid them, and the safety precautions that should become second nature.

## What is soldering?

Soldering is the process of joining two metal surfaces by melting a filler metal (solder) that flows between them, creating an electrical and mechanical connection when it cools and solidifies. In electronics soldering, the metals being joined are typically component leads (made of copper, tinned copper, or other alloys) and the copper pads or traces on a printed circuit board (PCB).

The key distinction between soldering and welding is temperature. Soldering occurs at relatively low temperatures — typically between 200°C and 400°C (390°F to 750°F) — and the base metals being joined do not melt. Only the solder melts and flows. This makes soldering well-suited to delicate electronic components that would be destroyed by higher temperatures.

## Equipment

### The soldering iron

The soldering iron is your primary tool. For amateur radio work, a temperature-controlled iron with interchangeable tips is the best investment you can make. Look for these features:

**Temperature control.** A station with adjustable temperature (usually 200–450°C / 390–840°F) lets you match the heat to the job. Through-hole components on standard PCBs typically work well at 315–370°C (600–700°F). Larger connections like antenna connectors or ground lugs may need higher settings. A fixed-temperature iron can work, but you have less control and may damage heat-sensitive components or struggle with larger joints.

**Wattage.** For general electronics work, 40 to 75 watts is a good range. Higher wattage does not mean higher temperature — it means the iron can deliver heat faster and recover temperature more quickly after making a joint. Irons below 25 watts often struggle to heat joints adequately, leading to cold solder joints.

**Tips.** A chisel tip (sometimes called a screwdriver tip) of about 1.5–2.5 mm (1/16" to 3/32") width is the best general-purpose choice. The flat face of the chisel transfers heat efficiently to both the component lead and the PCB pad simultaneously. Fine conical tips are useful for very small work but transfer heat more slowly. Keep spare tips on hand — they wear out over time.

### Solder

Electronics solder is a metal alloy in wire form, usually with a flux core. The two main types are:

**Leaded solder** (typically 60% tin / 40% lead, or the eutectic 63/37 blend) has been the standard for decades. It melts at a lower temperature (around 183°C / 361°F for 63/37), flows easily, and produces shiny, reliable joints. The 63/37 eutectic alloy is particularly good because it transitions directly from solid to liquid with no "pasty" intermediate phase, making it more forgiving for beginners.

**Lead-free solder** (typically tin/copper or tin/silver/copper alloys) melts at higher temperatures (around 217–227°C / 423–441°F) and requires slightly more skill to use well. It is mandated for commercial electronics in many countries under RoHS (Restriction of Hazardous Substances) regulations, but hobbyists are generally not required to use it. Lead-free joints often have a duller appearance than leaded joints, which is normal and does not indicate a problem.

For most amateur radio work, 0.8 mm (0.031") diameter solder with rosin flux core is a good all-around choice. Thinner solder (0.5 mm / 0.020") is helpful for fine-pitch work, while thicker solder (1.0–1.5 mm / 0.040"–0.060") is useful for larger connections like coaxial connectors.

### Flux

Flux is a chemical agent that cleans metal surfaces and promotes solder flow. Rosin-core solder has flux built into its centre, which is sufficient for most through-hole electronics work. Additional flux — applied as a paste, gel, or liquid — is helpful when soldering surface-mount components, reworking or desoldering joints, working with oxidised or tarnished surfaces, or soldering coaxial connectors where the joint area is large.

Use only flux intended for electronics (rosin-based or "no-clean" formulations). Never use plumbing flux (acid-core) on electronics — it is corrosive and will destroy circuits over time.

### Other essential tools

**Solder wick (desoldering braid).** A flat copper braid that absorbs molten solder through capillary action. Essential for removing excess solder or correcting mistakes.

**Solder sucker (desoldering pump).** A spring-loaded vacuum tool that sucks up molten solder. Useful for clearing through-holes when replacing components.

**Tip cleaner.** A brass wire sponge or damp cellulose sponge for cleaning the iron tip between joints. A clean, tinned tip transfers heat far better than a dirty one.

**Helping hands or PCB holder.** A device that holds the workpiece steady, freeing both hands for the iron and solder. An adjustable PCB vice is particularly valuable for board work.

**Flush cutters.** Side cutters for trimming component leads close to the board after soldering.

**Magnification.** A magnifying lamp, visor, or loupe helps you inspect joints, especially as components get smaller.

## Technique

### The basic through-hole solder joint

The most common joint in kit building and homebrew projects is attaching a through-hole component lead to a PCB pad. The correct technique is:

1. **Prepare.** Ensure the iron tip is clean and tinned (coated with a thin layer of fresh solder). Insert the component lead through the PCB hole.

2. **Heat both surfaces simultaneously.** Touch the iron tip to the junction where the component lead meets the PCB pad, making contact with both at the same time. The flat face of a chisel tip is ideal for this — one side touches the pad, the other touches the lead.

3. **Apply solder to the joint, not the iron.** After one to two seconds of heating, touch the solder wire to the opposite side of the joint from the iron. The solder should melt and flow around the joint, pulled by capillary action. If the solder melts on contact with the joint, the temperature is right.

4. **Remove the solder, then the iron.** Once enough solder has flowed to form a smooth, concave fillet around the lead and pad, pull the solder wire away first, then lift the iron. The entire process should take two to five seconds.

5. **Inspect.** A good solder joint is shiny (for leaded solder) or slightly satiny (for lead-free), smooth, and concave — it should look like a small tent or volcano shape where the solder wets both the lead and the pad. The outline of the lead should be visible through the solder.

### Common mistakes

**Cold joint.** The joint looks dull, grainy, or lumpy. This happens when the surfaces were not heated enough for the solder to flow properly, or when the joint was moved before the solder solidified. Cold joints have high resistance and may fail over time. The fix is to reheat the joint and add a small amount of fresh solder (which brings fresh flux).

**Too much solder.** A large blob that obscures the lead and may bridge to adjacent pads. Use less solder — you need far less than most beginners expect. If there is excess, remove it with solder wick.

**Solder bridge.** An unintended connection between adjacent pads or pins. Common with closely spaced IC pins. Remove with solder wick or a solder sucker, or drag a clean iron tip between the bridged pins to pull excess solder away.

**Lifted pad.** Applying too much heat or mechanical force can separate a copper pad from the PCB. This is difficult to repair and best avoided by using appropriate temperature and not prying at components. If it happens, a short piece of bare wire soldered between the component lead and the nearest trace can restore the connection.

**Burned flux.** Dark residue and a charred smell indicate excessive heat or time on the joint. The flux has burned away before the solder could flow. Clean the area, apply fresh flux if needed, and try again with a cleaner tip and brisker technique.

### Tinning wires and leads

Before soldering a wire to a terminal, connector, or another wire, **tin** the wire first: strip the insulation, apply the iron to the bare wire, and flow solder into the strands until they are coated. This makes the final joint much easier and more reliable. Pre-tinning is standard practice for coaxial cable centre conductors, speaker wires, and any stranded wire connection.

### Soldering connectors

Coaxial connectors (PL-259, BNC, SMA, and others) require more heat than small PCB work because the connector body acts as a heat sink. Use a higher iron temperature or a larger tip, and be patient — the solder needs to flow fully around the joint. For PL-259 connectors on RG-58 or RG-213 cable, pre-tin the braid, position it in the connector, and apply heat through the solder holes in the connector barrel to flow solder into the braid underneath. A good connector joint is worth taking time over, since feedline connections are a common source of intermittent problems.

## Desoldering

Mistakes happen, and components sometimes need to be replaced. The two main desoldering techniques are:

**Solder wick.** Place the braid over the joint, press the hot iron onto the braid, and wait for the solder to wick up into the copper braid. Lift the braid and iron together. Use fresh sections of braid as they become saturated.

**Solder sucker.** Heat the joint until the solder is molten, then quickly position the sucker nozzle at the joint and trigger it. The vacuum pulls the molten solder into the tool. Multiple passes may be needed.

For through-hole components, a combination of both methods often works best — use the sucker to remove the bulk of the solder, then wick away the remainder.

## Safety

Soldering safety deserves the same attention as any other workshop practice. The main hazards are:

**Burns.** A soldering iron tip is typically 300–400°C (570–750°F). Always return the iron to its stand when not actively soldering. Do not leave an iron unattended while hot. Be conscious of where the cord is — catching it on something can pull the iron off the bench.

**Fumes.** When solder flux is heated, it produces visible fumes. These are not "lead fumes" (lead does not vapourise at soldering temperatures), but rosin fumes can irritate the eyes, nose, and throat, and prolonged exposure can cause respiratory sensitisation. Work in a well-ventilated area, use a small fume extractor or fan to draw fumes away from your face, and take breaks during long sessions.

**Lead.** If you use leaded solder, small amounts of lead can remain on your hands. Do not eat, drink, or touch your face while soldering, and wash your hands thoroughly when you finish. Keep leaded solder and related materials away from children. Collect solder scraps and waste for proper disposal rather than putting them in household rubbish.

**Eye protection.** Wear safety glasses when cutting component leads — trimmed leads can fly with surprising force. Magnification lenses or visors serve double duty as eye protection.

## Building good habits

Experienced builders develop routines that produce consistently good results. Tin the tip before each joint and immediately after cleaning — a well-tinned tip transfers heat efficiently and resists oxidation. Clean the tip often by wiping it on the brass sponge or damp cellulose sponge every few joints. Work systematically through a board by soldering the lowest-profile components first (resistors, diodes), then taller ones (capacitors, sockets, connectors), using the flat board surface to hold components in place while you solder.

Always check orientation before soldering. Diodes, electrolytic capacitors, ICs, and transistors must be installed the correct way round. It is much easier to verify first than to desolder and replace. Inspect every joint before moving on — catching a problem immediately is far easier than troubleshooting a completed board.

## Surface-mount soldering

While through-hole soldering is the foundation, many modern kits and projects include surface-mount (SMD) components. Surface-mount work requires a finer tip, additional flux, steady hands, and good magnification, but the basic principles are the same — heat the pad and component lead together, apply solder, and let capillary action do the work. Tweezers replace your fingers for positioning parts. A flux pen or syringe of paste flux is nearly essential for clean SMD work.

For the occasional surface-mount component, hand soldering with a fine-tipped iron works well. For boards with many SMD parts, techniques like drag soldering (for multi-pin ICs) and hot-air rework become valuable additions to your skill set.

## Where to go next

- [Kit Building](/diy-projects/kit-building) — Put your soldering skills to work on a complete project
- [QRP Building](/diy-projects/qrp-building) — Homebrew low-power radios where soldering skills are essential
- [Basic Electricity](/electronics/basic-electricity) — Understand the circuits you are soldering
- [Semiconductors](/electronics/semiconductors) — Learn about the components you will be handling
