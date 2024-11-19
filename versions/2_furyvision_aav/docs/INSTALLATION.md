# FuryVision AAV Drone Installation Guide

![FuryVision AAV AI](/versions/2_furyvision_aav/media/fury-drone-cover.png "FuryVision AAV AI")

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
- **Holybro Tekko 4 in 1 ESC**
- **14.8V, 2200mAh LiPo battery**
- **Raspberry Pi 4 (optional)**
- **Propellers (5.0*5.5)**

You will also need:

- A computer with **Mission Planner** installed.
- **Screwdrivers**, **allen key set**, and **soldering equipment** (if required for motor/ESC wiring).

---

## 2. Hardware Assembly

For the complete step-by-step assembly process, including frame construction, motor and propeller installation, and camera mounting, please refer to the [**Assembly Guide (PDF)**](/versions/2_furyvision_aav/docs/Assembly%20of%20FuryVision%20AAV.pdf) located in the `docs/` folder of this repository.

---

## 3. Firmware Installation

### 3.1 Installing ArduCopter Firmware

1. Connect your **Pixhawk Orange Cube+** flight controller to your computer using a USB cable.
2. Open **Mission Planner** and navigate to the **Install Firmware** section.
3. Choose **ArduCopter** as the firmware and install **version 4.5.6 (7ce11b41)** or latest.
4. Wait for the installation to complete, and then reboot the Pixhawk.

**Referance for Installing ArduCopter Firmware: [Link](https://ardupilot.org/copter/docs/common-loading-firmware-onto-pixhawk.html)**

### 3.2 Uploading Tuned Parameters

1. After the firmware is successfully installed, go to the **Configuration** tab in Mission Planner.
2. Select **Full Parameter List** and upload the pre-tuned parameter file from the `/firmware` folder (`fury_drone1.param`).
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

### 4.3  Radio Channel Mapping and Calibration

#### Radio Channel Mapping:

1. Power on the FlySky FS-i6 transmitter and enter the setup menu.
2. Navigate to Functions Setup > Aux Channels and map the channels as follows:
   - **Throttle:** Channel 3 (Joystick A)
   - **Pitch:** Channel 2 (Joystick B)
   - **Roll:** Channel 1 (Joystick B)
   - **Yaw:** Channel 4 (Joystick A)

     **Flight Modes:**

     - Stabilize: Channel 5 (SWC1)
     - Loiter: Channel 5 (SWC2)
     - AltHold: Channel 5 (SWC3)
   - **Arm/Disarm**: Channel 6 (SWA)

#### Binding the X6B Receiver:

1. Connect the **X6B receiver** to the Pixhawk via the i-BUS port.
2. Bind the **X6B receiver** to the transmitter following the FlySky binding procedure.

#### Radio Calibration in Mission Planner:

1. In Mission Planner, navigate to **Initial Setup > Radio Calibration.**
2. Follow the instructions to calibrate **Throttle, Pitch, Roll, Yaw**, and test the flight modes

   **Referance for Radio Calibration: [Link](https://ardupilot.org/planner/docs/common-radio-control-calibration.html)**

### 4.4 Changing Motor Outputs to A1, A2, A3, A4

To change motor outputs from `M1, M2, M3, M4 to A1, A2, A3, A4`:

1. In Mission Planner, go to the **Full Parameter Tree/list**.
2. Locate the motor output parameters (`SERVO1_FUNCTION`, `SERVO2_FUNCTION`, etc.).
3. Update the SERVOX_FUNCTION values:
   - **A1:** `SERVO1_FUNCTION = 33`
   - **A2:** `SERVO2_FUNCTION = 34`
   - **A3:** `SERVO3_FUNCTION = 35`
   - **A4:** `SERVO4_FUNCTION = 36`
4. Save the parameters and reboot the Pixhawk.

### **Or else, this can done easily using Mission Planner’s `Servo Output` page**

- In Mission Planner, go to the **Initial Setup > Mandatory Hardware > Servo Output**.

![DShot setup](/versions/2_furyvision_aav/media/dshot-setup.png "DShot setup in MissionPlanner")

### 4.5 ESC Calibration using DShot

The **Holybro Tekko 4in1 ESC** supports **DShot** for digital motor control. Manual ESC calibration may not be necessary, but follow these steps to ensure correct setup:

1. In **Mission Planner**, go to **Initial Setup > Mandatory Hardware > ESC Calibration.**
2. Set **DShot** as the **ESC Protocol** under the **Motor Test** tab.
3. Ensure the motors are connected to **A1, A2, A3, A4** (instead of M1, M2, M3, M4).
4. Select the `DShot` appropriate `baud rate`.
5. Reboot the Pixhawk and test motor spin using the **Motor Test** function in Mission Planner.
6. Adjust **DShot settings** in **Mission Planner** as needed to fine-tune performance.

**Referance for Dshot ESC setup: [Link](https://ardupilot.org/copter/docs/common-dshot-escs.html)**

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

- [BOM for FuryVision AAV](/versions/2_furyvision_aav/hardware/BOM_furyvision_aav.pdf)

The BOM details all components used in the drone, including motors, sensors, flight controllers, and other hardware components.

---

## 7. Troubleshooting

If you encounter any issues during installation or calibration, consider the following:

- Ensure all firmware and parameter files are uploaded correctly.
- Double-check hardware connections (ESC, motors, GPS, etc.).
- Re-run calibration steps if the drone shows instability or drift during flight.
- Consult the [**TROUBLESHOOTING.md**](/versions/2_furyvision_aav/docs/TROUBLESHOOTING.md) file for additional guidance on common problems.

For more assistance, visit the project’s GitHub Issues page or contact the development team.

---

This guide focuses on the **firmware installation**, **Mission Planner configuration**, and **calibration** steps while referring users to the **detailed assembly PDF** for hardware instructions.
