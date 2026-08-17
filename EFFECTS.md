<div align="center">

# DAWWW-CORE · 16-effect production catalog

### Use a processor because it solves a problem or creates a deliberate color.

[**Open Desktop Studio**](https://dawww-core-local.com/app) · [Detailed web catalog](https://dawww-core-local.com/effects.html) · [Tutorials](https://dawww-core-local.com/en/tutorials) · [Instruments](INSTRUMENTS.md) · [Mixer guide](https://dawww-core-local.com/en/docs/mixer)

</div>

---

DAWWW-CORE currently includes **16 built-in effects** integrated into the mixer, automation and portable project workflow. This reference focuses on **what each processor is for, what to listen to, a reliable starting method and the common mistake most likely to make the result worse**.

## Corrective and tonal shaping

### EQ · 8-band parametric

**Use it for:** tonal balance and corrective shaping.  
**Listen to:** frequency, gain and Q/bandwidth.  
**Start with:** remove one audible problem first; use broad gentle moves for general tone.  
**Avoid:** boosting several bands without a clear reason.  
**Good chain positions:** before compression for cleanup; after compression for final tonal shaping.

### Filter · multi-mode

**Use it for:** frequency range control and musical movement.  
**Listen to:** mode, cutoff and resonance.  
**Start with:** set the static tone first, then automate cutoff only if movement serves the arrangement.  
**Avoid:** high resonance creating harsh peaks or level jumps.  
**Useful on:** pads, bass, plucks, transitions and automated sections.

[Practice: automate a filter →](https://dawww-core-local.com/en/tutorials/filter-automation)

## Dynamics

### Compressor

**Use it for:** reducing dynamic variation and keeping a part in a stable place.  
**Listen to:** threshold, ratio, attack, release and output level.  
**Start with:** use only enough gain reduction to make the role more consistent.  
**Avoid:** using compression only because the processed signal becomes louder.  
**Useful on:** bass, drums, keys and other parts whose level changes make them disappear or jump forward.

### Gate

**Use it for:** removing unwanted low-level material or creating chopped dynamics.  
**Listen to:** threshold, attack and release/hold behavior.  
**Start with:** set threshold while monitoring the quietest event you still want to keep.  
**Avoid:** cutting natural tails or room character unintentionally.  
**Useful on:** drums, noisy samples and deliberate rhythmic gating.

### Limiter

**Use it for:** catching peaks and protecting an output ceiling.  
**Listen to:** how hard the signal enters the limiter, the ceiling and release behavior.  
**Start with:** balance the mix before inserting the limiter.  
**Avoid:** trying to repair an overly hot mix only with limiting.  
**Useful on:** master peak protection or intentionally aggressive bus processing.

## Space and time

### Convolution Reverb

**Use it for:** depth, room and atmosphere.  
**Listen to:** decay, pre-delay feel, brightness/damping and wet level.  
**Start with:** choose the space while listening to the full mix, not only the solo track.  
**Avoid:** long bright reverb on every channel.  
**Useful on:** pads, orchestra, snares, keys, samples and transitions.

### Tempo-synced Delay

**Use it for:** rhythmic echoes and repeated space.  
**Listen to:** time/division, feedback, tone and wet level.  
**Start with:** choose a repeat rhythm that fills a real gap in the phrase.  
**Avoid:** repeats masking the next note or feedback running longer than the arrangement needs.  
**Useful on:** leads, plucks, keys, rimshots and transition material.

## Modulation

### Chorus

**Use it for:** width and slow pitch/time modulation.  
**Listen to:** rate, depth and wet level.  
**Start with:** apply subtly to sustained or clean material.  
**Avoid:** widening every source, especially the low-end foundation.  
**Useful on:** pads, electric piano, clean guitar and carefully on Reese bass.

### Flanger

**Use it for:** metallic short-delay sweep and obvious motion.  
**Listen to:** rate, depth, feedback and mix.  
**Start with:** treat it as a deliberate color or transition effect.  
**Avoid:** deep permanent flanging on important transients.  
**Useful on:** FX, hats, guitars and transitional elements.

### Phaser

**Use it for:** moving phase coloration.  
**Listen to:** rate, depth, feedback and mix.  
**Start with:** keep the movement slower than the musical gesture you want to preserve.  
**Avoid:** high depth on every sustained layer.  
**Useful on:** pads, keys, guitars and synth leads.

### Tremolo

**Use it for:** rhythmic amplitude movement.  
**Listen to:** rate, depth and phase feel.  
**Start with:** make the pulse relate to the groove.  
**Avoid:** heavy depth on the main rhythmic anchor.  
**Useful on:** electric piano, pads, guitars and creative FX.

### Vibrato

**Use it for:** pitch movement.  
**Listen to:** rate and depth.  
**Start with:** shallow depth for musical movement, deeper settings for an obvious effect.  
**Avoid:** strong vibrato on sub-bass or tuning-critical layers.  
**Useful on:** leads, pads, keys and special FX.

## Harmonic color and degradation

### Distortion

**Use it for:** aggressive harmonics and nonlinear edge.  
**Listen to:** drive, tone, output and mix.  
**Start with:** level-match before deciding the more distorted version is better.  
**Avoid:** clipping the next processor because drive also raised output.  
**Useful on:** acid bass, leads, drums and deliberately driven textures.

### Saturator

**Use it for:** softer harmonic density, weight and color.  
**Listen to:** drive, curve/tone feel, output and mix.  
**Start with:** increase until the color is obvious, then back off slightly.  
**Avoid:** mistaking louder for warmer.  
**Useful on:** bass, drums, keys, guitars and very lightly on a master when justified.

### Bitcrusher

**Use it for:** lo-fi digital texture.  
**Listen to:** bit depth, sample-rate reduction and wet mix.  
**Start with:** blend smaller amounts before fully crushing the signal.  
**Avoid:** uncontrolled high-frequency harshness.  
**Useful on:** drums, chiptune material, hats, transitions and FX.

## Utility

### Utility

**Use it for:** gain trim, mono compatibility and polarity management.  
**Available roles:** gain trim, mono sum and phase invert.  
**Start with:** use it before or after processors to keep levels under control and to diagnose compatibility issues.  
**Avoid:** phase inversion or mono summing without listening to the consequence.  
**Useful on:** any channel, especially for gain staging and compatibility checks.

## Practical chains

These are **starting structures**, not presets that should be copied blindly.

| Goal | Starting chain | What to check |
| --- | --- | --- |
| **Clean a source** | EQ → Compressor | Does the source actually need both? |
| **Add weight** | EQ → Saturator | Gain-match the processed version |
| **Lead with depth** | EQ/Filter → Delay → Reverb | Keep the attack readable |
| **Wide clean keys** | Chorus → Reverb | Check mono compatibility |
| **Aggressive bass** | Distortion/Saturator → EQ → Compressor | Control output after drive |
| **Transition** | Filter → Delay/Reverb | Make the effect stop before the next section if needed |
| **Final peak control** | Utility/gain staging → Limiter | The limiter should not replace a balanced mix |

## The production rule

Before adding an effect, be able to finish this sentence:

> **“I am adding this processor because…”**

If the answer is only “it sounds more finished,” bypass it, match the level and listen again.

Recommended path:

**[Choose the source](INSTRUMENTS.md) → shape the instrument → add justified processing → [balance in the mixer](https://dawww-core-local.com/en/docs/mixer) → [prepare export](https://dawww-core-local.com/en/docs/export)**

Useful practice sessions:

- [Shape a sound](https://dawww-core-local.com/en/tutorials/shape-sound)
- [Make kick and bass coexist](https://dawww-core-local.com/en/tutorials/kick-bass-space)
- [Automate a filter](https://dawww-core-local.com/en/tutorials/filter-automation)
- [Create a transition](https://dawww-core-local.com/en/tutorials/create-transition)
- [Build a pad](https://dawww-core-local.com/en/tutorials/build-pad)

## Automation and `.dw`

Effect state and automation are represented by the project rather than a separate post-production document. The cross-device `.dw` model is designed to carry the creative processing state between Desktop and Android without a second mobile effect-preset format.

[Read the cross-device overview →](CROSS_DEVICE.md)

---

<div align="center">

[**Open DAWWW-CORE Desktop →**](https://dawww-core-local.com/app)

[Detailed web catalog](https://dawww-core-local.com/effects.html) · [Instruments](INSTRUMENTS.md) · [Mixer guide](https://dawww-core-local.com/en/docs/mixer) · [Tutorials](https://dawww-core-local.com/en/tutorials)

</div>
