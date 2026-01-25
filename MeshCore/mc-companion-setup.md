---
title: MeshCore Companion Setup
description: 
published: true
date: 2026-01-25T13:12:54.773Z
tags: meshcore
editor: markdown
dateCreated: 2026-01-25T03:38:50.253Z
---

# Flash MeshCore

## Overview

This guide walks you through flashing **MeshCore** firmware onto a supported LoRa device using the **MeshCore Web Flasher**.

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

## Step 2: MeshCore Web Flasher

1. Open a Chromium-based browser (Chrome recommended).
2. Navigate to the MeshCore Web Flasher:

   https://flasher.meshcore.co.uk/

3. Connect your device to your computer using USB.
4. Begin typing your device model and select the correct device from the list.

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" width="256">
  <br/>click image to enlarge
</a>

5. Select either **`Companion Bluetooth`** or **`Companion USB`**, depending on how you plan to use the device.

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.21.20_pm.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.21.20_pm.png" width="256">
  <br/>click image to enlarge
</a>

6. Check the **`Erase device`** option.

> **Erase Warning**  
> All data on the device will be permanently deleted.  
>  
> This is **not required** when updating firmware unless specifically instructed.  
> Since this device is new and may have come preloaded with Meshtastic, erasing it is recommended in this case.
{.is-warning}

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.26.15_pm.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.26.15_pm.png" width="256">
  <br/>click image to enlarge
</a>

7. Click the **`Flash!`** button.

> **Flashing Warning**  
> Be patient while the device is erased and the new firmware is installed.  
> Do **not** unplug or power off the device during this process — doing so may permanently brick the device.
{.is-warning}

---

# Configure the Companion

Download the MeshCore companion app for your platform:

- **Android**:  
  [Google Play Store](https://play.google.com/store/apps/details?id=com.liamcottle.meshcore.android)  
  [APK download](https://files.liamcottle.net/MeshCore/)
- **iOS**:  
  [App Store](https://apps.apple.com/gb/app/meshcore/id6742354151)
- **Chrome / Desktop**:  
  [Web App](https://app.meshcore.nz/)

---

## Connect to the Device

1. Open the MeshCore app.
2. If using Bluetooth, pair your device with your phone or computer.
3. Click the **`Connect`** button.

<br/>
<a href="/meshcore/screenshot/5113415b73f29c47a4429f5bfb881e77d809043c82dc3e8b670dc5b50e05e1b7.jpg" target="_blank">
  <img src="/meshcore/screenshot/5113415b73f29c47a4429f5bfb881e77d809043c82dc3e8b670dc5b50e05e1b7.jpg" width="128">
  <br/>click image to enlarge
</a>

4. Select your companion device from the list.

<br/>
<a href="/meshcore/screenshot/6a106884b90b28ee5a0fe7b3e98e97c0bbd2f4f5ef8052babac9b0c8a8acd17f.png" target="_blank">
  <img src="/meshcore/screenshot/6a106884b90b28ee5a0fe7b3e98e97c0bbd2f4f5ef8052babac9b0c8a8acd17f.png" width="128">
  <br/>click image to enlarge
</a>

5. Click the **settings cog** at the top of the screen.

<br/>
<a href="/meshcore/screenshot/e86a90d01177e15ff867f943e51da1065d140aa64f84743aafcc79c1f933b399.jpg" target="_blank">
  <img src="/meshcore/screenshot/e86a90d01177e15ff867f943e51da1065d140aa64f84743aafcc79c1f933b399.jpg" width="128">
  <br/>click image to enlarge
</a>

---

## Network Configuration

Set the following values:

- **Name**: Optional but recommended. This identifies you on the network
- **Frequency (MHz)**: `910.525`
- **Bandwidth**: `62.5`
- **Spreading Factor**: `9`
- **Coding Rate**: `8`
- **Transmit Power**: Depends on your antenna; `10` is a reasonable default

Click the **white check mark** at the top to save your settings.

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-25_at_1.32.42_am.jpg" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-25_at_1.32.42_am.jpg" width="128">
  <br/>click image to enlarge
</a>

> 🎉 **Congratulations!**  
> Your device is now configured and connected to the MeshCore network.
{.is-success}
