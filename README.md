# ARP 2600

Documentation for the ARP 2600 at the [Frank-Ratchye STUDIO for Creative Inquiry](http://studioforcreativeinquiry.org), CMU.

[R. Luke DuBois](https://github.com/rev3rend), March 2016.

[Jet Townsend](https://github.com/functionalprototype), edits as needed, maintenance log


![overview](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/00overview.png "Overview")

### Introduction

The [ARP 2600](https://en.wikipedia.org/wiki/ARP_2600) is a 'semi-modular' [analog synthesizer](https://en.wikipedia.org/wiki/Analog_synthesizer) designed by Dennis Colin and [Alan Robert Pearlman](https://en.wikipedia.org/wiki/Alan_R._Pearlman) - [A.R.P.](https://en.wikipedia.org/wiki/ARP_Instruments) himself - and commercially released in 1971.  It was one of the first synthesizers extensively marketed for education, with a retail price of below $3,500.  It is considered one of the canonical synthesizers of its day, so a 'mint' (or fully-restored) ARP 2600 can easily fetch $10,000 or more today.

The ARP 2600 shows up in a lot of strange places... the synth was integral to the sound of artists ranging from [Jean Michel Jarre](https://en.wikipedia.org/wiki/Jean_Michel_Jarre) to [Joy Division](https://en.wikipedia.org/wiki/Joy_Division).  It's also well-known in the sound effects community because of its built-in envelope follower; sound designer [Ben Burtt](https://en.wikipedia.org/wiki/Ben_Burtt) used this to great effect in making the 'voice' of [R2-D2](https://en.wikipedia.org/wiki/R2-D2) in the Star Wars movies.

You can see an original ARP 2600 owner's manual [here](http://guitarfool.com/ARP2600/Arp%202600%20Owners%20Manual.pdf) and a service manual [here](http://guitarfool.com/ARP2600/2600ServiceManual.pdf).

#### Important:  ARP 2600 Cables Are Not 1/8" Audio Standard

The ARP synthesizers are built with Switchcraft(r) [Tini-Jax(r)](http://www.switchcraft.com/Category.aspx?Parent=60) sockets instead of standard 1/8" audio sockets.  The Tini-Jax connector is .141" in diameter, larger than a 1/8" jack (.125") or a contemporary 3.5mm jack (.138").  Contemporary plugs will work in a Tini-Jax socket but feel a bit loose even after the plug is fully inserted.

Because a Tini-Jax plug can destroy a 3.5mm or 1/8" socket we are not making vintage correct patch cables using Tini-Jax for the ARP 2600.  So far (11 August, 2019) we have not found **any** Tini-Jax cables in the STUDIO.

If you are working with other vintage analog synths in the STUDIO and bring in your own cables, verify with calipers whether or not you have Tini-Jax patch cables or 1/8" cables. 

### The Basics

The ARP 2600 is:
- **Semi-modular** : unlike pure modular synthesizers (like the [Buchla](https://en.wikipedia.org/wiki/Buchla_Electronic_Musical_Instruments), [Serge](https://en.wikipedia.org/wiki/Serge_synthesizer), and [Moog](https://en.wikipedia.org/wiki/Moog_synthesizer) synthesizers), the ARP 2600 has a *default internal wiring* between the individual modules (similar to [patchbay 'normalization'](https://en.wikipedia.org/wiki/Patch_panel#Normalization) in a recording studio) so that you could bring it home, plug it in, turn it on, and get sound out of the built-in speakers without any additional work.  The patch points on the front of the synthesizer then *override* these internal connections by breaking the internal connection, allowing you to customize how the modules are routed from one to another to make new sounds.  
- [**Monophonic / monotimbral**](https://en.wikipedia.org/wiki/Polyphony_and_monophony_in_instruments#Monophonic) : the ARP 2600, by default, is meant to be played with a keyboard controller, one note at a time, with each note making the same kind of 'sound,' or timbre.  However, with a little bit of work, you can re-patch an ARP to leverage the four sound sources independently of one another to create more than one sound at a time.
- **Voltage-based** : like most modular synthesizers of the day, the ARP uses voltage for both transmitting [analog audio signals](https://en.wikipedia.org/wiki/Analog_signal) (e.g. the sound coming from the oscillators) and [control voltage](https://en.wikipedia.org/wiki/CV/Gate) to modify parameters of the synthesizer.  These signals are *both* carried over [Switchcraft(R) Tini-D-Jax(R) brand audio jacks](https://en.wikipedia.org/wiki/Phone_connector_(audio)).  This allows you to treat audio signals as control voltage when using the synthesizer so that, for example, an oscillator can be used to 'sweep' the cutoff frequency of a filter.  The downside of this is that *you can accidentally patch a control voltage line into the signal path to the speakers*, which can damage both the speakers and your ears.
- **Subtractive** : the ARP 2600 makes sound based on the principles of [*subtractive synthesis*](https://en.wikipedia.org/wiki/Subtractive_synthesis) - the oscillators create waveforms rich in harmonic content which are then shaped by the filters and amplifiers.  This is in contrast to [*additive* synthesizers](https://en.wikipedia.org/wiki/Additive_synthesis) where simple waveforms (e.g. sine waves) are combined to make complex tones. Subtractive synthesis, along with a default (keyboard-oriented) wiring pathway, is part of what makes the ARP 2600 a classic [*"East Coast"*](https://reverb.com/news/the-basics-of-east-coast-and-west-coast-synthesis) synthesizer.
- **Multiple source / single destination** : many modules on the ARP can mix (add together) signals from a number of inputs without requiring an additional mixer module, but generally have only one patch point for the module's output.  This goes for control voltage as well, so that you can often modulate a parameter of the synthesizer with more than one source at once.  This is different from, e.g. a Buchla synthesizer, where separate mixer modules must be used to combine several oscillators through a single filter, or Serge synthesizers, where [banana jacks](https://en.wikipedia.org/wiki/Banana_connector) can be stacked to send a module's output to several places at once.  

### The Interface

The ARP 2600 has 14 or so modules, along with a keyboard, built-in speakers, and some other bits and pieces to make it easier to wire into an external sound system.  Larger modules are arrayed along a top row on the main panel, with some smaller modules fitted into a bottom row between the speakers.  The keyboard has some controls as well.  Controls on the ARP consist mostly of [slide potentiometers](https://en.wikipedia.org/wiki/Potentiometer) (sliders), along with a couple of knobs and a toggle switch or two.  Small trim pots are arrayed under rubber protective caps; these are used to fine tune the synthesizer.

*The most important thing to know about the ARP out is the default wiring between the modules*.  These are indicated by friendly diagrams under the patch points and sliders, e.g.:

![slider](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/16slider.png "Slider")

This slider lets you mix in a signal to a module (this particular slider is from the ARP filter, but this user interface is consistent across the synth).  Where it gets this signal from depends on *whether or not a cable is patched into the jack* below the slider.  If no cable exists, the synth's default wiring is used, and the symbol below the jack tells you the default source.  In this case, it's the square wave output from 'VCO 1' (the first oscillator on the synth).  If you patch a cable into the jack, that will break the default connection and override it, so that you can wire in any signal you like from elsewhere on the synthesizer.

*Nearly all modules have one or more sliders* that allow you to control the mix of one or more inputs.  If these sliders are down, the module will receive no input, from its default source or elsewhere, and will rely entirely on its internal circuitry to function.  When a module has multiple inputs, their voltages are summed; in addition, these voltages will also be mixed with any control voltage being generated directly by controls on the module, such as a frequency control on the VCO modules.  This elegant system allows you to *offset and scale* input voltages using controls mounted directly on the module itself rather than having to resort to separate voltage processing modules (although the ARP has one of those as well).  Generally-speaking, the vertical sliders will provide a scalar to the incoming voltage (a *multiplication* of voltage), while horizontal sliders will provide an offset to the incoming voltage (an *addition* of voltage).

The default wiring allows most of the modules on the ARP to interact with no patch cords; without any cables inserted, the ARP wires its oscillators (labeled VCO 1, 2, and 3) through the filter (VCF), into an amplifier (VCA), and from there to a mixer that is wired to the built-in speakers.  By looking at the symbols and adjusting the mix sliders, you can follow the signal path of the modules through the synthesizer.

### The Glossary

Analog synthesizers (and their skeuomorphic digital cousins... software synthesizers) have a jargon.  Before looking at the modules themselves, here's a brief glossary of terms:
- [**Control Voltage / Gate**](https://en.wikipedia.org/wiki/CV/Gate) (abbrev. CV/Gate) - a common schema for transmitting signals around a synthesizer that are not meant to be heard directly, but are meant to control and trigger sound-producing modules.  When the control voltage in question represents musical pitch, the ARP uses a standard scaling of 1 volt-per-octave over a range of 0-5 volts.  When the control voltage represents a trigger or a 'gate', then it is treated similar to digital signals, with 10 volts being 'high' and 0 volts 'low'. **Note**: Most(?) analog synths use gate values of 0-5 volts, including all Moog synths.  The ARP 2600 uses a gate range of 0-10v, so the output from one another synth's gate might not trigger gate input on an ARP 2600.  (Verified this with my Moog Werkstatt, it's 5v gate does not trigger the envelope on the ARP. --jet.)
- [**Voltage Controlled Oscillator**](https://en.wikipedia.org/wiki/Voltage-controlled_oscillator) (abbrev. VCO) - an oscillator with a variable frequency controllable by an external voltage source.  This is a core component of almost any analog synthesizer.  The ARP 2600 has three VCOs, all with slightly different capabilities.  Analog oscillators can generate a variety of waveforms depending on their design, and all ARP VCOs can generate more than one kind of sound.
- [**Voltage Controlled Filter**](https://en.wikipedia.org/wiki/Voltage-controlled_filter) (abbrev. VCF) - a filter with one or more parameters that can be adjusted dynamically by an external voltage source.  This module is what makes the ARP a *subtractive* synthesizer, allowing you to carve away parts of the frequency range of any input signal.  The ARP 2600 has one VCF which functions as a resonant [low-pass filter](https://en.wikipedia.org/wiki/Low-pass_filter), with the cutoff frequency adjustable through voltage control.
- [**Voltage Controlled Amplifier**](https://en.wikipedia.org/wiki/Variable-gain_amplifier) (abbrev. VCA) - an amplifier circuit where the amount of gain or attenuation applied to the incoming signal can be varied by an external voltage source, similar to a [transistor](https://en.wikipedia.org/wiki/Transistor).  The ARP 2600 has a single VCA.
- [**Low Frequency Oscillator**](https://en.wikipedia.org/wiki/Low-frequency_oscillation) (abbrev. LFO) - an oscillator used to generate low-frequency control voltage rather than an audible audio signal.  All three VCOs on the ARP 2600 can be used as an LFO.
- **Envelope Generator** - a circuit that generates time-varying control voltage intended to have a start and an end (as opposed to an oscillator).  These circuits often output these voltage 'envelopes' according to a common design, such as an [**ADSR**](https://en.wikipedia.org/wiki/Synthesizer#Attack_Decay_Sustain_Release_.28ADSR.29_envelope) (Attack/Decay/Sustain/Release) envelope.  The ARP 2600 has two envelope generators (an ADSR and a simpler AR) that have a common trigger circuit.
- [**Envelope Follower**](https://en.wikipedia.org/wiki/Envelope_detector) - a circuit that takes an audio signal and rectifies and low-passes it to generate a control voltage slope that follows the contours of the original signal.  These circuits are often used to allow an acoustic instrument (via a microphone) or an electric instrument (via a pickup) to control a parameter on a synthesizer.  They are also used in audio processing to generate the 'key' signal for a dynamics processor, such as a compressor, limiter, or noise gate.  The ARP 2600 has an envelope follower, designed to use with an external audio source.
- [**Ring Modulation**](https://en.wikipedia.org/wiki/Ring_modulation) - a simple signal processing technique where two audio signals are *multiplied* - the result is a signal with additional 'sideband' frequencies resulting from the sum and difference of the harmonic content of the two signals.  If one of the input signals is rectified, it is referred to as [**Amplitude Modulation**](https://en.wikipedia.org/wiki/Amplitude_modulation).  The ARP 2600 has a ring modulation circuit that can do both ring and CV-based amplitude modulation (to simulate musical ['tremolo'](https://en.wikipedia.org/wiki/Tremolo)).
- [**Frequency Modulation**](https://en.wikipedia.org/wiki/Frequency_modulation) - a signal processing technique where an oscillator's frequency is modified by a second source, such as an oscillator.  If the modulating source is an LFO, the result is a musical ['vibrato'](https://en.wikipedia.org/wiki/Vibrato) effect.  When high frequency oscillators provide the modulation, sidebands occur, as they do with ring modulation, but in a richer and [more complex manner](https://en.wikipedia.org/wiki/Bessel_function).  As a result, frequency modulation can be used to generate rich spectra from comparatively simple input sources.  In analog synthesizers (such as the ARP 2600), FM circuits are often designed so that multiple complex sources can be mixed together to modify the frequency of a VCO.
- [**Sample and Hold**](https://en.wikipedia.org/wiki/Sample_and_hold) (abbrev. S/H) - a circuit that 'samples' one voltage based on a secondary voltage fulfilling a triggering condition (e.g. rising in value above a certain value), and then 'holds' it until the trigger fires again.  In analog synthesizers, the two voltages are often oscillators run at different frequencies (or a noise source sampled and held by an LFO).  S/H circuits can be used to create arpeggio, sequencer, and rhythmic effects by generating control voltages for sound-producing modules in a synthesizer.  The ARP 2600 has a sample and hold module with a variety of inputs, outputs, and controls.

### The Modules

Below is a list of modules (left-to-right, top row then bottom row), an explanation of their capabilities, and their wiring (default input and output).

### 1 - Pre-Amplifier / Envelope Follower / Ring Modulator

![preamp](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/01preamp_envfol_ringmod.png "Pre-Amp")

This module consists of three-submodules:
- A [**Pre-Amplifier**](https://en.wikipedia.org/wiki/Preamplifier) that allows you to connect an external sound source (mic or line) into the synth, either for processing (e.g. through the filter and amplifier) or to control a parameter of the synth (most likely using the envelope follower).  The knob and the three-way toggle switch allow you to adjust the gain of the input signal.  The **output** patch point allows you to wire the pre-amplifier to the rest of the synthesizer.
  - *Default input* - none.  You can connect any source to the jack to the left of the 'gain' knob.
  - *Default output* - the *pre-amplifier* is wired by default as the input to the *envelope follower*.
- An **Envelope Follower**, which converts any input audio signal into a corresponding control voltage based on a smoothed representation of the amplitude (loudness) of the input.  For example, you can use a microphone input to the *pre-amplifier* to generate a CV slope that controls the amplitude of the synthesizers oscillators.  This module allowed Ben Burtt to create R2-D2's voice in Star Wars.
  - *Default input* - the output of the *pre-amplifier*.
  - *Default output* - none.  You can wire the output using a patch cable.
- A **Ring Modulator**, which multiplies two audio signals together (or one audio signal and one CV signal, for more traditional amplitude modulation), creating sideband effects that create a signature 'metallic' or 'robotic' sound.  The toggle switch labeled 'audio / dc' allows you to select whether the second input is a sound or a control voltage.
  - *Default input* - the sawtooth wave output of VCO 1 and the sine wave output of VCO 2.
  - *Default output* - the ring modulator is available as a hard-wired input for the VCF.

### 2 - Voltage Controlled Oscillator (VCO 1)

![vco1](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/02vco1.png "VCO 1")

This module is the first oscillator for the ARP.  Sliders at the top provide a base frequency (in two ranges) and the ability to fine tune the oscillator.  A toggle switch labeled 'AUDIO/LF' provides two functions - (1) it wires in control voltage from the keyboard so that you can 'play' the oscilator and (2) it switches the oscillator scaling between a low-frequency oscillator (LFO) mode where its range is between 0.3 and 30Hz ('LF' or 'kbd off') and a high frequency mode where it outputs waveforms between 10Hz and 10kHz ('AUDIO' or 'kbd on').  There are patch point output jacks for a sawtooth wave and a square wave from the VCO.  The mixer section at the bottom allows for frequency modulation of the oscilator.  These inputs *add* to the voltage set by the sliders at the top; this allows you to control the range of FM through a combination of the frequency control sliders and the mixer.
- *Default input* - the 'kbd on / kbd off' switch allows you to control the oscillator's frequency directly from the keyboard (or any CV source plugged into the left-most 'FM control' jack).  In addition, the mixer section lets you bring in three additional sources for FM; the hard-wired options are the output of the sample-and-hold (S/H) module, the ADSR envelope generator, and the sine wave output of VCO 2.
- *Default output* - the square wave output of VCO 1 is wired by default into the inputs for VCO 2 and the VCF.

### 3 - Voltage Controlled Oscillator (VCO 2)

![vco2](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/03vco2.png "VCO 2")

This module is the second oscillator for the ARP, and has more features than VCO 1.  As with the first oscillator, sliders at the top provide a base frequency and fine tune control.  A third slider allows you to set the pulse width for the pulse/pwm wave output.  The 'AUDIO / LF' switch provides the same function as on VCO 1, allowing keyboard control of the oscillator and switching between LFO and audible frequency mode.  There are four output jacks on VCO 2 - a triangle wave, a sawtooth wave, a sine wave, and a [pulse width modulation](https://en.wikipedia.org/wiki/Pulse-width_modulation) generator that can vary continuously between a square wave and a short pulse wave.  The mixer section at the bottom allows for frequency modulation of the oscilator, as well as modulation of the pulse width for the pulse/pwm wave output.
- *Default input* - as with VCO 1, the 'AUDIO / LF' switch allows you to control the oscillator's frequency directly from the keyboard (or any CV source plugged into the left-most 'FM control' jack).  In addition, the mixer section lets you bring in three additional sources for FM; by default, these are the sample-and-hold (S/H) module, the ADSR envelope generator, and the square wave output of VCO 1.
- *Default output* - the sine wave output of VCO 2 is wired by default into the inputs for VCO 1, VCO 3, and the VCF (as a control source).  The pulse/pwm wave output of VCO 2 is wired by default into the VCF as well, as an audio source.

### 4 - Voltage Controlled Oscillator (VCO 3)

![vco3](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/04vco3.png "VCO 3")

VCO3 is the ARP synthesizer's third oscillator, intermediate in complexity between VCO 1 and VCO 2.  As with VCO 2, there are sliders for a base frequency, fine tune, and pulse width.  The 'AUDIO / LF' switch toggles keyboard control of the oscillator and switches between LFO and audible frequency mode.  The oscillator has output jacks for a sawtooth and a pulse/pwm wave output.  The mixer section at the bottom allows for frequency modulation of the oscilator.
- *Default input* - as with VCO 1 and VCO 2, the 'AUDIO / LF' switch allows you to control the oscillator's frequency directly from the keyboard (or any CV source plugged into the left-most 'FM control' jack).  The mixer section lets you bring in three FM sources; by default, these are the output of the noise generator, the ADSR envelope generator, and the sine wave output of VCO 2.
- *Default output* - the sawtooth wave output of VCO 3 is wired by default into the input of the VCF.

### 5 - Voltage Controlled Filter / Resonator (VCF)

![vcf](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/05vcf.png "VCF")

The VCF is the ARP 2600's filter.  Early versions of the ARP 2600 (including ours) used a reverse-engineered clone of a ladder-filter design used in Moog synthesizers; as a result of legal action, these were replaced with ARP's own design after 1976.  In either case, the VCF consists of a resonant low-pass filter with sliders controlling the cut-off frequency (coarse and fine) and a resonance amount.  The mixer at the bottom allows you to control both audio inputs to the filter as well as control voltage inputs that vary the cutoff frequency.  As with the VCOs, the control voltage *adds* to the cutoff frequency set by the sliders, so that you can set the range of CV control with a combination of the frequency controls at the top and the mixer gain for the CV input at the bottom of the module.  There is an output jack for custom wiring of the output of the VCF.
- *Default input* - the VCF will mix in up to five audio sources - these default to the outputs of the ring modulator, the square wave output of VCO 1, the pulse/pwm output of VCO 2, the sawtooth output of VCO 3, and the output of the noise generator.  The VCF also allows for CV control of its cutoff frequency from three sources - these default to the CV output of the keyboard, the ADSR output of the envelope generator module, and the sine wave output of VCO 2.
- *Default output* - the VCF is wired by default into the input of the VCA and the mixer module.

### 6 - Envelope Generator (ADSR/AR)

![adsr](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/06adsr.png "ADSR")

The envelope generator on the ARP 2600 creates control voltage signals that rise and fall in response to a trigger.  These are used for amplitude curves, filter curves, etc.  This module generates no audio, but can be used with other modules to process audio (e.g. through the FM inputs on the VCOs or the CV input on the VCA).  The top half of the module controls an ADSR (attack/decay/sustain/release) envelope with sliders to control each stage of the envelope.  The bottom half controls a simple AR (attack/release) envelope with two sliders instead of four.  Both envelopes are 'fired' through the same trigger mechanism and cannot be controlled independently: there is a button for manual firing, as well as a jack for an external trigger.  There are output jacks for each envelope, as well as utility jacks outputting voltage from the keyboard - a 'gate' output (voltage high on key down, voltage low on key up) and a 'trigger' output (a voltage pulse on key down).
- *Default input* - the envelope generators can be controlled via the keyboard (with the toggle switch in the up position) or a voltage jack, with a default wired connection to the sample-and-hold output.
- *Default output* - the ADSR output is wired by default to FM inputs on all 3 VCOs, as well as a CV input on the VCF.  Both ADSR and AR outputs are wired by default to control inputs on the VCA.

### 7 - Voltage Controlled Amplifier (VCA)

![vca](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/07vca.png "VCA")

The VCA of the ARP 2600 modulates the amplitude of audio inputs based on control voltage sources.  This allows you to shape the volume of a synthesizer 'note', allowing it to fade in and out.  The VCA has a slider to set an 'initial gain' - as with other horizontal sliders on the ARP, these voltages are added to external control voltages, allowing you to offset and scale them when used together with the vertical 'mixer' sliders on the same module.  The VCA has two input sources and two control sources, but only one amplifier circuit, which will sum the audio signals and amplify them based on the control voltages to generate one shaped output.  There is a jack for the VCA output.
- *Default input* - the VCA has two audio inputs, which default to the outputs of the VCF and the ring modulator.  The two control inputs for the VCA are wired by default to the outputs from the envelope generator module (AR and ADSR).
- *Default output* - the VCA is wired by default to an input on the mixer module.

### 8 - Mixer / Reverb / Output

![mixer](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/08mixer_reverb_output.png "Mixer / Reverb / Output")

The right-hand module on the top row of the ARP 2600 consists of a final stage mixer, a reverberation unit, and jacks for audio output from the synthesizer:
- the [*Mixer*](https://en.wikipedia.org/wiki/Audio_mixing) module is a two-channel mixer with vertical sliders, a jack above each slider that can 'tap' a direct out of the channel, and a horizontal [pan](https://en.wikipedia.org/wiki/Panning_(audio)) slider to move the mixers output between the left and right output jacks from the synthesizer.  There are also additional input jacks to bypass the mixer entirely, wiring their voltage directly to their respective output jacks.
   - *Default input* - the mixer takes the outputs of the VCF and VCA as its default inputs.
   - *Default output* - the mixer terminates its signal path at the two output jacks (labeled 'left output' and 'right output'), as well as the internal speakers and the headphone jack.
- the *Reverberator* module is a stereo [spring reverb](https://en.wikipedia.org/wiki/Reverberation#Spring_reverberators) unit that feeds the output jacks, as well as an additional output.  Vertical sliders allow you to adjust the volume of the reverb in each channel.
   - *Default input* - the reverberator takes the output of the mixer module as its default input.

### 9 - Keyboard CV / 4-in-1 / Left Speaker

![keycv](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/09kbdcv_leftspeaker.png "Keyboard CV")

On the lower left of the ARP 2600, next to the left speaker, there is an extra jack that taps the control voltage output of the keyboard.  This CV output can be used to control modules on the synthesizer where the key being pressed (low to high) changes the voltage.  In addition, there is a passive 4-in-1 jack that allows you to take any voltage and split it into three outputs using patch cables.  On the right of the speaker is a vertical slider for its volume.  

### 10 - Noise Generator

![noise](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/10noise.png "Noise")

The noise generator for the ARP 2600 provides a random audio source that can be used for a variety of interesting things.  The two vertical sliders allow you to adjust between [white noise](https://en.wikipedia.org/wiki/White_noise) (constant power), [pink noise](https://en.wikipedia.org/wiki/Pink_noise) (1/f power), and [red noise](https://en.wikipedia.org/wiki/Brownian_noise) (1/f2), as well as control the output gain of the module.
- *Default output* - the noise generator is wired by default to the pulse width input on VCO 2, an FM input on VCO 3, an audio input on the VCF, and the trigger input of the sample-and-hold module

### 11 - Control Voltage Processor

![cvp](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/11voltageprocessor.png "Voltage Processor")

The control voltage processor module allows for four different control sources to be modified in a variety of ways, including scaling, inverting, summing, offseting, and smoothing (the 'lag' amount on the fourth control).  None of the outputs are hard-wired, but can be used to create more complex control voltage sources.
- *Default input* - the control voltage processor's four sub-modules are wired by default to a -10V DC source, the CV output of the keyboard, a +10V DC source, and the output of the envelope follower.

### 12 - Sample and Hold (S/H)

![sh](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/12sah.png "S/H")

The sample and hold (S/H) module on the ARP 2600 can be used to generate clocks and random audio sources by 'sampling' an input voltage based on an internal or external clock (which does not have to be a clock at all).  The internal controls allow for the generation of S/H control voltages with a gain and constant speed controlled by the vertical sliders.  Input and output jacks for the switches and clocks of the module allow you to create more complex sample-and-hold systems for the ARP which can simulate sequences, arpeggiators, and rhythmic voltage curves.
- *Default input* - the sample and hold module's input is wired by default to the output of the noise generator.
- *Default output* - the sample and hold module's output is wired by default to the inputs of the FM controls on VCOs 1 and 2; the 'gate' output of the module's clock is wired by default to the trigger input on the envelope generator module.

### 13 - Right Speaker / Power Switch / Headphone Output

![power](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/13rightspeaker_power_phones.png "Power Switch")

On the lower right of the ARP 2600 is the power switch for the synthesizer, next to the right speaker.  The headphone jack for the synthesizer is there as well, just below the power switch. On the left of the speaker is a vertical slider for its volume.

### 14 - Power Light

![powerlight](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/14powerlight.png "Power Light")

The power light above the power switch confirms whether the ARP 2600 is turned on.

### 15 - Keyboard

![keyboard](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/15keyboard.png "Keyboard")

The ARP 2600 keyboard (model 3604-P, if you're interested), outputs control voltage scaled to the key pressed, as well as a secondary voltage line that puts out a high (5 V) voltage when a key is depressed and 0 volts when no keys are touched.  The toggle switch allows you to adjust the keyboard's voltage scaling between a fixed (1 volt / octave) scaling and a custom scaling set by the knob on the left.  This allows you to 'tune' the keyboard to any tuning system you like where octaves have equal voltage spacing.  The knob on the bottom left is a master tuning control for the keyboard, scaling the entire voltage range up or down.  The ['portamento'](https://en.wikipedia.org/wiki/Portamento) knob, when engaged, smooths the control voltage from the keyboard over a certain amount of time, making a gliding pitch effect between keys.

### Maintenance and repairs for the ARP 2600 at the STUDIO

#### Completed work

- 12 June, 2019: Triage unit, estimate cost of repairs, order replacement parts.
- 10 July, 2019: All sliders replaced with new sliders.
- 1 Aug, 2019: Most sockets replced with new sockets, remaineder will be replaced after keyboard is repaired.
- 1 Aug, 2019: Several disconnected solder joints repaired at sockets while sockets were replaced.
- 11 Aug, 2019: Keyboard disassembled, gold spring keyboard contacts cleaned, keys cleaned, key height adjusted as needed, rubber pegs holding PCB board replaced.
- 13 Aug, 2019: Spring reverb is no longer and FM receiver.  Extension cables used while debugging were acting as antennas.

#### Remaining work

- Replace speakers
- Determine if right speaker is still not functioning (might be dead and needed replacement)
- Evaluate keyboard / cable (see [known issues](#known_issues))
- Verify all internal solder connections using patch cables, sockets, and VOM.
- Tune.
- Replace mains line with line that can be disconnected/replaced, plug existing ARP socket that is a shock hazard.

### <a name="known_issues"></a> Known issues with the ARP 2600 at the STUDIO

If you find any problems not listed below, ask someone in the STUDIO to update this list.

- The mixer and reverberator circuitry are partially blown.  As a result, in order to hear sound, you need to *bypass the mixer* by patching a single wire directly between the output of the VCA and the 'insert' input at the top of the mixer module (as shown in the photograph).
- The keyboard connection cable is flaky.  As a result, keyboard CV input, as well as the gate/trigger inputs from the keyboard in the envelope generator module, are unreliable.

Have fun!
