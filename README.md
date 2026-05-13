# pynq-image_processing-project
Hardware accelerated thresholding using PYNQ-Z2
Aim
To design and implement a hardware-accelerated image thresholding system using the PYNQ-Z2 by utilizing FPGA programmable logic for high-speed image processing and efficient real-time binary image generation.
Abstract

This project implements a hardware-accelerated image thresholding system using the PYNQ-Z2 FPGA development board. Image thresholding is a fundamental image processing technique used to separate objects from the background by converting grayscale images into binary images based on a selected threshold value.

The thresholding algorithm is implemented in hardware using FPGA acceleration to achieve high-speed image processing compared to conventional software execution. The programmable logic (PL) section of the PYNQ-Z2 board performs pixel-level thresholding operations in parallel, significantly improving processing speed and reducing latency.

Python running on the processing system (PS) is used to control the hardware accelerator, transfer image data, and display results through the PYNQ framework. The project demonstrates the advantages of FPGA-based hardware acceleration in real-time image processing applications.

Objective
To design a hardware accelerator for image thresholding.
To implement thresholding using FPGA programmable logic.
To interface PS and PL using AXI communication.
To achieve faster image processing using hardware acceleration.
To understand PS-PL co-design using the PYNQ framework.
Introduction

Image thresholding is one of the simplest and most widely used image segmentation techniques. It converts grayscale images into binary images by comparing each pixel intensity with a predefined threshold value.

If:

Pixel value > Threshold → White (255)
Pixel value ≤ Threshold → Black (0)

Thresholding is used in:

Object detection
Medical imaging
Industrial inspection
OCR systems
Surveillance systems

Traditional software-based thresholding may become slower for large image datasets or real-time applications. FPGA-based hardware acceleration enables parallel pixel processing, resulting in high-speed execution and reduced computational delay.

Hardware Used
Component	Purpose
PYNQ-Z2 Board	FPGA development platform
Zynq-7000 SoC	Processing System + Programmable Logic
HDMI/Display	Output visualization
PC/Laptop	Development environment
Software Used
Software	Purpose
Vivado	Hardware design and IP integration
PYNQ	Python-based FPGA interaction
Python	Control and image processing
Jupyter Notebook	Running Python applications
