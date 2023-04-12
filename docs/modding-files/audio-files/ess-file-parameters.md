---
layout: default
title: Ess file parameters
nav_order: 2
parent: Audio files
grand_parent: Modding files
---

# Information

.ess files are sound script files which use normal sound files, in combination with some parameters, to create a special audio "package".  
These packages can then be used for certain situations or events to create a realistic sound environment.

# Ess parameters
The following table shows the available ess parameters, their type and purpose.  

| Parameter | Value type | Purpose |
|:-------------|:--------------|
| audio_file | `string` | Path to the .wav or .ogg file in the game files. Mono .wav files are used for sound effects. Stereo .ogg files are used for dialogs |
| gain | `float / int` | Gain multiplier. If you need to make a sound quieter, choose gain in the range between 0 and 1. To make the sound louder, choose a number greater than 1. Going too high will cause clipping |
| streaming | `0 / 1` | Indicates whether the sound should be precached by the game or streamed from the hard drive. Music and dialogs normally get streamed, smaller files, like sound effects, cached |
| instance_limit | `int` | Indicates how many instances of the sound can be played at once or in a rapid succession. Lower this number to reduce the effect of the sounds stacking on top of one another and clipping or going out of phase. 0 sets the instance limit off |
| instance_limit_timeout | `float,` <br> `value is in seconds` | Dictates what amount of time needs to pass for the game not to consider the sound to go against the instance limit. For example, an instance limit of 0.25 will mean that sound X played within 0.25 seconds of another instance of sound X will go against the limit and won't be played. If sound X occurs 0.26 seconds after another instance of sound X, it will be played normally |
| spacial | `0 / 1` | Indicates whether the sound should be placed on the stereo scene according to its origin on the game scene. GUI sounds, dialogs and music are not spacial |
| freq_ratio | `float,` <br> `greater than zero` | Frequency multiplier. Values below 1 will lower the pitch of the sample. Values greater than 1 will make the pitch higher |
| freq_ratio_spread | `float,` <br> `between 0 and 1` | Allows the game to adjust the pitch of the sound between instances. 0 means no change - all instances of the sound will sound the same. 0.1 means that the game can change the pitch of the sample up to 10% higher or 10% lower between instances. Great for introducing slight variations between very repetitive sounds |
| group | `string` | Sound group determines which volume slider in the menu affects the sfx |
| rolloffFactor | `int` | Determines how quickly the sound will lose volume after you cross the referenceDistance. Like a slope - you are on a flat surface - volume is constant. referenceDistance (in meters) determines how far the apex of the slope is. Once you cross it, the sound gets quieter. Higher values for rolloffFactor will make the sound quieter more quickly |
| referenceDistance | `meters` | The stereo ears are located in the camera - 45 is the default distance of the camera from the ground. You shouldn't go lower than 45 |
| description | `string` | Internal description |
| notes | `string` | Internal note |
| status | `placeholder / beta / final` | Internal status |