---
title: The Electromagnetic Spectrum
description: Understanding the electromagnetic spectrum and where amateur radio frequencies fit within it
published: true
date: 2026-04-05T09:30:00.000Z
tags: electronics, theory, spectrum, propagation
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. *Remove this banner after human review is complete.*
{.is-warning}

# The Electromagnetic Spectrum

Radio waves are one part of a much larger family called the electromagnetic spectrum. Understanding where amateur radio fits within this spectrum — and how different parts of the spectrum behave — gives you a foundation for everything from band planning to propagation to RF safety.

## What is electromagnetic radiation?

Electromagnetic (EM) radiation is energy that travels through space as oscillating electric and magnetic fields. These fields are perpendicular to each other and to the direction of travel. All EM radiation travels at the speed of light in a vacuum (approximately 300,000,000 metres per second, or 3 × 10⁸ m/s) and is characterised by its **frequency** and **wavelength**, which are inversely related:

**λ = c / f**

Higher frequency means shorter wavelength, and vice versa. A 7 MHz amateur radio signal has a wavelength of about 43 metres, while a 440 MHz signal has a wavelength of only 68 centimetres.

## The spectrum from low to high frequency

The electromagnetic spectrum spans an enormous range of frequencies. From lowest to highest:

### Extremely low to very low frequency (ELF/VLF: 3 Hz – 30 kHz)

These very long wavelengths (100,000 km down to 10 km) can penetrate seawater and are used for submarine communications and natural phenomena like lightning-generated signals. Some radio amateurs experiment with reception at these frequencies, though transmission requires impractically large antennas.

### Low frequency (LF: 30 – 300 kHz)

Wavelengths from 10 km to 1 km. Used for longwave broadcasting, navigation beacons (NDBs), and the amateur 2200-metre band (135.7–137.8 kHz). LF signals follow the Earth's surface effectively (ground wave propagation) and can cover very long distances at low power.

### Medium frequency (MF: 300 kHz – 3 MHz)

Wavelengths from 1 km to 100 m. This includes the AM broadcast band and the amateur 630-metre band (472–479 kHz) and the lower end of the 160-metre band (1.8–2.0 MHz). MF propagation combines ground wave during the day with skywave propagation at night when the D layer of the ionosphere weakens.

### High frequency (HF: 3 – 30 MHz)

Wavelengths from 100 m to 10 m. This is the heart of amateur radio for long-distance (DX) communication. HF signals can refract off the ionosphere and travel thousands of kilometres — even to the other side of the world — without satellites or internet infrastructure. The amateur HF bands include 80 m, 60 m, 40 m, 30 m, 20 m, 17 m, 15 m, 12 m, and 10 m.

HF propagation is highly variable and depends on solar activity, time of day, season, and the specific frequency in use. This unpredictability is part of what makes HF operation fascinating for many amateurs. See [Propagation](/propagation/overview) for more detail.

### Very high frequency (VHF: 30 – 300 MHz)

Wavelengths from 10 m to 1 m. VHF is primarily used for local and regional communication, including the popular 2-metre band (144–148 MHz). VHF signals are generally line-of-sight but can be extended by repeaters, tropospheric ducting, sporadic E propagation, meteor scatter, and moonbounce (EME). FM voice, digital modes, and amateur television all see heavy use on VHF.

### Ultra high frequency (UHF: 300 MHz – 3 GHz)

Wavelengths from 1 m to 10 cm. Includes the 70-centimetre band (420–450 MHz) and the 23-centimetre band (1240–1300 MHz). UHF is used for local FM repeaters, amateur television, satellite communication, and increasingly for digital voice modes like DMR, D-STAR, and System Fusion.

### Super high frequency (SHF: 3 – 30 GHz) and above

Wavelengths from 10 cm down to 1 mm and beyond. These microwave and millimetre-wave bands are used for amateur experimentation, EME, and point-to-point links. Propagation is strictly line-of-sight, and even rain and atmospheric moisture can attenuate signals significantly. Equipment at these frequencies often involves specialised waveguides, parabolic dishes, and low-noise amplifiers.

### Beyond radio

Above the radio spectrum, electromagnetic radiation continues through infrared, visible light, ultraviolet, X-rays, and gamma rays. While these are not used for amateur radio communication, understanding that they are all the same type of energy — differing only in frequency — helps build a complete picture.

## Amateur radio band allocations

Amateur radio operators are allocated frequency bands across the spectrum by the International Telecommunication Union (ITU) and national regulators. These allocations vary somewhat by ITU region and country. The most commonly used amateur bands include:

| Band name | Frequency range | Wavelength | Typical use |
|-----------|----------------|------------|-------------|
| 2200 m | 135.7–137.8 kHz | ~2200 m | Experimental, CW |
| 630 m | 472–479 kHz | ~630 m | Experimental, CW/digital |
| 160 m | 1.8–2.0 MHz | ~160 m | Night-time DX, "Top Band" |
| 80 m | 3.5–4.0 MHz | ~80 m | Regional, evening/night |
| 60 m | 5.3–5.4 MHz | ~60 m | Channelised in many countries |
| 40 m | 7.0–7.3 MHz | ~40 m | Workhorse DX and regional |
| 30 m | 10.1–10.15 MHz | ~30 m | CW and digital only |
| 20 m | 14.0–14.35 MHz | ~20 m | Primary daytime DX band |
| 17 m | 18.068–18.168 MHz | ~17 m | DX, WARC band |
| 15 m | 21.0–21.45 MHz | ~15 m | DX during solar maxima |
| 12 m | 24.89–24.99 MHz | ~12 m | DX, WARC band |
| 10 m | 28.0–29.7 MHz | ~10 m | DX and local, solar-dependent |
| 6 m | 50–54 MHz | ~6 m | "Magic Band," sporadic E |
| 2 m | 144–148 MHz | ~2 m | Local/regional FM, SSB, digital |
| 70 cm | 420–450 MHz | ~70 cm | Local FM, digital, ATV |
| 23 cm | 1240–1300 MHz | ~23 cm | Microwave, ATV, satellite |

Exact frequency ranges and permitted modes vary by country and licence class. Always consult your national band plan.

## How frequency affects propagation

The behaviour of radio waves changes dramatically across the spectrum:

At **HF and below**, the ionosphere can refract signals back to Earth, enabling worldwide communication. Lower frequencies tend to propagate better at night, while higher HF frequencies work better during the day when solar radiation strengthens the ionosphere.

At **VHF**, signals are primarily line-of-sight, extending to the radio horizon (somewhat beyond the visual horizon due to atmospheric refraction). Occasional enhancements from tropospheric ducting, sporadic E, and other phenomena can extend VHF range dramatically.

At **UHF and above**, propagation becomes increasingly line-of-sight. Buildings, hills, and vegetation can block or attenuate signals. Rain fade becomes a factor at microwave frequencies. However, antennas become physically smaller at higher frequencies, making it practical to build high-gain directional antennas.

## Frequency vs. wavelength naming

Amateur bands are traditionally named by their approximate wavelength ("the 20-metre band") rather than their frequency. This convention dates to the early days of radio and remains in use today. When someone says they are "on 20 metres," they mean the 14 MHz band. Both naming conventions are used, and being comfortable with both is helpful.

## Electromagnetic compatibility

The electromagnetic spectrum is shared among many services — broadcasting, mobile phones, aviation, maritime, military, scientific, and more. Amateur radio operators must operate within their allocated bands and avoid causing interference to other services. Similarly, understanding the spectrum helps diagnose interference from other sources affecting your amateur radio reception.

## See also

- [Basic Electricity](/electronics/basic-electricity) — fundamentals of voltage, current, and power
- [AC Circuits](/electronics/ac-circuits) — how alternating signals behave in circuits
- [RF Safety](/electronics/rf-safety) — safe exposure limits across the spectrum
- [Propagation Overview](/propagation/overview) — how radio waves travel from transmitter to receiver
