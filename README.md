# ESP8266 LED Interfacing with Wi-Fi via Blynk App 💡🔘

This project demonstrates interfacing LEDs with a push button using an ESP8266 (D1 R1) and controlling them through Wi-Fi using the Blynk app. The LEDs are connected to pins D2, D3, D6, and D10, while pin D1 is used to indicate connectivity with the cloud and network. A total of 5 LEDs are used in this project.

<br>

<img src="./image/output.gif" alt="Connection Diagram" width="830">

<br>

                                   _____________________
                                  |          |          |
                                  |    D2    |    D3    |
                                  |__________|__________|
                                  |          |          |
                                  |    D6    |    D10   |
                                  |__________|__________|            ____________
                                  |          |          |           |            |
                                  |    D1    |    GND   |---------- |  ESP8266   |
                                  |__________|__________|           |____________|

- D2, D3, D6, D10: Pins connected to LEDs.
- D1: Pin used to indicate connectivity.
- GND: Ground connection.
- ESP8266: Wemos ESP8266 Wi-Fi Board (D1 R1)

## Setup Steps 🛠️

Follow these steps to set up the circuit:

### 1. Circuit Connection

Connect the components as follows:

- Connect LEDs (3.3V Red, Green, Blue, Yellow LEDs) to pins D2, D3, D6, and D10 on the ESP8266 board.
- Connect pin D1 to indicate network and cloud connectivity.
- Connect the negative (shorter) lead of each LED to the ground (GND) on the breadboard to complete the circuit.

For detailed connections and pinouts, refer to the component directories in the `components` folder.

### 2. Components Required 🧰

You will need the following components:

- **Wemos ESP8266 Wi-Fi Board (D1 R1)**: Microcontroller board.
  - **Specifications**:
    - Microcontroller: ESP8266 (D1 R1)
    - Clock Speed: 80MHz (up to 160MHz)
    - USB Converter: CH340G
    - Operating Voltage: 3.3V
    - Flash Memory: 4MB
    - Digital I/O: 11
    - Analog Inputs: 1
    - Communications: I2C, Serial, SPI
    - WiFi: Built-in
- **LEDs**: For lighting effects.
  - **Specifications**:
    - Type: 3.3V LEDs (Red, Green, Blue, Yellow)
- **Male to Male Jumper Wires**: For connecting components.

## Connecting LEDs on Breadboard 🍞💡

To connect LEDs on a breadboard, follow these steps:

1. Insert the LEDs into the breadboard, ensuring the longer lead (positive) is on one side and the shorter lead (negative) is on the other side.
2. Connect the positive (longer) lead of each LED to a digital pin on the ESP8266 board (D2, D3, D6, D10).
3. Connect the negative (shorter) lead of each LED to the ground (GND) on the ESP8266 board.
   <br><br>

For detailed specifications and connection diagrams of LEDs, refer to the LED component directory in the `components` folder.

## Components 🧩

### Wemos ESP8266 Wi-Fi Board (D1 R1) 💡

This directory contains information about the ESP8266 microcontroller board.

#### Specifications

- Microcontroller: ESP8266 (D1 R1)
- Clock Speed: 80MHz (up to 160MHz)
- USB Converter: CH340G
- Operating Voltage: 3.3V
- Flash Memory: 4MB
- Digital I/O: 11
- Analog Inputs: 1
- Communications: I2C, Serial, SPI
- WiFi: Built-in

For more details, refer to [Wemos ESP8266 Wi-Fi Board (D1 R1) Details](components/ESP8266)

### LED 💡

This directory contains information about the LEDs used in the project.

#### Specifications

- Type: 3.3V LEDs (Red, Green, Blue, Yellow)

For more details, refer to [LED Details](components/LED)

### Male to Male Jumper Wires 🚀

This directory contains information about the male to male jumper wires used in the project.

For more details, refer to [Jump Wires Details](components/JUMP_WIRE)

### Breadboard 🍞

This directory contains information about the breadboard used in the project.

#### Specifications

- Type: Full-size Breadboard
- Total Holes: 830
- Spacing: 2.54mm (0.1")
- Dimension: 16.5x5.5cm
- Common Rating: 1A @ 5V or 5 Watt

For more details, refer to [Breadboard Details](components/BREAD_BOARD)

## Arduino Software and Blynk App 📱

### Arduino Software

Before uploading the code to the ESP8266 board, make sure you have the Arduino software installed. You can download it from the [Arduino website](https://www.arduino.cc/en/software).

# Blynk App Setup 📱

Blynk is a platform that allows you to build IoT applications easily. Follow these steps to set up Blynk with your ESP8266 project:

## Web Interface Setup

1. Go to the [Blynk website](https://blynk.io/) and sign up for an account.
2. Once logged in, create a new project and select the ESP8266 board.
3. Configure the project settings and choose the appropriate connection type (Wi-Fi).
4. Add widgets to the project dashboard to control the LEDs and monitor connectivity.

## Variable Setup

1. Create virtual pins in your Blynk project to communicate with the ESP8266.
2. Assign each LED and connectivity indicator to a specific virtual pin.

## Arduino Code Configuration

1. Open the Arduino code file [`LED_Button_Interfacing.ino`](code/LED_Button_Interfacing/LED_Button_Interfacing.ino) from this repository.
2. Include the Blynk library and configure the Wi-Fi credentials.
3. Initialize Blynk with your authentication token and connect to the Blynk server.
4. Map the virtual pins to the corresponding LEDs and connectivity indicators.
5. Implement functions to handle LED control and monitor connectivity status.

## Mobile App Configuration

1. Download and install the Blynk app from the [App Store](https://apps.apple.com/us/app/blynk-control-arduino-raspberry/id808760481) or [Google Play](https://play.google.com/store/apps/details?id=cc.blynk).
2. Log in to the Blynk app using your account credentials.
3. Open the project created earlier in the web interface.
4. Configure the app interface by adding buttons, sliders, or other widgets to control the LEDs.
5. Create widgets to display the connectivity status of the ESP8266.

## Template Setup

1. Create templates on the Blynk web interface for the project dashboard.
2. Customize the templates with the desired layout and functionality.
3. Save the templates and ensure they are synchronized with the mobile app.

## Running the Project

1. Connect your mobile device to the same Wi-Fi network as the ESP8266.
2. Open the Blynk app and navigate to the project dashboard.
3. Use the widgets to control the LEDs and monitor connectivity.
4. Test different scenarios and functionalities to ensure proper operation.

## Screenshots 📸

<div>
  <img src="./image/output.png" alt="Output" width="830">
</div>

<br><br>

<div style="margin-top: 20px; border: 2px solid white; padding: 10px;">
  <img src="./image/image1.png" alt="Mobile Screenshot 1" width="400" style="float: left; margin-right: 20px;">
  <img src="./image/image2.png" alt="Mobile Screenshot 2" width="400" style="float: right; margin-left: 20px;">
</div>

<br><br>

<div style="margin-top: 20px; border: 2px solid white; padding: 10px;">
  <img src="./image/image4.png" alt="Mobile Screenshot 3" width="400" style="float: left; margin-right: 20px;">
  <img src="./image/image3.png" alt="Mobile Screenshot 4" width="400" style="float: right; margin-left: 20px;">
</div>

<br><br>

<div style="margin-top: 20px; border: 2px solid white; padding: 10px;">
  <img src="./image/image5.png" alt="Mobile Screenshot 5" width="400" style="float: left; margin-right: 20px;">
  <img src="./image/image6.png" alt="Mobile Screenshot 6" width="400" style="float: right; margin-left: 20px;">
</div>

## License 📝

This project is licensed under the [MIT License](LICENSE.md). Feel free to use, modify, and distribute this project for educational purposes.

_Disclaimer: This project is intended for educational purposes only and should not be used in production environments without proper testing and validation._
