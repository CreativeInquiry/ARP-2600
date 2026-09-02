A GUIDE TO VISUALIZING SIGNALS WITH THE ARP-2600
======

Setup
------

1. Differential probe
2. Alligator clips
3. Mini-jack patch cable
4. ARP2600
5. Oscilloscope
    - The oscilloscope used in this guide is the Tektronix 465 and some instructions are specific to this oscilloscope, but if you are familiar with another, it should not be difficult to adapt this guide to use it

### ARP2600

There are three types of jacks on the ARP: input, output, and both (only one exists). Following the convention of the manual, connections will be referred to by the unit they draw from and the unit they input to, so that the Mixer input from the VCF is called "VCF-Mixer." To *open* an input is to move the attenuator (slider) above it up, and to *close* is the opposite.

Setup:

1. Slide all input attenuators and output level conrols to their minimum/off position (for vertical sliders this is *down* and for horizontal this is *left*)
2. Center all VCO sliders and turn range switches to *audio*
3. Set VCF initial frequency and fine tune sliders to maximum (right), and resonance to minimum.
4. Set all envelope-generator control sliders to minimum and the gate selector switch to the keyboard (upper) position.
5. Center the panpot and set the reverb sliders to minimum.

### Oscilloscope

Setup:

1. Refer to page 2-6 "Obtaining Basic Displays" in the 456 instruction manual and follow the instructions for a normal sweep display
2. To prepare the probes, clip the ground (black) clip of the probe to the sleeve of the patch cable. Attach the alligator clip between the head of the patch cable and the main clip of the probe
3. Unless otherwise noted, the probe cable will be connected to the output of the VCF

![][probe_setup]

Producing Visuals
------

### Basic Waveforms

These periodic waveforms will be the basis of many of the effects produced later. This is not intended to be a comprehensive guide of the all the periodic waveforms the ARP can generate. These instructions assume the setup instructions are completed.

#### Sine (from VCO2):

1. Patch the sine output of VCO2 to Ring Mod-VCF
2. Open VCF-Mixer
3. Open the Ring Mod-VCF

The sine wave is the most fundamental wave; every other waveform can be decomposed into a combination of (sometimes infinite) sine waves. The sine wave has a very pure tone and a smooth appearance.  
![Oscilloscope producing a sine wave][sinewave]

#### Square (from VCO1):

- Open VCF-Mixer
- Open VCO1-VCF

The angular nature of the square wave is due to its composition of infinite odd harmonics of the fundamental. This gives it a more complex, richer sound than the sine wave. The sudden switching property of it is also interesting when used as a control signal.  
![][squarewave]

#### Sawtooth (from VCO3):

1. Open VCF-Mixer  
2. Open VCO3-VCF

The sawtooth contains every integer harmonic of the fundamental. This gives it an even richer sound than the square wave.  
![][sawtoothwave]

#### Pulse (from VCO2):

1. Open VCF-Mixer  
2. Open VCO2-VCF

Changing the pulse width will change the width of the pulses. A more general form of square wave. The thinner the pulse becomes, the stronger the harmonics, and the brighter it sounds.

For all of these, changing the initial oscillator frequency compresses or stretches the displayed signal. 

### Adding Signals

In general, when multiple signals are put into the same control, they are added linearly. This is most easily understood by doing the following:

1. Open VCF-Mixer  
2. Open VCO2-VCF  
3. Open VCO3-VCF

Adjusting the oscillators to bring them into tune with each other. The difference in frequency will be visible as the waves moving slightly out of phase with each other. Note how the waves lie on top of (in phase with) each other in the oscilloscope, moving only slightly. To tune to a resonant interval  
![][additive1]  
 Tuning the waves to fifths and octaves of each other produces similar effects. Each octave above introduces another period of that wave in the other.  
![][additive2]  
Tuning them away from each other instead produces chaotic patterns atop the wave being tracked, and it sounds as if two notes are being played.  
![][additive3]

### FM Synthesis

Providing a signal to the "FM Control" input of an oscillator allows it to modify the frequency of the wave produced. There are infinite possible effects derivable from this, but the general effect depends mostly on the difference in frequency between the signal modulating and the one being modulated.

#### Modulating Audio with LF

1. Open VCF-Mixer  
2. Open VCO2-VCO3  
3. Switch VCO2 to LF

If the modulating frequency is low enough, the modulated signal will change frequency over time in the oscilloscope and audibly. An interesting effect when modulating with a low frequency square or pulse wave is that that the signal will appear to instantly change frequency, while a smoother wave will cause this transition to look smoother.

[Video of a low frequency sine wave modulating a sawtooth wave](./images/osclilloscope_guide/FM_synth/lfsaw_sine.mp4)

#### Modulating Audio with Audio

1. Open VCF into mixer  
2. Open VCO2 into VCO3

If the audio frequencies are near each other, interesting effects will become visible as the shape of the modulating wave interferes with the shape of the modulated wave. Notice how the sine wave is visible in the warping of the sawtooth.  
![][fm1]  
 If the modulating wave is a few octaves or so below the modulated wave, the modulation will become visible as a stretching and squashing of the wave outlining the shape of the modulating wave. The amplitude will also decrease because of the slight low-pass effect of the circuits of the ARP.  
![][fm2]![][fm3]  
If the modulating wave is a few octaves above the modulated, the warping caused by modulation is visible in the waveform.  
![][fm4]

### Filtering

The VCF is a low-pass filter with a variable amount of resonance. A low-pass filter attenuates the higher frequencies of a signal, which will have the effect of "smoothing" the signal. Ideally the low-pass lets through any frequency lower than the cutoff frequency, and begins to absorb frequencies above it. Increasing the resonance reduces the response of the filter at frequencies other than the cutoff and increases the response at the cutoff. 

#### Low-Passing

1. Open VCF into mixer  
2. Open VCO3 into VCF  
3. Bring the initial filter frequency down

The sharp corners of the waveform are smoothed out as the filter frequency reaches the fundamental of the oscillator. Cutting out the higher frequencies makes the wave resemble a sine wave more. Bringing the filter frequency below the oscillator frequency starts to attenuate the fundamental.

[Video of the initial filter frequency being turned down until the input signal is totally attenuated](./images/oscilloscope_pics/filtering/filtering.mp4)

#### Resonance

1. Open VCF into mixer  
2. Open VCO3 into VCF  
3. Increase the resonance to about halfway  
4. Adjust the initial filter frequency to maximize the amplitude of the signal

When the resonance is increased, it causes the filter to amplify frequencies at the filter frequency. The range over which this amplification happens gets sharper and the amplification gets stronger as the resonance is increased. If the resonance is high enough, the filter will start to resonate on its own, called self-resonance, and will produce a sine wave at the filter frequency.

![][filter1]

#### Harmonics

1. Open VCF into mixer  
2. Open VCO3 into VCF  
3. Increase the resonance to about halfway  
4. Adjust the initial filter frequency to maximize the amplitude of the signal  
5. Sweep up the filter frequency and listen for points when distinct pitches ring out

When the resonator is amplifying a harmonic of the current signal, it will be audible as a ringing sound at that pitch, and visible as a sine wave added to the signal.

![][filter2]![][filter3]![][filter4]![][filter5]![][filter6]

[sinewave]: ./images/osclilloscope_guide/basic_waves/sine_wave.jpg
[squarewave]: ./images/osclilloscope_guide/basic_waves/sq_wave.jpg
[sawtoothwave]: ./images/osclilloscope_guide/basic_waves/sawtooth_wave.jpg
[additive1]: ./images/osclilloscope_guide/additive_synth/sq+saw.jpg
[additive2]: ./images/osclilloscope_guide/additive_synth/sq+saw1.jpg
[additive3]: ./images/osclilloscope_guide/additive_synth/saw+sq_complex.jpg
[fm1]: ./images/osclilloscope_guide/FM_synth/sine_saw.jpg
[fm2]: ./images/osclilloscope_guide/FM_synth/sine_hfsaw2.jpg
[fm3]: ./images/osclilloscope_guide/FM_synth/saw_sq.jpg
[fm4]: ./images/osclilloscope_guide/FM_synth/sine_saw3.jpg
[filter1]: ./images/osclilloscope_guide/filtering/filter1.jpg
[filter2]: ./images/osclilloscope_guide/filtering/filter2.jpg
[filter3]: ./images/osclilloscope_guide/filtering/filter3.jpg
[filter4]: ./images/osclilloscope_guide/filtering/filter4.jpg
[filter5]: ./images/osclilloscope_guide/filtering/filter5.jpg
[filter6]: ./images/osclilloscope_guide/filtering/filter6.jpg
[probe_setup]: ./images/osclilloscope_guide/setup/setup1.jpg
