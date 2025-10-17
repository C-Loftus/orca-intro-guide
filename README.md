# Orca Screen Reader Intro Guide

This document is the written version of a [video tutorial](https://youtu.be/ugcaDHSWtaE?si=JKzrzp18owBEkC-a) on my Youtube channel and is intended to provide new users of all abilities with a general intro on using the Orca screen reader.

This document was created by [Colton Loftus](https://github.com/C-Loftus) but is community driven; create an issue or PR on Github if you would like to make changes.

## Cheatsheet

A cheatsheet of many keyboard commands for Orca can be found [here](cheatsheet.md)

## Linux Background

- A modern, widely used Linux distribution like Ubuntu or Fedora is likely to be a good choice if you want a distribution for general use that is accessible.
    - Ubuntu and Fedora are both good defaults, but can sometimes have outdated Orca versions in their repositories
    - Using Debian backports, Arch Linux or NixOS can all work and get you newer packages, but may be more complicated to use
    - Special custom Linux distros for specific accessibility needs can be useful but may not be as actively maintained or updated.
- The choice of your desktop environment will make a significant difference to overall system accessibility 
    - Many blind folks prefer using MATE; Gnome is also a good choice for overall accessibility 

## Voices

- espeak-ng 
    - Orca's default voice
    - Click [here](https://github.com/C-Loftus/orca-intro-guide/blob/main/voices/espeak.mp3) to listen to a demo. 
    - espeak-ng supports many different languages, but is commonly criticized as being too robotic
- [Voxin](https://voxin.oralux.net/voice.php)
    - Paid, proprietary voices. 
    - Many voices in many languages, many of which sound very good
        - MacOS uses many of these voices, such as Samantha (the default VoiceOver voice)
    - Each voice averages $20 but it is probably worth it if you can afford it
    - Click [here](https://github.com/C-Loftus/orca-intro-guide/blob/main/voices/voxin/) to listen to multiple different voice demos
- [rhvoice](https://rhvoice.org/)
    - A free set of voices that is more natural than espeak
    - Easy to install and works cross platform if desired
- [piper](https://rhasspy.github.io/piper-samples/)
    - A free set of voices that are quite realistic without needing to pay or have a GPU
    - Generally too slow for screen reader use, but good for [generating audiobooks](https://github.com/C-Loftus/QuickPiperAudiobook) or other audio content outside of screen reader use
    - Must be installed with [pied](https://github.com/Elleo/pied) which is sporadically maintained or use Orca's experimental `spiel` integration

## Modes

- Browse Mode
    - Navigate between semantic sections of the page using the keyboard
    - Default way you navigate the desktop
    - For example, pressing up in a text box could move you to the previous element
    - Toggled with `Orca` + A
    - Essentially a form of structural navigation. 
- Focus Mode
    - Navigate inside of a focused element without moving outside of it
    - Automatically enabled when moving focus into certain editable text boxes
    - For example, pressing up in a text box could move the cursor to the previous line in the same text box
    - Toggled with `Orca` + A
- Learn Mode
    - Ignore all key presses and just echo out what they do
    - Toggled with `Orca` + H 
- Sleep Mode
    - Don't speak when a particular application is focused
    - Could be used to prevent duplicate speech when a self-speaking app is focused
    - Toggle for a specific application with `Alt` + `ctrl` + `shift` + q
- Structural Navigation vs Flat Review
    - Not a mode difference technically, but structural navigation keys can be toggled with `Orca + Z`
    - Structural navigation commands move around by the semantic tags of the a11y tree. 
    - Flat review goes through each line one a time without a structured hierarchy 

## Learning to Use Orca

- Begin by learning navigation commands for your desktop environment
- Workflows using the browser or electron applications like VSCode or Slack tend to have the best success
- Orca mailing list tends to be the best place to ask questions

### Downsides

- Lack of accessibility support in many applications
- There is no one central place for Linux accessibility discussions
- May need to recompile to get latest Orca updates
    - I have a written guide [here](https://gist.github.com/C-Loftus/5c71ebef18717a364e1ac2865a54e1e9), but dependencies may change over time
- There is no plugin system like in NVDA
    - You can [create scripts](#scripting-orca) and bundle them inside Orca but this is less straightforward

### Useful Websites for Documentation

* https://orca.gnome.org/
* https://help.gnome.org/users/orca/stable/index.html.en
* https://emmabuntus.org/wp-content/uploads/2024/07/Manual_Orca_20240711.pdf

### Scripting Orca

- Orca as of version 49.0 can now be controlled with dbus bindings which are documented [here](https://gitlab.gnome.org/GNOME/orca/-/blob/main/README-REMOTE-CONTROLLER.md)
- You can use my [golang bindings](https://github.com/C-Loftus/orca-controller) to control Orca from a higher level programming language

### Talks 

Unfortunately there are not many videos regarding Orca. However, these are some that are relvant to Linux accessibility in general:

* [My own technical Linux a11y overview video](https://www.youtube.com/watch?v=_RQBh7UmEps)
* [Odilia Screen Reader overview](https://www.youtube.com/watch?v=8EPTDCmS7nA) (this is a new experimental Linux screen reader but it is useful for a general overview on how Linux screen readers are written)

<!-- ## Other Useful a11y content -->
<!-- * https://www.youtube.com/watch?v=xseIsaxrlXo
* https://www.youtube.com/watch?v=w9psDfEFf9c -->
<!-- * http://htmlpreview.github.io/?https://github.com/brailcom/speechd/blob/master/doc/ssip.html -->
