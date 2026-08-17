<div align="center">

# DAWWW-CORE

### Local-first web music production studio

Compose, sequence, arrange, mix and export directly from your desktop browser — without making the cloud mandatory for your creative workflow.

[![Desktop Web](https://img.shields.io/badge/Desktop-available%20without%20payment-111827?style=flat-square)](https://dawww-core.com/studio)
[![Android](https://img.shields.io/badge/Android-coming%20%7C%20subscription-111827?style=flat-square)](#desktop-now--android-coming)
[![Cross-device](https://img.shields.io/badge/projects-100%25%20cross--device-111827?style=flat-square)](#desktop-now--android-coming)
[![Local-first](https://img.shields.io/badge/design-local--first-111827?style=flat-square)](https://dawww-core.com)
[![Project format](https://img.shields.io/badge/projects-.dw-111827?style=flat-square)](https://dawww-core.com/docs)
[![Source](https://img.shields.io/badge/source-private-111827?style=flat-square)](#about-this-repository)

[Open DAWWW-CORE](https://dawww-core.com/studio) · [Guides](https://dawww-core.com/docs) · [Status](https://dawww-core.com/status) · [Français](README.md)

</div>

---

## What is DAWWW-CORE?

DAWWW-CORE is a digital audio workstation designed for the desktop browser. The project aims to combine the immediate access of a web application with a structured music-production workflow: capture an idea, build patterns, arrange a timeline, shape sounds, mix, and export without a heavy installation process.

The product follows a **local-first** approach: projects and creative content remain primarily under the user's control. Optional online services are not the primary source of your creations.

## Desktop now · Android coming

| Platform | Availability | Model | Project continuity |
| --- | --- | --- | --- |
| **Desktop Web** | Available | **No payment on the desktop version** | Local and portable `.dw` projects. |
| **Android** | **Coming** | **Subscription** | **100% cross-device with Desktop** through the same `.dw` project contract. |

The Android version is designed as the mobile continuation of the studio: a project should move from Desktop to Android and back to Desktop without introducing a separate format or workflow.

The stated goal is a **100% cross-device** experience: same project, same `.dw` format, continuous work across both platforms.

## The studio

| Surface | What it provides |
| --- | --- |
| **Sequencer** | Pattern creation and rhythmic/melodic organization. |
| **Piano roll** | Note editing and MIDI programming. |
| **Arranger** | Song construction on a timeline. |
| **Mixer** | Routing, levels, processing and mix organization. |
| **Built-in instruments** | Sound creation directly inside the studio. |
| **Effects** | Processing chains integrated into the mixing workflow. |
| **Automation** | Time-based control of project parameters. |
| **Audio export** | Song rendering and export workflows according to platform capabilities. |
| **`.dw` projects** | Portable project format for saving, moving and restoring sessions. |

## A local-first workflow

```text
Create / import
      ↓
Sequencer + Piano roll
      ↓
Arranger
      ↓
Instruments + Effects + Automation
      ↓
Mixer
      ↓
Audio export / .dw project save
```

The `.dw` format is a core part of the product: it provides a portable way to preserve and move a project without requiring mandatory cloud synchronization, and forms the basis of cross-device continuity between Desktop and Android.

## Built for desktop web

DAWWW-CORE uses modern browser capabilities to deliver a rich audio-creation environment while keeping the studio directly accessible from the web.

Design principles:

- **local-first** projects and creative content;
- **portability** through the `.dw` project format;
- a **complete workflow** from pattern creation to export;
- a **desktop-focused interface** designed for dense music-production work;
- **modern web audio** built around Web Audio and AudioWorklet;
- **progressive web app** capabilities to bring the web experience closer to an installed application;
- **Desktop ↔ Android cross-device continuity** built around the same `.dw` project contract.

## Product stack

The desktop surface is primarily built around:

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · browser-local storage

The application also relies on specialized services for functions outside locally stored creative content, including account access, observability and web distribution. **The desktop version no longer includes a payment flow.**

## Privacy by design

The product principle is straightforward: **a music project should not need to live in a cloud in order to exist**.

DAWWW-CORE therefore prioritizes local storage for creative content and the ability to export a portable project. Account services remain separate from the musical content used as the primary project source.

## Project status

**DAWWW-CORE Desktop** is actively developed and available without payment on the desktop version. Priority is given to audio-engine reliability, project portability, the desktop workflow and validation of critical paths.

**DAWWW-CORE Android** is announced as an upcoming platform, offered by subscription and designed for 100% cross-device continuity with Desktop projects.

Features and platform limitations may evolve during development. The product's public pages remain the reference for user-visible status.

## Links

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

This repository is the **public presentation for DAWWW-CORE Desktop**, along with the upcoming cross-device Android continuity.

It exists to present the product, its positioning, its capabilities and its public links. **Production source code is not distributed through this repository**, and the content here should not be interpreted as an open-source release of the engine or application.

Internal architecture details, secrets, deployment configuration, provider contracts and security-sensitive material are intentionally kept outside this public showcase.

---

<div align="center">

**DAWWW-CORE** — make music in the browser without giving up control of your projects.

</div>
