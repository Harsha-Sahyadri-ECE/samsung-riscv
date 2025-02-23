# Implementation of LED Blinking using VSD Board for Embedded System Development

## Project Overview
This project demonstrates a simple LED blinking system using a **VSD (VLSI System Design) board**. The VSD board, an FPGA-based development platform, is programmed to control an LED, making it blink at a defined interval. This project provides foundational knowledge in **microcontroller/FPGA programming, digital logic implementation, and hardware interfacing**, making it an ideal starting point for embedded system development.  

## Applications
- **Embedded System Learning** – Helps beginners understand microcontroller/FPGA programming.  
- **Status Indicators** – Used in electronic devices to signal operation status.  
- **Debugging & Testing** – Useful for testing GPIO functionality in hardware circuits.  
- **IoT and Automation** – Forms the basis for controlling appliances using microcontrollers.  

## Components Required  

| **Component**          | **Specification** | **Quantity** |
|------------------------|------------------|--------------|
| VSD Board             | FPGA-based Development Board | 1 |
| LED                   | 5mm, Red/Green/Blue | 1 |
| Resistor              | 330Ω | 1 |
| Connecting Wires      | Jumper Wires | As required |
| Power Supply          | 5V (USB or External) | 1 |

## Circuit Connections  

| **VSD Board Pin** | **Component** | **Connection Details** |
|------------------|-------------|--------------------|
| GPIO Pin (e.g., GPIO1) | LED Anode (+) | Connected directly |
| GND Pin          | LED Cathode (-) | Connected via 330Ω Resistor |

## Working Mechanism
1. **Powering the Board:** The VSD board is connected to a **5V power supply** (via USB or external adapter).  
2. **GPIO Control:** A **GPIO pin** of the VSD board is configured as an **output** to control the LED.  
3. **Blinking Logic:** A delay-based logic is implemented in the program, where:  
   - The LED turns **ON** for a specific duration.  
   - The LED turns **OFF** for the same duration.  
   - This process repeats continuously, creating a **blinking effect**.  
4. **Code Execution:** The program is written in **Verilog/VHDL or embedded C**, compiled, and uploaded to the VSD board.  

## Conclusion
This project successfully demonstrates **LED blinking using a VSD board**, providing a fundamental understanding of **GPIO control, digital logic design, and embedded programming**. It serves as a stepping stone for more complex applications in **automation, signal processing, and FPGA-based system development**.
