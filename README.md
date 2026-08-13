<div align="center">

<img src="https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/ASSETS/PRJ-2026-PCB-0005-DERMSCOPE-REVIVE.png" width="100%" alt="DermScope REVIVE — Top View"/>

---

# ⚡ PRJ-2026-PCB-0005-DERMSCOPE-REVIVE

### Advanced High-Speed Carrier PCB for Handheld Dermatology Imaging

**Designed for [Revive Medical Technology](https://rmt-usa.com/) · Powered by INVENSOM-6UL SOM**

[![PCB Version](https://img.shields.io/badge/PCB%20Version-V2-00c8ff?style=for-the-badge)](#)
[![Layer Count](https://img.shields.io/badge/PCB%20Layers-4%20Layer-ff6b35?style=for-the-badge)](#)
[![Board Size](https://img.shields.io/badge/Board%20Size-90%20×%2062%20mm-22c55e?style=for-the-badge)](#)
[![RoHS](https://img.shields.io/badge/RoHS-Compliant-4ade80?style=for-the-badge)](#)
[![Impedance](https://img.shields.io/badge/Impedance-Controlled-a855f7?style=for-the-badge)](#)
[![Surface Finish](https://img.shields.io/badge/Finish-Immersion%20Gold%20(ENIG)-f59e0b?style=for-the-badge)](#)

[![License](https://img.shields.io/badge/License-Proprietary%20%C2%A9%20RMT-dc2626?style=for-the-badge)](./LICENSE)
[![Changelog](https://img.shields.io/badge/Changelog-V2%20Released-16a34a?style=for-the-badge)](./CHANGELOG.md)
[![Last Commit](https://img.shields.io/github/last-commit/hiibrarahmad/PRJ-PCB-1001-2024-Dermscope-Revive.github.io?style=for-the-badge&color=0891b2&label=Last%20Commit)](../../commits/main)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-22c55e?style=for-the-badge&logo=github)](https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/)
[![Visitors](https://visitor-badge.laobi.icu/badge?page_id=hiibrarahmad.PRJ-PCB-1001-2024-Dermscope-Revive.github.io&style=for-the-badge&color=0e7490)](https://github.com/hiibrarahmad/PRJ-PCB-1001-2024-Dermscope-Revive.github.io)

<br/>

[🔬 Interactive PCB View](https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/) · [📋 Project Assets](https://github.com/hiibrarahmad/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/tree/main/ASSETS) · [🌐 Revive Medical Technology](https://rmt-usa.com/) · [📜 License](./LICENSE) · [📝 Changelog](./CHANGELOG.md)
</div>

---

## 📖 Project Overview

**DermScope REVIVE** is a **pocket-size, high-speed embedded carrier PCB** developed for handheld dermatology diagnostics. Designed as the motherboard/carrier for the **INVENSOM-6UL System on Module**, this board bridges cutting-edge medical imaging hardware with a compact, power-efficient form factor — enabling clinicians and dermatologists to perform real-time skin examinations in any environment.

> 💡 This carrier board hosts the **NXP i.MX6UL ARM® Cortex®-A7** based INVENSOM-6UL SOM and routes its full peripheral set to a purpose-built medical imaging platform with multi-polarization dermoscopy optics, 2K touch display, and professional-grade camera pipeline.

---

## 🖼️ PCB Preview

<table>
<tr>
<td align="center" width="50%">

**🔝 Top Side**

<img src="https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/ASSETS/PRJ-2026-PCB-0005-DERMSCOPE-REVIVE.png" width="100%" alt="DermScope PCB — Top View"/>

</td>
<td align="center" width="50%">

**🔻 Bottom Side**

<img src="https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/ASSETS/PRJ-2026-PCB-0005-DERMSCOPE-REVIVE bot.png" width="100%" alt="DermScope PCB — Bottom View"/>

</td>
</tr>
</table>

<div align="center">

🔗 **[→ View Interactive PCB Online](https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/)**

</div>

---

## 🎯 Core Design Goals

| Goal | Specification |
|------|--------------|
| 🩺 **Medical Imaging** | High-res skin capture with cross & linear polarization |
| 📷 **Camera Pipeline** | MIPI CSI 4-Lane interface to high-resolution image sensor |
| 🖥️ **Display** | MIPI DSI 4-Lane to 2K touch panel (LVDS & HDMI alternative outputs) |
| 🔋 **Power** | Rechargeable battery via TP4056, ≥ 2 hours runtime |
| 📦 **Form Factor** | Compact & handheld (board: 90 × 62 mm) |
| 🔒 **Security** | Hardware-rooted trust via INVENSOM-6UL ARM TrustZone |
| 🌐 **Connectivity** | Wi-Fi, Bluetooth, 4G LTE NB-IoT, GPS, Ethernet |

---

## 🧠 System Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        DERMSCOPE REVIVE CARRIER PCB                 │
│                                                                     │
│  ┌──────────┐    ┌────────────────┐    ┌────────────────────────┐  │
│  │ MICRO USB│───▶│  TP4056 CHARGE │    │     INVENSOM-6UL SOM   │  │
│  └──────────┘    │    MODULE      │    │  NXP i.MX6UL Cortex-A7 │  │
│                  └───────┬────────┘    │   up to 900 MHz         │  │
│  ┌──────────┐            │            │   1GB DDR3 / 2GB NAND   │  │
│  │ BATTERY  │──────┐     ▼            └──────────┬─────────────┘  │
│  └──────────┘      │ ┌────────────┐              │                 │
│                    │ │ OVER/REVERSE│   ┌──────────▼──────────────┐  │
│  ┌──────────┐      └▶│  VOLTAGE   ├──▶│     POWER SUPPLY        │  │
│  │ 15V 1x2  │        │ PROTECTION │   │     (+5V, EN)           │  │
│  └──────────┘        └────────────┘   └─────────────────────────┘  │
│                                                                     │
│  ┌─────── DISPLAY OUTPUTS ─────────────────────────────────────┐   │
│  │  MIPI DSI 4-Lane ──▶ DSI-to-HDMI/LVDS ──▶ MIPI DSI CONN   │   │
│  │                                       ──▶ HDMI 1.4 CONN    │   │
│  │                                       ──▶ LVDS CONN        │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                                                                     │
│  ┌─────── CAMERA INPUT ────────────────────────────────────────┐   │
│  │  MIPI CSI 4-Lane ──────────────────────▶ MIPI CSI CONN     │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                                                                     │
│  ┌─────── USB & STORAGE ───────────────────────────────────────┐   │
│  │  USB1 ──▶ OTG Micro USB                                     │   │
│  │  USB2 ──▶ USB HUB ──▶ 4× USB 2.0 Type-A                   │   │
│  │  UART2/UART4 ──▶ Selection Header ──▶ USB TTL Debug        │   │
│  │  SDIO2 ──▶ SD Card Connector                               │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                                                                     │
│  ┌─────── ADC / GPIO / EXPANDERS ──────────────────────────────┐   │
│  │  eCSPI2 ──▶ MCP3208-B ADC (CH0–CH7) ──▶ ADC Connectors    │   │
│  │  GPIO_EXP 1–7 ──▶ GPIO Output Connector (Lens Interface)   │   │
│  │  GPIO_EXP 2–6 ──▶ GPIO EXT Connector                      │   │
│  │  I2C4 ──▶ J1102 Connector                                  │   │
│  │  UART3 ──▶ J1101 Connector                                  │   │
│  └─────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 💻 INVENSOM-6UL SOM — Processor Module

This carrier board is designed exclusively for the **INVENSOM-6UL** System on Module by Inventron.

<table>
<tr><th>Category</th><th>Specification</th></tr>
<tr><td>🧮 <strong>Processor</strong></td><td>NXP i.MX6UL ARM® Cortex®-A7 @ 528 MHz (up to 900 MHz), 128 KB L2 cache + NEON™ MPE</td></tr>
<tr><td>💾 <strong>Memory</strong></td><td>Up to 1 GB DDR3 · Up to 2 GB NAND Flash · Up to 128 MB SPI NOR Flash (optional)</td></tr>
<tr><td>📷 <strong>Camera</strong></td><td>8/10/16/24-bit Parallel CSI with BT.656 support</td></tr>
<tr><td>🖥️ <strong>Display</strong></td><td>8/16/18/24-bit parallel LCD up to WXGA (1366×768)</td></tr>
<tr><td>🔐 <strong>Security</strong></td><td>ARM TrustZone, Secure Boot (HAB), AES-128/256, RSA-4096 DPA, TRNG, eFUSE (OTP), Secure RTC, Tamper Detection</td></tr>
<tr><td>🌐 <strong>Ethernet</strong></td><td>2× 10/100 Mbit MAC + IEEE 1588</td></tr>
<tr><td>⚡ <strong>USB</strong></td><td>2× HS USB 2.0 OTG (up to 480 Mbps) with integrated PHY</td></tr>
<tr><td>📡 <strong>Wi-Fi</strong></td><td>802.11 b/g/n, 65 Mbps (optional)</td></tr>
<tr><td>🔵 <strong>Bluetooth</strong></td><td>v4.2 BR/EDR/LE, 3 Mbps (optional)</td></tr>
<tr><td>📶 <strong>Cellular</strong></td><td>4G LTE Cat M1/NB-IoT + 2G EGPRS fallback (optional)</td></tr>
<tr><td>🛰️ <strong>GNSS</strong></td><td>GPS, GLONASS, BeiDou, Galileo, QZSS</td></tr>
<tr><td>🔌 <strong>Serial I/O</strong></td><td>5× UART · 4× I2C · 3× SPI · 2× CAN · 3× I2S · 8× PWM · 2× 12-bit ADC</td></tr>
<tr><td>📐 <strong>Form Factor</strong></td><td>40 × 40 × 5.2 mm · 152-pin 1 mm pitch edge-castellated SMT</td></tr>
<tr><td>🌡️ <strong>Operating Temp</strong></td><td>−30°C to +70°C (standard) · −40°C to +85°C (no Wi-Fi)</td></tr>
<tr><td>⚡ <strong>Operating Voltage</strong></td><td>3.4V – 4.2V (typ. 3.8V)</td></tr>
</table>

---

## 🔌 PCB Interface Map

### 🖥️ Display Interfaces
- **MIPI DSI 4-Lane** → MIPI DSI to HDMI/LVDS converter
- **HDMI 1.4** output connector
- **LVDS** display output connector
- **VDD_3V3** and **VDD_1V8** power rails for display logic

### 📷 Camera Interface
- **MIPI CSI 4-Lane** → High-resolution image sensor connector
- Supports RAW10/RAW12 capture for dermoscopy imaging

### 🔋 Power System
- **Micro USB** charging input
- **TP4056** Li-Ion charge management module
- **Over & Reverse Voltage Protection** circuit
- **Buck-up Battery** backup rail
- **ON/OFF Button** and **Reset Button**
- **VBAT** and **+5V** regulated supply rails

### 💾 Storage & Boot
- **SDIO2** → SD Card connector
- **Boot Mode** and **Boot Config** jumper headers

### 🔗 USB Connectivity
- **USB HUB** → 4× USB 2.0 Type-A host ports (2× dual connectors)
- **OTG Micro USB** for device/host mode
- **USB TTL** debug via Selection Header (UART2 / UART4)

### 📟 Serial Expansion
- **UART3** → J1101 general-purpose connector
- **I2C4** → J1102 expansion connector
- **eCSPI2** → MCP3208-B 8-channel 12-bit SPI ADC
  - CH0 & CH1 → ADC connector (J1103)
  - CH2–CH7 → ADC_Conn expansion

### 🔧 GPIO Expansion
- **GPIO_EXP 1–7** → GPIO Output CON / **Lens Connector** (J1100)
- **GPIO_EXP 2–6** → GPIO EXT CON (external LED/optics control)

---

## 📐 PCB Specifications

<table>
<tr><th>Parameter</th><th>Value</th></tr>
<tr><td>PCB Version</td><td>V2</td></tr>
<tr><td>PCB Definition</td><td>Carrier Board</td></tr>
<tr><td>Board Thickness</td><td>1.6 ±0.16 mm</td></tr>
<tr><td>Layer Count</td><td>4 Layers</td></tr>
<tr><td>Board Size</td><td>90 × 62 mm</td></tr>
<tr><td>Panel</td><td>2×2 (5 mm stripe on edges)</td></tr>
<tr><td>Material</td><td>FR4</td></tr>
<tr><td>Surface Finish</td><td>Immersion Gold (ENIG)</td></tr>
<tr><td>Min. Drill Diameter</td><td>0.2 mm</td></tr>
<tr><td>Min. Via Pad Size</td><td>0.4 mm</td></tr>
<tr><td>Outer Layer Line/Space</td><td>4 mil / 4 mil</td></tr>
<tr><td>Inner Layer Line/Space</td><td>4 mil / 4 mil</td></tr>
<tr><td>Via Plating Thickness</td><td>Min. 20 µm</td></tr>
<tr><td>Solder Mask</td><td>Top & Bottom · Color: Green</td></tr>
<tr><td>Silkscreen</td><td>Top & Bottom · Color: White</td></tr>
<tr><td>Impedance Control</td><td>✅ Yes</td></tr>
<tr><td>RoHS</td><td>✅ Compliant</td></tr>
<tr><td>Via Tenting</td><td>✅ Yes</td></tr>
</table>

---

## 🧱 PCB Stack-Up

```
┌─────────────────────────────────────────┐
│  TOP LAYER     │  CU     │ 0.035 mm (1.4 mil)  │
├─────────────────────────────────────────┤
│  PREPREG       │         │ 0.066 mm (2.6 mil)  │
├─────────────────────────────────────────┤
│  LAYER 1       │  CU     │ 0.035 mm (1.4 mil)  │
├─────────────────────────────────────────┤
│  PREPREG       │         │ 1.27 mm  (50 mil)   │  ← CORE
├─────────────────────────────────────────┤
│  LAYER 2       │  CU     │ 0.035 mm (1.4 mil)  │
├─────────────────────────────────────────┤
│  PREPREG       │         │ 0.066 mm (2.6 mil)  │
├─────────────────────────────────────────┤
│  BOTTOM LAYER  │  CU     │ 0.035 mm (1.4 mil)  │
└─────────────────────────────────────────┘
```

---

## 📏 Impedance Control Reference

| Target Impedance | Layer | Trace Width / Gap |
|-----------------|-------|-------------------|
| 100 Ω ±10% | TOP LAYER | 4 mil / 5.575 mil |
| 100 Ω ±10% | BOTTOM LAYER | 4 mil / 5.575 mil |
| 90 Ω ±10% | TOP LAYER | 4.495 mil / 4 mil |
| 90 Ω ±10% | BOTTOM LAYER | 4.495 mil / 4 mil |
| 85 Ω ±10% | TOP LAYER | 5.051 mil / 4 mil |
| 85 Ω ±10% | BOTTOM LAYER | 5.051 mil / 4 mil |
| 50 Ω ±10% | TOP LAYER | 4 mil (single-ended) |
| 50 Ω ±10% | BOTTOM LAYER | 4 mil (single-ended) |

> ⚠️ All high-speed signals (MIPI CSI, MIPI DSI, USB 2.0 HS, SDIO) are impedance-controlled. Reference layers: **TOP → Layer 1**, **BOTTOM → Layer 2**.

---

## 🩺 DermScope Device — User Requirements

The carrier PCB is designed to fulfill the following product-level requirements for the DermScope REVIVE handheld dermatoscope:

- ✅ Compact, portable, and easy to carry
- ✅ Durable and field-ready construction
- ✅ Magnified, high-resolution skin image capture
- ✅ Rechargeable with ≥ 2 hours single-charge runtime
- ✅ High-resolution display (MIPI DSI / LVDS / HDMI)
- ✅ Onboard and expandable image storage (SD + NAND)
- ✅ Digital zoom functionality via iMX6UL GPU pipeline
- ✅ **Cross and linear polarization** switching via GPIO lens interface
- ✅ Smooth operation via Linux BSP on ARM Cortex-A7

---

## 🛠️ Software & BSP

| Component | Details |
|-----------|---------|
| OS | Yocto Linux / Debian / Ubuntu |
| Kernel | Linux 4.9.11 |
| Bootloader | U-Boot 2017.03 |
| Security | OpenSSL, TLS/DTLS, Hardware Crypto Dev |
| Connectivity | Ethernet, Wi-Fi, BT, 4G/2G, GNSS drivers |
| IoT Protocols | MQTT, AMQP, CoAP, OPC-UA, LWM2M, oneM2M |
| Cloud | Microsoft Azure, AWS, Google Cloud |
| Graphics | Qt5, Wayland, XServer |
| OTA Updates | OS and Application update management |

---

## 🏢 About Revive Medical Technology

This board was designed for **[Revive Medical Technology (RMT)](https://rmt-usa.com/)** — a US-based medical technology company focused on advancing diagnostic tools for dermatology and skin health.

---

## 📁 Repository Structure

```
PRJ-PCB-1001-2024-Dermscope-Revive.github.io/
│
├── ASSETS/
│   ├── PRJ-2026-PCB-0005-DERMSCOPE-REVIVE.png       ← Top view (PNG)
│   ├── PRJ-2026-PCB-0005-DERMSCOPE-REVIVE.jpg       ← Top view (JPG)
│   ├── PRJ-2026-PCB-0005-DERMSCOPE-REVIVE bot.png   ← Bottom view (PNG)
│   └── PRJ-2026-PCB-0005-DERMSCOPE-REVIVE bot.jpg   ← Bottom view (JPG)
│
├── .github/
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md                             ← Bug report template
│       ├── feature_request.md                        ← Feature request template
│       ├── question.md                               ← Question template
│       └── config.yml                                ← Issue chooser config
│
├── index.html                                        ← Interactive PCB viewer
├── README.md                                         ← This file
├── LICENSE                                           ← Proprietary © RMT
├── CHANGELOG.md                                      ← Version history
└── CONTRIBUTING.md                                   ← Contribution guidelines
```

---

## 🔗 Links

| Resource | URL |
|----------|-----|
| 🌐 Interactive PCB View | [hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io](https://hiibrarahmad.github.io/PRJ-PCB-1001-2024-Dermscope-Revive.github.io/) |
| 🏢 Revive Medical Technology | [rmt-usa.com](https://rmt-usa.com/) |
| 📦 INVENSOM-6UL SOM | [Inventron](https://www.inventron.net/) |
| 📜 License | [LICENSE](./LICENSE) |
| 📝 Changelog | [CHANGELOG.md](./CHANGELOG.md) |
| 🤝 Contributing | [CONTRIBUTING.md](./CONTRIBUTING.md) |

---

<div align="center">

**PRJ-2026-PCB-0005-DERMSCOPE-REVIVE**

*Designed with precision for Revive Medical Technology · Built on INVENSOM-6UL*

[![Revive Medical Technology](https://img.shields.io/badge/Client-Revive%20Medical%20Technology-0ea5e9?style=for-the-badge)](https://rmt-usa.com/)
[![Platform](https://img.shields.io/badge/Platform-INVENSOM--6UL-ef4444?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-Proprietary%20%C2%A9%20RMT-dc2626?style=for-the-badge)](./LICENSE)

© 2026 Revive Medical Technology. All Rights Reserved.

</div>
