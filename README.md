# Autonomous Combat Sumo Robot | BattleLab Robotica

A high-performance autonomous robot designed for professional Sumo competitions. This project was a collaborative multidisciplinary effort, where I was involved in the full development cycle, from mechanical assembly and electronics to low-level C++ programming.

## Project Vision
The goal was to create a robust, fast, and intelligent robot capable of autonomous combat. In a team where "everyone did everything," I contributed to both the hardware design and the software architecture to ensure a perfectly synchronized machine.

## Technical Specifications & Components
To build the Sumo robot, we used a combination of high-torque mechanical parts and precise electronic sensors:

### Core Electronics
- **Microcontroller:** Arduino Nano (ATmega328P) - chosen for its small footprint and reliable processing.
- **Motor Driver:** TB6612FNG Dual H-Bridge - used for high-efficiency current handling for the DC motors.
- **Sensors (Opponent):** 2x Sharp IR Distance Sensors - for high-speed, long-range opponent detection (the "eyes").
- **Sensors (Line):** 2x TCRT5000 Infrared Reflectance sensors - mounted under the blade for millisecond edge detection.
- **Power:** 3S LiPo Battery - to provide the high discharge rates required for rapid acceleration.

### Mechanical Parts
- **Chassis:** Custom laser-cut acrylic frame designed for a low profile and high structural integrity.
- **Magnetic Downforce:** Neodymium N52 magnets - strategically placed for maximum adhesion to the metal ring (Dohyo).
- **Motors:** 2x High-torque DC Gear Motors (600 RPM) - balanced for both speed and pushing force.
- **Wheels:** High-friction silicone wheels for maximum grip on the metallic surface.
- **Offensive Blade:** Front-mounted steel blade designed to lift the opponent and neutralize their traction.

## Software Architecture
The robot runs on a real-time **State Machine** written in **C++/AVR**:
- **Search Mode:** Controlled rotation to scan the environment using the Sharp IR sensors.
- **Attack Mode:** Once an opponent is detected, the robot switches to a **PID-controlled** charge for maximum impact.
- **Safety Mode:** High-priority interrupts that trigger evasive maneuvers (reverse and spin) the moment the line sensors detect the white ring border.

## Team & Contribution
This project was developed in a team of 4 for the **BattleLab Robotica** competition.
- **Collaborative Effort:** We worked together on all stages: soldering components, calibrating sensors, and refining the combat strategy.
- **My Involvement:** I was involved in both the **hardware assembly** and the **autonomous logic implementation**, ensuring the software correctly interpreted sensor data to control the high-torque motors.

---
*Note: The original source code from the competition is archived. This documentation serves as a technical overview of the architecture and logic developed for the event.*
