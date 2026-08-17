<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="DAWWW-CORE emblem" width="170" />

# DAWWW-CORE

### One DAW. One project. Desktop and Android.

DAWWW-CORE is a **local-first music production workstation for the browser**, built around a complete project that can move between Desktop and Android without changing format, losing devices or switching to a reduced mobile workflow.

[![Desktop](https://img.shields.io/badge/Desktop-AVAILABLE%20NOW-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Desktop access](https://img.shields.io/badge/Desktop-NO%20PAYMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Cross-device](https://img.shields.io/badge/Desktop%20↔%20Android-100%25%20CROSS--DEVICE-111827?style=for-the-badge)](#one-project-across-desktop-and-android)
[![Instruments](https://img.shields.io/badge/Built--in%20instruments-51-111827?style=for-the-badge)](#instruments-and-synthesis)
[![Effects](https://img.shields.io/badge/Built--in%20effects-16-111827?style=for-the-badge)](#effects)
[![Android](https://img.shields.io/badge/Android-COMING%20%7C%20SUBSCRIPTION-111827?style=for-the-badge)](#one-project-across-desktop-and-android)

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Product](https://dawww-core-local.com/en/studio) · [Documentation](https://dawww-core-local.com/en/docs) · [Status](https://dawww-core-local.com/en/status) · [Français](README.fr.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="DAWWW-CORE Desktop project launcher" width="100%" />
</p>

## One project across Desktop and Android

Cross-device is not an extra sync feature in DAWWW-CORE. It is part of the project model itself.

The same `.dw` project is designed to contain the state required to reopen the session on either platform: arrangement, notes and patterns, instruments, effect settings, automation, routing and referenced sampler content. Desktop and Android use the **same project format**, not two partially compatible versions.

That means the intended exchange is direct:

```text
Desktop  →  .dw  →  Android  →  .dw  →  Desktop
```

No conversion step. No Android-only project variant. No companion/viewer mode. A project created on one surface remains the same DAWWW-CORE project on the other.

Cloud synchronization is not required for this compatibility. A `.dw` file can be moved independently; online services can be added around the workflow without becoming the authority that makes the project exist.

| Platform | Availability | Access model | Project support |
| --- | --- | --- | --- |
| **Desktop Web** | Available now | **No payment** | Full DAWWW-CORE project |
| **Android** | Coming | **Subscription** | Same full `.dw` project |
| **Desktop ↔ Android** | Native project continuity | — | **No conversion / no reduced format** |

## Production modules

DAWWW-CORE is organized around separate production modules that all operate on the same project.

| Module | What it provides |
| --- | --- |
| **Transport** | Shared playback position, tempo and project timing |
| **Sequencer** | Pattern-based writing and step programming |
| **Step editor** | Velocity, probability, gate, ratchets, articulation and timing offset |
| **Piano roll** | Note-level MIDI editing for pitched material |
| **Arranger** | Song structure and timeline organization |
| **Mixer** | Channel levels, routing, processing and master control |
| **Automation** | Parameter changes over time for instruments, effects and mix behavior |
| **Instrument devices** | Dedicated interfaces for the built-in sound engines |
| **Effects** | Integrated processing directly inside the project/mixer workflow |
| **Project I/O** | Local save/restore and portable `.dw` import/export |
| **Audio export** | Master and stem-oriented export workflows |

The point is not to reproduce one giant editor. Patterns, note editing, arrangement, sound design and mixing remain distinct working surfaces while sharing one project state.

## Instruments and synthesis

DAWWW-CORE currently includes **51 built-in instruments**: 50 dedicated synthesis engines plus a sampler.

Rather than shipping one generic synth with dozens of renamed presets, the sound engines are grouped by musical role and several families expose their own dedicated editors.

| Family | Included engines |
| --- | --- |
| **Orchestra · 12** | Violin, viola, cello, contrabass, trumpet, French horn, trombone, tuba, flute, oboe, clarinet, bassoon |
| **Drums · 12** | Kick, snare, clap, closed/open hi-hat, low/mid/high toms, cowbell, rimshot, claves, maracas |
| **Bass · 3** | Sub, acid, Reese |
| **Electronic · 7** | Mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys, noise/transition FX |
| **Pads · 5** | Warm, glass, choir, evolving, ambient |
| **Keys & bells · 7** | Acoustic piano, electric piano, clavinet, tonewheel organ, celesta, music box, tubular bell |
| **Guitars · 4** | Nylon, steel-string, clean electric, driven electric |
| **Sampler · 1** | Sample-based instrument workflow |

Dedicated device panels allow an instrument to expose controls that match its sound model instead of forcing every instrument through the same generic UI. The Electric Piano, for example, has its own tone, tremolo and envelope-oriented controls; percussion devices expose parameters more relevant to transient shaping.

## Effects

The current built-in processing set contains **16 effects**:

`8-band Parametric EQ` · `Compressor` · `Convolution Reverb` · `Tempo-synced Delay` · `Chorus` · `Flanger` · `Phaser` · `Distortion` · `Filter` · `Gate` · `Limiter` · `Saturator` · `Tremolo` · `Vibrato` · `Bitcrusher` · `Utility`

Effects are part of the project rather than an external post-processing layer. Their settings can live with the session, participate in routing and automation, and move with the same `.dw` project across compatible DAWWW-CORE surfaces.

## Current Studio surfaces

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="DAWWW-CORE sequencer" width="100%" /><br />
      <sub><b>Sequencer</b> — pattern tracks, instrument access and step programming.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="DAWWW-CORE step editor" width="100%" /><br />
      <sub><b>Step editor</b> — velocity, probability, gate, ratchets, articulation and timing.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="DAWWW-CORE mixer" width="100%" /><br />
      <sub><b>Mixer</b> — channel levels, routing, processing and master stage.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="DAWWW-CORE piano roll and instrument editor" width="100%" /><br />
      <sub><b>Piano roll + instrument</b> — note editing and sound controls in the same project context.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="DAWWW-CORE Electric Piano editor" width="82%" /><br />
      <sub><b>Dedicated instrument editor</b> — controls adapted to the instrument instead of a one-size-fits-all panel.</sub>
    </td>
  </tr>
</table>

## Local-first by design

Desktop runs the audio engine directly on the user's machine through modern browser audio capabilities. Normal playback does not depend on a remote audio-rendering service.

Projects are kept locally during work and can be exported as `.dw`. This gives DAWWW-CORE two levels of persistence:

- **local working storage** for fast day-to-day sessions;
- **portable `.dw` projects** that can be archived, moved or opened on another DAWWW-CORE surface.

The Desktop app is browser-based and PWA-oriented, so it can stay directly accessible from the web while behaving more like an installed application on supported systems.

## What is tested

The production codebase uses automated and scenario-based validation around the parts that matter most for a DAW.

Current test coverage includes:

- project save, restore, import and `.dw` portability;
- Desktop ↔ Android project compatibility and round-trip behavior;
- transport and playback synchronization;
- sequencer, piano roll, arranger and mixer behavior;
- routing, sends and processing paths;
- instruments, effects and automation;
- master/stem export paths;
- long-running playback and stress-oriented sessions;
- browser E2E and performance checks.

The public repository deliberately does not expose internal gate names, implementation details or security/release internals. The useful public information is the coverage itself: **project portability, audio continuity, modules, effects, routing and export are treated as testable product behavior rather than assumptions.**

## Session size and current limits

DAWWW-CORE does not impose a marketing-style fixed limit such as “X tracks” or “Y minutes” because the Desktop engine runs locally.

The real limit of a project depends on the machine and on what the project is doing:

- many simultaneous synth voices increase CPU load;
- large sample sets increase memory and local-storage use;
- long effect chains and complex routing increase real-time processing cost;
- large stem exports require more rendering time and temporary memory;
- browser storage capacity varies by browser, operating system and device.

So a light 30-track project can be easier to run than a smaller project with very high polyphony, multiple reverbs and heavy processing. Session complexity matters more than a single track-count number.

Important projects should be exported periodically as `.dw`, especially when using large sample libraries, because browser-local storage is controlled by the host browser and does not provide one universal quota across every machine.

### Export and browser differences

**WAV** is the baseline export path. **MP3 availability depends on platform/runtime capability** rather than being guaranteed by a bundled universal encoder.

Audio latency, storage quota, codec support and maximum practical project complexity can also vary between browsers and operating systems. DAWWW-CORE is built to run in the browser, but identical hardware behavior cannot be assumed across every environment.

## Desktop now, Android next

**Desktop Web** is the current public DAWWW-CORE surface and has **no payment flow**.

**Android** is coming as a **subscription version**. It is not a separate lightweight product: it uses the same full project model, instruments/effects state and `.dw` compatibility described above.

The distinction is therefore commercial and platform-specific, not creative:

> **Desktop and Android are two places to work on the same DAWWW-CORE project.**

## Public stack

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · local browser storage · `Capacitor` for Android

## Current scope

The current product does not require:

- mandatory cloud project synchronization;
- real-time collaboration;
- iOS;
- a third-party plugin marketplace.

The focus remains the DAW itself: modules, instruments, effects, automation, mixing, export, local project ownership and complete Desktop ↔ Android continuity.

## Resources

- **Desktop Studio** — https://dawww-core-local.com/app
- **Product overview** — https://dawww-core-local.com/en/studio
- **Documentation** — https://dawww-core-local.com/en/docs
- **Tutorials** — https://dawww-core-local.com/en/tutorials
- **FAQ** — https://dawww-core-local.com/en/faq
- **Status** — https://dawww-core-local.com/en/status
- **Roadmap** — https://dawww-core-local.com/en/roadmap
- **Changelog** — https://dawww-core-local.com/en/changelog
- **Contact** — https://dawww-core-local.com/en/contact

## About this repository

`Daw-core-desktop` is the public product showcase for DAWWW-CORE. The production source code remains private.

This repository documents what the product does, its available tools, its cross-device model, its validation approach and its current practical limits without exposing internal architecture, deployment details or security-sensitive implementation.

---

<div align="center">

### One project. Full DAW workflow. Desktop and Android.

[**Open DAWWW-CORE Desktop**](https://dawww-core-local.com/app)

</div>
