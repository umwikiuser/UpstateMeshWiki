---
title: Meshtastic Companion Setup
description: 
published: true
date: 2026-01-25T18:51:44.348Z
tags: meshtastic
editor: markdown
dateCreated: 2026-01-25T18:33:47.348Z
---

# Flash Meshtastic as a Companion

This is a general guide for setting up a companion that will work with the Upstate Mesh Meshtastic network. It will not cover all device specifics.

## Overview

This guide walks you through flashing **Meshtastic** firmware onto a supported LoRa device using the **Meshtastic Web Flasher**.

The web flasher is the recommended method for most users. It does not require installing local tools and helps avoid common flashing mistakes.

> **Antenna Warning**  
> Before powering on your device, ensure that the antenna is connected.  
> Powering a LoRa radio without an antenna can permanently damage the device.
{.is-warning}

> **USB-C Power Warning**  
> If your LoRa device uses USB-C, it is strongly recommended to use a **USB-A (standard USB) to USB-C cable** when flashing or powering the device.  
> Some LoRa boards have been damaged when connected with **USB-C to USB-C cables**, as certain host devices may negotiate and supply more current than the board is designed to handle.
{.is-warning}

---

## Prerequisites

Before you begin, make sure you have:

- A supported LoRa device
- A USB **data** cable (not charge-only)
- A computer running Windows, macOS, or Linux
- A modern **Chromium-based browser** (Chrome, Edge, or Brave)  
  ⚠️ Firefox does **not** work at this time
- The correct antenna for your device’s frequency band (e.g. **915 MHz in the US**)

---

## Step 1: Identify Your Device

Determine the exact model of your LoRa board before flashing.

Firmware is **device-specific**. Selecting the wrong device may prevent the device from booting.

If you are unsure which device you have, stop and ask for help before continuing.

---

## Step 2: Meshtastic Web Flasher

1. Open a Chromium-based browser (Chrome recommended).
2. Navigate to the MeshCore Web Flasher:

   https://flasher.meshtastic.org/

3. Connect your device to your computer using USB.

> DFU/Flash Mode
You will likely have to put your device in DFU mode or flash mode. In order to flash the firmware. To do this you'll need to locate the instructions for your device model. 
{.is-info}

4. Click `Select Target Device`, then slect your device from the list.

<br/>
<a href="/meshtastic/screenshot/screenshot_2026-01-25_at_12.36.03_pm.png" target="_blank">
  <img src="/meshtastic/screenshot/screenshot_2026-01-25_at_12.36.03_pm.png" width="256">
  <br/>click image to enlarge
</a>

<br/>
<a href="/meshtastic/screenshot/screenshot_2026-01-25_at_12.38.21_pm.png" target="_blank">
  <img src="/meshtastic/screenshot/screenshot_2026-01-25_at_12.38.21_pm.png" width="256">
  <br/>click image to enlarge
</a>


5. The latest most stable firmware will automatically be slected for you. Click the `Flash` button.

<br/>
<a href="/meshtastic/screenshot/screenshot_2026-01-25_at_12.39.35_pm.png" target="_blank">
  <img src="/meshtastic/screenshot/screenshot_2026-01-25_at_12.39.35_pm.png" width="256">
  <br/>click image to enlarge
</a>

You'll also see the latest change log, scroll to the bottom and click `Continue`.

6. Tick the **`Full Erase and Install`** option.

> **Erase Warning**  
> All data on the device will be permanently deleted.  
>  
> This is **not required** when updating firmware unless specifically instructed.
> Since this device is new, erasing it is recommended in this case.
{.is-warning}

7. Click the **`Erase Flash and Install`** button.

<br/>
<a href="/meshtastic/screenshot/screenshot_2026-01-25_at_12.42.50_pm.png" target="_blank">
  <img src="/meshtastic/screenshot/screenshot_2026-01-25_at_12.42.50_pm.png" width="256">
  <br/>click image to enlarge
</a>

Select your device from the list when prompted and click `Connect`.

<br/>
<a href="/meshtastic/screenshot/screenshot_2026-01-25_at_12.47.34_pm.png" target="_blank">
  <img src="/meshtastic/screenshot/screenshot_2026-01-25_at_12.47.34_pm.png" width="256">
  <br/>click image to enlarge
</a>

> **Flashing Warning**  
> Be patient while the device is erased and the new firmware is installed.  
> Do **not** unplug or power off the device during this process — doing so may permanently brick the device.
{.is-warning}

---

# Configure the Companion

Download the MeshCore companion app for your platform:

- **Android**:  
  [Google Play Store](https://msh.to/android)
- **Apple (iOS/macOS)**:  
  [App Store](https://msh.to/ios)
- **Chrome / Desktop**:  
  [Web App](https://client.meshtastic.org/)

---

## Connect to the Device

1. Open the Meshtastic app.
2. Using Bluetooth, pair your device with your phone or computer.
3. Click the on the device from the node list.
4. Click the `Set LoRa Region` button under the connected device.

<br/>
<a href="/meshtastic/screenshot/7e47cab797790f9ef4a2e2832acac1b3c2faa48fb76ee4ceafc9db238f9c4127.jpg" target="_blank">
  <img src="/meshtastic/screenshot/7e47cab797790f9ef4a2e2832acac1b3c2faa48fb76ee4ceafc9db238f9c4127.jpg" width="128">
  <br/>click image to enlarge
</a>

5. Click the `Region` dropdown and select `United States` from the list.

<br/>
<a href="/meshtastic/screenshot/4a16f6f3ebf9ae8434d8f365a7668901d5810a798d627d8442d47a0365d1a554.jpg" target="_blank">
  <img src="/meshtastic/screenshot/4a16f6f3ebf9ae8434d8f365a7668901d5810a798d627d8442d47a0365d1a554.jpg" width="128">
  <br/>click image to enlarge
</a>

6. Click `Save`. Your device will reboot.

<br/>
<a href="/meshtastic/screenshot/5d037f3fcb14c28c77c9785913609582b54feb07674d1c079c70f8e5f8682fe5.jpg" target="_blank">
  <img src="/meshtastic/screenshot/5d037f3fcb14c28c77c9785913609582b54feb07674d1c079c70f8e5f8682fe5.jpg" width="128">
  <br/>click image to enlarge
</a>

> 🎉 **Congratulations!**  
> Your device is now configured and connected to the Meshtastic network.
{.is-success}
