Motion Detection System LCD and Buzzer

This project illustrates an integration of PIR Motion Sensor, 16x2 I2C LCD, and a Buzzer in an Arduino-based motion detection system.67 words
clear
The system shows the number of motion events detected on the LCD and gives an audio sound feedback in the form of buzzer sound when motion is detected. It logs the motion detection event and time stamp in 12-hour format to the Serial Monitor. Components Used:

PIR Motion Sensor: Detects motion and provides an output signal to the Arduino.
16x2 I2C LCD: Shows the motion count and system status.
Buzzer: Sounds when there is detection of motion.
Arduino: Controls the motion detection process and controls the buzzer and display output.
Wiring Setup:

PIR Motion Sensor:
VCC → 5V on Arduino
GND → GND on Arduino
OUT → Pin 2 digital de Arduino

16x2 I2C LCD
VCC to 5V on Arduino
GND to GND in Arduino
SDA to Analog Pin A4 of Arduino
SCL → Analog Pin A5 Arduino

Buzzer: VCC → Digital Pin 8 on Arduino GND → GND in Arduino
Code Overview:

The code starts the PIR sensor, LCD, and Buzzer.It increases the motion count, shows on the LCD, and beeps the buzzer when it senses motion. It also prints the motion count along with the time in 12-hour format to the Serial Monitor for reference. The debounce feature avoids false readings from multiple triggers from a single motion event.

The motionDetected variable monitors the output of the PIR sensor.
    The motionCount variable stores the number of motion detections.
    A brief debounce delay guarantees only genuine motion triggers are tallied.
    The formatTime function prepares the time to display in a 12-hour AM/PM format.
This basic yet useful system can be extended or tailored for other purposes like security systems, attendance tracking, or smart home applications.
