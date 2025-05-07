---
title: "High‑Performance Barcode Scanner Firmware"
order: 3
date: 2025-04-01
description: "Ultra‑low‑latency firmware for 2D retail barcode scanning on STM32 with USB HID interface."
repo: "https://github.com/yourusername/barcode-firmware"
technologies:
  - C
  - STM32
  - FreeRTOS
  - USB-HID
# image: "/assets/img/projects/barcode-firmware-demo.png"
layout: post
toc: true
---

## Overview

I architected and optimized the entire firmware stack for a handheld 2D barcode scanner based on an STM32F7 MCU. By leveraging DMA for image transfer and a custom USB HID driver, I achieved **< 30 ms total decode latency**.

## Key Features

- **DMA‑Accelerated Image Capture**  
  Offloaded frame grabs from the CMOS sensor into SDRAM with zero CPU cycles lost.  
- **Real‑Time 2D Decoding**  
  Integrated an open‑source QR/DataMatrix library, tuned for fixed‑point arithmetic on Cortex‑M7.  
- **USB HID Emulation**  
  Presented decoded data as keystrokes to the host PC—no driver install required.  
- **RTOS‑Based Task Scheduling**  
  Used FreeRTOS to isolate sensor I/O, decode logic, and USB endpoint handling into dedicated threads.

## Results

- **Latency**: Reduced end‑to‑end read time from 85 ms → 28 ms.  
- **Throughput**: Sustained > 25 scans/sec on live retail barcodes.  
- **Footprint**: Entire firmware fits in 512 KB Flash and 256 KB SRAM.

---

You can clone the repo and follow the **README** there to build and deploy on your own STM32 development board.

