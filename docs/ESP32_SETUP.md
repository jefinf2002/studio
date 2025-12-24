# ESP32 Setup Guide for EEZ Studio Projects

This guide will help you set up the Arduino IDE with ESP32 board support for use with EEZ Studio LVGL projects.

## Prerequisites

- Arduino IDE 1.8.x or 2.x installed
- Internet connection

## Installing ESP32 Board Package in Arduino IDE

### Method 1: Using Arduino IDE 2.x (Recommended)

1. **Open Arduino IDE 2.x**

2. **Add ESP32 Board Manager URL:**
   - Go to `File` → `Preferences` (or `Arduino IDE` → `Settings` on macOS)
   - In the "Additional Boards Manager URLs" field, add:
     ```
     https://espressif.github.io/arduino-esp32/package_esp32_index.json
     ```
   - Click `OK`

3. **Install ESP32 Board Package:**
   - Go to `Tools` → `Board` → `Boards Manager`
   - In the search box, type `esp32`
   - Find **"esp32 by Espressif Systems"**
   - Select the version you want:
     - **Recommended: Latest stable version (3.0.x or newer)**
     - For compatibility with older projects: version 2.0.x
   - Click `Install`
   - Wait for the installation to complete

### Method 2: Using Arduino IDE 1.8.x

1. **Open Arduino IDE 1.8.x**

2. **Add ESP32 Board Manager URL:**
   - Go to `File` → `Preferences`
   - In the "Additional Boards Manager URLs" field, add:
     ```
     https://espressif.github.io/arduino-esp32/package_esp32_index.json
     ```
   - Click `OK`

3. **Install ESP32 Board Package:**
   - Go to `Tools` → `Board` → `Boards Manager`
   - In the search box, type `esp32`
   - Find **"esp32 by Espressif Systems"**
   - Select the version you want
   - Click `Install`

## Troubleshooting Common Issues

### Issue: Board Manager Installation Fails

**Problem:** Download fails or times out when installing ESP32 board package

**Solutions:**

1. **Check your internet connection**
   - Make sure you have a stable internet connection
   - Try disabling VPN or proxy temporarily

2. **Clear Arduino cache:**
   - Close Arduino IDE
   - Delete the cache folder:
     - **Windows:** `C:\Users\<YourUsername>\AppData\Local\Arduino15\`
     - **macOS:** `~/Library/Arduino15/`
     - **Linux:** `~/.arduino15/`
   - Restart Arduino IDE and try again

3. **Use manual installation:**
   - Download the package manually from: https://github.com/espressif/arduino-esp32
   - Follow the manual installation instructions in the repository

4. **Try a different version:**
   - If version 3.3.5 specifically fails, try:
     - Latest stable version (3.0.x series)
     - Or stable version 2.0.17
   - Note: Version 3.3.5 may not exist; check available versions in Board Manager

5. **Check firewall/antivirus:**
   - Temporarily disable firewall or antivirus
   - Add Arduino IDE to exceptions list

### Issue: Board Not Showing in Tools Menu

**Problem:** After installation, ESP32 board doesn't appear in the boards list

**Solutions:**

1. **Restart Arduino IDE**
   - Close and reopen Arduino IDE completely

2. **Verify installation:**
   - Check `Tools` → `Board` → `ESP32 Arduino`
   - You should see various ESP32 board options

3. **Reinstall the package:**
   - Go to Boards Manager
   - Find ESP32 package
   - Click `Remove`
   - Click `Install` again

## Recommended ESP32 Board Package Versions

- **For new projects:** Version 3.0.x (latest stable)
- **For legacy compatibility:** Version 2.0.17
- **Minimum supported:** Version 2.0.0

## Verifying Installation

1. Go to `Tools` → `Board` → `ESP32 Arduino`
2. You should see board options like:
   - ESP32 Dev Module
   - ESP32-S2 Dev Module
   - ESP32-S3 Dev Module
   - ESP32-C3 Dev Module
   - And many more...

## Using ESP32 with EEZ Studio

Once you have ESP32 board support installed:

1. **Create or open an EEZ Studio LVGL project**
2. **Configure the build settings** in EEZ Studio:
   - Set the destination folder for generated code
   - Configure LVGL include path
3. **Build the project** in EEZ Studio
4. **Open the generated Arduino sketch**
5. **Select your ESP32 board** in Arduino IDE
6. **Select the COM port** for your ESP32
7. **Upload to your ESP32 board**

## Example ESP32 Projects

Check out these example projects that use EEZ Studio with ESP32:

- [Nscreen_32-esp32-eez-flow-demo](https://github.com/eez-open/Nscreen_32-esp32-eez-flow-demo)
- [esp32-lvgl-eez-demo](https://github.com/eez-open/esp32-lvgl-eez-demo)

## Additional Resources

- [ESP32 Arduino Core Documentation](https://docs.espressif.com/projects/arduino-esp32/en/latest/)
- [ESP32 Arduino Core GitHub](https://github.com/espressif/arduino-esp32)
- [EEZ Studio Documentation](https://github.com/eez-open/studio)
- [LVGL Documentation](https://docs.lvgl.io/)

## Getting Help

If you continue to experience issues:

1. Check the [EEZ Studio Issues](https://github.com/eez-open/studio/issues)
2. Visit the [EEZ Studio Discord](https://discord.gg/q5KAeeenNG)
3. Consult the [ESP32 Arduino Core Issues](https://github.com/espressif/arduino-esp32/issues)
