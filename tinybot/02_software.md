# Step 2: Software Setup

In this step, you'll configure the robot's software and upload it to the TinyPICO microcontroller.

## Before You Start

- Make sure you completed [Step 1: Preparation](01_prep.md)
- Attach the TinyPICO and Dynamixel motors to your laptop via USB

## About the Control Modes

The robot has 3 control modes, selected by editing `platformio.ini`:

| Mode | Source File | Description |
|------|-------------|-------------|
| **2-motor** | `+<2motor.cpp>` | Control each motor's position (0-360 degrees) |
| **Tilty** | `+<tilty.cpp>` | Dashboard robot that turns and looks around |
| **Drive** | `+<drive.cpp>` | Wheeled driving robot |

We'll start in **2-motor mode** for initial setup. You'll switch modes later when you build your robot.

## 1. Select the Control Mode

Open `platformio.ini`. You can select which mode to use by commenting/uncommenting lines with `;`:

```ini
; Comment out modes you don't want with a semicolon
;+<drive.cpp>
;+<tilty.cpp>
+<2motor.cpp>     ; This is the active mode
```

For now, keep it in **2-motor mode**.

## 2. Set Your WiFi Name

Your robot hosts its own local WiFi network (no internet). Each group needs a unique network name.

Open `src/network.h` and set a unique SSID (we recommend using your name):

```cpp
const char* ssid = "YourNameHere";
```

## 3. Upload Firmware to TinyPICO

Upload the C++ firmware code to the microcontroller:

1. Click the **arrow button (->)** at the bottom of VS Code to upload.
2. Wait for the upload to complete.

## 4. Build the Filesystem Image

The browser control interface (HTML/JS/CSS in the `data` folder) needs to be uploaded separately:

1. Click the **ant icon** on the sidebar.
2. Go to **Platform > Build Filesystem Image**.

## 5. Upload the Filesystem Image

1. **Important:** Close the Serial Monitor first (hover over "Monitor" at the bottom and click the trash icon).
2. Click the **ant icon** > **Platform > Upload Filesystem Image** (NOT OTA!!).

## 6. Connect Your Phone to the Robot

1. Open the **Serial Monitor** in VS Code and note the IP address displayed. If no IP appears, press the **reset button** on the TinyPICO.
2. On your phone, connect to the WiFi network with the name you set in step 2.
3. Open a browser and go to the URL shown in the Serial Monitor (e.g., `https://192.168.XX.YY/2motor.html`).
4. Press the **Activate** button on the control panel.
5. Move the sliders — if numbers appear in the Serial Monitor, you're connected!

> **Important:** Always set both motors to position **0** before unplugging them.

## 7. Audio (Optional)

You can also make the robot produce sounds:

### Connect a Bluetooth Speaker
1. Turn on a Bluetooth speaker.
2. Have a group member connect their phone to the same WiFi network and pair with the speaker.

### Use the Audio Feature
1. In your phone's browser, go to `https://{IP address}/sounds.html`.
2. Allow microphone access if prompted.
3. Press **Record** to start recording, **Stop** to finish.
4. Name your recording and press **OK** to save.
5. Press **Play** to play it back through the speaker.

---

**Next step:** [Hardware Assembly](03_hardware.md)
