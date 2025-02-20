# Com_led_Flutter_MQTT_esp32

This project demonstrates how to control LEDs connected to an ESP32 using MQTT protocol. The ESP32 connects to a WiFi network and subscribes to an MQTT topic to receive messages that control the LEDs. Additionally, a Flutter application is used to send MQTT messages to control the LEDs.

## Hardware Requirements

- ESP32 development board
- Two LEDs
- Two resistors (appropriate value for your LEDs)
- Breadboard and jumper wires

## Software Requirements

- Arduino IDE
- PubSubClient library for MQTT
- WiFi library
- Flutter SDK

## Circuit Diagram

Connect the LEDs to the ESP32 as follows:

- LED 1: Connect the anode to GPIO 2 and the cathode to GND through a resistor.
- LED 2: Connect the anode to GPIO 4 and the cathode to GND through a resistor.

## Code Explanation

### ESP32 Code

The code initializes the WiFi connection and sets up the MQTT client. It subscribes to the `led_topic` topic and controls the LEDs based on the received messages.

#### Libraries

```cpp
#include <WiFi.h>
#include <PubSubClient.h>