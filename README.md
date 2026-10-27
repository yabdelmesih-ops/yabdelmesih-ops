# Youssef Abdelmesih

Electrical Engineering student at **UMass Amherst** (Class of 2029), interested in FPGA design, embedded systems, and navigation and control hardware. Currently building a real-time IMU attitude estimator on a Tang Nano 9K.

[LinkedIn](https://www.linkedin.com/in/youssef-abdelmesih-848a5738a) · [Email](mailto:yabdelmesih@umass.edu)

---

## Featured Projects

### [FPGA IMU Attitude Estimator](https://github.com/yabdelmesih-ops/imu-attitude-fpga)
A real-time FPGA attitude estimator that reads an inertial measurement unit over SPI and computes roll and pitch 1,000 times per second, the core function behind stabilization and navigation in aircraft.

**Stack:** SystemVerilog · Python · Icarus Verilog · Tang Nano 9K (Gowin FPGA)

- Fuses accelerometer and gyroscope data with a **complementary filter** in **fixed-point hardware**, with on-chip gyro bias calibration
- Computes tilt with a time-shared **CORDIC** unit (shifts and adds, no multipliers), 1.4 µs latency per sample
- Verified **bit-exact** against a Python reference model with 3 self-checking testbenches covering 25,000+ test cases
- Full-system test drives the design from a simulated IMU and checks every SPI command and UART data packet
- 0.12° RMS roll error in simulation, versus 1.17° from the accelerometer alone and 16.4° from the gyroscope alone
- Status: design and verification complete in simulation; hardware bring-up in progress

[Source](https://github.com/yabdelmesih-ops/imu-attitude-fpga)

---

### [CircuitScope](https://github.com/yabdelmesih-ops/circuitscope)
An interactive DC circuit solver: draw a schematic in the browser, solve it with Modified Nodal Analysis, and see why every node has its voltage.

**Stack:** Python · NumPy · Streamlit · JavaScript/SVG

- Solves DC circuits using **Modified Nodal Analysis (MNA)**
- Computes **Thévenin and Norton equivalents** between any two nodes
- Models **ideal op amps** in negative-feedback and open-loop comparator modes
- Drag-and-drop schematic editor with click-to-explain KCL lessons and current arrows
- Validated against **ngspice** across 29 configurations (293 comparisons) and against hand calculations
- SPICE netlist export, guided practice questions, and an end-to-end browser test suite

[Source](https://github.com/yabdelmesih-ops/circuitscope)

---

## Technical Skills

**Languages:** Python · Verilog · SystemVerilog · MATLAB
**Tools & Libraries:** NumPy · Streamlit · LTspice · Git

---

## Interests
Digital Design · FPGA Development · Embedded Systems · Circuit Analysis Software · Python Engineering Tools
