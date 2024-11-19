
# **FuryVision AAV - Version 2**

![FuryVision AAV](/versions/2_furyvision_aav/media/cover-furyVision.jpg "FuryVision AAV")

## **Overview**
The **FuryVision AAV** is an advanced, multi-mission Autonomous Air Vehicle (AAV) designed for enhanced visual sensing and autonomous navigation. Built upon a custom carbon fiber frame, it integrates cutting-edge technologies such as **Intel RealSense cameras**, a **Pixhawk Orange Cube+ flight controller**, and a **Here 3+ GPS module**, making it ideal for missions requiring precise spatial mapping and navigation.

---

## **Core Specifications**

| **Component**            | **Details**                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Frame**                 | Custom-designed carbon fiber frame, with 3D-printable parts included        |
| **Motors**                | Emax Brushless Motor, 2306-2400KV                                           |
| **Propellers**            | Tri Blade, 5.0*5.5                                                         |
| **Flight Controller**     | Pixhawk Orange Cube+                                                       |
| **Radio Receiver**        | X6B 2.4G 6CH i-BUS PPM PWM Receiver                                        |
| **Battery**               | 14.8V, 2200mAh LiPo                                                        |
| **All-Up Weight**         | 1161g (frame, battery, 4 cameras)                                          |
| **Weight (Without Battery)** | 923g (frame and cameras only)                                           |
| **GPS/Compass (Optional)**| Here 3+ GPS module                                                         |
| **ESC**                   | Holybro Tekko 4in1 ESC (50A Continuous, 60A Burst, Supports 4-6S battery)  |
| **Companion Computer (Optional)** | Raspberry Pi 4, 8GB                                               |
| **Firmware**              | ArduCopter v4.5.6 (7ce11b41)                                               |
| **Flight Time**           | 8 minutes 40 seconds (all-up weight: 1161g, RTL voltage: 3.3V per cell)    |
| **Cell Voltage**          | Before: 16.15V, After: 13.5V                                               |
| **Flight Modes**          | Stabilize, Altitude Hold, Loiter                                           |
| **Remote Controller Mapping** | Throttle (Ch3), Pitch (Ch2), Roll (Ch1), Yaw (Ch4), Modes (Ch5), Arm/Disarm (Ch6) |
| **Motor Temperatures (Post-Flight)** | Max: 50.1°C, ESC Max: 53.5°C                                  |

---

## **Key Features**
- **Advanced Sensing**: Four Intel RealSense cameras for superior depth perception and obstacle detection.
- **Precision Navigation**: Here 3+ GPS and Pixhawk Orange Cube+ for accurate positional awareness.
- **Optimized Flight Performance**: Pre-configured firmware for stable operation across all flight modes.
- **Scalable Design**: Optional integration with a Raspberry Pi for advanced processing capabilities.

---

## **What’s Included**
- Custom frame and component designs ([STL](hardware/STL/) and [CAD](hardware/CAD/)).
- Pre-tuned parameters ([fury_drone1.param](firmware/fury_drone1.param)) for optimal performance.
- ROS integration support for RealSense cameras (coming soon).

---

## **Documentation**

- [Assembly Guide](/versions/2_furyvision_aav/docs/Assembly%20of%20FuryVision%20AAV.pdf)  
  Instructions for assembling the drone frame and components.

- [Installation Guide](docs/INSTALLATION.md)  
  Step-by-step guide for firmware installation, calibration, and setup.

- [Troubleshooting Guide](docs/TROUBLESHOOTING.md)  
  Solutions for common issues during assembly, configuration, and flight.

- [Performance Test Results](tests/performance_test_results.pdf)  
  `/tests` folder contains all test logs and performance metrics.

---

## **Basic Folder Structure**
```plaintext
furyvision_aav/
├── docs/
│   ├── README.md
│   ├── ASSEMBLY_GUIDE.md
│   ├── INSTALLATION.md
│   └── TROUBLESHOOTING.md
├── hardware/
├── firmware/
├── tests/
└── media/
```

---

## **Performance Highlights**
- **Flight Time**: 8 minutes 40 seconds with an all-up weight of 1161g.
- **Battery Performance**: Voltage dropped from 16.15V to 13.5V after flight.
- **Temperature**: Motors peaked at 50.1°C, ESC at 53.5°C after flight.

---

## **Next Steps**
1. Assemble the drone using the provided **Assembly Guide**.
2. Install the firmware and calibrate sensors with **Mission Planner** as described in the **Installation Guide**.
3. Refer to **Troubleshooting** for resolving any issues during setup or flight.

---

## **FuryVision AAV in Action**
![FuryVision AAV flying](media/furryVision_fly.gif "FuryVision AAV flying")

---

## **Contributing and Feedback**
- For issues or feature requests, please open an issue on our [GitHub Issues](https://github.com/sidharthmohannair/Fury-Drone-Project/issues) page.
- Contributions are welcome! Refer to [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## **License**
This project is licensed under the [MIT License](LICENSE.md). You’re free to use, modify, and distribute it under the terms of the license.
