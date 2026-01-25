---
title: MeshCore Repeter Setup
description: 
published: true
date: 2026-01-25T17:03:06.994Z
tags: meshcore
editor: markdown
dateCreated: 2026-01-25T03:39:40.128Z
---

> This page is a work in progress
{.is-warning}

# Flash MeshCore as a Repeater

This is a general guide for setting up a repeater that will work with the Upstate Mesh MeshCore network. It will not cover all device specifics.

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

> DFU/Flash Mode
You will likely have to put your device in DFU mode or flash mode. In order to flash the firmware. To do this you'll need to locate the instructions for your device model. 
{.is-info}

4. Begin typing your device model and select the correct device from the list.

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-24_at_11.16.28_pm.png" width="256">
  <br/>click image to enlarge
</a>

5. Select **`Repeater`**.

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
<a href="/meshcore/screenshot/screenshot_2026-01-25_at_11.39.16_am.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-25_at_11.39.16_am.png" width="256">
  <br/>click image to enlarge
</a>

7. Click the **`Flash!`** button. Then select your device from the list and click `Connect`

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-25_at_11.51.49_am.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-25_at_11.51.49_am.png" width="256">
  <br/>click image to enlarge
</a>

> **Flashing Warning**  
> Be patient while the device is erased and the new firmware is installed.  
> Do **not** unplug or power off the device during this process — doing so may permanently brick the device.
{.is-warning}

8. Once the web flasher says `Flashing complete!` reboot your device if needed. Then click `Configure via USB`.

<br/>
<a href="/meshcore/screenshot/screenshot_2026-01-25_at_11.55.29_am.png" target="_blank">
  <img src="/meshcore/screenshot/screenshot_2026-01-25_at_11.55.29_am.png" width="256">
  <br/>click image to enlarge
</a>

---

# Configure the Repeater



