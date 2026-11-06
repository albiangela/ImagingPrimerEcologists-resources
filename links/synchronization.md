---
layout: default
---

# Synchronization

Synchronizing acquisitions across cameras ensures frames are collected at fixed
intervals. Trigger signals can be generated through hardware or software, each
with distinct trade-offs.

## Hardware Trigger

A hardware trigger uses a physical timing device (typically a microcontroller or
single-board computer) that sends periodic electrical pulses directly to each
camera's trigger input. Because the signal propagates near-instantaneously across
wired connections, this enables microsecond-level synchronization, essential for
high-speed acquisition (see also
[Workflow Automation](workflow-automation.md) for single-board computers and
microcontrollers).

## Software Trigger

A software trigger sends acquisition commands via the camera's communication
interface (USB, GigE, etc.) using manufacturer APIs or SDKs. It is more flexible
and easier to implement but inherently less precise (millisecond-level), since
timing is affected by OS scheduling and network latency. Where triggers are
unavailable, cameras can also be synchronized post-hoc through sound, using
frequency decomposition (Fourier transform) of the audio signal to recover the
temporal offset (Francisco et al. 2020).

## Acquisition software

Overview of camera acquisition software supporting single- and multi-camera setups.

| Software | Description | Reference |
|----------|-------------|-----------|
| [mokap](https://github.com/FlorentLM/mokap) | Acquisition software | https://github.com/FlorentLM/mokap |
| [campy](https://github.com/ksseverson57/campy) | Acquisition software with realtime-compression | https://github.com/ksseverson57/campy |
| [pypylon](https://github.com/basler/pypylon) | Official Python wrapper of the Basler API pylon | https://github.com/basler/pypylon |
| [flirpy](https://doi.org/10.5281/zenodo.3866331) | Python library to interact with FLIR cameras | https://doi.org/10.5281/zenodo.3866331 |

## Post-processing audio alignment

The final manuscript (§4.1.2) also names [audalign](https://pypi.org/project/audalign/) and [Blender](https://www.blender.org/) for post-hoc alignment. Record a distinctive shared audio event and verify the resulting frame offsets; audio alignment does not replace precise hardware triggering when sub-frame timing is required.

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
