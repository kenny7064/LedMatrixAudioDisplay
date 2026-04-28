# 🎵 LED Matrix Audio Visualizer

An audio-reactive **WS2812B LED matrix display** powered by an ESP32 running WLED and a Raspberry Pi Zero.
The system converts audio signals into dynamic pixel art, creating a visual experience for music playback.

---

## 📌 Overview

This project was designed as a creative way to visualize audio from a record player while also learning more about addressable LEDs and embedded systems.

The display consists of four 16×16 WS2812B panels mounted in a custom 3D-printed frame, with power distributed safely across each panel.

---

## 💰 Parts & Cost Breakdown

| Part                              | Cost ($) |
| --------------------------------- | -------: |
| LED Displays (4 pack)             |    24.04 |
| Power Supply                      |    32.43 |
| Fuses                             |        1 |
| Wire                              |       10 |
| ESP32                             |        6 |
| Raspberry Pi Zero                 |       20 |
| Analog to Digital Audio Converter |        7 |
| 3D Prints                         |        2 |
| Miscellaneous                     |       10 |

**Total:** ~115 USD

> Not as cheap as intended — parts could definitely be sourced better, but this was built with what was available.

---

## 🧰 Materials

* 4× 16×16 WS2812B LED panels
* ESP32 WROOM (WLED controller)
* Raspberry Pi Zero (audio processing)
* 4× fuse holders + 10A blade fuses
* 14 AWG wire (power distribution)
* 22 AWG wire (signal wiring)
* Heat shrink tubing
* 3D printed PLA frame
* 12×12 inch, 2mm melamine board
* Hot glue
* Analog-to-digital audio converter

---

## ⚡ Power Notes

* Each panel can draw significant current at full brightness
* Panels are powered **individually (not daisy-chained)** to prevent voltage drop
* 14 AWG wire was used for main power lines to improve safety and reduce losses

---

## 🛠 Build

### STEP ONE — Frame Assembly

Attach the 3D printed pieces together using glue.
Tape around the outside for added rigidity.

> This is a prototype — future version will use snap-fit parts.

---

### STEP TWO — Mount Panels

Attach the LED matrices to:

* a 12×12 inch backing board
  **or**
* directly to the 3D printed frame

---

### STEP THREE — Prepare Power Wires

* Strip ~5–7mm of insulation
* Tin exposed wire
* Crimp lugs for PSU connection

For positive wires:

* Solder in fuse holder
* Add heat shrink

---

### STEP FOUR — Solder Power to Panels

* Solder power wires directly to each panel
* Do **not daisy-chain power**

> Each panel can draw high current — direct wiring is safer

* Tin pads and wires before soldering
* Clean flux with isopropyl alcohol

Optional:

* Run smaller power leads to ESP32 and Pi

---

### STEP FIVE — Data Connections

Connect panels in sequence:

```
Panel 1 DOUT → Panel 2 DIN
Panel 2 DOUT → Panel 3 DIN
Panel 3 DOUT → Panel 4 DIN
```

---

### STEP SIX — Controller Wiring

**ESP32:**

* GND → LED Ground
* 5V → LED 5V
* GPIO 5 → LED DIN

**Raspberry Pi Zero:**

* GND → LED Ground
* 5V → LED 5V

Audio input can be soldered directly to the Pi GPIO pins if no adapter is available.

---

### STEP SEVEN — Power Supply

* Connect all positive wires to PSU **V+**
* Connect all negative wires to PSU **V-**
* Use 2 connections per terminal if needed
* Connect AC input using a grounded power cable

⚠️ Be careful when working with AC power

---

## 🚀 Future Improvements

* Snap-fit frame design
* Cleaner wiring layout
* Better power distribution system
* Improved enclosure aesthetics

---

## 📷 Media

(Add your build images here)

---

## 🧠 What I Learned

* Power distribution for high-current LED systems
* ESP32 + WLED configuration
* Audio signal processing with Raspberry Pi
* Importance of wire gauge and voltage drop

---

## 🔥 Final Thoughts

This project was a first dive into LED systems and turned into a fully functional audio visualizer.
While not perfect, it laid the groundwork for more advanced builds in the future.

---
