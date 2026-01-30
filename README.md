# Side-Projects

Blue Light Noise Trigger (Raspberry Pi)

A Raspberry Pi project that listens to microphone input and turns a light ON when sound levels exceed a defined threshold, then turns it OFF when levels drop back down.

Designed for real-world use:

✔ debounce protection

✔ daily logging

✔ hourly breakdowns

✔ max dB tracking

✔ auto-start on boot via systemd

✔ safe shutdown handling

What this does

Continuously monitors microphone audio levels

Converts audio RMS values to relative dB

When sound level ≥ threshold (default: 90 dB):

Turns a GPIO-controlled light ON

Logs the event

When sound level drops below threshold:

Turns the light OFF

Creates daily log files with:

Number of times the light turned ON

Hourly breakdown of triggers

Maximum dB observed that day

Hardware Requirements

Raspberry Pi (tested on Pi OS)

USB microphone or sound input device

Relay module, MOSFET, or LED connected to a GPIO pin

Light or device being controlled

Important:
Most microphones do not provide true SPL dB readings. Values are relative unless you calibrate with a real sound meter.

Software Requirements

Python 3

Raspberry Pi OS

Required Python packages:

numpy

sounddevice

RPi.GPIO
