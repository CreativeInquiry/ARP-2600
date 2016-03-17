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

![overview](https://github.com/CreativeInquiry/ARP-2600/raw/master/images/15slider.png "Slider")

This slider lets you mix in a signal to a module (it's from the ARP filter, but this user interface is consistent across the synth).  Where it gets this signal from depends on whether a cable is patched into the jack below the slider.  If no cable exists, the synth's default wiring is used, and the friendly symbol below the jack tells you the default source.  In this case, it's the square wave output from 'VCO 1' (the first oscillator on the synth).  If you patch a cable in there, that will break the default connection and override it, so that you can write in any signal you like from elsewhere on the synthesizer.









