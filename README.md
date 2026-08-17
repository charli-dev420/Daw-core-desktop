<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="DAWWW-CORE emblem" width="170" />

# DAWWW-CORE

### Browser-native DAW · local-first runtime · one portable project across Desktop and Android

DAWWW-CORE is a desktop-oriented digital audio workstation built on **Web Audio API + AudioWorklet**, with a React/TypeScript application layer, browser-local persistence and a single portable `.dw` project contract shared by Desktop and Android.

[![Desktop](https://img.shields.io/badge/Desktop-AVAILABLE%20NOW-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Desktop access](https://img.shields.io/badge/Desktop-NO%20PAYMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Instruments](https://img.shields.io/badge/Built--in%20instruments-51-111827?style=for-the-badge)](#production-tools)
[![Effects](https://img.shields.io/badge/Built--in%20effects-16-111827?style=for-the-badge)](#production-tools)
[![Cross-device](https://img.shields.io/badge/Desktop%20↔%20Android-100%25%20CROSS--DEVICE-111827?style=for-the-badge)](#cross-device-architecture)
[![Android](https://img.shields.io/badge/Android-COMING%20%7C%20SUBSCRIPTION-111827?style=for-the-badge)](#cross-device-architecture)

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Product](https://dawww-core-local.com/en/studio) · [Documentation](https://dawww-core-local.com/en/docs) · [Status](https://dawww-core-local.com/en/status) · [Français](README.fr.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="DAWWW-CORE desktop project surface" width="100%" />
</p>

## Technical overview

DAWWW-CORE is a **client-side, local-first DAW**. The creative runtime is not hosted on a remote audio service and the project is not defined by a cloud database record. The browser runs the audio graph, stores the active working state locally and can serialize the complete project into `.dw`.

The architecture is split deliberately:

| Layer | Implementation | Responsibility |
| --- | --- | --- |
| **Application / UI** | TypeScript · React · Vite | Workspace, editors, navigation, state presentation |
| **Audio runtime** | Web Audio API | Audio graph, instruments, effects, mixer, master path |
| **Timing / real-time workers** | AudioWorklet | Timing-critical processing outside React/DOM scheduling |
| **Transport / synchronization** | Shared transport + sync modules | Common musical time for sequencer, arranger and playback |
| **Project runtime** | Serializer / restorer services | Conversion between live runtime state and persistent project state |
| **Local persistence** | Browser-local database/storage | Primary Desktop working storage |
| **Portable project layer** | `DWFormat` / `DWPackagePipeline` | Full `.dw` export/import, verification, recovery and transfer |
| **Desktop distribution** | Web app + PWA-oriented runtime | Direct browser access, optional installed-like PWA behaviour |
| **Android distribution** | Capacitor Android runtime | Upcoming subscribed Android surface using the exact same project contract |
| **Validation** | Vitest · Playwright · custom certification gates | Unit, integration, portability, playback, stress and release checks |

The core separation is simple: **React is not the audio scheduler**. UI work stays in the application layer; timing-sensitive work is handled by the audio/runtime layer and AudioWorklet-backed paths.

## How the audio engine runs

The audio engine executes on the user's device.

A project is restored into a live runtime that builds a Web Audio graph: instrument nodes feed project tracks, track processing and routing feed the mixer, and the mixer feeds the master path. Sequencer and arranger playback use the shared transport so musical time is not tied to component render timing.

AudioWorklet is used for timing-sensitive or processing-sensitive tasks where main-thread JavaScript scheduling would be too fragile. The codebase contains dedicated worklet paths for clock/timing and selected processors/analyzers.

This design means normal Desktop playback does **not** require remote audio rendering. It also means the real-time capacity of a session is ultimately bounded by the local machine: browser implementation, CPU, memory, audio device and the complexity of the active graph.

Audio export is handled through a separate render/export path rather than simply recording the interactive output. Dedicated exporter/render services and audio-parity tests allow rendered output to be checked independently from the UI.

## Production tools

DAWWW-CORE exposes separate DAW surfaces over one shared runtime rather than placing everything in a single editor.

| Surface | Current capabilities | Validation in the production repository |
| --- | --- | --- |
| **Transport** | Play/stop, project time, shared timing state | Playback fixtures + transport certification profiles |
| **Sequencer** | Pattern tracks, step programming, instrument routing | Module fixture + stress fixture |
| **Step properties** | Velocity, probability/chance, gate, ratchet, articulation, timing offset | Sequencer/runtime coverage |
| **Piano roll** | Note-level MIDI editing | Module fixture + stress fixture |
| **Arranger** | Timeline and song structure | Module fixture + stress fixture |
| **Mixer** | Channels, levels, routing, sends/processing, master path | Unit coverage + routing/PDC/send scenarios |
| **Automation** | Parameter automation and live effect automation paths | Dedicated automation/effects scenario |
| **Project I/O** | Local save/restore, `.dw` import/export | Dedicated `.dw` proof suite + serializer/restorer tests |
| **Audio export** | Master and stem workflows, WAV baseline, capability-gated MP3 | Export scenarios, long-export checks, performance budget tests |

### 51 built-in instruments

The built-in registry currently contains **50 dedicated synthesis engines plus one sampler**.

- **12 orchestral engines:** violin, viola, cello, contrabass, trumpet, French horn, trombone, tuba, flute, oboe, clarinet, bassoon
- **12 drum engines:** kick, snare, hand clap, closed/open hi-hat, low/mid/high toms, cowbell, rimshot, claves, maracas
- **3 bass engines:** sub, acid, Reese
- **7 electronic engines:** mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys, noise/transition FX
- **5 pad engines:** warm, glass, choir, evolving, ambient
- **7 keys/bells engines:** acoustic piano, electric piano, clavinet, tonewheel organ, celesta, music box, tubular bell
- **4 guitar engines:** nylon, steel-string, clean electric, driven electric
- **1 sampler** for sample-based instruments

Several instrument families expose dedicated device editors. The UI is therefore able to expose controls related to the actual synthesis model instead of presenting every instrument through one generic parameter list.

### 16 built-in effects

`8-band Parametric EQ` · `Compressor` · `Convolution Reverb` · `Tempo-synced Delay` · `Chorus` · `Flanger` · `Phaser` · `Distortion` · `Filter` · `Gate` · `Limiter` · `Saturator` · `Tremolo` · `Vibrato` · `Bitcrusher` · `Utility`

The effects live inside the mixer/automation model and are serialized as part of the project state.

## Current Studio surfaces

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="DAWWW-CORE sequencer" width="100%" /><br />
      <sub><b>Sequencer</b> — pattern tracks and instrument routing inside the shared project runtime.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="DAWWW-CORE step properties" width="100%" /><br />
      <sub><b>Per-step properties</b> — velocity, chance, gate, ratchets, articulation and timing offset.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="DAWWW-CORE mixer" width="100%" /><br />
      <sub><b>Mixer</b> — routing, inserts/processing, levels and master stage.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="DAWWW-CORE piano roll and instrument device" width="100%" /><br />
      <sub><b>Piano roll + device</b> — note editing and instrument controls remain connected to the same live project.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="DAWWW-CORE electric piano device editor" width="82%" /><br />
      <sub><b>Dedicated device editor</b> — instrument-specific synthesis controls rather than a generic parameter dump.</sub>
    </td>
  </tr>
</table>

## `.dw` project contract

`.dw` is the **single project contract** of DAWWW-CORE.

The live runtime is serialized through `ProjectRuntimeSerializer` and the `DWFormat` / `DWPackagePipeline` layer. The reverse path restores the runtime through `ProjectRuntimeRestorer`. The package is not a lightweight interchange file or an Android subset: it is the portable representation of the project.

A valid `.dw` is expected to preserve the project information needed to rebuild the session, including project structure, instrument/effect snapshots and sampler assets referenced by the project. The cross-device certification criteria explicitly cover:

- accepted import;
- valid checksum;
- sampler assets present;
- instrument/effect snapshots preserved;
- re-export from the destination surface.

The `.dw` proof stack also includes format validation, portability invariants, fuzz testing, export verification, runtime serialization/restoration, engine rendering, audio parity, **cross-device rendering** and **production-parity** tests.

## Cross-device architecture

DAWWW-CORE is **100% cross-device by project contract**.

Desktop and Android are two application surfaces over the same project model, not two products with partially compatible files.

```text
Desktop Web runtime
        │
        ├── ProjectRuntimeSerializer
        ▼
     .dw project
        │
        ├── ProjectRuntimeRestorer
        ▼
Android / Capacitor runtime
        │
        ├── ProjectRuntimeSerializer
        ▼
     same .dw
        │
        └── back to Desktop without conversion
```

The contract is intentionally strict:

- **one `.dw` schema** for both platforms;
- **same project semantics** for arrangement, MIDI/note data, instruments, effects, automation and routing state represented by the project;
- **same serializer/restorer rules**;
- **import and re-export in both directions**;
- **no Android-only reduced project format**;
- **no conversion step when moving Desktop → Android → Desktop**;
- **cloud sync is optional infrastructure, not the compatibility mechanism**.

Android is still an upcoming subscription product, but that affects distribution and release qualification, **not the cross-device contract**. The Android surface is designed to implement the complete DAWWW-CORE project model, not a companion/viewer subset.

| Surface | Availability | Access model | Project model |
| --- | --- | --- | --- |
| **Desktop Web** | Available now | No payment | Full `.dw` runtime |
| **Android** | Coming | Subscription | Same full `.dw` runtime contract |
| **Project transfer** | Desktop ↔ Android | File/local transfer and future service layers | No format conversion |
| **Cloud project sync** | Not required | Optional | Never required for a project to exist |

## Persistence, recovery and local storage

Desktop uses browser-local storage/database infrastructure as the primary working persistence layer.

The project stack contains explicit save and recovery mechanisms: serialization/restoration, save-trust state, recovery flows and a local-database repair path. `.dw` is the durable external boundary: once exported, a project exists independently from the browser database.

Browser storage has no universal fixed quota. Capacity and eviction policy depend on the browser, profile, operating system and device. That means DAWWW-CORE cannot publish one meaningful storage figure that applies to every user.

Large sample libraries and many locally stored projects are therefore limited by the host browser's storage policy. Periodic `.dw` export is recommended for important projects because it provides a portable copy outside browser persistence.

## Validation strategy

The production repository uses several layers of validation rather than a single global test number.

### Unit and integration tests

**Vitest** covers audio-engine code, storage, project format, instruments/effects, serialization/restoration and other runtime components.

The portability-critical `test:dw:proof` suite has a last documented count of **459 tests**. Its selected coverage includes:

- `DWPackagePipeline`;
- `DWPortabilityInvariants`;
- `DWFormat` and fuzz tests;
- `DWExportVerification`;
- `DWCrossDeviceRender`;
- `DWProductionParity`;
- `ProjectRuntimeSerializer` / `ProjectRuntimeRestorer`;
- `EngineRenderService`;
- `AudioParity.integration`;
- playback fixture builders and production synth gates.

### Desktop module certification

Dedicated certification profiles exist for:

- sequencer, arranger, piano roll and mixer **1-minute module fixtures**;
- dedicated **1-minute stress fixtures** for the same modules;
- transport/shared-state checks;
- **1-hour continuous-work** stability;
- **1-hour stress** stability;
- **1-hour alternating-sync** stability;
- complete Desktop certification and scoped release-candidate gates.

### E2E and performance

**Playwright** is used for browser E2E/performance scenarios. The repository also contains performance reporting, regression gates and specific export/stems budget tests.

### Retained release evidence

The last retained documented Desktop freeze is dated **2026-07-18**. At that freeze:

- 9 tracked Desktop components were green through composed evidence;
- the visible Desktop `complete-gate` reported **12/12 passed**;
- `findings=0` and `advisoryFindings=0` were retained for that gate;
- a long Desktop playback gate reached **55 minutes**;
- `.dw` export/import proof was retained.

The application has changed since that freeze, so those figures are retained technical evidence rather than a statement that every later commit automatically inherits the same result. Release claims are rerun through the scoped release gate.

## Current session envelope and practical limits

DAWWW-CORE currently does **not publish arbitrary hard caps** for track count, note count, project duration, simultaneous voices or `.dw` size. The Desktop audio engine runs locally, so a single hard number would be misleading across different machines.

The practical session ceiling is mainly determined by:

- **real-time CPU budget** — synth voices, effects, analyzers and complex routing all consume Web Audio processing time;
- **memory** — decoded samples, buffers, render state and large projects consume browser-process memory;
- **browser storage quota** — local projects and assets share quota controlled by the host browser/platform;
- **export workload** — long masters and many stems increase render time and temporary memory use;
- **audio device / browser implementation** — latency and stable real-time capacity vary across systems.

The existing 1-minute module/stress fixtures and 1-hour stability profiles are **validation envelopes**, not claims of unlimited session size. The retained 55-minute playback proof demonstrates a long-running tested path, not an infinite-duration guarantee for every possible graph.

For very sample-heavy, highly polyphonic or heavily processed sessions, the effective limit is therefore the local device. Important sessions should also be exported periodically as `.dw` so project recovery does not depend on one browser profile.

### Export limits

**WAV** is the baseline export path. **MP3 is capability-gated** and depends on the available runtime path; the project does not ship a universal LAME/Shine/FFmpeg/libmp3lame fallback encoder in the normal runtime.

### Browser variability

AudioWorklet behaviour, codec support, storage quotas, memory limits and audio-device latency are browser/platform dependent. A browser/OS combination should only be described as certified once it has been explicitly rerun through the relevant checks.

### Android release state

Android already has a Capacitor build path plus Android-specific build, worklet, security and bundle-budget tooling. The public Android application is still upcoming. Device qualification belongs to Android release engineering; **the project contract itself remains the same full cross-device `.dw` contract described above.**

## Current scope

The current product does not depend on:

- mandatory cloud project synchronization;
- real-time collaboration;
- iOS;
- a third-party plugin marketplace.

The engineering focus is the audio runtime, production surfaces, project portability/recovery and one complete Desktop ↔ Android project model.

## Public technology stack

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · browser-local storage · `Capacitor` for Android

The private production repository also contains dedicated QA, compatibility, recovery, observability, security and release tooling. This public repository presents the product without exposing operational or security-sensitive internals.

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

`Daw-core-desktop` is the **public technical/product showcase for DAWWW-CORE**.

The production application and audio engine remain private. This repository documents architecture, available surfaces, validation strategy, project portability, platform model and current limits without publishing deployment configuration, provider contracts, security mechanisms or other sensitive internals.

---

<div align="center">

### One project. Desktop and Android. No conversion layer.

[**Open DAWWW-CORE Desktop**](https://dawww-core-local.com/app)

</div>
