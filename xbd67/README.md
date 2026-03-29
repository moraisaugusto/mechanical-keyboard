# XB67 (KBD67 MKII)

A 65% mechanical keyboard pcb featuring hot-swap design, USB-C interface, and per-key RGB backlighting. Compatible with QMK/VIA firmware.

---

## VIA Website Configuration

The easiest way to customize your XB67 keyboard is using the VIA software through your web browser. This method requires no manual flashing and the PCB is pre-configured for VIA use.

**Important:** If using the UseVia website (https://usevia.app/), you may encounter device access errors on Linux. Check your browser logs at `brave://device-log/` or `chrome://device-log/` for permission issues.

#### Linux Permission Fix

If you see an error message like:

`Failed to open '/dev/hidraw3': FILE_ERROR_ACCESS_DENIED`

Grant read/write permission to the HID device:

```bash
sudo chmod a+rw /dev/hidraw3
```

*(Note: The device number varies - check your browser logs for the correct `/dev/hidraw` path)*

### Steps to Configure with VIA

**Step 1: VIA Software or website**

1. Visit [VIA official website](https://www.usevia.app/)
2. Plug your XB67 keyboard into your computer via USB-C
3. Wait for the VIA software to detect the device
4. Configure the keyboard as you wish and save it
5. Done, everything is already applied

## Manual Configuration (QMK Configurator)

**This step can completely brick the keyboard. Please, do the backup of your firmware.**

For advanced users who prefer manual flashing:

1. Visit [QMK Configurator](https://config.qmk.fm/)
2. Select "KBD67 Mark II RGB" as your keyboard (or customize layout manually)
3. Configure keymap, macros, and layers
4. Click "Download .hex" to get your firmware file
5. Use QMK Toolbox to flash the keyboard
6. The PCB will reboot with your new configuration

---

## Specification
- **PCB**: KBD67 MKII hot-swap wired PCB
- **Interface**: USB-C
- **RGB**: Per-key RGB backlighting
- **Layout**: 65% (67 keys)
- **Firmware Support**: QMK and VIA
- **Mount Style**: Silicone gasket mount
- **Plate**: FR4/Aluminum/Polycarbonate options
- **Typing Angle**: 6° adjustable
- **Assembly Weight**: ~1.6kg

---

### Links
* [KBD67 MKII RGB V3 VIA Binary](https://drive.google.com/file/d/1GeBpT_ko0yr4zOiQWoyC03d7ZK1YeO6j/view)
* [Flash Manual](https://docs.google.com/document/d/1KhxKkIncCOCKx9nUxhKok5NISU-FQ4tTHofdl_noNZQ/edit)
* [QMK VIA Official Documentation](https://docs.qmk.fm/#/getting_started_build_guide?id=via)
