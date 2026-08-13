# Contributing Guidelines

Thank you for contributing to this Arduino project! Contributions, improvements, bug fixes, documentation, and new ideas are welcome.

These guidelines apply to Arduino, ESP32, ESP8266, and other embedded projects in this repository.

## 1. Before Contributing

Before making changes:

* Read the project's `README.md`.
* Check the existing code and project structure.
* Make sure your contribution does not break existing functionality.
* Check whether an issue already exists for the problem or feature you want to address.
* Test your changes on the appropriate hardware whenever possible.

## 2. Types of Contributions

You can contribute in several ways:

* Fix bugs and hardware-related issues.
* Improve existing Arduino/ESP32/ESP8266 code.
* Add new features.
* Improve Wi-Fi, Bluetooth, sensor, display, or motor-control functionality.
* Improve circuit diagrams and wiring documentation.
* Improve comments and documentation.
* Add examples or test sketches.
* Improve code efficiency and reliability.
* Report bugs or suggest new features.

## 3. Hardware Contributions

When contributing hardware-related changes, clearly document:

* Microcontroller/board used.
* Sensors and modules used.
* Motor drivers and actuators.
* Power supply requirements.
* Pin assignments.
* Communication protocols such as I2C, SPI, UART, Wi-Fi, or Bluetooth.
* Any required libraries.
* Important voltage and current requirements.

Avoid changing pin assignments without documenting the change.

**Important:** Never connect components that require a different voltage or current directly to a microcontroller without appropriate protection or interfacing.

## 4. Code Guidelines

Keep the code:

* Simple and readable.
* Properly indented.
* Clearly commented where necessary.
* Consistent with the existing project style.
* Organized into logical functions.
* Free from unnecessary delays and repeated code where possible.

Use meaningful variable and function names.

For example:

```cpp
// Good
const int LEFT_MOTOR_PIN = 25;

// Avoid
int x = 25;
```

Avoid adding unnecessary libraries or dependencies.

## 5. Pin Configuration

Keep hardware pin definitions in one clearly identifiable section whenever possible.

Example:

```cpp
// Motor pins
#define LEFT_MOTOR_IN1 25
#define LEFT_MOTOR_IN2 26

// Sensor pins
#define TRIG_PIN 5
#define ECHO_PIN 18
```

If you change a pin, update:

* The source code.
* The README.
* Wiring diagrams.
* Any relevant documentation.

## 6. Libraries and Dependencies

If your contribution requires a new library:

1. Mention the library in the README.
2. Specify the required version when version compatibility matters.
3. Explain what the library is used for.
4. Avoid unnecessary dependencies.

Do not include library files directly in the repository unless there is a specific reason to do so.

## 7. Testing

Before submitting a contribution, test the project as much as possible.

Check:

* Does the code compile?
* Does it upload successfully?
* Does the hardware behave correctly?
* Do existing features still work?
* Does Wi-Fi/Bluetooth connectivity work if applicable?
* Are sensors providing correct readings?
* Are motors and actuators behaving safely?
* Does the device recover correctly after restarting?

For hardware projects, test under realistic operating conditions whenever possible.

## 8. Safety

Hardware projects can involve batteries, motors, high currents, heat, and moving parts.

Contributors should:

* Check voltage and current requirements.
* Avoid short circuits.
* Use appropriate power supplies.
* Ensure motors and actuators cannot cause unexpected movement.
* Disconnect power before modifying wiring.
* Use proper protection for inductive loads and motors.
* Never assume a pin can safely drive a high-current device directly.

If a contribution introduces a potential hardware risk, clearly document it.

## 9. Commit Guidelines

Use clear and descriptive commit messages.

Good examples:

```text
Add ESP32 Wi-Fi control
Fix left motor direction
Update OLED display logic
Add ultrasonic sensor support
Fix motor driver pin configuration
Improve Wi-Fi connection handling
Update wiring documentation
```

Avoid vague messages such as:

```text
update
changes
fixed
test
new code
final
```

## 10. Pull Requests

Before submitting a pull request:

* Explain what you changed.
* Explain why the change was necessary.
* Mention the hardware used for testing.
* Mention any new libraries or dependencies.
* Include screenshots, serial-monitor output, or wiring diagrams when useful.
* Make sure the project still compiles.

A good pull request should make it easy for another contributor to understand and reproduce the change.

## 11. Bug Reports

When reporting a bug, include as much useful information as possible:

* Board name and version.
* Arduino IDE or development environment.
* Operating system.
* Library versions.
* Wiring information.
* Error messages.
* Serial Monitor output.
* Steps to reproduce the problem.
* Expected behavior.
* Actual behavior.

Example:

```text
Board: ESP32 DevKit V1
IDE: Arduino IDE 2.x
Problem: Left motor does not rotate
Expected: Both left motors rotate forward
Actual: Only the rear motor rotates
```

## 12. Feature Requests

For new features, explain:

* What the feature does.
* Why it would be useful.
* Which hardware is required.
* Whether additional libraries are required.
* Any possible compatibility issues.

## 13. Documentation

Keep documentation updated when making changes.

If your contribution changes:

* Pin assignments
* Hardware
* Installation steps
* Libraries
* Configuration
* Network setup
* Usage instructions

update the relevant documentation as well.

## 14. Keep Projects Beginner-Friendly

These projects are intended to be understandable and useful for learning.

Prefer clear and maintainable solutions over unnecessarily complicated implementations.

Explain complicated sections of code with comments when appropriate.

## 15. Respect Existing Work

Do not remove or significantly modify existing functionality without a good reason.

If a major change is required, discuss it before making the change.

Give proper credit when using:

* Open-source code.
* Libraries.
* Circuit designs.
* Tutorials.
* External resources.

Follow the licenses of third-party projects.

## 16. Final Checklist

Before submitting your contribution:

* [ ] Code compiles successfully.
* [ ] Code has been tested on the intended hardware.
* [ ] Existing functionality still works.
* [ ] Pin assignments are documented.
* [ ] New libraries are documented.
* [ ] README/documentation has been updated if necessary.
* [ ] No unnecessary files or dependencies were added.
* [ ] Commit messages are clear.
* [ ] Hardware safety has been considered.
* [ ] The contribution is clearly explained.

## 17. Questions and Suggestions

If you are unsure about a change, open an issue or discussion before making a major modification.

All constructive contributions are welcome.

**Happy building! 🤖🔧**
