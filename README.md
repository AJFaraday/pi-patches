Pi-patches
----------
By Andrew Faraday


Basically, after some discussion with @gadgetoid on twitter it seems there is a real interest amongst hardware hackers in using Pure Data as a tool to instantly sonify the result of human inputs, but there appears to be something of a skilsl gap. 

The patches held within are fairly straight-forward pure data patches with customisable input to allow this to take place.

Patches
-------

keybord slicer
--------------

This is a beat slicer designed to use keyboard input. Simply put each key on the keyboard will skip the sound to a corresponding position in the sample. 

Inputs:

* Midi notes

Customisations:

* min - The lowest note easily accessible on your keyboard
* max - The highset note easily accessible on your keyboard
* newfile - click this button IF you want to load a different wav file to play with.

In-patch changes:

* on - Turns overall sound production on or off
* mode - when off the sample will continue to play, when on the sample will only play when one or more key is pressed.

skywriter FM synth
------------------

Found in skywriter/fm-synth.pd - this is a frequency modulation synthesizer designed to work with 'skywriter' controller.

Inputs:

* 3d position (X, Y and Z)
* tap event
* touch on and off events

There are two ways to control this: 

* with midi inputs with the input-midi abstraction. 
* With the skywriter with input-skywriter abstraction (copy input-midi as input-skywriter and modify to accept these inputs, then rename the object in the synth patch)

Currently the controls are mapped like this:

* tap - turn sound production on and off
* X - pitch
* Y - modulation speed
* z - Volume

Contributors
------------

* Andrew Faraday (@MarmiteJunction)

Testers
-------

* Phil Howard (@gadgetoid)
