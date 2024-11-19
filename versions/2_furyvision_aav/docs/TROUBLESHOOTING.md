
# **FuryVision AAV Drone - Troubleshooting Guide**

This guide addresses common issues encountered during assembly, firmware installation, calibration, and flight, and provides actionable solutions to resolve them.

---

## **Table of Contents**
1. [Firmware and Parameter Issues](#1-firmware-and-parameter-issues)
2. [Radio Calibration Issues](#2-radio-calibration-issues)
3. [ESC and Motor Issues](#3-esc-and-motor-issues)
4. [Sensor Calibration Issues](#4-sensor-calibration-issues)
5. [Flight Issues](#5-flight-issues)
6. [Camera and Sensor Integration Issues](#6-camera-and-sensor-integration-issues)
7. [General Hardware Issues](#7-general-hardware-issues)
8. [Additional Resources](#8-additional-resources)

---

## **1. Firmware and Parameter Issues**

### **1.1 Firmware Upload Fails**
- **Problem**: Mission Planner cannot detect the Pixhawk or fails to upload firmware.
  - **Solution**:
    1. Ensure the USB cable is securely connected to the Pixhawk and computer.
    2. Use a different USB port or cable if the issue persists.
    3. Reboot the Pixhawk and try again.
    4. Verify that the correct firmware type (ArduCopter) is selected.

### **1.2 Parameter Upload Fails**
- **Problem**: Tuned parameter file does not load or fails to apply changes.
  - **Solution**:
    1. Ensure the `.param` file is correct and complete.
    2. Reload the parameter file from the **Full Parameter List** in Mission Planner.
    3. Manually verify and adjust any missing parameters.

---

## **2. Radio Calibration Issues**

### **2.1 Transmitter Not Responding**
- **Problem**: The FlySky FS-i6 transmitter inputs are not recognized.
  - **Solution**:
    1. Verify that the transmitter and X6B receiver are properly bound.
    2. Check the connection between the X6B receiver and Pixhawk (i-BUS port).
    3. Power cycle the transmitter and receiver.

### **2.2 Incorrect Channel Mapping**
- **Problem**: Flight modes or controls do not behave as expected.
  - **Solution**:
    1. Confirm that the transmitter’s channel mapping matches the drone’s configuration:
       - Throttle: Channel 3
       - Pitch: Channel 2
       - Roll: Channel 1
       - Yaw: Channel 4
       - Flight Modes: Channel 5
    2. Recalibrate the radio in Mission Planner.

---

## **3. ESC and Motor Issues**

### **3.1 Motor Does Not Spin**
- **Problem**: One or more motors fail to spin during the motor test.
  - **Solution**:
    1. Check the ESC wiring for loose connections.
    2. Ensure the motor outputs (A1, A2, A3, A4) are correctly mapped in the **Full Parameter Tree**.
    3. Verify that the ESC protocol is set to **DShot**.

### **3.2 Incorrect Motor Direction**
- **Problem**: A motor spins in the wrong direction.
  - **Solution**:
    1. Reverse the motor wiring by swapping any two wires connected to the motor.
    2. Use Mission Planner’s **Motor Test** to confirm proper motor rotation.

---

## **4. Sensor Calibration Issues**

### **4.1 Accelerometer Calibration Fails**
- **Problem**: Calibration does not complete or the drone behaves erratically.
  - **Solution**:
    1. Ensure the drone is placed on a flat, stable surface during calibration.
    2. Reboot the Pixhawk and retry the calibration.

### **4.2 Compass Calibration Fails**
- **Problem**: Compass calibration shows interference or fails to complete.
  - **Solution**:
    1. Check for nearby magnetic interference during calibration.
    2. Move the GPS/compass module away from power wires and other electronics.
    3. Perform a **compass-motor calibration** to account for magnetic interference from motors.

---

## **5. Flight Issues**

### **5.1 Drone Drifts in Stabilize Mode**
- **Problem**: The drone does not maintain its position and drifts excessively.
  - **Solution**:
    1. Recalibrate the accelerometer and compass.
    2. Check for loose propellers or motors.

### **5.2 Drone Fails to Maintain Altitude**
- **Problem**: The drone oscillates or struggles to hold altitude.
  - **Solution**:
    1. Ensure the barometer is not exposed to direct airflow or light.
    2. Verify battery voltage; a low battery can affect performance.

### **5.3 GPS-Related Issues**
- **Problem**: Drone fails to hold position in Loiter mode.
  - **Solution**:
    1. Ensure the GPS has a strong lock (minimum 8 satellites).
    2. Reposition the GPS module for optimal signal reception.

---

## **6. Camera and Sensor Integration Issues**

### **6.1 Intel RealSense Camera Not Detected**
- **Problem**: RealSense cameras are not recognized by the onboard system.
  - **Solution**:
    1. Verify the USB connection to the onboard computer.
    2. Ensure the RealSense ROS package is installed and configured correctly.

### **6.2 Poor Camera Performance**
- **Problem**: Cameras experience frame drops or poor image quality.
  - **Solution**:
    1. Check that the onboard computer has sufficient processing power.
    2. Use a high-quality USB cable and verify connections.

---

## **7. General Hardware Issues**

### **7.1 Loose or Faulty Connections**
- **Problem**: Components (motors, GPS, cameras) are not responsive.
  - **Solution**:
    1. Inspect all wiring and connectors for secure connections.
    2. Check solder joints on ESCs and motors.

### **7.2 Frame Vibration Issues**
- **Problem**: Excessive vibrations affect flight stability.
  - **Solution**:
    1. Tighten all screws and mounts on the frame.
    2. Add vibration dampeners between the frame and the Pixhawk.

---

## **8. Additional Resources**

- Refer to the [Mission Planner Documentation](https://ardupilot.org/planner/) for advanced configurations.
- Consult the [ArduPilot Forums](https://discuss.ardupilot.org/) for community support.
- Visit the project’s GitHub Issues page for additional troubleshooting.

---

This guide addresses a range of issues you might encounter during the installation and operation of the **FuryVision AAV Drone**. Let me know if you'd like to expand or modify this further!
