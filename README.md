# Grainstation-C

Written by Micah Frank under GPLv3

<http://micahfrank.com>

<http://micahfrank.bandcamp.com>

Grainstation-C is an open-source, granular performance workstation designed to build realtime, evolving sound sculptures with optional ambisonics. It seamlessly integrates with a Novation LaunchControl XL Mark 2 (easily modifiable for any other controller) and can processes 4 disk tracks and 3 live input streams. You can save any state as a snapshot and morph to that snapshot at any point in a performance. It has 6 independent pitch delay lines, 6 switchable low pass and high pass filters, live audio looping and multiple granular processing controls including granular time-stretching, frame animation and granular pitch shifting.

Grainstation-C was originally inspired by the Make Noise System Concrete but shortly took on many unique characteristics of its own. http://www.makenoisemusic.com/synthesizers/system-concrete

I used it on my latest album [Quetico](https://micahfrank.bandcamp.com/album/quetico) extensively to process field recordings and create walls of textures. I very happy happy to now offer it to the public!

Watch this [demo video](https://youtu.be/BQ5MSDqFaX8) to see what it can do!

<a href="https://youtu.be/BQ5MSDqFaX8" target="_blank"><img src="http://img.youtube.com/vi/BQ5MSDqFaX8/0.jpg" alt="Grainstation-C Demo" width="240" height="180" border="0" /></a>

**Controller**

Grainstation-C has been developed to integrate with the Novation Launch Control XL Mark2. However, any other controller should work as well. The MIDI note and controller mapping schema is written at the end of this page.

This repository includes 4 template pages for the Novation Launch Control XL. To change pages, press [User + Track Focus 1-4] buttons

• Page 1 - Granular Controls - pitch, time-stretch, grain size

• Page 2 - Granular and Filter Controls - grain duration, filter type (low pass, high pass), filter frequency

• Page 3 - Pitch Delay Controls - delay time, delay feedback, delay pitch shift

• Page 4 - Delay and Convolution Controls - delay send amount, convolution send amount

• Page 5 - Ambisonics / Spatial Audio Controls - azimuth angle, altitude angle

Download the Launch Control XL Mk2 software (for loading the templates): https://bit.ly/2y3rWul

**Recording**

You can render a file in real-time to the /renders folder simply by pressing the [Record Arm] button on the Launch Control XL. The button will begin to blink and your performance will be recorded. You can stop and restart recording as needed by pressing the button again.

**Ambisonics**

You can enable the ambisonics flag and immediately tweak the azimuth and altitude for any track. When you render the performance, a multichannel B-encoded file will also be rendered to the "b_format" folder.

**Installation**

Grainstation requires Csound: http://csound.com/download.html CsoundQT comes with Csound and will enable you to run Grainstation C.

See this video for a quick explanation about installation and setup
https://www.dropbox.com/s/im1vivrjv98isub/Grainstation-C_config.mp4?dl=0

**Page Controls Overview**

<img src= "https://github.com/chronopolis5k/Grainstation-C/blob/master/LaunchControl%20XL%20Templates/Page_Overviews/Page1.jpg" width="450" height="507">
<img src= "https://github.com/chronopolis5k/Grainstation-C/blob/master/LaunchControl%20XL%20Templates/Page_Overviews/Page2.jpg" width="450" height="507">
<img src= "https://github.com/chronopolis5k/Grainstation-C/blob/master/LaunchControl%20XL%20Templates/Page_Overviews/Page3.jpg" width="450" height="507">
<img src= "https://github.com/chronopolis5k/Grainstation-C/blob/master/LaunchControl%20XL%20Templates/Page_Overviews/Page4.jpg" width="450" height="507">
<img src= "https://github.com/chronopolis5k/Grainstation-C/blob/master/LaunchControl%20XL%20Templates/Page_Overviews/Page5.jpg" width="450" height="507">

**MIDI Specification**

Track 1 Volume = CC 77, CHANNEL 1
Track 2 Volume = CC 78, CHANNEL 1
Track 3 Volume = CC 79, CHANNEL 1
Track 4 Volume = CC 80, CHANNEL 1
Track 5 Volume = CC 81, CHANNEL 1
Track 6 Volume = CC 82, CHANNEL 1
Track 7 Volume = CC 83, CHANNEL 1

MORPH FADER = CC 84, CHANNEL 1

RECORD PERFORMANCE TO FILE = NOTE C7, CHANNEL 1

Grain Pitch 1 = CC 1, CHANNEL 1
Grain Pitch 2 = CC 4, CHANNEL 1
Grain Pitch 3 = CC 7, CHANNEL 1
Grain Pitch 4 = CC 10, CHANNEL 1
Grain Pitch 5 = CC 13, CHANNEL 1
Grain Pitch 6 = CC 16, CHANNEL 1
Grain Pitch 7 = CC 19, CHANNEL 1

Grain Stretch 1 = CC 2, CHANNEL 1
Grain Stretch 2 = CC 5, CHANNEL 1
Grain Stretch 3 = CC 8, CHANNEL 1
Grain Stretch 4 = CC 11, CHANNEL 1
Grain Stretch 5 = CC 14, CHANNEL 1
Grain Stretch 6 = CC 17, CHANNEL 1
Grain Stretch 7 = CC 20, CHANNEL 1

Grain Size 1 = CC 3, CHANNEL 1
Grain Size 1 = CC 6, CHANNEL 2  
Grain Size 1 = CC 9, CHANNEL 3  
Grain Size 1 = CC 12, CHANNEL 4
Grain Size 1 = CC 15, CHANNEL 5  
Grain Size 1 = CC 18, CHANNEL 6  
Grain Size 1 = CC 21, CHANNEL 7

Grain Duration 1 = CC 1, CHANNEL 2
Grain Duration 2 = CC 4, CHANNEL 2
Grain Duration 3 = CC 7, CHANNEL 2  
Grain Duration 4 = CC 10, CHANNEL 2
Grain Duration 5 = CC  13, CHANNEL 2
Grain Duration 6 = CC 16, CHANNEL 2
Grain Duration 7 = CC 19, CHANNEL 2

FILTER TYPE 0-64 = Lowpass, 65-127 = High Pass

Filter Type 1 = CC 2, CHANNEL 2
Filter Type 2 = CC 5, CHANNEL 2
Filter Type 3 = CC 8, CHANNEL 2
Filter Type 4 = CC 11, CHANNEL 2
Filter Type 5 = CC 14, CHANNEL 2
Filter Type 6 = CC 17, CHANNEL 2
Filter Type 7 = CC 20, CHANNEL 2

Filter Frequency 1 = CC 3, CHANNEL 2
Filter Frequency 2 = CC 6, CHANNEL 2
Filter Frequency 3 = CC 9, CHANNEL 2
Filter Frequency 4 = CC 12, CHANNEL 2
Filter Frequency 5 = CC 15, CHANNEL 2
Filter Frequency 6 = CC 18, CHANNEL 2
Filter Frequency 7 = CC 21, CHANNEL 2

Delay Time 1 = CC 1, CHANNEL 3
Delay Time 2 = CC 4, CHANNEL 3
Delay Time 3 = CC 7, CHANNEL 3
Delay Time 4 = CC 10, CHANNEL 3
Delay Time 5 = CC 13, CHANNEL 3
Delay Time 6 = CC 16, CHANNEL 3
Delay Time 7 = CC 19, CHANNEL 3

Delay Feedback 1 = CC 2, CHANNEL 3
Delay Feedback 2 = CC 5, CHANNEL 3
Delay Feedback 3 = CC 8, CHANNEL 3
Delay Feedback 4 = CC 11, CHANNEL 3
Delay Feedback 5 = CC 14, CHANNEL 3
Delay Feedback 6 = CC 17, CHANNEL 3
Delay Feedback 7 = CC 20, CHANNEL 3

Delay Pitch Shift 1 = CC 3, CHANNEL 3
Delay Pitch Shift 2 = CC 6, CHANNEL 3
Delay Pitch Shift 3 = CC 9, CHANNEL 3
Delay Pitch Shift 4 = CC 12, CHANNEL 3
Delay Pitch Shift 5 = CC 15, CHANNEL 3
Delay Pitch Shift 6 = CC 18, CHANNEL 3
Delay Pitch Shift 7 = CC 21, CHANNEL 3

Delay Send 1 = CC 1, CHANNEL 4
Delay Send 2 = CC 4, CHANNEL 4
Delay Send 3 = CC 7, CHANNEL 4
Delay Send 4 = CC 10, CHANNEL 4
Delay Send 5 = CC 13, CHANNEL 4
Delay Send 6 = CC 16, CHANNEL 4
Delay Send 7 = CC 19, CHANNEL 4

Reverb Send 1 = CC 2, CHANNEL 4
Reverb Send 2 = CC 5, CHANNEL 4
Reverb Send 3 = CC 8, CHANNEL 4
Reverb Send 4 = CC 11, CHANNEL 4
Reverb Send 5 = CC 14, CHANNEL 4
Reverb Send 6 = CC 17, CHANNEL 4
Reverb Send 7 = CC 20, CHANNEL 4


AMBISONICS

Azimuth 1 = CC 1, CHANNEL 5
Azimuth 2 = CC 4, CHANNEL 5
Azimuth 3 = CC 7, CHANNEL 5
Azimuth 4 = CC 10, CHANNEL 5
Azimuth 5 = CC 13, CHANNEL 5
Azimuth 6 = CC 16, CHANNEL 5
Azimuth 7 = CC 19, CHANNEL 5


Altitude 1 = CC 2, CHANNEL 5
Altitude 2 = CC 5, CHANNEL 5
Altitude 3 = CC 8, CHANNEL 5
Altitude 4 = CC 11, CHANNEL 5
Altitude 5 = CC 14, CHANNEL 5
Altitude 6 = CC 17, CHANNEL 5
Altitude 7 = CC 20, CHANNEL 5

SNAPSHOT BUTTONS

Snapshot 1 = NOTE C#-2, CHANNEL 2
Snapshot 2 = NOTE D-2, CHANNEL 2
Snapshot 3 = NOTE D#-2, CHANNEL 2
Snapshot 4 = NOTE E-2, CHANNEL 2
Snapshot 5 = NOTE F-2, CHANNEL 2
Snapshot 6 = NOTE F#-2, CHANNEL 2
Snapshot 7 = NOTE G-2, CHANNEL 2
Snapshot 8 = NOTE G#-2, CHANNEL 2
