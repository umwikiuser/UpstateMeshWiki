---
title: MeshCore Companion Setup
description: 
published: true
date: 2026-01-25T04:40:31.756Z
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

  ![screenshot_2026-01-24_at_11.16.28_pm.png](/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png){.align-left}

5. Select either `Companion Bluetooth` or `Companion USB` depending on how you plan to use the device.

  ![screenshot_2026-01-24_at_11.21.20_pm.png](/meshcore/screenshot/screenshot_2026-01-24_at_11.21.20_pm.png){.align-left}

6. Check the `Erase device` button.

  > **Erase Warning**
  All data on the device will be destroyed. There is no need to do this when updating firmware unless specifically noted. Since this device is new and may have come pre-loaded with Meshtastic it makes sense to wipe it in this case.
  {.is-warning}

  ![screenshot_2026-01-24_at_11.26.15_pm.png](/meshcore/screenshot/screenshot_2026-01-24_at_11.26.15_pm.png){.align-left}

7. Finally click the `Flash!` button.

  > **Warning**
  Be patient while the device erases and installs the new firmware. Do not unplug or power off the device, this could result in bricking your device.
  {.is-warning}


## Step 3: Configure The Companion

Download the MeshCore app for your device:

* **Android**: [Google Play Store](https://play.google.com/store/apps/details?id=com.liamcottle.meshcore.android) / [APK](https://files.liamcottle.net/MeshCore/)
* **iOS**: [App Store](https://apps.apple.com/gb/app/meshcore/id6742354151)
* **Chrome**: [Web App](https://app.meshcore.nz/)

