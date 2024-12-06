# How to Upload/Upgrade Drone Firmware Using Mission Planner Software

**Mission Planner** is a free software tool widely used for drones and other autonomous vehicles. It helps you manage, program, and monitor missions, including updating your drone's firmware to ensure optimal performance. 

## Requirements
- A Windows PC with Mission Planner installed
- Assembled drone or its flight controller
- USB cable

>Note: Firmware updates via Mission Planner are only supported on Windows OS.

## Steps to upload/upgrade Firmware

### Preparation

- **Remove Propellers**: Always remove the drone's propellers before powering it up to ensure safety.

- **Check Power Source**: While updating firmware, the USB connection is usually sufficient. A battery is not mandatory unless specifically required for your flight controller. 

---

### Steps

 1. **Open Mission Planner** : Launch the Mission Planner software on your Windows PC.

	![Open Mission Planner](/Update%20drone%20firmware%20images/Img001.png)

 2. **Connect the Flight Controller** : Use a USB cable to connect the flight controller to your computer.
 	>Tip:  Ensure the USB cable is securely connected to avoid interruptions during the update.

 3. **Check COM Port**: 
 - In Mission Planner, locate the available **COM port**.
 - Select the correct port and configure the **baud rate** (usually set to **115200**).

	![Select port and baud rate](/Update%20drone%20firmware%20images/Img002.png)

 4. **Do Not Click Connect**: **Do not click** the **Connect** button in Mission Planner during this process.

	![Do not click Connect](/Update%20drone%20firmware%20images/Img02.png)

 5. **Navigate to Firmware Installation**: Go to **Setup** → **Install Firmware** → Choose the desired drone type (Quadcopter, Hexacopter, etc.).

	![Select Setup tool](/Update%20drone%20firmware%20images/Img003.png)

6. **Confirm Firmware Version**:
A popup will display the available firmware version. Click Yes to proceed.

	![Cofirm to Update firmware version](/Update%20drone%20firmware%20images/Img005.png)

7. **Select the Platform**: Use the dropdown menu to select the appropriate flight controller for your drone (e.g., Pixhawk, Cube Orange).

	![Select Flight controller](/Update%20drone%20firmware%20images/Img006.png)
	 
8. **Upload Firmware**:
- Click to upload the firmware.
- Follow the on-screen instructions carefully to avoid errors.

	![Click to upload firmware](/Update%20drone%20firmware%20images/Img007.png)
9. **Follow the Instruction**: Carefully read and follow any additional popup messages for specific instructions during the process.

	![Popup Message](/Update%20drone%20firmware%20images/Img008.png)

10. **Wait for Upload to Complete**:
Allow the upload process to finish without interruptions.

	![Processing](/Update%20drone%20firmware%20images/Img009.png)

11. **Completion**:

- Once the update is complete, Mission Planner will display an "Upload Done" message.
- The flight controller will emit a beep sound to confirm the update.

	![Upload Done](/Update%20drone%20firmware%20images/Img010.png)
	
12. **Reboot the Flight Controller**:
Reboot the flight controller to apply the firmware update.
	
---

### Post-Update Tips
- Check the firmware version on your flight controller to ensure it matches the one you uploaded.
- Perform a basic system check to confirm all sensors and components are functioning correctly.
- If required, recalibrate sensors (e.g., accelerometer, compass).	
---
## Your firmware update is now complete!

Enjoy improved performance and new features on your drone. For further assistance, refer to the Mission Planner documentation or support forums.
	 
	 
	
		 
	
	
