# Youssef Abdelmesih

Electrical Engineering student at **UMass Amherst** (Class of 2029), interested in FPGA design, embedded systems, and navigation and control hardware. Currently building a real-time IMU attitude estimator on a Xilinx Artix-7 FPGA (Alchitry Au).

[LinkedIn](https://www.linkedin.com/in/youssef-abdelmesih-848a5738a) · [Email](mailto:yabdelmesih@umass.edu)

---

## Featured Projects

### [FPGA IMU Attitude Estimator](https://github.com/yabdelmesih-ops/imu-attitude-fpga)
A real-time FPGA attitude estimator that reads an inertial measurement unit over SPI and computes roll and pitch 1,000 times per second, the core function behind stabilization and navigation in aircraft.

**Stack:** SystemVerilog · Python · Icarus Verilog · Xilinx Artix-7 (Alchitry Au)

- Fuses accelerometer and gyroscope data with a **complementary filter** in **fixed-point hardware**, with on-chip gyro bias calibration
- Computes tilt with a time-shared **CORDIC** unit (shifts and adds, no multipliers), 0.40 µs latency per sample at 100 MHz
- Verified **bit-exact** against a Python reference model with 4 self-checking testbenches covering 28,000+ test cases
- Full-system test drives the design from a simulated IMU and checks every SPI command and UART data packet
- 0.12° RMS roll error in simulation, versus 1.17° from the accelerometer alone and 16.4° from the gyroscope alone
- **Validated on hardware:** 20,000/20,000 samples bit-exact on a Xilinx Artix-7 through hardware-in-the-loop testing; timing met at 100 MHz (WNS +1.163 ns). Live-sensor bring-up in progress

[Source](https://github.com/yabdelmesih-ops/imu-attitude-fpga)

---

### [CircuitScope](https://github.com/yabdelmesih-ops/circuitscope)
An interactive DC circuit solver: draw a schematic in the browser, solve it with Modified Nodal Analysis, and see why every node has its voltage.

**Stack:** Python · NumPy · Streamlit · JavaScript/SVG

- Solves DC circuits using **Modified Nodal Analysis (MNA)**
- Computes **Thévenin and Norton equivalents** between any two nodes
- Step-by-step **Circuits I methods** on your own drawing: supernodes, superposition, source transformations, voltage dividers, summing amplifiers
- Models **ideal op amps** in negative-feedback and open-loop comparator modes
- Drag-and-drop schematic editor with click-to-explain KCL lessons and current arrows
- Validated against **ngspice** across 29 configurations (293 comparisons) and against hand calculations
- SPICE netlist export and an end-to-end browser test suite that caught and fixed interface bugs

[Source](https://github.com/yabdelmesih-ops/circuitscope)

---

## Technical Skills

**Languages:** Python · Verilog · SystemVerilog · MATLAB

**Tools & Libraries:** Vivado · Icarus Verilog · NumPy · Streamlit · LTspice · Git

**Hardware:** Xilinx Artix-7 FPGA (Alchitry Au)

---

## Interests
Digital Design · FPGA Development · Embedded Systems · Circuit Analysis Software · Python Engineering Tools
