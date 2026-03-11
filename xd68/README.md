# XD68 Configuration Guide

Follow these steps to customize and flash your XD68 mechanical keyboard using QMK.

NOTE: Try to use Windows. Up to this date, there isn't a Linux version for QMK Toolbox.

---

### 1. Prerequisite Software
Before starting, ensure you have the necessary tools and drivers installed on your system.

* **Flash Tool:** Download and install the [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases).
* **Drivers (Windows Only):** Install the [QMK Driver Installer](https://msys.qmk.fm/) to ensure your computer recognizes the keyboard in bootloader mode.

---

### 2. Create Your Keymap
Use the official QMK web configurator to define your layout.

1.  Navigate to the [QMK Configurator for XD68](https://config.qmk.fm/#/xiudi/xd68/LAYOUT_65_ansi).
2.  **Customize:** Drag and drop your preferred keycodes onto the layout.
3.  **Compile:** Click the **Compile** button and wait for the "Potato" to finish cooking.
4.  **Download:** Click **Firmware** to save the `.hex` file to your computer.

---

### 3. Flashing the Keyboard
The XD68 uses a specific bootloader process that differs from "mass storage" (USB drive) keyboards like the TADA68.

1.  **Open QMK Toolbox:** Launch the application you installed in Step 1.
2.  **Load Firmware:** Click **Open** and select the `.hex` file you just downloaded.
3.  **Enter Bootloader Mode:** Press the **Reset button** on the bottom of the PCB. 
    > **Note:** The keyboard will **not** appear as a USB drive. QMK Toolbox will instead display a message in yellow: `*** Atmel DFU device connected`.
4.  **Flash:** Click the **Flash** button.
5.  **Finish:** Wait for the "Flash complete" message. Your keyboard will automatically restart with the new layout.

---

### 4. Verification
Test your new keys using a tool like [Key test](https://en.key-test.ru/) or the **Test Keyboard** tab in the QMK Configurator.

