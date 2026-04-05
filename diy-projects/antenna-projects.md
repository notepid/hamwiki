---
title: Antenna Projects
description: Practical DIY antenna building projects for amateur radio — from simple wire antennas to multi-band designs
published: true
date: 2026-04-05T09:30:00.000Z
tags: diy, antennas, building, homebrew, projects
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# Antenna Projects

Building your own antennas is one of the most practical and rewarding aspects of amateur radio. Antennas are often the single biggest factor in station performance, and a well-built homebrew antenna can dramatically improve what you hear and who hears you — frequently for very little money. Unlike many electronic projects, antenna building uses basic materials and tools, making it accessible even to operators with no prior construction experience.

This page focuses on the practical side of building antennas — materials, techniques, and project ideas at various skill levels. For the theory behind how antennas work, see the [Antennas](/antennas/overview) section.

## Why build your own antennas?

Commercial antennas work well, but building your own offers distinct advantages. Cost is the most obvious — a homebrew wire dipole or end-fed antenna can cost a fraction of a commercial equivalent while performing just as well. Custom dimensions let you optimise for your exact operating frequency, available space, and installation situation. The process of building, testing, and tuning an antenna teaches you more about antenna behaviour than any amount of reading. And when something breaks in the field — a common occurrence with portable and field-day antennas — a builder who understands the design can repair it on the spot.

## Essential materials and tools

Most antenna projects use a common set of materials. Wire is the most fundamental — stranded copper wire is flexible and easy to work with, while solid copper or copper-clad steel wire holds its shape better in permanent installations. Common wire gauges for HF antennas range from 12 AWG to 18 AWG (2.0 mm to 1.0 mm diameter). Insulated wire works as well as bare wire for most designs, and the insulation provides weather protection.

Coaxial cable connects the antenna to the radio. RG-58 is adequate for low-power and short runs, while RG-213 or LMR-400 handle higher power and longer distances with less loss. The correct connectors — usually PL-259/SO-239 for HF work, or BNC and N-type for VHF/UHF — complete the feedline. See [Feedlines](/antennas/feedlines) for detailed guidance on cable selection.

Insulators keep wire elements from shorting to support structures. Commercial antenna insulators, ceramic or plastic egg insulators, or even lengths of PVC pipe all work. For temporary antennas, heavy-duty cable ties or short sections of nylon rope serve as insulators.

Support hardware depends on the installation. Rope, pulleys, mast clamps, wall brackets, and various fasteners are all common. UV-resistant materials are important for anything exposed to sunlight long-term.

The basic tool set for antenna building is modest: wire cutters and strippers, pliers, a tape measure (essential for cutting elements to length), a soldering iron for connector work, a drill for mounting hardware, and weatherproofing supplies (self-amalgamating tape, heat-shrink tubing, or silicone sealant for outdoor connections).

## Beginner projects

### Half-wave dipole

The [dipole](/antennas/dipole) is the natural first antenna project. A half-wave dipole for a single HF band requires only two lengths of wire, a centre insulator (which can be a simple piece of plastic with hardware for connecting the feedline), two end insulators, and a length of coaxial cable. The formula for the total wire length in metres is approximately 143 divided by the frequency in MHz (or 468 divided by the frequency in MHz for length in feet). Cut the wire slightly long, install it, measure the [SWR](/antennas/swr-and-matching), and trim small amounts from each end until the SWR is minimised at your target frequency.

A dipole strung between two trees, between a tree and a mast, or in an inverted-V configuration from a single support point is an excellent all-round HF antenna. It costs almost nothing, it performs well, and the process of cutting, measuring, and tuning teaches the fundamental relationship between wire length and resonant frequency.

### End-fed half-wave (EFHW)

The [end-fed half-wave](/antennas/end-fed-half-wave) antenna has become extremely popular because it requires only a single elevated support point — one end is high, the other can be near ground level at the operating position. An EFHW needs a matching transformer (a simple toroidal transformer, often called an "unun") at the feed point to transform the high impedance at the end of a half-wave wire to something closer to 50 ohms. Winding this transformer is a straightforward project in itself. Many designs use a multi-band approach by cutting the wire for the lowest desired frequency — harmonically related bands (for example, 40 m and 20 m, or 80 m and 40 m/20 m/10 m) often present usable impedances on the higher bands through the same transformer.

### Ground-plane vertical for VHF/UHF

A quarter-wave ground-plane antenna for 2 m (146 MHz) or 70 cm (440 MHz) is a quick project using rigid wire or brazing rod. The vertical element is a quarter wavelength long, and three or four radial elements of the same length extend outward at a slight downward angle from the base. A chassis-mount SO-239 connector at the centre serves as both the mounting point and the feedpoint — the vertical element connects to the centre pin, and the radials connect to the ground lugs. This antenna outperforms the "rubber duck" antenna on a handheld radio by a wide margin.

### Slim Jim for VHF/UHF

The slim jim is a popular VHF/UHF antenna made from a single length of 300-ohm or 450-ohm ladder line (twin-lead or window line). It is essentially a half-wave vertical with a matching section built in. Dimensions are widely published for the common amateur bands. The completed antenna can be rolled up for transport and hung from a tree branch or mast with a piece of string, making it ideal for portable use.

## Intermediate projects

### Fan dipole

A fan dipole uses multiple dipole elements — each cut for a different band — connected at a common feedpoint and fanning out from the centre. The elements are close enough that they can share the same support rope at each end, with small spacers keeping them separated by a few centimetres. A three-band fan dipole (for example, covering 20 m, 15 m, and 10 m) gives you multi-band capability with a single feedline and no traps or tuner required. Interaction between the elements means the final lengths need to be adjusted by measurement rather than pure calculation, but the tuning process is methodical and educational.

### Linked dipole

A linked dipole uses a single wire element with plug-in connectors (typically Anderson Powerpole connectors or banana plugs) at specific points along each leg. By removing or inserting links, you change the electrical length of the antenna to resonate on different bands. This is a favourite of portable operators — especially those doing POTA (Parks on the Air) or SOTA (Summits on the Air) — because a single lightweight antenna covers multiple bands.

### Wire Yagi

A two-element wire Yagi — a driven element and a reflector, both made of wire suspended from a rope — provides modest gain and directivity on HF with minimal materials. The elements are typically spaced 0.1 to 0.15 wavelengths apart. While it does not compare to a rotary aluminium Yagi on a tower, a wire Yagi between two supports can provide 3–5 dB of gain in the forward direction, which is a real improvement for DX work.

### Small magnetic loop

A small magnetic loop antenna is particularly valuable for operators with limited space or antenna restrictions. It consists of a loop of copper tubing or coaxial cable, typically 1/8 to 1/4 wavelength in circumference, with a variable capacitor to tune it to resonance. The loop is electrically small and has a very narrow bandwidth (a few kHz on HF), so it must be retuned when you change frequency. Building the loop itself is straightforward, but the variable capacitor must handle high RF voltages even at QRP power levels, which requires careful component selection. Magnetic loops are effective despite their small size because they are efficient when properly tuned and inherently reject local electrical noise.

## Advanced projects

### Multi-band trapped dipole

A trapped dipole uses LC trap circuits at specific points along the wire to create multiple resonant lengths within a single physical antenna. The traps are parallel-resonant circuits that present a high impedance at their resonant frequency, effectively shortening the antenna for that band. Building the traps requires winding coils and matching them with capacitors, then adjusting the wire lengths for each band. The result is a single-feedline antenna that covers several bands without a tuner.

### Hex beam

A hex beam is a broadband directional antenna that covers multiple HF bands in a compact hexagonal frame. It offers modest gain (similar to a two-element Yagi) with a much smaller turning radius than a conventional beam. Building a hex beam involves constructing a fibreglass or aluminium spreader frame and stringing wire elements in a specific pattern. It is a more ambitious project but produces an antenna that is light enough for a modest mast and rotator.

### VHF/UHF Yagi arrays

Building a VHF or UHF Yagi beam from aluminium rod and tubing is a satisfying project that introduces precision measurement and mechanical construction alongside electrical design. At these frequencies, elements are short enough to be practical on a workshop bench. Designs for high-performance VHF Yagis with 5 to 15 elements are widely available, and [antenna modelling software](/antennas/antenna-modeling) can help you optimise a design for your specific requirements.

## Construction tips

**Measure carefully.** Antenna performance is directly related to element length and spacing. A tape measure is your most important tool. For critical dimensions, measure twice and cut once — or better yet, cut slightly long and trim to final length after testing.

**Weatherproof all outdoor connections.** Water ingress into connectors and junctions is the single most common cause of antenna failure over time. Self-amalgamating (self-vulcanising) tape is excellent for sealing coaxial connectors. Silicone sealant, heat-shrink tubing with adhesive lining, and even electrical tape with an outer wrap of waterproof tape all help. No weatherproofing is permanent in all climates, so inspect and renew it periodically.

**Use strain relief.** Wind, ice, and thermal cycling put mechanical stress on antenna connections. Ensure that the wire, not the solder joint or connector, bears the mechanical load. Tie wire elements to insulators before connecting them electrically. Secure coaxial cables so that they do not hang from their connectors.

**Test and tune.** An antenna analyser or SWR meter is essential for tuning any antenna. Measure the SWR across the intended frequency range after installation, and adjust element lengths as needed. The antenna's behaviour changes with height, nearby objects, and ground conditions, so always tune in the final installed position.

## Safety

Antenna construction and installation involves several hazards. **Never work near overhead power lines** — contact between an antenna, mast, or support rope and a power line is potentially fatal. Maintain a safe distance that accounts for the possibility of something falling. Use a spotter when raising masts or towers. Wear eye protection when cutting wire and drilling metal. Be aware that aluminium and copper cuttings are sharp. When working at height, use appropriate fall protection and never work alone.

See [Building Antennas](/antennas/building-antennas) for a more detailed treatment of construction safety practices.

## Where to go next

- [Antenna Fundamentals](/antennas/antenna-fundamentals) — The theory behind resonance, impedance, and radiation patterns
- [Dipole Antennas](/antennas/dipole) — In-depth coverage of the most fundamental antenna
- [SWR and Matching](/antennas/swr-and-matching) — Understanding and using SWR measurements
- [Feedlines](/antennas/feedlines) — Choosing and using coaxial cable and other feedlines
- [Antenna Modeling](/antennas/antenna-modeling) — Simulate before you build
- [Soldering Basics](/diy-projects/soldering-basics) — Skills for connector and feedpoint work
- [Portable Antennas](/antennas/portable-antennas) — Lightweight designs for field use
