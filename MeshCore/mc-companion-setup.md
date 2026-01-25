---
title: MeshCore Companion Setup
description: 
published: true
date: 2026-01-25T06:52:49.053Z
tags: meshcore
editor: markdown
dateCreated: 2026-01-25T03:38:50.253Z
---

> This page is a work in progress
{.is-warning}

# Flash MeshCore

## Overview


This guide walks you through flashing **MeshCore** firmware onto a supported LoRa device using the **MeshCore Web Flasher**.

The web flasher is the recommended method for most users. It does not require installing local tools and helps avoid common flashing mistakes.

> **Antenna Warning**
Before powering on your device, ensure that you have the antenna connected.
Powering a LoRa radio without an antenna can permanently damage the device.
{.is-warning}

> **USB-C Power Warning**
If your LoRa device uses USB-C, it is strongly recommended to use a USB-A (standard USB) to USB-C cable when flashing or powering the device.
Some LoRa boards have been damaged when connected with USB-C to USB-C cables, as certain host devices may negotiate and supply more current than the board is designed to handle.
{.is-warning}

## Prerequisites

Before you begin, make sure you have:

* A supported LoRa device
* A USB data cable (not charge-only)
* A computer running Windows, macOS, or Linux
* A modern Chromium-based browser (Chrome, Edge, Brave), FireFox does not work at this time.
* The correct antenna for your device’s frequency band (e.g. 915 MHz in the US)

---

## Step 1: Identify Your Device

Determine the exact model of your LoRa board before flashing.

Firmware images are **device-specific**. Flashing the wrong firmware may prevent the device from booting.

---

## Step 2: MeshCore Web Flasher

1. Open a Chrome browser.
2. Navigate to the MeshCore Web Flasher:

   https://flasher.meshcore.co.uk/

3. Connect your device to your computer using USB.
4. Type your device model in the list and select your device type.
  
<br/>
  <a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" target="_blank">
    <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" width="256">
  </a>

5. Select either `Companion Bluetooth` or `Companion USB` depending on how you plan to use the device.
  
<br/>
  <a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.21.20_pm.png" target="_blank">
    <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.21.20_pm.png" width="256">
  </a>

6. Check the `Erase device` button.

  > **Erase Warning**
  All data on the device will be destroyed. There is no need to do this when updating firmware unless specifically noted. Since this device is new and may have come pre-loaded with Meshtastic it makes sense to wipe it in this case.
  {.is-warning}

<br/>
  <a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.26.15_pm.png" target="_blank">
    <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.26.15_pm.png" width="256">
  </a>

7. Finally click the `Flash!` button.

  > **Warning**
  Be patient while the device erases and installs the new firmware. Do not unplug or power off the device, this could result in bricking your device.
  {.is-warning}


## Step 3: Configure The Companion

Download the MeshCore app for your device:

* **Android**: [Google Play Store](https://play.google.com/store/apps/details?id=com.liamcottle.meshcore.android) / [APK](https://files.liamcottle.net/MeshCore/)
* **iOS**: [App Store](https://apps.apple.com/gb/app/meshcore/id6742354151)
* **Chrome**: [Web App](https://app.meshcore.nz/)

Open the app. If using Bluetooth and pair the companion.

Connect to the companion by clicking the `Connect` button.

<br/>
  <a href="/meshcore/screenshot/5113415b73f29c47a4429f5bfb881e77d809043c82dc3e8b670dc5b50e05e1b7.jpg" target="_blank">
    <img src="/meshcore/screenshot/5113415b73f29c47a4429f5bfb881e77d809043c82dc3e8b670dc5b50e05e1b7.jpg" width="128">
  </a>

Select the companion device from the list.

<br/>
  <a href="/meshcore/screenshot/6a106884b90b28ee5a0fe7b3e98e97c0bbd2f4f5ef8052babac9b0c8a8acd17f.png" target="_blank">
    <img src="/meshcore/screenshot/6a106884b90b28ee5a0fe7b3e98e97c0bbd2f4f5ef8052babac9b0c8a8acd17f.png" width="128">
  </a>

Click the settings cog at the top.

<br/>
  <a href="/meshcore/screenshot/e86a90d01177e15ff867f943e51da1065d140aa64f84743aafcc79c1f933b399.jpg" target="_blank">
    <img src="/meshcore/screenshot/e86a90d01177e15ff867f943e51da1065d140aa64f84743aafcc79c1f933b399.jpg" width="128">
  </a>


Next set the following values:

* **Name**: Optional but reccomended, set a name for yourself on the network.
* **Frequency (MHz)**: Set to `910.525`
* **Bandwidth**: Set to `62.5`
* **Spreading Factor**: Set to `9`
* **Coding Rate**: Set to `8`
* **Transmit Power**: Depends on your antenna but `10` is a reasonable default.

Then click the white check mark at the top to save the settings.

<br/>
  <a href="/meshcore/screenshot/screenshot_2026-01-25_at_1.32.42_am.jpg" target="_blank">
    <img src="/meshcore/screenshot/screenshot_2026-01-25_at_1.32.42_am.jpg" width="128">
  </a>

> Congratulations! Your companion is configured to connect with our MeshCore network! 
{.is-success}
