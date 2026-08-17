<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="DAWWW-CORE emblem" width="170" />

# DAWWW-CORE

### Browser-native DAW · local-first projects · portable `.dw` format

DAWWW-CORE is a desktop-oriented digital audio workstation built on **Web Audio API + AudioWorklet**, with a React/TypeScript application layer, browser-local project storage and a portable project contract shared with the upcoming Android application.

[![Desktop](https://img.shields.io/badge/Desktop-AVAILABLE%20NOW-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Desktop access](https://img.shields.io/badge/Desktop-NO%20PAYMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Instruments](https://img.shields.io/badge/Built--in%20instruments-51-111827?style=for-the-badge)](#production-tools)
[![Effects](https://img.shields.io/badge/Built--in%20effects-16-111827?style=for-the-badge)](#production-tools)
[![Android](https://img.shields.io/badge/Android-COMING%20%7C%20SUBSCRIPTION-111827?style=for-the-badge)](#cross-device-model)

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Product](https://dawww-core-local.com/en/studio) · [Documentation](https://dawww-core-local.com/en/docs) · [Status](https://dawww-core-local.com/en/status) · [Français](README.fr.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="DAWWW-CORE desktop project surface" width="100%" />
</p>

## Technical overview

DAWWW-CORE is designed as a **local-first workstation**, not as a cloud sequencer. The account layer, public website and optional online services are separate from the creative project runtime. The authoritative working session lives locally, and `.dw` provides the portable project representation used for export/import, recovery and cross-device compatibility.

| Layer | Current implementation | Role |
| --- | --- | --- |
| **Application UI** | TypeScript, React, Vite | Desktop workspace, project surfaces, editors and routing |
| **Audio runtime** | Web Audio API | Audio graph, instruments, mixer, effects and playback |
| **Timing / DSP workers** | AudioWorklet | Timing-critical processing and worklet-based audio tasks outside the React render loop |
| **Transport / synchronization** | Shared transport + sync modules | Playback position, sequencer/arranger timing and shared runtime state |
| **Project runtime** | Serializer / restorer services | Converts live application state to and from the persistent project representation |
| **Local persistence** | Browser-local database/storage | Primary working storage for projects and creative state |
| **Portable project** | `.dw` package pipeline | Export/import, recovery and platform-neutral project transfer |
| **Desktop delivery** | Web app + PWA-oriented build | Direct browser access without a traditional installer requirement |
| **Android delivery** | Capacitor Android build | Upcoming subscribed application using the same project contract |
| **Validation** | Vitest, Playwright, dedicated certification/gate scripts | Unit, integration, portability, playback, module, stress and release checks |

The main architectural boundary is intentional: **React controls the application; Web Audio controls the audio graph**. UI rendering is not the audio scheduler. Timing-sensitive code is kept in the audio/runtime layer, including AudioWorklet-backed components and a shared transport model.

## Audio runtime

The audio engine runs entirely on the client device. There is no remote audio-rendering service required for normal Desktop playback.

At runtime, DAWWW-CORE builds a Web Audio graph from project state: instruments feed tracks, tracks pass through routing and processing, and the mixer ultimately feeds the master path. Transport and synchronization modules provide the common timing reference used by the sequencer, arranger and playback state.

AudioWorklet is used where browser main-thread scheduling is not sufficient. The codebase contains dedicated worklet paths for clock/timing and selected processing/analyser workloads. This reduces the dependency of audio timing on React rendering or DOM activity, although the final real-time capacity still depends on the user's browser, CPU, memory and audio device.

Export is treated as a separate technical path from interactive playback. The codebase contains dedicated exporter/render services and parity tests so project rendering can be validated independently from the UI.

## Production tools

The current Desktop application exposes the main surfaces expected from a DAW rather than a single monolithic editor.

| Surface | Available capabilities | Validation present in the codebase |
| --- | --- | --- |
| **Transport** | Play/stop state, project time, shared timing | Playback fixtures and transport certification profiles |
| **Sequencer** | Pattern tracks and step programming | Module fixture + stress fixture |
| **Step editor** | Velocity, chance/probability, gate, ratchet, articulation, timing offset | Covered through sequencer/runtime tests |
| **Piano roll** | Note-level MIDI editing | Module fixture + stress fixture |
| **Arranger** | Timeline/song structure | Module fixture + stress fixture |
| **Mixer** | Channels, level, routing, sends/processing, master path | Unit coverage plus routing/PDC/send scenarios |
| **Automation** | Parameter automation and live effect automation paths | Dedicated automation/effects scenario |
| **Project I/O** | Local save, restore, `.dw` import/export | Dedicated `.dw` proof suite and runtime serializer/restorer tests |
| **Audio export** | Master and stem-oriented export; WAV baseline, MP3 when capability is available | Export scenarios, long-export checks and performance budget tests |

### 51 built-in instruments

The internal registry currently contains **50 dedicated synthesis engines plus the sampler**. They are grouped by musical role rather than shipped as one generic synth with different presets:

- **12 orchestral engines:** violin, viola, cello, contrabass, trumpet, French horn, trombone, tuba, flute, oboe, clarinet and bassoon;
- **12 drum engines:** kick, snare, hand clap, closed/open hi-hat, low/mid/high toms, cowbell, rimshot, claves and maracas;
- **3 bass engines:** sub, acid and Reese;
- **7 electronic engines:** mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys and noise/transition FX;
- **5 pad engines:** warm, glass, choir, evolving and ambient;
- **7 keys/bells engines:** acoustic piano, electric piano, clavinet, tonewheel organ, celesta, music box and tubular bell;
- **4 guitar engines:** nylon, steel-string, clean electric and driven electric;
- **1 sampler** for sample-based instruments.

Several families expose dedicated device editors instead of a universal parameter panel. The instrument UI can therefore reflect the synthesis model: for example, the Electric Piano editor exposes its own tone-shaping, tremolo and envelope controls, while percussion devices use controls relevant to transient design.

### 16 built-in effects

The current built-in processing registry contains:

`8-band parametric EQ` · `Compressor` · `Convolution Reverb` · `Tempo-synced Delay` · `Chorus` · `Flanger` · `Phaser` · `Distortion` · `Filter` · `Gate` · `Limiter` · `Saturator` · `Tremolo` · `Vibrato` · `Bitcrusher` · `Utility`

These processors are part of the mixer/automation architecture rather than a separate post-processing application.

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
      <sub><b>Mixer</b> — channel routing, inserts/processing, levels and master stage.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="DAWWW-CORE piano roll and instrument device" width="100%" /><br />
      <sub><b>Piano roll + device</b> — note editing and instrument controls remain connected to the same live project.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="DAWWW-CORE electric piano device editor" width="82%" /><br />
      <sub><b>Dedicated instrument editor</b> — device-specific synthesis controls instead of a generic parameter dump.</sub>
    </td>
  </tr>
</table>

## `.dw` project model

`.dw` is the compatibility boundary of DAWWW-CORE.

The live project runtime is serialised into a portable package through the `DWFormat` / `DWPackagePipeline` layer. The corresponding restore path reconstructs the runtime state from the package. The project pipeline is deliberately separated from the account layer so that a creative session is not defined by a server-side account record.

The `.dw` proof suite includes format validation, portability invariants, fuzz testing, export verification, runtime serialization/restoration, engine rendering, audio parity, **cross-device rendering** and **production-parity** checks.

That distinction matters for the Android roadmap: cross-device is not defined as “sync the same database row from two clients”. It is defined as **two runtimes implementing the same project contract**.

## Cross-device model

The target architecture is:

```text
Desktop Web runtime
        │
        ├── ProjectRuntimeSerializer
        │
        ▼
     .dw project
        │
        ├── ProjectRuntimeRestorer
        │
        ▼
Android / Capacitor runtime
```

The Desktop and Android surfaces are intended to share the project schema, runtime serialization rules and audio/project semantics. This is why the codebase contains cross-device `.dw` render tests and production-parity tests before the Android product is publicly released.

**100% cross-device is a project-compatibility target, not a claim that the current Android APK is already production-certified on every device.** The latest retained release documentation explicitly separates format/runtime evidence from native-device validation.

The public platform model is therefore:

| Surface | Status | Access | Project contract |
| --- | --- | --- | --- |
| **Desktop Web** | Available now | No payment | Current `.dw` reference surface |
| **Android** | Coming | Subscription | Same `.dw` contract / 100% compatibility target |
| **Cloud project sync** | Not required | — | Not the authority for project existence |

## Persistence, recovery and local storage

Desktop projects are primarily stored in browser-local storage/database infrastructure. This gives DAWWW-CORE the local-first behaviour, but it also creates constraints that are different from a server-backed DAW.

The project stack contains explicit save/recovery handling, including project serialization/restoration, save-trust state, recovery flows and a local-database repair path. `.dw` is the external recovery boundary: a project exported as `.dw` can exist independently from the browser database.

A browser does **not** provide a fixed universal storage quota. Available space and eviction behaviour depend on browser, profile, platform and device. DAWWW-CORE can reason about local storage state, but it cannot promise the same number of gigabytes on every machine. Large sample libraries and many locally stored projects therefore remain bounded by the browser's storage policy.

For that reason, `.dw` export is not only a sharing feature; it is also the durable escape path from browser-local persistence.

## Validation strategy

The production repository uses several different levels of validation rather than one global “tests passed” number.

### Unit and integration

**Vitest** covers the audio engine, storage, project format, instruments/effects, serialization, restoration and other runtime components.

The dedicated `test:dw:proof` command aggregates the portability-critical tests. The last documented proof count is **459 tests** and includes, among others:

- `DWPackagePipeline`;
- `DWPortabilityInvariants`;
- `DWFormat` + fuzz tests;
- `DWExportVerification`;
- `DWCrossDeviceRender`;
- `DWProductionParity`;
- `ProjectRuntimeSerializer` / `ProjectRuntimeRestorer`;
- `EngineRenderService`;
- `AudioParity.integration`;
- playback fixture builders and production synth gates.

### Desktop module certification

The repository contains explicit certification profiles for:

- sequencer, arranger, piano roll and mixer **1-minute module fixtures**;
- dedicated **1-minute stress fixtures** for those modules;
- transport/shared-state checks;
- **1-hour continuous-work**, **1-hour stress** and **1-hour alternating-sync** stability profiles;
- a complete Desktop certification gate and a scoped release-candidate gate.

### E2E and performance

**Playwright** is used for browser E2E/performance scenarios. The repository also contains performance reporting and a P5 regression gate, plus specific export/stems budget tests.

### Last retained documented proof

The last retained release freeze documented in the private repository is dated **2026-07-18**. At that point:

- the 9 tracked Desktop components were green through composed evidence;
- the visible Desktop `complete-gate` reported **12/12 passed** with `findings=0` and `advisoryFindings=0`;
- a long Desktop playback gate reached **55 minutes**;
- `.dw` export/import proof was retained;
- Android web build and account/billing preflight evidence existed, but **APK / physical device / native rendering / speaker output were not revalidated in that freeze**.

There have been later application/UI changes after that freeze. Those numbers should therefore be read as **retained technical evidence**, not as a claim that the current head has already been freshly recertified. A new release gate is required for a current release claim.

## Current session envelope and known limits

DAWWW-CORE does **not currently publish a certified hard maximum** for tracks, notes, project duration, simultaneous voices or project file size. Publishing arbitrary limits would be misleading because the Desktop runtime executes on the user's device.

The practical ceiling of a session is currently defined by several resources:

- **CPU / real-time audio budget** — more simultaneous synth voices, effects and routing increase Web Audio processing cost;
- **memory** — decoded audio, samples, render buffers and large project state consume browser-process memory;
- **browser storage quota** — local projects and imported assets share storage controlled by the browser/platform;
- **export workload** — long masters or many stems require additional render time and temporary memory;
- **audio device / browser implementation** — latency and stable real-time capacity are not identical across operating systems and browsers.

The existing 1-minute module/stress profiles and 1-hour stability profiles are therefore **validation envelopes**, not infinite-session guarantees. The 55-minute retained playback proof demonstrates a long-running Desktop path, but it is not a promise that every arbitrarily large project will run for unlimited time on every device.

For sample-heavy or highly polyphonic sessions, the current public guidance should be conservative: project complexity should be increased according to the actual machine, and important work should be exported periodically as `.dw`.

### Export limitations

WAV is the baseline audio-export path. **MP3 is capability-gated**: availability depends on the platform/runtime path and the project deliberately does not rely on a bundled LAME/Shine/FFmpeg/libmp3lame runtime encoder as a universal fallback.

### Browser compatibility

The codebase is browser-native, but the retained QA evidence does not certify every browser/OS combination as equivalent. AudioWorklet behaviour, storage quotas, codec/export support and device latency can vary. A public compatibility matrix should only list environments that are explicitly rerun and verified.

### Android status

The Android code path and build/audit tooling already exist, but Android remains an **upcoming product surface**. Cross-device `.dw` and runtime parity can be tested before the native product is released; real-device validation still has to be treated separately.

## Deliberate current scope

The current product is not based around:

- mandatory cloud project synchronization;
- real-time collaboration;
- iOS;
- a third-party plugin marketplace.

Those are outside the current active scope. The engineering focus remains the local project runtime, audio engine, core production surfaces, portability, recovery and Desktop ↔ Android project compatibility.

## Public stack

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · `Capacitor` · browser-local storage · `Vitest` · `Playwright`

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

`Daw-core-desktop` is the public technical/product presentation of DAWWW-CORE. The production application and audio engine are developed in a private repository.

This repository intentionally exposes the product architecture, available surfaces, validation model, platform strategy and known limits without publishing secrets, deployment configuration, private QA artifacts or security-sensitive implementation.

---

<div align="center">

**DAWWW-CORE Desktop — available now, no payment.**

[**Open the Desktop Studio**](https://dawww-core-local.com/app)

</div>
