# Arduino Shield – MAX7219 7-Segment Display + DS1307 RTC

> Eagle CAD PCB Design | 2-Layer Shield | MAX7219 + DS1307

---

## Project Description
An Arduino shield PCB designed using **Eagle CAD** that integrates a **MAX7219CNG** SPI LED driver and a **DS1307** I2C real-time clock. The shield drives a **4-digit 7-segment display (NFD-5641AS)** and shows real-time clock data. A **CR1220 backup battery** and **32.768kHz crystal** maintain RTC timekeeping during power-off. Standard Arduino R3 headers allow direct plug-in to Arduino UNO or Mega.

**Short Description (≤350 chars):**
> Arduino shield PCB using MAX7219 SPI 7-segment driver + DS1307 I2C RTC. Displays real-time clock data on 4-digit display. CR1220 battery backup, 32.768kHz crystal. Designed in Eagle CAD.

---

## Key Components

| Component | Description |
|-----------|-------------|
| **MAX7219CNG** | SPI-controlled 8-digit LED display driver |
| **DS1307** | I2C real-time clock IC |
| **NFD-5641AS** | 4-digit 7-segment common-cathode display |
| **CR1220 (SMT)** | 3V backup battery for RTC |
| **32.768kHz Crystal** | Precise RTC time reference |
| **Arduino R3 Headers** | Standard shield interface (ICSP + pins) |
| **Pull-up Resistors (4.7kΩ)** | I2C SDA/SCL pull-ups |
| **Decoupling Caps (0.1µF)** | Supply noise filtering |

---

## Design Features
- MAX7219 drives 4-digit 7-segment display via 3-wire SPI
- DS1307 provides seconds/minutes/hours/date over I2C (TWI)
- CR1220 backup battery keeps RTC running when Arduino is off
- 32.768kHz crystal ensures accurate 1-second RTC tick
- Standard Arduino R3 form factor – direct plug-in, no wiring needed
- Both SPI and I2C interfaces used simultaneously on Arduino

---

## Signal Flow
```
Arduino UNO / Mega – Host MCU
       ↓ SPI (MOSI / SCK / SS)
  MAX7219CNG – LED Driver
       ↓
  NFD-5641AS – 4-Digit 7-Segment Display
       ↓ I2C (SDA / SCL)
  DS1307 RTC – Real-Time Clock
       ↑
  32.768kHz Crystal ← RTC Clock Reference
  CR1220 Battery ← RTC Backup Power
```

---

## Files Included
- a_Arduino Shield MAX7219.sch – Eagle Schematic
- a_Arduino Shield MAX7219.brd – Eagle PCB Layout
- Gerber_files_a_Arduino Shield MAX7219_2026-05-20.zip – Gerber files

---

