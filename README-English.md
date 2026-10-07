# STM32 MCU Development Notes

[中文](README.md) | [English](README-English.md)

This repository organizes learning materials for STM32 microcontroller development. It covers basic peripherals, communication protocols, memory, low-power operation, real-time functions, and embedded development workflows. The materials are based on the Basic, Advanced, and Extended PDF and DOCX documents in `docs/`.

## Materials

### Basic

- [001 STM32 MCU Basic PDF](docs/001_STM32单片机（基础篇）.pdf)
- [001 STM32 MCU Basic DOCX](docs/001_STM32单片机（基础篇）.docx)

### Advanced

- [002 STM32 MCU Advanced PDF](docs/002_STM32单片机（高级篇）.pdf)
- [002 STM32 MCU Advanced DOCX](docs/002_STM32单片机（高级篇）.docx)

### Extended

- [003 STM32 MCU Extended PDF](docs/003_STM32单片机（扩展篇）.pdf)
- [003 STM32 MCU Extended DOCX](docs/003_STM32单片机（扩展篇）.docx)

## Learning Roadmap

```text
STM32 fundamentals
    ├── ARM core, STM32 families, and development tools
    ├── Minimal system, development board, and project creation
    ├── GPIO, clocks, and HAL
    ├── Interrupts, USART, I2C, and timers
    ├── DMA, ADC, SPI, and external memory
    └── FSMC, LCD, and register mapping
            ↓
Advanced STM32 communication
    ├── CAN bus
    ├── W5500 Ethernet
    ├── ESP32-C3 Wi-Fi
    ├── ESP32-C3 Bluetooth LE
    └── LoRa nodes and gateways
            ↓
System-level STM32 features
    ├── Power management and low power
    ├── RTC and backup registers
    ├── Alarm wake-up and data retention
    ├── Independent and window watchdogs
    └── HAL project structure, build process, and program states
```

## Contents

## Basic: STM32 Peripherals and Development Workflow

### 1. MCU, Board, and Development Environment

- Learn the ARM core, STM32 families, application areas, and naming rules.
- Understand register-level development and HAL-based development.
- Use Keil MDK, STM32CubeMX, ST-LINK, and VSCode.
- Learn about development boards, core boards, expansion boards, and the STM32 minimal system.
- Create, configure, build, download, and debug the first STM32 project.

### 2. GPIO and Registers

- Understand GPIO input, output, alternate-function, and analog modes.
- Learn GPIO configuration and input/output data registers.
- Study `GPIOx_CRL`, `GPIOx_CRH`, `GPIOx_IDR`, `GPIOx_ODR`, `GPIOx_BSRR`, `GPIOx_BRR`, and `GPIOx_LCKR`.
- Implement a running-light example with direct register access.
- Improve the embedded development workflow with Keil and VSCode.

### 3. System Architecture and Clocks

- Understand the overall STM32 architecture.
- Learn the clock tree and the role of different system clocks.
- Build the clock foundation required for peripheral initialization and timing.

### 4. HAL Development

- Understand the purpose and development model of the HAL library.
- Install the Java runtime, STM32CubeMX, and device support packages.
- Generate a HAL project with STM32CubeMX.
- Implement an LED running-light example and understand generated code and user-code organization.

### 5. Interrupts

- Understand interrupt concepts, purposes, and handling flow.
- Learn the STM32 interrupt architecture, NVIC, and external interrupt controller.
- Compare register-level and HAL-based interrupt configuration.
- Use a button-detection example to understand GPIO external interrupts.

### 6. USART Communication

- Distinguish parallel and serial communication, simplex, half-duplex, full-duplex, synchronous, and asynchronous communication.
- Understand serial protocols and the USART peripheral.
- Receive serial data with polling and interrupt-based methods.
- Implement communication between a computer and an STM32 board.
- Redirect `printf` to create an embedded debugging output channel.

### 7. I2C Communication

- Understand I2C fundamentals and transaction timing.
- Implement software I2C with an M24C02 memory example.
- Use the STM32 I2C peripheral for hardware I2C.
- Implement device access with both registers and the HAL library.

### 8. Timers

- Learn SysTick, basic timers, general-purpose timers, and advanced timers.
- Use system and basic timers to blink an LED.
- Use PWM to implement an LED breathing-light effect.
- Measure PWM frequency, period, and duty cycle.
- Generate a PWM waveform with a limited number of cycles.

### 9. DMA

- Understand the purpose, block diagram, and transfer flow of DMA.
- Transfer data from ROM to RAM.
- Transfer data from RAM to peripherals such as USART.
- Compare register-level and HAL-based DMA configuration.

### 10. ADC

- Understand ADCs and the successive-approximation ADC principle.
- Use the STM32 ADC peripheral for single-channel sampling.
- Implement independent multi-channel sampling.
- Understand ADC initialization and data acquisition through registers and HAL.

### 11. SPI and Flash

- Understand SPI communication and data-exchange timing.
- Learn the W25Q32 Flash structure, read/write commands, and operating constraints.
- Implement software SPI to read and write Flash.
- Use the STM32 SPI peripheral to access Flash.

### 12. Memory, Registers, and FSMC

- Learn common memory types and the STM32 memory structure.
- Understand memory mapping and register mapping.
- Learn FSMC bus interfaces, NOR/PSRAM, NAND, and peripheral interfaces.
- Expand external SRAM with FSMC.
- Control an LCD with FSMC using an 8080-style timing interface.

## Advanced: IoT Communication

### 1. CAN

- Understand the CAN physical layer, protocol layer, data frames, remote frames, and bus arbitration.
- Learn the STM32 CAN controller, transmit mailboxes, receive FIFO, and receive filters.
- Test CAN with loopback silent mode.
- Implement two-node CAN communication with one sender and one receiver.
- Build CAN projects with both registers and HAL.

### 2. Ethernet and W5500

- Understand Ethernet, the Internet, the OSI seven-layer model, and the TCP/IP four-layer model.
- Learn the W5500 hardware structure, features, and host-controller interaction.
- Port the official W5500 library into an STM32 project.
- Build basic Ethernet communication.
- Implement a TCP server, TCP client, and UDP communication.
- Build a simple web server.

### 3. Wi-Fi and ESP32-C3

- Learn Wi-Fi, WLAN, IEEE 802.11, APs, and the 2.4 GHz and 5 GHz bands.
- Understand Wi-Fi channels, wall penetration, and common network terminology.
- Learn the ESP32-C3 module and its connection to STM32.
- Control the Wi-Fi module with ESP-AT firmware and AT commands.
- Implement UART interaction between STM32 and ESP32-C3.
- Establish TCP communication over Wi-Fi.

### 4. Bluetooth LE

- Learn Bluetooth history, technology types, and common architectures.
- Understand PHY, LL, HCI, GAP, ATT, and GATT in the BLE stack.
- Learn BLE roles, addresses, advertising, scanning, and communication.
- Implement data transfer in ESP32-C3 Bluetooth transparent-transmission mode.

### 5. LoRa

- Learn common wireless protocols and low-power wide-area networks.
- Understand LoRa features, application scenarios, and network architecture.
- Learn the E220-400M22S module, pins, and key communication parameters.
- Implement a LoRa node.
- Port the official driver and build a LoRa gateway.
- Verify data transmission from a node to the gateway.

## Extended: System-Level Features

### 1. Power Control and Low Power

- Understand the STM32 power diagram, power-on reset, power-down reset, and programmable voltage detector (PVD).
- Learn sleep, stop, and standby modes.
- Implement low-power examples with both registers and HAL.
- Pay attention to wake-up sources, clock recovery, and peripheral behavior in low-power states.

### 2. RTC and Backup Domain

- Understand the RTC block diagram and power-loss continuity.
- Learn backup registers, tamper detection, RTC calibration, and backup data storage.
- Preserve data across power loss with backup registers.
- Wake the device from standby mode with an RTC alarm.
- Implement a real-time clock that retains time across power loss.

### 3. Watchdogs

- Understand how watchdogs monitor program execution and recover abnormal systems.
- Learn independent and window watchdog operation.
- Compare their trigger conditions and use cases.
- Implement an independent-watchdog reset example.

### 4. HAL Projects and Build Process

- Analyze the HAL directory structure and STM32CubeMX-generated projects.
- Understand the roles of `startup_stm32f103xe.s`, `system_stm32f1xx.c`, `stm32f1xx_it.c`, `stm32f1xx_hal_conf.h`, and `stm32f1xx_hal.c`.
- Understand initialization functions such as `HAL_Init()`, `SystemClock_Config()`, `MX_GPIO_Init()`, and `MX_USART1_UART_Init()`.
- Learn how a C source file becomes an executable program.
- Understand the Keil MDK build process.
- Distinguish the static state of a program from its runtime state.

## Development Approaches

| Approach | Main characteristic | Focus |
| --- | --- | --- |
| Register-level | Directly operates peripheral registers and stays close to hardware | Addresses, bit fields, timing, and reference manuals |
| HAL-based | Uses ST abstraction interfaces to improve productivity | CubeMX configuration, callbacks, states, and generated code |
| Hybrid | Uses registers for selected functions inside a HAL project | Abstraction boundaries, timing, and maintainability |

The course implements many examples with both registers and HAL, which helps connect hardware principles with engineering productivity.

## Suggested Study Order

1. Complete GPIO, clocks, HAL, and the first download-and-run project in the Basic material.
2. Learn USART, I2C, and SPI as the core on-chip communication interfaces.
3. Study interrupts, timers, DMA, and ADC to build event-driven and data-transfer skills.
4. Learn memory mapping, FSMC, and LCD control for external-device expansion.
5. Move to CAN, Ethernet, Wi-Fi, Bluetooth, and LoRa in the Advanced material.
6. Finish with low power, RTC, backup domain, watchdogs, and HAL project analysis.
7. For every peripheral, record the hardware connection, clock configuration, register or HAL setup, data flow, and verification method.

## Directory Structure

```text
stm32-mcu-development-notes/
├── README.md
├── README-English.md
└── docs/
    ├── 001_STM32单片机（基础篇）.pdf
    ├── 001_STM32单片机（基础篇）.docx
    ├── 002_STM32单片机（高级篇）.pdf
    ├── 002_STM32单片机（高级篇）.docx
    ├── 003_STM32单片机（扩展篇）.pdf
    └── 003_STM32单片机（扩展篇）.docx
```

## Current Scope

The repository currently focuses on STM32 course PDFs, DOCX source files, and a learning index. It does not include additional Keil projects, STM32CubeMX projects, driver source code, or hardware project files. Future work can add standalone drivers, board projects, communication wrappers, and test records by topic.

## Keywords

`STM32` `ARM Cortex-M` `GPIO` `HAL` `USART` `I2C` `SPI` `CAN` `Ethernet` `Wi-Fi` `Bluetooth LE` `LoRa` `Timer` `DMA` `ADC` `FSMC` `RTC` `Low Power` `Watchdog`
