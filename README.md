# Pynq-Image_processing-Project
## **Hardware accelerated thresholding using PYNQ-Z2**

## **Aim:**

To design and implement a hardware-accelerated image thresholding system using the PYNQ-Z2 by utilizing FPGA programmable logic for high-speed image processing and efficient real-time binary image generation.

## **Abstract:**

This project implements a hardware-accelerated image thresholding system using the PYNQ-Z2 FPGA development board. Image thresholding is a fundamental image processing technique used to separate objects from the background by converting grayscale images into binary images based on a selected threshold value.

The thresholding algorithm is implemented in hardware using FPGA acceleration to achieve high-speed image processing compared to conventional software execution. The programmable logic (PL) section of the PYNQ-Z2 board performs pixel-level thresholding operations in parallel, significantly improving processing speed and reducing latency.

Python running on the processing system (PS) is used to control the hardware accelerator, transfer image data, and display results through the PYNQ framework. The project demonstrates the advantages of FPGA-based hardware acceleration in real-time image processing applications.

## **Objective:**

- To design a hardware accelerator for image thresholding.
- To implement thresholding using FPGA programmable logic.
- To interface PS and PL using AXI communication.
- To achieve faster image processing using hardware acceleration.
- To understand PS-PL co-design using the PYNQ framework.
  
## **Introduction:**

Image thresholding is one of the simplest and most widely used image segmentation techniques. It converts grayscale images into binary images by comparing each pixel intensity with a predefined threshold value.

### **Thresholding Condition**

- Pixel value > Threshold → White (255)
- Pixel value ≤ Threshold → Black (0)

Thresholding is used in:

Object detection
Medical imaging
Industrial inspection
OCR systems
Surveillance systems

Traditional software-based thresholding may become slower for large image datasets or real-time applications. FPGA-based hardware acceleration enables parallel pixel processing, resulting in high-speed execution and reduced computational delay.


## **Hardware Used**

| S.No | Hardware Component | Description |
|------|-------------------|-------------|
| 1 | PYNQ-Z2 Board | FPGA development board used for hardware acceleration |
| 2 | Zynq-7000 SoC | Combines Processing System (PS) and Programmable Logic (PL) |
| 3 | HDMI Display/Monitor | Used for displaying processed image output |
| 4 | USB Cable | Used for programming and communication |
| 5 | PC/Laptop | Used for development and execution |

---

## **Software Used**

| S.No | Software | Purpose |
|------|----------|---------|
| 1 | Vivado Design Suite | Hardware design and IP integration |
| 2 | PYNQ Framework | Python-based FPGA interaction |
| 3 | Python | Image processing and hardware control |
| 4 | Jupyter Notebook | Running Python applications on PYNQ |

## **Working Principle**

The image is first converted into grayscale format. Each pixel intensity is then compared with a fixed threshold value.

### **Thresholding Formula**
The thresholding operation converts grayscale images into binary images.

$$
g(x,y)=
\begin{cases}
255, & f(x,y) > T \\
0, & f(x,y) \leq T
\end{cases}
$$

Where:

- \(f(x,y)\) = Input pixel intensity  
- \(T\) = Threshold value  
- \(g(x,y)\) = Output binary pixel

The programmable logic performs this operation for all pixels efficiently in parallel.

## **FPGA Hardware Acceleration**

Traditional software execution processes image pixels sequentially, which increases execution time for large images.

In FPGA-based acceleration:

- Multiple pixels are processed simultaneously
- Parallel processing improves speed
- Reduced latency is achieved
- Real-time image processing becomes possible

The thresholding algorithm is implemented inside the programmable logic (PL) of the FPGA, significantly improving processing efficiency compared to software-only execution.

## **Design Methodology**
### **1. Hardware Design in Vivado**

- Created custom thresholding logic
- Designed AXI-based hardware accelerator
- Integrated PS and PL blocks
- Generated bitstream file

### **2. Export Hardware**

- Generated `.bit` and `.hwh` files
- Exported hardware platform

### **3. Software Development**

- Loaded overlay in PYNQ
- Used Python for image transfer and control
- Displayed thresholded image output

## **Features**

- High-speed image processing
- Parallel hardware execution
- Reduced latency
- Efficient PS-PL communication
- Real-time processing capability

## **Advantages**

- Faster than software-only implementation
- Suitable for real-time systems
- Low processing delay
- Efficient hardware utilization
- Scalable for advanced image processing applications
  
## **Applications**

- Medical image analysis
- Traffic monitoring systems
- Face detection systems
- Industrial automation
- Security and surveillance
- Object segmentation

## **Results**

The hardware accelerator successfully performed binary image thresholding on grayscale images using the FPGA programmable logic of the PYNQ-Z2 board. Compared to software execution, the hardware implementation achieved improved processing efficiency and faster execution time.

## **Conclusion**

The project successfully demonstrates hardware-accelerated image thresholding using the PYNQ-Z2 FPGA platform. By implementing the thresholding operation in programmable logic, high-speed image processing was achieved with reduced computational overhead. The project highlights the effectiveness of FPGA acceleration for real-time embedded vision applications.

## **Future Scope**

- Adaptive thresholding
- Real-time video thresholding
- Edge detection accelerator
- AI-based image processing
- Integration with OpenCV
- Hardware acceleration for deep learning preprocessing
