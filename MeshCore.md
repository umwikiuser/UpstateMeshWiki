---
title: MeshCore
description: MeshCore is a multi platform system for secure text based communications using LoRa radio hardware
published: true
date: 2026-01-25T07:54:24.061Z
tags: meshcore
editor: markdown
dateCreated: 2026-01-24T05:29:26.004Z
---

# <img src="/meshcore_logo.png" alt="meshcore_logo" width="32" height="32"> Upstate Mesh MeshCore

## UM MeshCore Quick Reference

The following radio values are used on the Upstate Mesh MeshCore network

* **Frequency (MHz)**: 910.525
* **Bandwidth**: 62.5
* **Spreading Factor**: 9
* **Coding Rate**: 8

To quickly set those values via commandline:

```python
set radio 910.525,62.5,9,8
```


## What Is MeshCore?

> MeshCore is a multi platform system for enabling secure text based communications utilising LoRa radio hardware. It can be used for Off-Grid Communication, Emergency Response & Disaster Recovery, Outdoor Activities, Tactical Security including law enforcement and private security and also IoT sensor networks. - [MeshCore](https://meshcore.co.uk/)

In short MeshCore is software that runs on various kinds of hardware that have integrated LoRa radios. In even simpler terms think of MeshCore like an operating system like Anroid or iOS and the LoRa hardware like an iPhone or Galaxy S phone.

## Device Roles

There are a few kinds of MeshCore devices that serve different functions on the mesh network:

* **Companion Bluetooth** - LoRa board that pairs with a phone or computer via bluetooth to send text messages from the phone or computer over the LoRa radio.
* **Companion USB** - LoRa board that pairs with a phone or computer via USB to send text messages from the phone or computer over the LoRa radio.
* **Repeater** - A standalone LoRa board that repeats incoming packets to the wider mesh network. Often paired with strong antenna and solar pannels to run coninously outdoors.
* **Room Server** - Room servers store message history on them and push the stored messages to users. Room servers allow roaming users to come back later and retrieve message that were recieved while the user was out of range.

The most common devices are `Companion Bluetooth/USB` and `Repeater`. There is also the ability to configure IoT devices called sensors but we will focus on the message and communications aspects of MeshCore.

## MeshCore Index

* [MeshCore Companion Setup](/MeshCore/mc-companion-setup)
* [MeshCore Repeater Setup](/MeshCore/mc-repeater-setup)
