# rofi-sound-output-chooser

## Introduction
I wanted a way to quickly switch between my bluetooth headset, and my on-board
speakers.  After a little bit of poking around (and getting some inspiration
from [rofi-bluetooth](https://github.com/nickclyde/rofi-bluetooth), I came up
with this.  I have not done any extensive testing.  I don't know if this even
works anywhere other than my computer.  I also don't know long-term if I am even
sticking with I3.  I simply built this to scratch a curiosity itch with I3 and
pactl.

![demo](images/sound_change.gif)

## Installation

### Dependencies

This script requires two additional commands

1. pactl - This is the main requirement for determining the devices
2. dunstify - Used for notifications when the device is changed.  Technically
   not needed, but currently there are no checks or config options to not use
   it.

For Fedora this would be done with the following:

`dnf install pulseaudio-utils dunst`

I don't know where any other distros keep those things, but it's probably pretty
similar to those.

### Installing this script

1. Clone this repo
2. Copy rofi-sound-output-chooser to somewhere in your $PATH


# I3wm keybinding

I have this bound within a mode, but you could do something like 

`bindsym $mod+0 exec --no-startup-id rofi -show rofi-sound -modi "rofi-sound:rofi-sound-output-chooser"`
