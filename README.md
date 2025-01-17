# Orca Screen Reader Intro Guide

This document is the written version of a video tutorial which is soon to be made and is intended to provide new users of all abilities with a general intro on using the Orca screen reader.

This document was created by [Colton Loftus](https://github.com/C-Loftus) but is community driven; create an issue or PR on Github if you would like to make changes.

## Cheatsheet

A cheatsheet of many keyboard commands for Orca can be found [here](cheatsheet.md)

## Linux Background

- Use a modern, accessible Linux distribution like Ubuntu or Fedora for Orca.
- Any distro using the Gnome desktop environment is generally a reasonable choice. 
    - Ubuntu and Fedora are both good defaults, but can sometimes have outdated orca versions in their repositories
    - Using Debian backports, Arch Linux or NixOS can all work but come with their own tradeoffs.
- MATE is preferred by some but I feel Gnome is better and has more overall support and a larger community.

## Voices

- espeak-ng 
    - Orca's default voice
    - Click [here](https://github.com/C-Loftus/orca-intro-guide/blob/main/voices/espeak.mp3) to listen to a demo. 
    - espeak-ng supports many different languages, but is commonly criticized as being too robotic
- [Voxin](https://voxin.oralux.net/voice.php)
    - Paid, proprietary voices. 
    - Many languages which sound fairly good
    - Each voices averages $20 and can get rather expensive
    - Click [here](https://github.com/C-Loftus/orca-intro-guide/blob/main/voices/voxin/) to listen to multiple different voice demos
- [rhvoice](https://rhvoice.org/)
    - A free set of voices that is more natural than espeak
    - My preferred option
    - Easy to install and works cross platform if desired
- [piper](https://rhasspy.github.io/piper-samples/)
    - A free set of voices that are quite realistic without needing to pay or have an expensive GPU
    - Generally too slow for screen reader use, but good for [generating audiobooks](https://github.com/C-Loftus/QuickPiperAudiobook) or other audio content outside of screen reader use
    - Must be installed with [pied](https://github.com/Elleo/pied) which is sporadically maintained or use Orca's experimental `spiel` integration

## Modes

- Browse Mode
    - Navigate the page with the keyboard
    - Default way you navigate the desktop
    - i.e. pressing up in a text box could move you to the previous element
    - Toggled with `Orca` + A
    - Essentially a form of structural navigation. 
    - Currently supported only in web browsers, but may one day be added to other apps like LibreOffice
- Focus Mode
    - Navigate inside of a focused element without moving outside of it
    - Automatically enabled when moving focus into certain editable text boxes
    - i.e. pressing up in a text box could move the cursor to the previous line in the same text box
    - Toggled with `Orca` + A
- Learn Mode
    - Ignore all key presses and just echo out what they do
    - Orca + H 
- Sleep Mode
    - Don't speak when a particular application is focused
    - i.e. don't duplicate speech when a self-speaking app is focused
    - Toggle for a specific application with `Alt` + `ctrl` + `shift` + q
- Structural Navigation vs Flat Review
    - Not a mode difference technically, but structural navigation keys can be toggled with `Orca + Z`
    - Structural navigation commands move around by the semantic tags of the a11y tree. 
    - Flat review goes through each line one a time without a structured hierarchy 

## Learning to Use Orca

- Begin by learning navigation commands for your desktop environment
- Workflows using the browser of electron applications like VSCode or Slack tend to have the best success
- Orca mailing list tends to be the best place to ask questions

### Downsides

- Lack of accessibility support in many applications
- There is no one central place for Linux accessibility discussions
- May need to recompile to get latest Orca updates
    - I have a written guide [here](https://gist.github.com/C-Loftus/5c71ebef18717a364e1ac2865a54e1e9), but dependencies may change over time
- There is no plugin system like in NVDA
    - You can create scripts and bundle them inside Orca but this is less straightforward

### Web Pages

* https://orca.gnome.org/
* https://help.gnome.org/users/orca/stable/index.html.en
* https://emmabuntus.org/wp-content/uploads/2024/07/Manual_Orca_20240711.pdf

### Talks 

* [General a11y overview](https://www.youtube.com/watch?v=_RQBh7UmEps)

<!-- ## Other Useful a11y content -->
<!-- * https://www.youtube.com/watch?v=xseIsaxrlXo
* https://www.youtube.com/watch?v=w9psDfEFf9c -->
<!-- * http://htmlpreview.github.io/?https://github.com/brailcom/speechd/blob/master/doc/ssip.html -->