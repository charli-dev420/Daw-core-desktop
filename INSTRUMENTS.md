<div align="center">

# DAWWW-CORE · Instruments & synthesis

### 51 built-in instruments designed to make a new project immediately playable.

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Main overview](README.md) · [Cross-device](CROSS_DEVICE.md) · [Modules](MODULES.md) · [Effects](EFFECTS.md)

</div>

---

DAWWW-CORE currently includes **50 dedicated synthesis engines plus one sampler**. The goal is not to replace every external plugin ecosystem, but to give the DAW a broad internal sound palette that works directly inside the project and moves with it across devices.

## Instrument families

| Family | Count | Included instruments |
| --- | ---: | --- |
| **Orchestra** | 12 | Violin, viola, cello, contrabass, trumpet, French horn, trombone, tuba, flute, oboe, clarinet, bassoon |
| **Drums** | 12 | Kick, snare, hand clap, closed/open hi-hat, low/mid/high toms, cowbell, rimshot, claves, maracas |
| **Bass** | 3 | Sub, acid, Reese |
| **Electronic** | 7 | Mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys, noise/transition FX |
| **Pads** | 5 | Warm, glass, choir, evolving, ambient |
| **Keys & bells** | 7 | Acoustic piano, electric piano, clavinet, tonewheel organ, celesta, music box, tubular bell |
| **Guitars** | 4 | Nylon, steel-string, clean electric, driven electric |
| **Sampler** | 1 | Sample-based instrument workflow |

## Dedicated sound engines, not only preset names

Many of the instruments are separate sound engines rather than a single generic synth hidden behind renamed presets. That lets DAWWW-CORE adapt the device interface to the type of sound being produced.

For example, percussion devices can expose controls relevant to transients and decay, while an Electric Piano can present tone shaping, tremolo and envelope-oriented controls.

<p align="center">
  <img src="asset/capture/Screenshot_20260817-034152.png" alt="DAWWW-CORE Electric Piano editor" width="88%" />
</p>

## Instruments inside the writing workflow

The instrument Browser is connected directly to the production modules. Instruments can be used from the sequencer and then edited alongside the piano roll or other project surfaces without leaving the session.

<p align="center">
  <img src="asset/capture/Screenshot_20260817-034141.png" alt="DAWWW-CORE instrument editor with piano roll" width="88%" />
</p>

This makes the built-in palette useful for more than previewing sounds: the instrument state remains part of the project as the track moves through sequencing, arrangement, automation and mixing.

## Drums and detailed steps

The drum family works naturally with the sequencer’s per-step controls. A pattern can use velocity, probability, gate, ratchets, articulation and timing offset to create variation before the project reaches the arranger or mixer.

That combination is especially useful for percussion because the sequencing detail and the drum sound engine remain in one workflow.

## Sampler content and portability

The sampler extends the built-in synthesis palette with sample-based instruments. Referenced sampler content required by a project is part of the portability considerations of `.dw`, so the project model is designed around more than parameter-only synth sessions.

## Instruments across Desktop and Android

Instrument state is part of the DAWWW-CORE project rather than a Desktop-only layer. The cross-device model is built around carrying the project, including its instrument configuration, between Desktop and Android without creating a separate mobile project format.

[Read the cross-device overview →](CROSS_DEVICE.md)

## Practical performance

The number of instruments listed above is not a statement that every engine can run at maximum polyphony simultaneously on every device. DAWWW-CORE runs locally, so practical session capacity depends on CPU, memory, browser/runtime behavior, polyphony, active effects and routing complexity.

A light instrument can cost much less than a highly polyphonic or heavily processed one. For this reason, DAWWW-CORE describes its sound palette separately from the maximum practical size of a session.

---

<div align="center">

[**Open DAWWW-CORE Desktop →**](https://dawww-core-local.com/app)

[Main overview](README.md) · [Cross-device](CROSS_DEVICE.md) · [Modules](MODULES.md) · [Effects](EFFECTS.md)

</div>
