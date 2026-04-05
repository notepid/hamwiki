---
title: Keyers and Paddles
description: CW keyers, paddles, and straight keys — types, operation, and choosing your first key
published: true
date: 2026-04-05T09:30:00.000Z
tags: equipment, cw, keyers, morse
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---

> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}

# Keyers and Paddles

**CW** (continuous wave) — the radio mode used for Morse code — remains one of the most effective and popular modes in amateur radio. A CW signal occupies very little bandwidth, cuts through noise and interference better than voice, and requires minimal equipment. The key (or paddle) is the operator's physical interface to the transmitter, and choosing the right one is a surprisingly personal decision.

This page covers the different types of keys and paddles, how electronic keyers work, and how to choose equipment that suits your operating style.

## The Straight Key

The **straight key** is the oldest and simplest type of Morse key. It consists of a lever (the arm) mounted on a pivot, with an electrical contact at one end and a knob at the other. Pressing the knob closes the contact, keying the transmitter. Releasing it opens the contact. The operator manually controls the length of every dit (short element), dah (long element), and the spacing between them.

Straight keys are how Morse code was sent for over a century, from the earliest telegraph lines through the World War II era and beyond. They are still widely used today, particularly by operators who enjoy the traditional skill of hand-sent Morse and by newcomers learning CW.

**Advantages:** Simple, no electronics needed, full manual control over timing and rhythm, and a tactile connection to the history of radio communication. Straight keys are required equipment for events like the ARRL Straight Key Night (January 1 each year).

**Disadvantages:** Speed is limited by human physiology — most operators top out around 15–20 WPM (words per minute) with a straight key, and sustained high-speed sending causes fatigue. Timing inconsistencies (dit/dah ratio, spacing) are common and require practice to minimise.

Popular straight keys include the **Bencher RJ-1/RJ-2**, **Vibroplex Original Standard**, **MFJ-553**, and various military-surplus keys (the J-38, used by the US military from World War II onward, remains a beloved classic).

## The Bug (Semi-Automatic Key)

The **bug** (also called a **semi-automatic key** or **Vibroplex bug**, after the most famous manufacturer) was invented in the early 1900s to increase sending speed. A bug uses a weighted, spring-loaded horizontal lever. Pressing the lever to one side (the dit side) causes the weight to vibrate back and forth, automatically producing a string of dits at a speed determined by the weight's position. Pressing to the other side (the dah side) produces manual dahs, just like a straight key — one dah per press.

The bug dramatically increases achievable speed (30+ WPM is possible) and reduces fatigue compared to a straight key. The trade-off is that the dah timing is still manual, and bugs have a distinctive "swing" to their sound — experienced operators can often identify a bug-sent signal by its slightly irregular rhythm.

Bugs are less common today than electronic keyers, but they retain a devoted following among CW enthusiasts who appreciate their mechanical elegance and characteristic sound. The **Vibroplex** company has been producing bugs since 1905, and vintage Vibroplex bugs are collectors' items.

## Paddles

A **paddle** is a dual-lever device designed to work with an **electronic keyer**. The paddle itself has no keying intelligence — it is simply two switches (contacts) that the operator activates by pressing the levers with the thumb and index finger.

### Single-lever paddle

A single-lever paddle has one lever that swings left and right. Pressing it one direction closes the dit contact; pressing the other direction closes the dah contact. Both contacts cannot be closed simultaneously by normal operation (though squeezing hard enough may close both on some paddles). Single-lever paddles are simpler and some operators find them easier to learn.

### Dual-lever (iambic) paddle

A dual-lever paddle has two independently moving levers — one for dits and one for dahs — that can be pressed individually or squeezed together simultaneously. When used with an **iambic keyer** (see below), squeezing both levers produces alternating dits and dahs automatically, which can increase sending speed and efficiency for certain character sequences. Dual-lever paddles are the most common type used with electronic keyers today.

Popular paddles include the **Bencher BY-1 and BY-2** (classics that have been in production for decades), **Vibroplex Vibrokeyer**, **Begali** (Italian-made high-end paddles known for superb craftsmanship), **American Morse Equipment (N3ZN)** paddles, **CW Morse** paddles, and the **Palm Radio Pico Paddle** and similar miniature paddles for portable operation.

Paddle quality and feel are highly personal. Factors that matter include the weight of the base (heavier bases stay put on the desk), the smoothness of the lever bearings, the adjustability of contact spacing and spring tension, and the overall tactile feedback. Many experienced CW operators consider their paddle a lifetime investment and choose carefully.

## Electronic Keyers

An **electronic keyer** is a circuit (or software) that generates properly timed Morse code elements from paddle inputs. When the operator presses the dit lever, the keyer produces a stream of dits at the set speed with correct timing. Pressing the dah lever produces dahs at three times the dit length (the standard Morse ratio). The keyer handles element timing and spacing, freeing the operator to focus on the content of the message.

### How iambic keying works

When used with a dual-lever paddle, an electronic keyer can operate in **iambic mode**. When both levers are squeezed simultaneously, the keyer alternates between dits and dahs automatically. This is useful for characters that contain alternating elements — for example, the letter "C" (dah-dit-dah-dit) can be sent by squeezing both levers together and releasing at the right moment.

There are two common iambic modes:

**Iambic A** — when both paddles are squeezed and then released during the last element, no additional element is added. The output stops cleanly at the last element being sent when the levers were released.

**Iambic B** — when both paddles are squeezed and then released during the last element, one additional alternating element is inserted after the current one completes. This produces one extra element, which can be useful or problematic depending on the operator's habits.

Most keyers let the operator choose between Iambic A and B, and many also offer a non-iambic (single-lever emulation) mode. Which mode works best is entirely a matter of personal preference and training.

### Built-in keyers

Nearly all modern HF transceivers include a **built-in electronic keyer**. The paddle plugs directly into the transceiver's key jack (typically 3.5 mm stereo — tip for dit, ring for dah, sleeve for ground), and the transceiver's menu settings control speed, iambic mode, weight (dit/dah ratio), and sidetone. This eliminates the need for a separate keyer box for most operators.

### Standalone keyers

External keyer units offer additional features beyond what a transceiver's built-in keyer provides: message memories (storing frequently sent strings like CQ calls, contest exchanges, and signal reports), adjustable weighting and element timing, speed pots with a wide range, and contest-specific features like serial number generators and automatic logging integration.

Popular standalone keyers include the **K1EL WinKeyer** series (widely used and supported by most contest logging software), **Begali CW Machine**, **MFJ-464** and other MFJ keyers, and the **Mortty** open-source keyer.

### Software keyers

Logging and contest software (N1MM+, Win-Test, Log4OM, etc.) can act as keyers, using a computer interface to key the transmitter. The operator triggers stored messages with keyboard function keys, and the software handles the timing. This is the standard approach in contesting, where the same messages (CQ, exchange, acknowledgement) are repeated hundreds or thousands of times.

## Choosing Your First Key or Paddle

**If you are learning CW:** Start with a **straight key**. It forces you to develop an internal sense of timing and rhythm. Inexpensive straight keys from MFJ or surplus military keys work fine for learning. Once you are comfortable at 10–15 WPM, consider transitioning to a paddle and keyer for higher speeds.

**If you want to jump straight to a paddle:** A **dual-lever paddle** with the transceiver's built-in keyer is the most common and versatile setup. The Bencher BY-1 is a widely recommended entry point — sturdy, smooth, and affordable. Budget alternatives from CW Morse and other makers also work well.

**If you prioritise portability:** Miniature paddles like the **Palm Radio Pico Paddle**, **American Morse Equipment Porta Paddle**, **CW Morse Pocket Paddle**, or even homebrew designs that fit in an Altoids tin are popular for SOTA, POTA, and field operation.

**If you want the finest feel:** High-end paddles from **Begali**, **N3ZN**, **Schurr**, and **GHD** (Japan) are precision instruments with outstanding bearings, weight, and adjustability. These are investments that last a lifetime.

## Key Connections

Most modern transceivers accept a paddle or straight key through a **3.5 mm (⅛-inch) stereo jack**:

- **Straight key:** Connects across tip and sleeve (a mono plug works, or a stereo plug with tip and sleeve).
- **Paddle (for built-in keyer):** Dit contact to tip, dah contact to ring, common to sleeve. A stereo plug is required.

Some older transceivers use ¼-inch phone jacks or other connectors. Adapters are readily available.

If using a standalone keyer, the paddle connects to the keyer's input, and the keyer's output connects to the transceiver's key jack. The keyer output is a simple on/off keying signal, so it connects as a straight-key input on the radio (tip and sleeve).

## CW Practice and Training

The best key in the world will not help without practice. Learning CW is a skill that develops with consistent, daily practice. Resources for learning and improving CW include:

- **LCWO.net** — Learn CW Online, a free web-based training tool using the Koch method
- **CW Academy** — the CWops (CW Operators' Club) free training programme with live instructors at all levels
- **MorseFree** and **Morse Trainer** — mobile apps for practice on the go
- **On-air practice** — calling CQ at a comfortable speed, joining slow-speed CW nets, and participating in QRS (slow speed) contests

See the [CW/Morse Code](/operating/cw-morse) page for more on operating CW.

## See Also

- [Equipment Overview](/equipment/overview)
- [CW/Morse Code](/operating/cw-morse)
- [HF Transceivers](/equipment/hf-transceivers)
- [Contesting](/contesting/overview)
- [DIY Projects](/diy-projects/overview)
