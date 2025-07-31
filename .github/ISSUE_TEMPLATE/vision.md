---
name: '[LEARNING] Vision'
about: Brief guide on PhotonVision. Assign yourself to the task and complete it by following the instructions.
title: '[LEARNING] Vision'
labels: ''
assignees: ''
---

## 🎯 Description

This ticket is a quick introduction on how to use PhotonVision to config Arducams and Limelights.

## 📂 Acceptance Criteria
- [ ] Coprocessor Networking
  - [ ] When multiple cameras are needed on a robot, our team uses a configuration that utilizes a network switch in order to send data to each coprocessor. Remeber, each camera needs both data and power in order to operate correctly.
  - [ ] Use the following configuration when wiring the network switch, coprocessor, and camera.
<img width="682" height="501" alt="Screenshot 2025-07-31 at 1 52 38 PM" src="https://github.com/user-attachments/assets/65ba1fc3-75b9-4415-9738-2c3dbec19750" />

- [ ] Coprocessor Setup
  - [ ] Dowload the corresponding image for your coprocessor from the [Github page](https://github.com/PhotonVision/photonvision/releases/tag/v2025.3.2)
  - [ ] Use [BalenaEtcher](https://etcher.balena.io/) to transfer the Photonvision image to an micro-SD card. (The SD card must be plugged into your computer.)
  - [ ] Sometimes the micro-SD card is corrupted and cannot be transferred files using BalenaEtcher. In this instance, use a different micro-SD card.
- [ ] Photonvision Pipeline
  - [ ]  If you have no existing camera with Photonvision Pipeline settings you wish to copy, follow instructions from the [PhotonVision Docs](https://docs.photonvision.org/en/v2025.3.2/docs/quick-start/networking.html).
  - [ ]  If you wish to copy the settings of an existing camera, use the following steps:
      NOTICE: Step order is incredibly important!
    - [ ]  Navigate to '10.TE.AM.XX' (where TE.AM is the team number and XX is the camera number.) Of the camera you wish to copy settings from.
    - [ ]  Press the export all settings button of the camera you want to copy from in PhotonVision.
    - [ ]  Unplug all wires going from the network switch to the coprocessor except for the coprocessor you want to configure, as having multiple coprocessors with the same IP address will confuse PhotonVision Pipeline.
    - [ ]  Assuming that the camera you want to configure is brand new, navigate to 'photonvision.local:5800'. Otherwise, navigate to 10.TE.AM.XX for the camera you wish to configure.
    - [ ]  Press the import all settings button in PhotonVision tab for the coprocessor you want to configure.
    - [ ]  Rename the camera to the corresponding direction it faces, reset the ip address of the coprocessor, and reset the name of the coprocessor.
    - [ ]  Rewire the coprocessors that were previously unplugged.
    - [ ]  Set the static IP in the networking tab of Photonvision to 10.TE.AM.11 (for team #5804: 10.58.04.11)
    - [ ]  Set the static IP for the RoboRIO to the default static IP.
    - [ ]  Power cycle the robot.
    - [ ]  Access the camera configuration settings at 10.TE.AM.11:5800 (for team #5804: 10.58.04.11:5800)
    - [ ]  Read the PhotonVision docs if more thourough documentation is needed.

## 🔗 Additional References
[PhotonVision Docs](https://docs.photonvision.org/en/v2025.3.2/index.html)
[Image download](https://github.com/PhotonVision/photonvision/releases/tag/v2025.3.2)
[BalenaEtcher](https://etcher.balena.io/)

## 📓 Notes
- Reach out in the #programming channel on the 5804 Discord if you have any questions or need assistance!

## 🎈 Size
2
