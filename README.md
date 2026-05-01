# R2-D2 Sphero Console

A single-file Web Bluetooth control console for an R2-D2 Sphero droid. The app provides a dark, dashboard-style browser interface for connecting to the droid, driving it, controlling lights and sounds, running onboard animations, reading device information, and streaming live sensor data.

<img width="2705" height="1353" alt="image" src="https://github.com/user-attachments/assets/5248d76f-96d3-4ed2-9f53-f8cd16208715" />

## Features

- Connects to a compatible Sphero droid over Web Bluetooth
- Wake, sleep, disconnect, and emergency stop controls
- Battery, voltage, Bluetooth name, app version, and SKU readouts
- Joystick-based driving with heading and speed controls
- Direction buttons for forward, backward, left, and right movement
- Drive flags for reverse, turbo, fast turn, drift, and stabilization
- Raw motor controls for left and right drive motors
- R2-D2 leg actions, including tripod stance, two-leg stance, and waddle
- Dome/head positioning controls
- Front and rear LED color controls
- Logic and holoprojector LED brightness controls
- Built-in sound browser with droid and mood filters
- Audio playback, queue mode, volume control, and stop audio
- Animation selector and playback controls
- Live sensor streaming with graph output
- Collision, gyro, acceleration, and battery event logging
- Raw command and shell command tools for advanced experimentation
- Built-in hover tooltips for most controls

## Project Structure

```text
.
└── index.html
````

This project is intentionally self-contained. The HTML, CSS, and JavaScript are all included in `index.html`, so no build step or package installation is required.

## Requirements

* A browser with Web Bluetooth support
* A compatible Sphero R2-D2 droid
* Bluetooth enabled on the host device
* The page must be opened from a context where Web Bluetooth is available, such as `localhost` or a secure origin

## Usage

1. Clone or download this repository.
2. Open `index.html` in a Web Bluetooth-capable browser.
3. Power on or wake your Sphero R2-D2 droid.
4. Click **Connect**.
5. Select the droid from the Bluetooth chooser.
6. Use the console panels to control the droid.

## Console Panels

### Bot

Displays device and power information, including battery estimate, voltage, battery state, Bluetooth name, app version, and SKU. This panel also includes advanced tools for setting the Bluetooth name, sending shell commands, and sending raw command packets.

### Drive

Provides movement controls through a joystick, heading input, speed slider, and directional buttons. The panel also includes tripod drive preparation, yaw reset, stabilization, drive flags, and raw motor controls.

### Droid

Controls R2-D2-specific behavior, including animations, leg actions, dome/head position, LED colors, brightness values, sounds, audio mode, volume, and audio stopping.

### Sensors

Streams live telemetry from the droid and draws sensor data to a canvas graph. The panel includes controls for collision detection, gyroscope events, acceleration events, battery events, and locator reset.

## Safety Notes

Use this console in an open area where the droid has room to move. The **Stop All** button is intended as a quick emergency stop for drive, raw motors, animation, and audio. Be careful with raw commands and shell commands, as they are intended for advanced experimentation.

## Development Notes

The app defines a `SpheroV2` controller class that handles Bluetooth connection setup, handshake behavior, command sending, notifications, device queries, driving, animation, lighting, sound, sensor streaming, and event handling.

Because the program is implemented as a single static HTML file, it can be edited directly and served without a bundler.

## Disclaimer

This is an experimental browser-based control console for hobbyist use. It is not an official Sphero or Star Wars product.

## Licence

This project is released under the MIT Licence. See [`LICENSE`](LICENSE) for details.
