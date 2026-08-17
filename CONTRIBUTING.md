# Contributing to the DAWWW-CORE public showcase

Thank you for helping improve DAWWW-CORE.

This repository is the **public product showcase, documentation and feedback surface**. The production application source code is maintained privately, so contribution here is primarily about product feedback, reproducible testing, documentation corrections and clear requests rather than production-code pull requests.

## Best ways to contribute

### Report a reproducible bug

Use the dedicated **Bug report** issue form and include the browser, platform, steps to reproduce and visible result. A small reproducible project description is more useful than speculation about the internal cause.

### Propose a feature

Use the **Feature request** form. Explain:

1. the current workflow;
2. the friction or limitation;
3. the desired result;
4. why it matters in a real production session.

### Request an instrument or effect

Use the **Instrument / FX request** form. Describe the musical or processing role, useful controls and typical context rather than naming a plugin to clone.

### Test cross-device behavior

Use the **Cross-device feedback** form for `.dw` Desktop ↔ Android portability. State the source and destination platform and what was preserved after transfer.

### Improve documentation

Documentation corrections are welcome when they concern public behavior: inaccurate wording, broken links, unclear explanations, missing examples or outdated screenshots.

For a small correction, opening an Issue is sufficient. A documentation-only pull request may also be considered when it changes only public showcase/documentation content and does not assume access to private production internals.

## What not to submit

Please do not submit:

- production implementation code intended to replace private application internals;
- reverse-engineered private implementation details;
- copied proprietary plugin code or copyrighted material without permission;
- secrets, API keys, credentials or private user/project data;
- vulnerability details in a public Issue — use [SECURITY.md](SECURITY.md).

## Writing a useful report

Prefer observable facts:

- **Good:** “On Chrome 151 / Windows 11, exporting after these four steps produces a silent file.”
- **Less useful:** “The audio engine probably has a race condition.”

For performance reports, include approximate track count, instrument count, FX count, sample usage and session duration.

## Product decisions

A request being technically possible does not mean it will automatically become part of DAWWW-CORE. Changes are evaluated against product coherence, cross-device project compatibility, local-first behavior, performance, stability and maintenance cost.

See [SUPPORT.md](SUPPORT.md) for the support workflow and [SECURITY.md](SECURITY.md) for private vulnerability reporting.