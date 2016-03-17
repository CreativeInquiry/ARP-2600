# ARP 2600

Documentation for the ARP 2600 at the [Frank-Ratchye STUDIO for Creative Inquiry](http://studioforcreativeinquiry.org), CMU.

[R. Luke DuBois](https://github.com/rev3rend), March 2016.

![overview](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/00overview.png "Overview")

### Introduction

The [ARP 2600](https://en.wikipedia.org/wiki/ARP_2600) is a 'semi-modular' synthesizer designed by Alan Robert Pearlman - A.R.P. himself - and commercially released in 1971.  It was one of the first synthesizers extensively marketed for education, with a retail price of below $3500.  It is considered a canonical vintage analog synthesizer, so a 'mint' (or fully-restored) ARP 2600 can easily fetch $10K or more today.

The ARP 2600 shows up in a lot of strange places... the synth was integral to the sound of artists from Jean Michel Jarre to Joy Division.  It's also well-known in the sound effects community because of its built-in envelope follower; sound designer Ben Burtt used this to great effect in making the 'voice' of R2-D2 in the Star Wars movies.

You can see an original ARP 2600 owner's manual [here](http://guitarfool.com/ARP2600/Arp%202600%20Owners%20Manual.pdf) and a service manual [here](http://guitarfool.com/ARP2600/2600ServiceManual.pdf).

### The Basics

The ARP 2600 is:
- **semi-modular** : unlike pure modular synthesizers (like the Buchla, Serge, and Moog synthesizers), the ARP 2600's has a *default internal wiring* between the individual modules (similar to patchbay 'normalization' in a recording studio) so that you could bring it home, plug it in, turn it on, and get sound out of the built-in speakers without any additional work.  The patch points on the front of the synthesizer then *override* these internal connections, allowing you to customize how the modules are routed from one to another to make new sounds.  
- **monophonic / monotimbral** : the ARP 2600, by default, is meant to be played with a keyboard controller, one note at a time, with each note making the same kind of 'sound,' or timbre.  However, with a little bit of work, you can re-patch an ARP to leverage the four sound sources independently of one another to create more than one sound at a time.
- **voltage-based** : like most modular synthesizers of the day, the ARP uses voltage for both transmitting analog audio signals (e.g. the sound coming from the oscillators) and control voltage to modify parameters of the synthesizer.  These signals are *both* carried over 3.5mm / 1/8" 'mini'-style audio jacks.  This allows you to treat audio signals as control voltage when using the synthesizer so that, for example, an oscillator can be used to modify a parameter on a filter.  The downside of this is that *you can accidentally patch a control voltage line into the signal path to the speakers*, which can damage both the speakers and your ears.
- **subtractive** : the primary synthesis technique in an ARP is based on *subtraction* - the oscillators create waveforms rich in harmonic content which are then shaped by the filters and amplifiers.  This is in contrast to *additive* synthesizers where simple waveforms (e.g. sine waves) are combined to make complex tones.
- **multiple source / single destination** : many modules on the ARP can 'mix' signals from a number of inputs without requiring an additional mixer module, but generally have only one patch point for the module's output.  This goes for control voltage as well, so that you can often modulate a parameter of the synthesizer with more than one source at once.  This is different from, e.g. a Buchla synthesizer, where separate mixer components must be used to, e.g. have several oscillators send their sound through a single filter, or Serge synthesizers, where banana jacks can be stacked to send a module's output to several places at once.  

### The Modules

The ARP 2600 has 14 or so modules, along with a keyboard, built-in speakers, and some other bits and pieces to make it easier to wire into an external sound system.  Larger modules are arrayed along a top row on the main panel, with some smaller modules fitted into a bottom row between the speakers.  The keyboard has some controls as well.  Controls on the ARP consist mostly of slide potentiometers (sliders), along with a couple of knobs and a button or two.  Small trim pots are arrayed under rubber protective caps; these are used to fine tune the synthesizer.

The most important thing to know about the ARP out is the default wiring between the modules.  These are indicated by friendly diagrams under the patch points and sliders, e.g.:

![slider](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/16slider.png "Slider")

This slider lets you mix in a signal to a module (this particular slider is from the ARP filter, but this user interface is consistent across the synth).  Where it gets this signal from depends on whether a cable is patched into the jack below the slider.  If no cable exists, the synth's default wiring is used, and the symbol below the jack tells you the default source.  In this case, it's the square wave output from 'VCO 1' (the first oscillator on the synth).  If you patch a cable in there, that will break the default connection and override it, so that you can write in any signal you like from elsewhere on the synthesizer.

Nearly all modules have one or more sliders that allow you to control the mix of one or more inputs.  If these sliders are down, the module will receive no input, from its default wiring or elsewhere.  The default wiring  allows most of the modules on the ARP to interact with no patch cords; without any cables inserted, the ARP wires its oscillators (labeled VCO 1, 2, and 3) through the filter (VCF), into an amplifier (VCA), and from there to a mixer that is wired to the built-in speakers.  By looking at the symbols and adjusting the mix sliders, you can follow the signal path of the modules through the synthesizer.

Below is a list of modules (left-to-right, top row then bottom row), an explanation of their capabilities, and their default wiring (input and output).

### 1 - Pre-Amplifier / Envelope Follower / Ring Modulator

![preamp](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/01preamp_envfol_ringmod.png "Pre-Amp")

This module consists of three-submodules:
- a **pre-amplifier** that allows you to connect an external sound source (mic or line) into the synth, either for processing (e.g. through the filter and amplifier) or to control a parameter of the synth (most likely using the envelope follower).  The knob and the three-way toggle switch allow you to adjust the gain of the input signal.  The **output** patch point allows you to wire the pre-amplifier to the rest of the synthesizer.
  - *default input* - none.  You can connect any source to the jack to the left of the 'gain' knob.
  - *default output* - the *pre-amplifier* is wired by default as the input to the *envelope follower*.
- an **envelope follower**, which converts any input audio signal into a corresponding control voltage based on a smoothed representation of the amplitude (loudness) of the input.  For example, you can use a microphone input to the *pre-amplifier* to generate a CV slope that controls the amplitude of the synthesizers oscillators.  This module allowed Ben Burtt to create R2-D2's voice in Star Wars.
  - *default input* - the output of the *pre-amplifier*.
  - *default output* - none.  You can wire the output using a patch cable.
- a **ring modulator**, which multiplies two audio signals together (or one audio signal and one CV signal, for more traditional amplitude modulation), creating sideband effects that create a signature 'metallic' or 'robotic' sound.  The toggle switch labeled 'audio / dc' allows you to select whether the second input is a sound or a control voltage.
  - *default input* - the sawtooth wave output of VCO 1 and the sine wave output of VCO 2.
  - *default output* - the ring modulator is available as a hard-wired input for the VCF.

### 2 - Voltage Controlled Oscillator (VCO 1)

![vco1](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/02vco1.png "VCO 1")

This module is the first oscillator for the ARP.  Sliders at the top provide a base frequency (in two ranges) and the ability to fine tune the oscillator.  A toggle switch labeld 'kbd on / kbd off' provides two functions - (1) it wires in control voltage from the keyboard so that you can 'play' the oscilator and (2) it switches the oscillator scaling between a low-frequency oscillator (LFO) mode where its range is between 0.3 and 30Hz ('kbd off') and a high frequency mode where it outputs waveforms between 10Hz and 10kHz ('kbd on').  There are patch point output jacks for a sawtooth wave and a square wave from the VCO.  The mixer section at the bottom allows for frequency modulation of the oscilator.
- *default input* - the 'kbd on / kbd off' switch allows you to control the oscillator's frequency directly from the keyboard (or any CV source plugged into the left-most 'FM control' jack).  In addition, the mixer section lets you bring in three additional sources for FM; the hard-wired options are the output of the sample-and-hold (S/H) module, the ADSR envelope generator, and the sine wave output of VCO 2.
- *default output* - the square wave output of VCO 1 is wired by default into the inputs for VCO 2 and the VCF.



