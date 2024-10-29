
# FuryVision AAV Drone Installation Guide

This guide provides an overview of the setup process for the **FuryVision AAV (v2)** drone, focusing on firmware installation, configuration, and calibration using **Mission Planner**. For detailed instructions on hardware assembly, please refer to the **Assembly Guide PDF** provided in the repository.

---

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Hardware Assembly](#hardware-assembly)
3. [Firmware Installation](#firmware-installation)
   - [Installing ArduCopter Firmware](#installing-arducopter-firmware)
   - [Uploading Tuned Parameters](#uploading-tuned-parameters)
4. [Mission Planner Configuration and Calibration](#mission-planner-configuration-and-calibration)
   - [Accelerometer Calibration](#accelerometer-calibration)
   - [Compass Calibration](#compass-calibration)
   - [Radio Calibration](#radio-calibration)
5. [Testing](#testing)
   - [Motor Spinning Test](#motor-spinning-test)
   - [Flight Test](#flight-test)
6. [Bill of Materials (BOM)](#bill-of-materials-bom)
7. [Troubleshooting](#troubleshooting)

---

## 1. Prerequisites

Before proceeding, ensure you have the following:
- **Pixhawk Orange Cube+ flight controller**
- **Intel RealSense Cameras (if applicable)**
- **Here 3+ GPS module**
- **Emax brushless motors**
- **Holybro Tekko 4in1 ESC**
- **14.8V, 2200mAh LiPo battery**
- **Raspberry Pi 4 (optional)**
- **Propellers (5.0*5.5)**

You will also need:
- A computer with **Mission Planner** installed.
- **Screwdrivers** and **soldering equipment** (if required for motor/ESC wiring).

---

## 2. Hardware Assembly

For the complete step-by-step assembly process, including frame construction, motor and propeller installation, and camera mounting, please refer to the **Assembly Guide (PDF)** located in the `docs/` folder of this repository.

---

## 3. Firmware Installation

### 3.1 Installing ArduCopter Firmware
1. Connect your **Pixhawk Orange Cube+** flight controller to your computer using a USB cable.
2. Open **Mission Planner** and navigate to the **Install Firmware** section.
3. Choose **ArduCopter** as the firmware and install **version 4.5.6 (7ce11b41)**.
   - If required, you can find the firmware file in the `firmware/pixhawk_firmware/` folder.
4. Wait for the installation to complete, and then reboot the Pixhawk.

**Referance for Installing ArduCopter Firmware: [Link](https://ardupilot.org/copter/docs/common-loading-firmware-onto-pixhawk.html)**

### 3.2 Uploading Tuned Parameters
1. After the firmware is successfully installed, go to the **Configuration** tab in Mission Planner.
2. Select **Full Parameter List** and upload the pre-tuned parameter file from the `firmware/parameter/` folder (`fury_drone1.param`).
3. Verify that all parameters are loaded correctly and correspond to your specific setup.

---

## 4. Mission Planner Configuration and Calibration

To ensure optimal flight performance, you will need to calibrate various sensors and settings using **Mission Planner**.

### 4.1 Accelerometer Calibration
1. In Mission Planner, navigate to the **Initial Setup** tab.
2. Select **Accelerometer Calibration** and follow the on-screen instructions to calibrate the drone’s orientation and leveling.

   **Referance for Accelerometer Calibration: [Link](https://ardupilot.org/planner/docs/common-accelerometer-calibration.html)**

### 4.2 Compass Calibration
1. Go to **Initial Setup** > **Compass**.
2. Perform the compass calibration by rotating the drone in different orientations as prompted.
   - Make sure there is no significant magnetic interference during calibration.

   **Referance for Compass Calibration: [Link](https://ardupilot.org/planner/docs/common-compass-calibration-in-mission-planner.html)**

### 4.3 Radio Calibration
1. Bind your remote controller to the drone and ensure that it is properly connected.
2. In Mission Planner, navigate to **Initial Setup** > **Radio Calibration**.
3. Follow the on-screen instructions to calibrate the radio channels (Throttle, Pitch, Roll, Yaw).

   **Referance for Radio Calibration: [Link](https://ardupilot.org/planner/docs/common-radio-control-calibration.html)**

---

## 5. Testing

### 5.1 Motor Spinning Test
1. Use Mission Planner to perform a motor spinning test.
   - Go to **Optional Hardware** > **Motor Test** and ensure that all motors spin in the correct direction.
2. Verify that there are no unusual vibrations or noises during the test.

### 5.2 Flight Test
1. Conduct initial test flights in the following modes:
   - **Stabilize Mode**: Test the drone’s stability and control response.
   - **Altitude Hold Mode**: Verify altitude-hold functionality.
   - **Loiter Mode**: Test GPS-based position hold.
2. Monitor the drone’s performance and make any necessary adjustments based on flight logs.

---

## 6. Bill of Materials (BOM)

The complete **Bill of Materials (BOM)** for the FuryVision AAV can be found in the repository at the following location:

- [BOM for FuryVision AAV](https://github.com/sidharthmohannair/Fury-Drone-Project/blob/main/versions/2_furyvision_aav/BOM_furyvision_aav.pdf)

The BOM details all components used in the drone, including motors, sensors, flight controllers, and other hardware components.

---

## 7. Troubleshooting

If you encounter any issues during installation or calibration, consider the following:
- Ensure all firmware and parameter files are uploaded correctly.
- Double-check hardware connections (ESC, motors, GPS, etc.).
- Re-run calibration steps if the drone shows instability or drift during flight.
- Consult the **TROUBLESHOOTING.md** file for additional guidance on common problems.

For more assistance, visit the project’s GitHub Issues page or contact the development team.

---

This guide focuses on the **firmware installation**, **Mission Planner configuration**, and **calibration** steps while referring users to the **detailed assembly PDF** for hardware instructions.
