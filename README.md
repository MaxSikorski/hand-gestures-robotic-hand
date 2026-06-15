# Hand Gesture Controlled Humanoid Robotic Hand

*First things first: this is entirely Marina's (mmm1712) project. I am just a contributor cleaning up the documentation and structure so it's easier for others to build. All credit for the computer vision pipeline and the ESP32 integration goes to her.*

[![YouTube Demo](https://img.youtube.com/vi/_GSqwtdkvcs/0.jpg)](https://www.youtube.com/watch?v=_GSqwtdkvcs)
> *Watch the YouTube Demo*

A webcam tracks your hand movements. A Python script interprets those gestures and sends serial commands to an ESP32, which drives four servos to mirror your hand on a 3D-printed model. 

Python handles the high-level logic (figuring out if a finger is open or closed). The ESP32 handles the precise motor control.

## Repository Structure

```text
hand-gestures-robotic-hand/
├── docs/
│   ├── BOM.md               # Parts you need to buy and print
│   ├── ASSEMBLY.md          # Hardware wiring and physical build
│   └── SOFTWARE.md          # Flashing the ESP32 and running the Python tracker
├── Python/
│   └── ...                  # MediaPipe and PySerial scripts
├── esp32/
│   └── ...                  # C++ code for the microcontroller
└── README.md                # You are here
```

## Quick Start

If you want to build this, check the `docs/` folder.
1. **Get the parts:** The [Bill of Materials (BOM)](docs/BOM.md) lists the electronics and links to the 3D printable files.
2. **Build the hardware:** The [Assembly Guide](docs/ASSEMBLY.md) covers how to put it together and wire the servos.
3. **Run the code:** The [Software Guide](docs/SOFTWARE.md) explains how to set up Python and flash the ESP32.

## Hardware setup
- ESP32 
- PCA9685 16-channel servo driver (I2C)
- 4 servo motors (Thumb, Index, Middle, and a shared servo for the Ring and Pinky fingers)

*The ring and pinky fingers currently share one servo to keep the mechanics simple. They might be separated in a later revision.*
