
# USB2 High Speed Core
This core is a customization of the [LUNA project](https://github.com/greatscottgadgets/luna),
which is a USB analyzer.

The aim of this project is to strip down the original project to
its USB2 highspeed-capable core which is easy to integrate into your own
FPGA project.

## Notable differences to the LUNA project

This project implements stream based isochronous
in and out endpoints, with a FIFO-like interface,
which the LUNA project does not.

The original motivation for this project was to provide everything
needed to get a working USB2 audio class compliant example, supporting audio and MIDI.

## Project Structure

This project is broken down into several directories:

* `luna` -- the primary LUNA python toolkit; generates gateware and provides USB functionality
  * `luna/gateware` -- the core gateware components for LUNA; and utilities for stitching them together
* `examples` -- simple LUNA-related examples; mostly gateware-targeted, currently
* `docs` -- sources for the LUNA Sphinx documentation
* `applets` -- pre-made gateware applications that provide useful functionality on their own (e.g., are more than examples)

## Project Documentation

LUNA's documentation is captured on [Read the Docs](https://luna.readthedocs.io/en/latest/). Raw documentation sources
are in the `docs` folder.

## Related Projects
* [jt51-synth](https://github.com/hansfbaier/jt51-synth/), a FM synthesizer,
based on jotego's open source implementation of the Yamaha YM2151.
The project uses this core as USB MIDI interface.
* [adat-usb2-audio-interface](https://github.com/hansfbaier/adat-usb2-audio-interface),
an USB2 high speed audio interface with ADAT inputs and outputs
