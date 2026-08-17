<div align="center">

# DAWWW-CORE

### A real music production workstation in your browser.

**Compose. Sequence. Arrange. Mix. Automate. Export.**  
No heavy installation, no payment on Desktop, and no mandatory cloud ownership of your creative work.

[![Desktop](https://img.shields.io/badge/Desktop-available%20without%20payment-111827?style=for-the-badge)](https://dawww-core.com/studio)
[![Android](https://img.shields.io/badge/Android-coming%20%7C%20subscription-111827?style=for-the-badge)](#desktop-now--android-next)
[![Cross-device](https://img.shields.io/badge/projects-100%25%20cross--device-111827?style=for-the-badge)](#desktop-now--android-next)
[![Local-first](https://img.shields.io/badge/architecture-local--first-111827?style=for-the-badge)](#local-first-by-design)
[![Project format](https://img.shields.io/badge/projects-.dw-111827?style=for-the-badge)](#dw--a-project-you-can-keep)

[**Open the Studio**](https://dawww-core.com/studio) · [Guides](https://dawww-core.com/docs) · [Tutorials](https://dawww-core.com/tutorials) · [Roadmap](https://dawww-core.com/roadmap) · [Français](README.fr.md)

</div>

---

## The browser can be a real studio

DAWWW-CORE is a desktop digital audio workstation built around a simple idea: **opening a browser should not mean accepting a reduced music-production workflow**.

The studio brings the core stages of production into one workspace: pattern creation, note editing, arrangement, instruments, effects, automation, mixing and export. The goal is not to ship a DAW demo or a disposable musical sketchpad. It is to provide a coherent environment where an idea can become a finished track.

The **Desktop version is available without payment**. Open the studio from the web, work on your project, then keep that work in a portable `.dw` project format that remains under your control.

DAWWW-CORE is also designed to go further. An **Android version is coming as a subscription product**, built around **100% cross-device project continuity** with Desktop.

> One project. One format. Two platforms. Not two disconnected workflows.

## At a glance

| | DAWWW-CORE |
| --- | --- |
| **Desktop Web** | Available now, **no payment** |
| **Android** | **Coming**, subscription-based |
| **Continuity** | **100% cross-device Desktop ↔ Android** |
| **Project format** | Portable `.dw` sessions |
| **Product philosophy** | Local-first, no mandatory cloud for creative content |
| **Studio workflow** | Sequencer, piano roll, arranger, mixer, instruments, effects, automation |
| **Outputs** | Audio export, master and stem workflows where supported |
| **Core technologies** | TypeScript, React, Vite, Web Audio API, AudioWorklet, PWA |
| **Production source** | Private — this repository is the public product showcase |

## From an idea to a track, in one workspace

DAWWW-CORE is designed to keep the creative process continuous instead of splitting each stage across disconnected tools.

```text
New idea / import
        ↓
Patterns & sequencer
        ↓
Piano roll / note editing
        ↓
Arranger & timeline
        ↓
Instruments + effects
        ↓
Automation
        ↓
Mixer & routing
        ↓
Master / stems / audio export
        ↓
Portable .dw project
```

Start with a pattern, expand the structure in the arranger, refine notes in the piano roll, shape sounds, automate parameters, build the mix and prepare the export without leaving the studio.

## What the studio brings together

### Sequencer

Build rhythmic and melodic patterns quickly, organize musical material and turn a first loop into something ready to develop inside the arrangement.

### Piano roll

Edit notes inside a dedicated MIDI-writing surface. Placement, duration, structure and musical precision remain part of the same project workflow.

### Arranger

Move from pattern to full track. The timeline gives the project a central structure for sections, transitions, repetition and progression.

### Mixer

Handle levels, routing and processing from a dedicated mixing surface that stays connected to the rest of the studio instead of feeling like an isolated final-stage tool.

### Built-in instruments

DAWWW-CORE includes its own instruments and dedicated editors so sound creation can happen directly inside the project without requiring an external plugin collection just to start producing.

### Effects

Audio processing is integrated into the mixing and automation workflow. Filtering, dynamics and other treatments can become part of the musical construction rather than an afterthought.

### Automation

Write parameter movement over time. Mix changes, effects, transitions and evolving textures can become part of the composition instead of being reproduced manually on every playback.

### Audio export

A session only matters if it can leave the studio. DAWWW-CORE includes master and stem-oriented export workflows according to the capabilities available on the platform.

## `.dw`: a project you can keep

The `.dw` project format is one of the central pieces of DAWWW-CORE.

A browser project should not be trapped in a tab, permanently depend on a remote database, or become inaccessible because a synchronization service is unavailable. `.dw` is designed as **the portable container for a DAWWW-CORE project**: a way to save, move, restore and transfer a session.

That portability serves two important goals:

- preserving a local exit path for your creative work;
- providing the common project contract required for the future Desktop ↔ Android workflow.

Cloud services can be useful around a product. They should not have to become the technical owner of the music itself.

## Local-first by design

DAWWW-CORE starts from a deliberately different assumption than a cloud-first workflow: **creative content exists primarily on the user's device**.

That means the core product is designed around local storage, project portability and recoverability. Optional online services remain peripheral to that model and are not treated as the primary source of the musical project.

The practical goal is straightforward: keep control of project files, reduce unnecessary network dependencies, make sessions portable and preserve a recovery path that users can actually understand.

## Desktop now · Android next

### Desktop Web — available now

Desktop is the primary DAWWW-CORE surface today. It is designed for larger displays, dense workflows and extended work in the timeline, piano roll and mixer.

**There is no longer a payment flow on the Desktop version.** The Desktop studio is intended to remain the direct web entry point into DAWWW-CORE.

It uses modern browser technologies and can take advantage of a PWA-style experience to move closer to the convenience of an installed application while keeping web distribution.

### Android — coming as a subscription

Android is not being positioned as a separate product or a simple mobile viewer. The upcoming version is designed as **the cross-device continuation of the same studio**.

It will be offered **by subscription** and is being built around full project compatibility with Desktop: open the same `.dw`, continue working on Android, then return to Desktop without converting the project into a second format.

```text
Desktop
   ↓
 .dw project
   ↓
Android
   ↓
 same .dw project
   ↓
Desktop
```

The product goal is **100% cross-device project continuity** while preserving the local-first model. Cross-device therefore does not mean “mandatory cloud sync”: portable project ownership remains a fundamental part of the design.

## Why build a DAW for the web?

Because the web offers an immediate, continuously deployable and broadly accessible application platform, while modern browser audio capabilities can support far more than a basic player or demo sequencer.

DAWWW-CORE uses technologies such as the **Web Audio API** and **AudioWorklet** to build an audio architecture suited to real-time browser processing.

The goal is not to reproduce a traditional desktop workstation pixel for pixel. It is to preserve what matters in a serious production workflow — control, continuity, precision and portability — while taking advantage of the web as a distribution and application platform.

## Public technology stack

The Desktop surface is primarily built with:

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · browser-local storage

The wider product also includes dedicated layers for testing, observability, project compatibility and distribution. Sensitive internal architecture and production details are intentionally not published in this repository.

## Reliability before showcase metrics

A DAW cannot be judged only by screenshots. A polished interface does not compensate for unstable transport, fragile project restoration or an export path that fails when it matters.

DAWWW-CORE development therefore places strong emphasis on critical paths: transport and playback, stability of the main studio modules, `.dw` portability, project restoration, audio export, routing and the platform-specific behavior that matters on Desktop and Android.

This public repository does not turn internal QA evidence into inflated marketing numbers. It presents the product and its direction; detailed release gates, validation artifacts and security-sensitive implementation remain private.

## Who is DAWWW-CORE for?

DAWWW-CORE is especially relevant for people who want to:

- start a production session quickly from a desktop browser;
- work with something more complete than a lightweight music sketchpad;
- keep projects in a portable file format;
- produce without making cloud synchronization mandatory;
- move from composition to mixing and export inside one environment;
- prepare for a workflow where the same project can continue on Android.

## Project status

**DAWWW-CORE Desktop** is actively developed and is the currently available product surface. The Desktop version is available **without payment**.

**DAWWW-CORE Android** is an **upcoming** platform, planned as a **subscription** product with **100% cross-device project continuity** with Desktop as a core product goal.

The product continues to evolve. Interfaces, features, compatibility and platform limits may change as development progresses. Official public product pages remain the reference for user-facing information.

## Resources

- **Website** — https://dawww-core.com
- **Desktop Studio** — https://dawww-core.com/studio
- **Guides** — https://dawww-core.com/docs
- **Tutorials** — https://dawww-core.com/tutorials
- **FAQ** — https://dawww-core.com/faq
- **Status** — https://dawww-core.com/status
- **Roadmap** — https://dawww-core.com/roadmap
- **Changelog** — https://dawww-core.com/changelog
- **Contact** — https://dawww-core.com/contact

## About this repository

`Daw-core-desktop` is the **public GitHub showcase for DAWWW-CORE**.

The repository documents the product, its direction, its main surfaces and its platform model. **The production source code for the application and audio engine remains private**; this repository is not an open-source distribution of DAWWW-CORE.

Secrets, production configuration, deployment internals, provider contracts, security mechanisms and other sensitive implementation details are intentionally kept outside this public repository.

---

<div align="center">

### Open the studio. Keep the project.

**DAWWW-CORE — music production on the web, with your project still under your control.**

[Open DAWWW-CORE](https://dawww-core.com/studio)

</div>
