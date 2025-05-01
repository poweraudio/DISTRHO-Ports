**PowerAudio fork of DISTRHO Ports**

This fork of DISTRHO Ports has the following changes:

* In this branch, `with-license-info`, license information has been added in
  a README file for each plugin. Additionally, GPLv2-only plugins are built
  with a GPLv2-licensed version of JUCE.
* Plugins are built with [a fork of JUCE] that includes fixes for IBM Power.
* Modified Vitalium to use [SIMDe] on architectures without native SIMD
  support, enabling builds on Power. SIMDe v0.8+ must be installed on your
  system.
* Modified pitchedDelay to use [SIMDe] \(if installed) to support architectures
  other than x86 and ARM.

The following changes have since been merged upstream:

* Added support for Power to build scripts.

[a fork of JUCE]: https://github.com/poweraudio/distrho-juce
[SIMDe]: https://github.com/simd-everywhere/simde

---

# DISTRHO Ports

[![Build Status](https://travis-ci.org/DISTRHO/DISTRHO-Ports.png)](https://travis-ci.org/DISTRHO/DISTRHO-Ports)

DISTRHO is an open source project with the goal of making cross-platform audio plugins and GNU/Linux + LV2 ports.

<b>This repository contains the GNU/Linux and LV2 ports, specifically those made with [JUCE](https://travis-ci.org/DISTRHO/JUCE)</b>

## BUILD DEPENDENCIES

To build plugins, you first need to install the following dependencies:

All OSes:

- meson

GNU/Linux: (development versions of these)

- ALSA
- freetype2
- fftw3
- OpenGL/Mesa
- X11 core and extensions (XShm, XRender and XCursor)

## BUILD and INSTALL

In order to build and install the plugins, just run the usual steps for a meson project:

```
meson setup build --buildtype release
ninja -C build
ninja -C build install
```
