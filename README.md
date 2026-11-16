# Hi there! I'm an Embedded Software Engineer

I specialize in low-level, register-level development (**Bare Metal**) and firmware optimization for ARM Cortex-M, AVR, and STM8 microcontrollers. I focus on writing highly efficient, non-blocking peripheral drivers, wireless telemetry systems, and creating custom automation tools to streamline the development workflow.

---

## Technical Stack

### Microcontrollers (MCUs)
- **STMicroelectronics:** STM32 and STM8
- **Nordic Semiconductor:** nRF52832
- **Microchip:** ATmega8 (AVR)

### Peripherals & Protocols
- **Wireless/Radio:** Proprietary 2.4GHz (nRF24L01), BLE (nRF52)
- **Sensors:** BME280 (Bosch), DS18B20 (Dallas/Maxim)
- **Interfaces:** Register-level control of UART, SPI, I2C, 1-Wire, DMA, and Timers

### Languages & Automation Tools
- **Firmware:** C (Primary for MCU), C++
- **Automation & Scripting:** Python (code generation, parsing), Bash / Shell scripting
- **Methodology:** Pure CMSIS & Register-level development (No heavy HAL abstractions), CPU overhead optimization, and Low Power management

---

## Featured Projects

Here are the key repositories that reflect my engineering approach and code quality:

### 1. [stm32-async-1wire — Non-Blocking 1-Wire Library](https://github.com/a5021/stm32-async-1wire)
- **Overview:** A universal, register-level 1-Wire master layer for STM32 with non-blocking DS18B20 temperature, DS2431 EEPROM and DS2413 dual-channel switch drivers built on top. The MCU-independent core rides a small port interface; header-only per-family backends cover STM32F0, F1, F3, F4, G0, G4, L4, C5, H5, U5 and H7.
- **Key Feature:** Every bus slot is generated and captured by TIM1 + DMA hardware automation — zero interrupts, zero busy-waits. Multi-sensor Search ROM, alarm search, per-device addressing, non-blocking command transactions, a full DS2431 read/write EEPROM cycle and DS2413 PIO control, verified on real hardware including a 30-minute soak with 0 CRC failures on STM32U585CIU6 at 160 MHz.
- **Stack:** C, CMSIS / Register-Level Programming, TIM + DMA, Cortex-M0/M0+/M3/M4/M33/M7; TrustZone-aware secure build (`-mcmse`) on STM32U5.

### 2. [Wireless Sensor](https://github.com/a5021/STM32F030F4P6-WIRELESS-MULTISENSOR) → [Repeater](https://github.com/a5021/ATMEGA8-NRF24L01-REPEATER) → [Receiver](https://github.com/a5021/STM8S-NRF24L01-RECEIVER)
- **Overview:** A complete three-link wireless telemetry system spanning three MCU architectures. An STM32F030F4P6 multisensor node (BMP180, Si7021, BH1750) transmits environmental data over nRF24L01+ to an ATmega8 repeater, which controls a load relay and retransmits the datagram across multiple channels. An STM8S003F3 receiver decodes the relayed data and sends it over UART to an OpenWrt-based router, which forwards the telemetry to the internet via a set of scripts.
- **Key Feature:** Demonstrates cross-architecture interoperability (ARM Cortex-M0, AVR, STM8) with a shared radio protocol, bare-metal drivers, and relay-based automation, with end-to-end telemetry delivery to an internet-connected endpoint.
- **Stack:** C, STM32F030F4P6, ATmega8, STM8S003F3, nRF24L01+.

### 3. [nRF52832 + BME280 Wireless Sensor Node](https://github.com/a5021/NRF52832-BME280-RADIO)
- **Overview:** Firmware for a wireless environmental sensor node measuring pressure, humidity, and temperature.
- **Key Feature:** Implements direct radio communication on Nordic chips with a strong focus on low-power optimization and standalone efficiency.
- **Stack:** C, nRF52832, BME280.

### 4. [BluePill Project Generator](https://github.com/a5021/BluePill_Project_Generator)
- **Overview:** A shell script for instantaneous scaffolding of a clean, CMSIS-ready project structure for BluePill boards, bypassing bulky IDE project wizards.
- **Stack:** Bash / Shell.

### 5. [stm32codegen - Initialization Code Generator](https://github.com/a5021/stm32codegen)
- **Overview:** A Python-based CLI tool designed to automatically generate CMSIS-compliant peripheral initialization templates for STM32 MCUs.
- **Key Feature:** Serving as a lightweight alternative to heavy IDE tools (like STM32CubeMX) for developers who prefer clean, bloat-free bare-metal code.
- **Stack:** Python, CMSIS, Bare-metal workflow.

---

## Profile Analytics

This dynamic card updates automatically and analyzes the codebase across all my public repositories:

[![a5021's GitHub stats](https://github-stats-extended.vercel.app/api?username=a5021&show_icons=true&theme=dark)](https://github.com/stats-organization/github-stats-extended)
