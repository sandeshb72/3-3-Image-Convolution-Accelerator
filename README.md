# 🖥️ 3×3 Fixed-Point Convolution Accelerator in Verilog

A hardware implementation of a **3×3 Convolution Filter** using **Verilog HDL**. The design performs convolution on grayscale images using **Q8.8 fixed-point arithmetic**, making it suitable for FPGA-based image processing and digital logic design projects.

---

## 📌 Features

- 3×3 convolution operation
- Q8.8 fixed-point arithmetic
- Parameterized image size (up to 8×8)
- Modular architecture
- Multiply-Accumulate (MAC) implementation
- Fully synthesizable Verilog code
- Testbench for functional verification

---

## 📂 Project Structure

```text
DLD_Project-main/
│── conv3x3.v
│── mac_3x3.v
│── fxp_mult.v
│── fxp_add.v
│── tb_conv3x3.v
```

---

## 🏗️ Architecture

- **conv3x3.v** – Controls the convolution process and extracts 3×3 windows.
- **mac_3x3.v** – Performs multiply-accumulate operations.
- **fxp_mult.v** – Signed Q8.8 fixed-point multiplier.
- **fxp_add.v** – Signed Q8.8 fixed-point adder.
- **tb_conv3x3.v** – Testbench for simulation and verification.

---

## ⚙️ Fixed-Point Format

This project uses **Q8.8 Fixed-Point Representation**.

- Total bits: **16**
- Integer bits: **8**
- Fractional bits: **8**

| Decimal | Q8.8 |
|---------:|------:|
| 1.0 | 0x0100 |
| 0.5 | 0x0080 |
| -1.0 | 0xFF00 |

---

## 🚀 Simulation

Compile:

```bash
iverilog -o conv_test tb_conv3x3.v conv3x3.v mac_3x3.v fxp_mult.v fxp_add.v
```

Run:

```bash
vvp conv_test
```

View waveform:

```bash
gtkwave wave.vcd
```

---

## 🛠️ Applications

- FPGA Image Processing
- CNN Hardware Acceleration
- Digital Signal Processing
- Edge Detection
- Computer Vision Hardware

---

## 📚 Concepts Used

- Verilog HDL
- Digital Logic Design
- Fixed-Point Arithmetic
- Multiply-Accumulate (MAC)
- Image Convolution

---

## 🎯 Future Improvements

- Support 5×5 and 7×7 kernels
- Streaming image interface
- Pipelined MAC architecture
- FPGA implementation
- RGB image support

---

## 👨‍💻 Author

**Sandesh Bairagi**

B.Tech Computer Science and Engineering  
Indian Institute of Technology Ropar

---

## 📄 License

This project is intended for educational and academic purposes.
