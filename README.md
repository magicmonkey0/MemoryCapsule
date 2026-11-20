# Memory Capsule 📝 ❤️ 🔋 ⚡
### A portable, offline-first electronic keepsake built with ESP32

**Memory Capsule** is an independently designed electronics project inspired by the idea that meaningful moments deserve to be preserved.

Life moves quickly, and between school, work, and everyday responsibilities, it's easy to overlook the little moments that make life special. I wanted to create something physical that could preserve these memories in a more personal and tangible way.

The result is a compact, battery-powered electronic keepsake that allows the user to record and revisit memories through an OLED display and physical buttons, with data stored locally on a microSD card.

This project was independently conceptualized, assembled, and developed over approximately two months: September to November 2026.

---

## Project Overview

Memory Capsule is an embedded system built around an ESP32 development board. It provides a simple interface for browsing stored memories without relying on an internet connection or external application.

Each memory consists of three pieces of information:
- **Date:** When the memory occurred.
- **Activity type:** A short category describing the activity.
- **Note:** A brief description accompanying the memory.

Memories are stored in a text file on a microSD card and retrieved by the device when needed.

## Features

- **OLED interface:** Display and browse saved memories through a 0.96-inch OLED screen.
- **Physical navigation:** Button-based interaction with the device.
- **Local data storage:** Persistent memory storage using a 4GB microSD card.
- **Structured memory records:** Each entry contains a date, activity type, and accompanying note.
- **Offline functionality:** Access stored memories without an internet connection.
- **Portable operation:** Battery-powered design with a 5V boost conversion stage.
- **Compact enclosure:** Housed in a small metal tin.

**Some other features**

- Keyboard for typing using the buttons for navigation (for custom typing activity type and making notes)
- Each saved memory is editable and deletable
- The memory used from the SD card and battery voltage is read and displayed in the settings screen
- On initial startup, a random memory is selected and displayed! (Just for fun!!)
- The case is decorated but is not shown for privacy

## Hardware & Components

| Component | Purpose |
|---|---|
| ESP32 development board | Main microcontroller |
| 0.96-inch OLED display | User interface |
| MicroSD card reader module | External storage interface |
| 4GB microSD card | Persistent data storage |
| Push buttons | User input and navigation |
| Slide switch | Power control |
| MT3608 boost converter | Boosts the 3× AA battery supply to 5V, which powers the ESP32 development board |
| 3× AA batteries and holder | Power source |
| Resistors | Voltage divider and supporting circuitry |
| Prototype board | Circuit assembly |
| Metal tin | Enclosure |

Additional materials included solder, hookup wires, and supporting components.

## Software & Implementation

The firmware was developed in C++ for the ESP32.

A key part of the implementation was developing a system to organize, store, and retrieve memory entries from the microSD card.

Software concepts and techniques applied include:

- **File handling:** Reading and managing memory records stored in a text file.
- **Structures (`struct`):** Organizing memory information into structured records.
- **Enumerations (`enum`):** Representing predefined activity types and states.
- **Data management:** Parsing and retrieving individual memory entries.
- **Embedded interface development:** Managing button inputs, navigation, and OLED display updates.
- **Hardware interfacing:** Integrating the ESP32 with the display and microSD card module.

This project provided an opportunity to apply C++ concepts learned through my coursework to a practical embedded systems application.

## Development Process & Challenges

Building the Memory Capsule involved several iterations and design decisions, particularly during hardware assembly and power integration.

### 1. Hardware Assembly & Prototyping

The circuit was first prototyped, of course, using a breadboard! After testing its functionality, I assembled it using a prototype board, requiring careful component placement, soldering, and wire management.

Having previously encountered soldering difficulties and accidental shorts in an earlier electronics project, I approached this build with greater attention to circuit connections and assembly.

Although the final wiring could still be improved, this project helped me develop more confidence and precision when working with physical electronics.

### 2. Power Supply Selection

The original design intended to use a rechargeable Li-ion battery. However, difficulties with the battery setup led me to reconsider the power architecture.

I ultimately switched to three AA batteries and an MT3608 boost converter configured for a 5V output. 
The boost converter supplies 5V to the ESP32 development board through its 5V input, allowing the board's onboard voltage regulation to provide the required 
operating voltage for the microcontroller and connected peripherals.

### 3. SD Card Integration & Data Management

Integrating the microSD card was one of the most interesting parts of the project.

Rather than relying on temporary data stored in memory, I implemented text-file-based storage to preserve memory entries between uses.

This involved applying C++ concepts such as structures, enumerations, and file handling to organize and retrieve individual records.

## Future Improvements

While the current prototype achieves its intended functionality, there are several areas I would like to explore in future iterations.

**Hardware**
- Design a custom PCB to replace the prototype board, reduce wiring complexity, and improve compactness.
- Integrate a rechargeable Li-ion battery with appropriate charging and protection circuitry.
- Design a purpose-built enclosure using 3D printing.

**Software & Functionality**
- Improve memory navigation and organization.
- Expand the amount of information that can be displayed for each entry.
- Develop an optional web or mobile companion application.
- Allow users to attach photographs and longer descriptions to individual memories through a digital interface.

## Demonstration

https://github.com/user-attachments/assets/8749b3e8-0e8b-4ec1-8f62-4512d21c8f5d

- video was sped up and compressed so I could upload to this markdown file!

**Project photographs:**

<img height="500" alt="IMG_0519" src="https://github.com/user-attachments/assets/7e42fc88-5d3a-453a-aa14-40554984348b" />
<img height="500" alt="IMG_0521" src="https://github.com/user-attachments/assets/e34e96b8-157f-462c-b97b-0ba0b628988f" />

* the back wiring:
<img height="400" alt="IMG_0516" src="https://github.com/user-attachments/assets/1d790e91-c544-415a-b946-4061d76ea27c" />


## Block Diagram

<mark>COMING SOON</mark>

## What I Learned

This project gave me the opportunity to take an original idea from concept to a working physical product.

Throughout development, I gained practical experience in:
- Embedded C++ programming and data management.
- Microcontroller and peripheral integration.
- Hardware prototyping and soldering.
- DC-DC voltage conversion and battery-powered systems.
- Debugging hardware and software interactions.
- Making design trade-offs under component and space constraints.

Most importantly, this project strengthened my interest in embedded systems and electronics design, 
and gave me the confidence to independently develop a product that combines hardware, software, and personal design goals.

<mark><strong>This project was designed and built independently with curiosity, experimentation, and a lot of sentimentality <3.</strong></mark>
