# TADA68 Configuration Guide

Follow these steps to customize and flash your TADA68 mechanical keyboard using QMK.

NOTE: Try to use Windows. Up to this date, there isn't a Linux version for QMK Toolbox.

---

### 1. Prerequisite Software
Before starting, ensure you have the necessary tools and drivers installed on your system.

* **Flash Tool:** Download and install the [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases).
* **Drivers (Windows Only):** Install the [QMK Driver Installer](https://msys.qmk.fm/) to ensure your computer recognizes the keyboard in bootloader mode.

---

### 2. Create Your Keymap
Use the official QMK web configurator to define your layout.

1.  Navigate to the [QMK Configurator for TADA68](https://config.qmk.fm/#/tada68/LAYOUT_65_ansi).
2.  **Customize:** Drag and drop your preferred keycodes onto the layout.
3.  **Compile:** Click the **Compile** button and wait for the "Potato" to finish cooking.
4.  **Download:** Click **Firmware** to save the `.bin` file to your computer.

---

### 3. Flashing the Keyboard
There are two ways to do it. You can do it using QMK Toolbox or just use the "mass storage" (USB drive). 
For the first one follow the steps:

The TADA68 uses a specific bootloader process that differs from "mass storage" (USB drive) keyboards like the TADA68.

1.  **Open QMK Toolbox:** Launch the application you installed in Step 1.
2.  **Load Firmware:** Click **Open** and select the `.bin` file you just downloaded.
3.  **Enter Bootloader Mode:** Press the **Reset button** on the bottom of the PCB. 
    > **Note:** The keyboard will **not** appear as a USB drive. QMK Toolbox will instead display a message in yellow: `*** Atmel DFU device connected`.
4.  **Flash:** Click the **Flash** button.
5.  **Finish:** Wait for the "Flash complete" message. Your keyboard will automatically restart with the new layout.


For the USB storage, do the following:

1. Generate the .bin file using QMK
2. Click the Reset button on the bottom of the PCB
3. A USB drive will pop up, just replace the bin file.
4. Disconnect the keyboard and connect again.
5. Done. Test it.

---

### 4. Verification
Test your new keys using a tool like [Key test](https://en.key-test.ru/) or the **Test Keyboard** tab in the QMK Configurator.

