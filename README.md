# PetFeeder

**Video Demo:** [Watch Here](https://youtu.be/PR3a7ENNi-8)

## Description
PetFeeder is a project designed to remotely feed pets, offering convenience and peace of mind for pet owners. This system was created with the specific goal of allowing me to feed my cat from anywhere, anytime. By combining simple hardware components and internet-based communication, the PetFeeder provides an easy-to-use solution for automated pet feeding.

### Components Used
The PetFeeder utilizes the following hardware components:
- **PVC Pipes**: Used to construct the physical feeding mechanism.
- **1 ESP32 Microcontroller**: The brain of the system, which connects to the internet and processes commands.
- **1 Servo Motor**: Operates the feeding mechanism to release food.

The ESP32 microcontroller was selected for its built-in Wi-Fi capabilities, making it ideal for IoT applications. The use of a servo motor ensures precise control over the feeding mechanism, while the PVC pipes provide a cost-effective and durable structure.

### Key Features
1. **Remote Feeding**: Instantly feed your pet with a simple command from your smartphone.
2. **Scheduled Feeding**: Set a specific feeding time using the scheduling feature.
3. **Telegram Integration**: Communicate with the PetFeeder through a custom Telegram bot.

These features ensure that your pet is fed on time, whether you're at work, traveling, or simply not near the feeding device.

## How It Works
The PetFeeder leverages the ESP32’s internet connectivity to communicate with a custom Telegram bot. The system works as follows:

1. **Telegram Bot Setup**:
   - A bot was created using the Telegram Bot API. This bot serves as the interface between the user and the ESP32.
   - Commands available:
     - **Feed**: Triggers the servo motor to release food instantly.
     - **ScheduleTime**: Allows the user to specify a feeding time using a 24-hour format.

2. **Internet Connection**:
   - The ESP32 connects to your home Wi-Fi network. To enable this, you must enter your Wi-Fi name (SSID) and password in the code before uploading it to the microcontroller.

3. **Bot Communication**:
   - The bot communicates with the ESP32 through the internet. To link your Telegram account to the system, you’ll need to provide your chat ID in the code. This ensures that only authorized users can control the device.

4. **Command Execution**:
   - When a command is sent via Telegram, the ESP32 processes it and performs the corresponding action. For example, the “Feed” command activates the servo motor to dispense food immediately, while the “ScheduleTime” command sets a timer for a future feeding event.

5. **Feedback and Status Updates**:
   - The bot provides real-time feedback, confirming when the device is connected, commands are received, and actions are executed.

## Setup Instructions
To set up the PetFeeder, follow these steps:

### 1. Hardware Assembly
- Assemble the feeding mechanism using PVC pipes and securely attach the servo motor.
- Connect the servo motor to the ESP32 microcontroller.

### 2. Software Configuration
- Download the required libraries for the ESP32 and Telegram communication. Ensure you have the Arduino IDE installed.
- Open the project code in the Arduino IDE and configure the following:
  - **Wi-Fi Credentials**: Replace placeholders with your Wi-Fi SSID and password.
  - **Telegram Chat ID**: Insert your Telegram chat ID to link the bot with your account.

### 3. Upload Code
- Connect the ESP32 to your computer using a USB cable.
- Upload the configured code to the ESP32.

### 4. Test the System
- Power on the ESP32 and verify that it connects to the internet.
- Open the Telegram bot and send a command (e.g., “Feed”) to test functionality.

## Use Case Example
Imagine you’re at work and realize it’s your pet’s feeding time. Open the Telegram bot on your phone, press the “Feed” command, and the PetFeeder will instantly dispense food. Alternatively, if you’re planning a late night out, use the “ScheduleTime” command to set a specific time for feeding, ensuring your pet is taken care of in your absence.

## Potential Improvements
While the current version of the PetFeeder is functional and efficient, there are several ways to enhance its capabilities:
- **Camera Integration**: Add a camera to monitor the pet while feeding.
- **Multiple Commands**: Introduce additional commands, such as portion control or checking food levels.
- **Mobile App**: Develop a dedicated mobile application for a more user-friendly interface.
- **Battery Backup**: Include a battery backup to ensure functionality during power outages.

## Limitations
- The system requires a stable internet connection to operate.
- Manual refilling of the food container is needed.
- Users must have basic knowledge of programming to configure the system initially.

## Conclusion
The PetFeeder is a practical and customizable solution for remote pet feeding. By combining IoT technology and simple hardware, this project addresses a common need for pet owners who wish to ensure their pets are cared for even when they are not at home. The integration with Telegram makes it accessible and easy to use, requiring no additional applications or complex setups.

By following the instructions provided, you can replicate this project and enjoy the benefits of automated pet feeding. Whether for convenience or necessity, the PetFeeder is a valuable tool for any pet owner.
