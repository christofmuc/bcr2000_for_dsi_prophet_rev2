# Behringer BCR2000 for DSI Prophet Rev 2 #

This is a Behringer BCR2000 template for the DSI Prophet Rev2 synthesizer I made, because while the Rev2 is a great piece of gear with a very good knob to function ratio, the excellent gated sequencer can only be used in a really tiring way - unless you own a Behringer BCR2000!

### What's in it ###

The SYX file contains a preset for your BCR2000, ready to be sent to your BCR 2000 via any Sysex capable MIDI tool (e.g. MIDI-OX). 

The BCL file located above contains the cleartext instructions in BCL format (an enormous thanks to Mark van den Berg for providing the excellent document on the B-Control MIDI Implementation, which can be found at https://mountainutilities.eu/). 

The BCL can be modified by you if you like, for example to change the $store instructions to use different preset slots, 
and then must be converted to SYX format e.g. with the extremely helpful BC-convert tool from https://www.sequencer.de/synth/index.php/BC-Convert.

### Layout ###

The layout on the BCR2000 after upload of the file is actually pretty simple:

* The top row of encoders is the first 8 steps of the gated sequence. The encoder group selects which of the 4 tracks of the sequencer you are editing
* The 16 buttons at the top determine if the gate is actually sent or if it is a rest. When the light is on, there will be a gate on the step, if the light is off, not. This effectively modifies track 1, so the buttons are logically coupled to the encoders.
* The second encoder row is step 9 to 16 for track 1
* The third encoder row is step 9 to 16 for track 2
* The fourth encoder row is step 9 to 16 for track 3

And yes, the BCR2000 misses 8 encoders to also allow editing the last 8 steps of track 4, but hey, this is already much better than with the Rev2 alone!

### MIDI Channel ###

Uh, as the MIDI channel is encoded into all the messages the BCR2000 is instructed to send, there is easy way to change the MIDI channel of the Rev2 - it should be set to channel zero.

In case you absolutely can not live with channel zero, contact me and we'll find a way!
