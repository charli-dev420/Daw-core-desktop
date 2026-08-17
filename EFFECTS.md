<div align="center">

# DAWWW-CORE · Built-in effects

### 16 processors integrated into the mixer, automation and portable project workflow.

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Main overview](README.md) · [Cross-device](CROSS_DEVICE.md) · [Modules](MODULES.md) · [Instruments](INSTRUMENTS.md)

</div>

---

DAWWW-CORE currently includes **16 built-in effects**. They are part of the project and mixer workflow rather than a separate post-processing application, which means effect state can stay attached to the session, participate in automation and move with the project.

## Processing set

| Effect | Main role |
| --- | --- |
| **8-band Parametric EQ** | Tonal shaping and corrective EQ |
| **Compressor** | Dynamic-range control |
| **Convolution Reverb** | Space and ambience |
| **Tempo-synced Delay** | Rhythmic echoes and time-based effects |
| **Chorus** | Modulation / width |
| **Flanger** | Short-delay modulation |
| **Phaser** | Phase-based modulation |
| **Distortion** | Harmonic drive and saturation-style sound design |
| **Filter** | Frequency shaping and movement |
| **Gate** | Level-based control |
| **Limiter** | Peak control / output protection |
| **Saturator** | Harmonic coloration |
| **Tremolo** | Amplitude modulation |
| **Vibrato** | Pitch modulation |
| **Bitcrusher** | Digital degradation / texture |
| **Utility** | General signal-management tasks |

## Effects are part of the mix, not an afterthought

The effects belong to the same project workflow as tracks, routing, mixer channels and the master path. They can therefore be used while composing rather than only after a track has been exported.

<p align="center">
  <img src="asset/capture/Screenshot_20260817-034213.png" alt="DAWWW-CORE mixer" width="92%" />
</p>

This matters for projects where processing is part of the sound itself: a filter movement, delay change or distortion amount can be treated as part of the composition instead of as a separate mastering step.

## Automation

Effect parameters can participate in the automation model. That allows processing to evolve with the arrangement—for example, changing filter behavior, increasing an effect during a transition or moving a mix parameter over time.

Automation and effects remain part of the same project rather than being recreated manually every time the session is reopened.

## Effects travel with `.dw`

The cross-device model includes the state of instruments and effects represented by the project. Moving a `.dw` between Desktop and Android is therefore intended to preserve the creative processing choices of the session, not only its raw note data.

There is no separate Android effect preset format and no conversion layer between platforms.

[Read the cross-device overview →](CROSS_DEVICE.md)

## Effects and session capacity

Processing cost is one of the main factors that determines how large a local session can become.

A project with several convolution reverbs, high polyphony and complex routing can require much more CPU and memory than a project with many simple tracks. DAWWW-CORE therefore does not advertise a universal maximum track count: the effective limit depends on the actual audio graph and the device running it.

This is particularly important in a browser-native DAW because processing happens locally rather than on a remote render server.

## Export

The effects used in the project feed the audio-rendering workflow so the resulting master or stems can reflect the project’s processing. WAV is the baseline export path; some additional formats depend on platform/runtime capability.

---

<div align="center">

[**Open DAWWW-CORE Desktop →**](https://dawww-core-local.com/app)

[Main overview](README.md) · [Cross-device](CROSS_DEVICE.md) · [Modules](MODULES.md) · [Instruments](INSTRUMENTS.md)

</div>
