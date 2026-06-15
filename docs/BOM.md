# Bill of Materials (BOM)

*Note: This repository is a fork of Marina's original project. I am contributing these docs to make her build easier to follow.*

## 3D parts
The hand itself is an existing open-source model. 
- Model: [InMoov Hand / Robotic Hand](https://www.thingiverse.com/thing:2269115)
- Creator: Ryan Gross ([grossrc](https://www.thingiverse.com/grossrc/designs))

Grab the STL files for the fingers, palm, and wrist mounting directly from that Thingiverse link.

## Electronics
You need the following hardware to make it move:
- 1 ESP32 Microcontroller (an ESP32 WROOM-32 DevKit works fine).
- 1 PCA9685 16-channel PWM/servo driver.
- 4 servo motors. MG996R or SG90 servos will work depending on what scale you print the hand at.
- 1 webcam. A built-in laptop camera is fine, or an external USB one.
- A 5V or 6V power supply. It needs to handle enough current for four servos moving at once, so get one rated for at least 3 amps.
- Jumper wires.
- Fishing line or braided thread to act as tendons for the fingers.
- Elastic cord for the back of the fingers so they snap back open when the servos release tension.

---
**Next Step: [Hardware Assembly & Wiring](ASSEMBLY.md)**
