+++
date = "2017-01-02T08:31:01-08:00"
toc = true
prev = "/development"
weight = 5
title = "Overview"

+++

#### Playground

The [Dodo Playground](https://play.dodolabs.io) provides an integrated development environment completely in the browser. 

![Dodo Playground](/development/playground.png?width=50%)

- Navigation Bar
	- Choose Language (C / Assembly)
	- Run - Compiles code in Cloud and then runs simulator in browser
	- Flash - Appears only when [Dodo Flashing Utility](https://chrome.google.com/webstore/detail/dodo-flash-utility/bckholjcbphjhdfgbejkjflcafdgbdkb) is installed
	- Sign in With Github - Required to save and manage multiple projects
- Editor
	- Shows syntax highlighting for C only
	- By default loads a sample project
- Documentation
	- Fully documents the Dodo API for both C and Assembly
- Status Bar
	- Shows compilation results and other messages

#### Running

Upon succesfully compiling a program, the playground will run the application in the simulator. Input is mapped to the 'A', 'B' and Arrow Keys. Below the display shows the number of CPU cycles per game loop. The number needs to be below 50,000 or frames will be skipped.

Every time unique game is compiled, a URL is generated that can be copied and pasted to send to 

#### Examples

[Tetris](https://play.dodolabs.io/?code=89e9a475)

[Nibbles](https://play.dodolabs.io/?code=ce1ea831)

#### Flashing

Flashing from the browser requires the following:

- Either a Chromebook or the [Dodo CLI](https://github.com/peternoyes/gododo)
- USB to Serial cable such as [this one](https://www.amazon.com/gp/product/B00DCJRD2Y/ref=od_aui_detailpages01?ie=UTF8&psc=1)

#### Chromebook

The following is required when using a Chromebook

- [Dodo Flashing Utility](https://chrome.google.com/webstore/detail/dodo-flash-utility/bckholjcbphjhdfgbejkjflcafdgbdkb)

With the App installed the Flash button will be available in the Navigation bar. Click flash and then pick the correct COM port. On a Mac with the above serial cable, /dev/tty.usbserial-A6040I72 is the correct COM port. Finally, be sure Dodo is turned plugged in and waiting on the splash screen. Clicking Start will transfer the current game to the cartridge. (The video on the App page is slightly outdated).

#### Dodo CLI

Once your game is developed use the Download button for fram.bin and save the file locally where it can be accessed from the terminal.

To use the CLI, follow the instructions [here](https://github.com/peternoyes/gododo) to install Go and the CLI. The CLI can be run from the terminal using:

```gododo -f```

Be sure to run the gododo command from the same folder where fram.bin is located.

You will then be prompted for the serial port and whether to flash a game or the firmware. Select G for Game to flash fram.bin to the Dodo!

#### Known Quircks

- Ctrl+C will not copy the URL on the simulator screen, right click copy must be used
- After signing in using GitHub for the first time, create and save a project right away, otherwise work might be lost.