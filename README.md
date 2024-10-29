
# **Fury Drone Project**

![FuryVision AAV](/images/cover.jpg "FuryVision AAV")

Welcome to the **Fury Drone Project** repository! This project showcases the development of **Fury**, a high-performance, multi-mission **Autonomous Air Vehicle (AAV)** platform designed for various aerial missions, incorporating advanced sensors and components.

The repository contains everything you need to build, modify, and fly the **Fury Drone**, including design files, firmware, software, and documentation for multiple versions of the drone.

## **Overview**

The **Fury Drone** is engineered to push the boundaries of **unmanned aerial systems (UAS)** technology. It integrates components such as the **Pixhawk Orange Cube+ flight controller**, **Intel RealSense cameras**, **Emax brushless motors**, and **Here 3+ GPS module** for precise navigation and mission versatility.

This repository covers:
- **Original Fury Drone**: Developed as the core platform for high-performance UAS missions, the original version was designed by **SPIN Laboratory (ACES 307), Dept. of Electrical Engineering, IIT Kanpur**.
- **FuryVision AAV**: A modified version designed to accommodate **four Intel RealSense cameras** for enhanced visual and spatial sensing. This version was developed by the **Open Drone Team, CDOH Lab, ICFOSS, Thiruvananthapuram**, based on the requirements specified by IIT Kanpur.

---

## **Versions**

This repository contains two main versions of the Fury drone:

1. **Original Fury Drone**  
   - The foundational version of the Fury platform, designed for general high-performance UAS missions.
   - Developed by **SPIN Laboratory (ACES 307), Dept. of Electrical Engineering, IIT Kanpur**.
   - This version features basic flight capabilities using the **Pixhawk Orange Cube+** and standard UAS components.

2. **FuryVision AAV**  
   - An upgraded version of the Fury drone, modified to mount and integrate **four Intel RealSense cameras** for enhanced visual and spatial sensing.
   - Developed by the **Open Drone Team, CDOH Lab, ICFOSS, Thiruvananthapuram**, based on requirements specified by **IIT Kanpur**.
   - Includes advanced capabilities for visual sensing, spatial mapping, and autonomous navigation.

Each version has its own folder within the `versions/` directory, containing specific design files, firmware, and instructions.

---

## **Getting Started**

To get started with building and flying the **Fury Drone**, follow these steps:

### 1. **Clone the Repository**
   ```bash
   git clone https://github.com/sidharthmohannair/Fury-Drone-Project.git

   cd Furry-Drone-Project
   ```

### 2. **Choose a Version**
   Navigate to the version you're interested in:
   - For the original version: `versions/original_fury/`
   - For the modified version: `versions/furyvision_aav/`

### 3. **Follow the Setup Instructions**
   Refer to the detailed setup guides in the **`INSTALLATION.md`** and **`assembly_instructions.md`** files for each version.

### 4. **Upload Firmware**
   Upload the appropriate firmware for the version you’re working on. Check the **firmware/** directory for instructions.

---

## **Hardware Requirements**

The Fury drone is built using high-quality components to ensure robust performance. Some of the key hardware includes:

- **Flight Controller**: Pixhawk Orange Cube+
- **Motors**: Emax Brushless Motor, 2306-2400KV
- **GPS**: Here 3+ GPS Module
- **Cameras** (FuryVision AAV): Intel RealSense D435i
- **ESC**: Holybro Tekko 4in1 50A
- **Battery**: 14.8V, 2200mAh LiPo

A full Bill of Materials (BOM) is provided in the hardware directories for each version.

---

## **Testing and Logs**

Test data, including flight logs, motor thrust tests, and temperature data, can be found in the **`tests/`** directory. This folder includes logs from various performance evaluations and flight tests, which are critical for tuning and performance analysis.

---

## **Contributing**

We welcome contributions to the **Fury Drone Project**! If you'd like to contribute:
- Fork the repository.
- Create a new branch with your feature or fix.
- Submit a pull request for review.

Please read the **CONTRIBUTING.md** file for detailed guidelines.

---

## **License**

This project is licensed under the **MIT License** – see the **LICENSE.md** file for details.

---

## **Contact**

If you have any questions or need further assistance, feel free to reach out by opening an issue on GitHub.

---

### **Mission Statement**

The **Fury Drone Project** is more than just a platform—it's a symbol of innovation, collaboration, and the relentless pursuit of excellence in the field of unmanned aerial systems. Whether you're building, modifying, or flying Fury, we hope this project provides valuable insights and serves as a robust foundation for your journey in aerial autonomy.
