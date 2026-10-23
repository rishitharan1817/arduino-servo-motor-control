# Servo Motor Control System Using Arduino

## Project overview
This mini project demonstrates how to control a servo motor's angular position using an Arduino Uno. The servo moves gradually from 0° to 180° and then returns to 0°, repeating continuously.

## Components required
- Arduino Uno
- Servo motor (for example, SG90)
- Jumper wires
- USB cable compatible with the Arduino board
- Arduino IDE

## Wiring
Connect the servo motor to the Arduino as follows:

| Servo wire (typical SG90) | Arduino connection |
|---|---|
| Signal (usually orange/yellow) | Digital pin 9 |
| VCC (usually red) | 5V |
| GND (usually brown/black) | GND |

Wire colours can vary by servo model, so confirm the labels or datasheet for your motor. If the servo causes the Arduino to reset or behave erratically, disconnect power and ask your instructor to check whether a separate suitable 5V supply is needed. Connect the grounds together when using a separate supply.

## Arduino IDE setup
1. Open Arduino IDE.
2. Create a new sketch.
3. Copy the code from `servo_control.ino` into the sketch.
4. Save the sketch as `servo_control.ino`.
5. Select **Tools → Board → Arduino Uno** (or your actual board).
6. Select the correct port under **Tools → Port**.
7. Click **Upload**.

The Arduino IDE's Servo library is commonly included with the IDE. If the IDE reports that `Servo.h` is missing, install **Servo** from **Sketch → Include Library → Manage Libraries**.

## How it works
- `#include <Servo.h>` includes the Servo library.
- `Servo myServo;` creates a servo control object.
- `myServo.attach(9);` connects servo control to digital pin 9.
- `myServo.write(angle);` commands the servo to move to the requested angle.
- `delay(15);` gives the servo a short time between commands.
- The two `for` loops move the servo from 0° to 180° and back to 0°.

## Expected result
The servo should sweep smoothly between approximately 0° and 180° and repeat continuously. Actual movement range and speed can vary by servo model.

## Troubleshooting
- **Servo does not move:** Check the signal pin, 5V, GND, and selected board/port.
- **Arduino resets or the servo jitters:** The servo may draw more current than the Arduino USB supply can provide. Ask your instructor to check the power arrangement; do not exceed the board's power limits.
- **Upload fails:** Confirm the correct board and port, and close other programs using the serial port.

## Project title
Design and Implementation of a Servo Motor Control System Using Arduino
