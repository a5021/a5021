# Hi there! I'm an Embedded Software Engineer

I specialize in low-level, register-level development (**Bare Metal**) and firmware optimization for ARM Cortex-M microcontrollers. I focus on writing highly efficient, non-blocking peripheral drivers and creating custom automation tools to streamline the development workflow.

---

## Technical Stack

### Microcontrollers (MCUs)
- **STMicroelectronics:** STM32F103 (Blue Pill), STM32F030
- **Nordic Semiconductor:** nRF52832

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

### 1. [Non-Blocking DS18B20 Register-Level Driver](https://github.com/a5021/non-blocking-ds18B20-driver-for-stm32f103c8t6)
- **Overview:** An asynchronous, non-blocking driver for the DS18B20 thermometer on STM32F103, built strictly at the register level.
- **Key Feature:** Eliminates blocking hardware delays entirely, resulting in minimal CPU overhead and making it safe for time-critical, multi-tasking systems.
- **Stack:** C, STM32, Reference Manual Registers.

### 2. [stm32codegen — Initialization Code Generator](https://github.com/a5021/BluePill_Project_Generator)
- **Overview:** A Python-based CLI tool designed to automatically generate CMSIS-compliant peripheral initialization templates for STM32 MCUs.
- **Key Feature:** Serving as a lightweight alternative to heavy IDE tools (like STM32CubeMX) for developers who prefer clean, bloat-free bare-metal code.
- **Stack:** Python, CMSIS, Bare-metal workflow.

### 3. [nRF52832 + BME280 Wireless Sensor Node](https://github.com/a5021/NRF52832-BME280-RADIO)
- **Overview:** Firmware for a wireless environmental sensor node measuring pressure, humidity, and temperature.
- **Key Feature:** Implements direct radio communication on Nordic chips with a strong focus on low-power optimization and standalone efficiency.
- **Stack:** C, nRF52832, BME280.

### 4. [Wireless Sensor → Repeater → Receiver Chain](https://github.com/a5021/STM32F030F4P6-WIRELESS-MULTISENSOR)
- **Overview:** A complete three-link wireless telemetry system spanning three MCU architectures. An STM32F030F4P6 multisensor node (BMP180, Si7021, BH1750) transmits environmental data over nRF24L01+ to an ATmega8 repeater, which controls a load relay and retransmits the datagram across multiple channels. An STM8S003F3 receiver decodes the relayed data and sends it over UART to an OpenWrt-based router, which forwards the telemetry to the internet via a Perl script.
- **Key Feature:** Demonstrates cross-architecture interoperability (ARM Cortex-M0, AVR, STM8) with a shared radio protocol, bare-metal drivers, and relay-based automation, with end-to-end telemetry delivery to an internet-connected endpoint.
- **Stack:** C, STM32F030F4P6, ATmega8, STM8S003F3, nRF24L01+.

### 5. [BluePill Project Generator](https://github.com/a5021/BluePill_Project_Generator)
- **Overview:** A shell script for instantaneous scaffolding of a clean, CMSIS-ready project structure for BluePill boards, bypassing bulky IDE project wizards.
- **Stack:** Bash / Shell.

---

## Profile Analytics

This dynamic card updates automatically and analyzes the codebase across all my public repositories:

[![a5021's GitHub stats](https://github-readme-stats.vercel.app/api?username=a5021&show_icons=true&theme=dark)](https://github.com/anuraghazra/github-readme-stats)

---

## Connect with Me

- **Telegram:** [@a5021](https://t.me)
- **Explore More:** Feel free to check out the [Repositories](https://github.com) tab for other low-level projects (including multi-sensor setups on STM32F030 + nRF24L01).
