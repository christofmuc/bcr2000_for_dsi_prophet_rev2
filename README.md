# Behringer BCR2000 for DSI Prophet Rev 2 #

This is a Behringer BCR2000 template for the DSI Prophet Rev2 synthesizer I made, because while the Rev2 is a great piece of gear with a very good knob to function ratio, the excellent gated sequencer can only be used in a really tiring way - unless you own a Behringer BCR2000!

### What's in it ###

The SYX file contains a preset for your BCR2000, ready to be sent to your BCR 2000 via any Sysex capable MIDI tool (e.g. MIDI-OX). 

The BCL file located above contains the cleartext instructions in BCL format (an enormous thanks to Mark van den Berg for providing the excellent document on the B-Control MIDI Implementation, which can be found at https://mountainutilities.eu/). 

The BCL can be modified by you if you like, for example to change the $store instructions to use different preset slots, 
and then must be converted to SYX format e.g. with the extremely helpful BC-convert tool from https://www.sequencer.de/synth/index.php/BC-Convert.

### Layout 1 - single page ###

The first layout file "bcr2000_for_DSIProphetRev2.syx" uses no preset and can be send to the BCR2000 without overwriting the stored data. After upload of the file the layout is actually pretty simple:

* The top row of encoders is the first 8 steps of the gated sequence. The encoder group selects which of the 4 tracks of the sequencer you are editing
* The 16 buttons at the top determine if the gate is actually sent or if it is a rest. When the light is on, there will be a gate on the step, if the light is off, not. This effectively modifies track 1, so the buttons are logically coupled to the encoders.
* The second encoder row is step 9 to 16 for track 1
* The third encoder row is step 9 to 16 for track 2
* The fourth encoder row is step 9 to 16 for track 3

This is for testing, when it works and you want the full glory skip to the next section

### Layout 2 - Presets 1 to 8 for the 8 tracks of the gated sequencer ###

The file "bcr2000_preset_1_to_8_for_DSIProphetRev2.syx" will store 8 new presets on the BCR2000 in the slots 1 to 8. So please make sure you save anything you have in there to your computer before sending this file!

The layout is easier to remember, but doesn't use all encoders. I found this to be easy to remember:

* The top left encoder selects the tracks destination. If you don't renumber the number (and it's 52 of these), use the Rev2 instead. I still found it handy because if you dial it to 0 the gated track is effectively turned off.
* The top right encoder is used to select the gated sequencer's mode, with 0 being normal, 1 being no reset, etc. And clicking the encoder will actually toggle between Poly Seq and Gated Seq on the Rev2.
* The 16 buttons work as above
* The next 16 encoders are the 16 steps of the track. If you want less than 16 steps, turn one of the all the way up, because value 126 is reset and will stop the sequencer at that step and start from the front.
* The lower 8 encoders are not used in this setup.

But most importantly: The Presets of the BCR2000 can now be used to select the gated sequencer track, with 1-4 being track 1-4 of layer A and 5-8 being track 1-4 of layer B.

### MIDI Channel ###

Uh, as the MIDI channel is encoded into all the messages the BCR2000 is instructed to send, there is easy way to change the MIDI channel of the Rev2 - it should be set to channel zero.

In case you absolutely can not live with channel zero, contact me and we'll find a way!
