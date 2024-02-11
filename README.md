## Project Name Symbolism

KanPi combines "Kanshi" (monitoring or oversight in Japanese) with "Pi" from Raspberry Pi, reflecting the project's focus on automotive monitoring through innovative technology. It aims to provide car enthusiasts and DIYers with a powerful tool for enhancing their vehicle's performance and health monitoring capabilities.

## Project Goals

- [ ] Develop a real-time vehicle performance monitoring system.
- [ ] Provide diagnostics and fault code reading capabilities using the ELM327 chip for simplified communication with the vehicle’s OBD-II system.
- [ ] Offer a customizable display for vehicle metrics.
- [ ] Enable data logging for in-depth performance analysis.

## Research and Planning

- [X] OBD2 Protocol: Understanding the standardized system used by cars for self-diagnostics and reporting.
- [X] CAN Bus System: Learning how the Controller Area Network (CAN) bus allows microcontrollers and devices to communicate with each other without a host computer.
- [X] UART: Investigating how UART is used in automotive environments for diagnostics, module communication, and serial data transmission.
- [ ] Hardware Requirements: Raspberry Pi Pico, SparkFun OBD-II UART board with ELM327, CAN bus interface, display screen (OLED/TFT LCD), connectors, and necessary cabling.
- [ ] Software Requirements: Developing the software in Python or C++, using libraries for CAN bus communication, interfacing with the ELM327 chip via UART, and designing the UI for the display.

## GitHub Repository Structure

- `/src`: Source code files.
- `/docs`: Documentation, including setup instructions and usage guides.
- `/hardware`: Schematics and hardware design files, including integration details for the SparkFun OBD-II UART board.
- `README.md`: Project overview, setup instructions, and contribution guidelines.

## Core Components

### Raspberry Pi Pico
The central microcontroller unit for the project, featuring an RP2040 chip.

### Communication Interfaces

- **SparkFun OBD-II UART Board (ELM327)**: For accessing the vehicle's OBD-II system via UART, simplifying the process of reading diagnostic information.
- **CAN Bus Module**: A module like the MCP2515 CAN Bus Module with an SPI interface, compatible with the Raspberry Pi Pico, for accessing the vehicle's CAN network directly.

### Display Options

- **OLED Display**: For showing diagnostics and performance metrics. A small OLED screen with I2C or SPI interface can be easily integrated with the Pico.
- **TFT LCD Display**: A larger color display option for more detailed graphics or complex interfaces, also with SPI or I2C connectivity.

### Additional Components

- **MicroSD Card Module**: To log data for later analysis. Ensure it's compatible with the Pico for SPI communication.
- **Power Supply**: A stable 5V power supply or battery pack with a micro USB connector to power the Raspberry Pi Pico and potentially the display, depending on its power requirements.
- **Breadboard and Jumper Wires**: For prototyping the connections between the Pico, CAN bus module, SparkFun OBD-II UART board, displays, and any other components.
- **Custom PCB (Optional)**: For a more permanent setup after prototyping, designing a custom PCB that integrates all these components can be beneficial.