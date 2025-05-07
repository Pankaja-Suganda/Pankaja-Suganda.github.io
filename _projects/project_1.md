---
title: "Hardware Accelerators for Real-Time Facial Computing"
description: "Developed a custom hardware IP to enhance real-time facial computing on the PYNQ Z2 board."
date: 2024-12-15
# image: /assets/images/project1.png
layout: post
order: 1
status: Completed
project: false
---

## Overview

Developed a custom hardware IP to enhance real-time facial computing on the PYNQ Z2 board. The project involved optimizing memory hierarchy and data transfer efficiency for Convolutional Neural Networks (CNN) and max-pooling operations in a embedded system.


<p style="text-align: center;">
  <img src="https://img.shields.io/badge/status-Completed-brightgreen" alt="Project Status">
</p>
## Key Contributions

- **Hardware IP Design**: Created a hardware IP core for CNN and max-pooling operations using Vivado.
- **AXI & AXIS Integration**: Implemented AXI to configure the hardware IP and AXIS for establishing DMA transfers.
- **Driver Development**: Developed a driver to interface the custom hardware IP with the Processing System (PS) side, facilitating seamless integration with the Pnet model.
- **System Integration**: Integrated the custom hardware IP with the PYNQ Z2 board and the Pnet model in MTCNN, improving real-time facial recognition performance on resource-constrained devices.

**NOTE**: The paper publication is in progress