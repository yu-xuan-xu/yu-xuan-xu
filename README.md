# Hi, I'm Yuxuan Xu

I'm studying electrical engineering at Washington University in St. Louis and expect to graduate in 2029. I work on FPGA design and verification, circuit boards, and hardware test.

## FPGA projects

### [FPGA Spectral Doppler Engine](https://github.com/yu-xuan-xu/fpga-spectral-doppler-engine)

August to October 2026

My cardiac flow research got me curious about how Doppler estimates are made in hardware. I used a shared FFT to fit a fixed point SystemVerilog design on the iCE40UP5K. The demo checks signed velocity estimates against a Python model. The AXI design adds atomic result snapshots, soft reset, and a sticky interrupt.

[Architecture](https://github.com/yu-xuan-xu/fpga-spectral-doppler-engine/blob/main/docs/doppler_data_path.svg) · [Run the simulation](https://github.com/yu-xuan-xu/fpga-spectral-doppler-engine#see-it-run)

### [SPI Readback Debugger](https://github.com/yu-xuan-xu/spi-readback-debugger)

October to November 2026

I built a read only SPI to APB bridge to see why a read could look successful and still return the old byte. The fix holds BUSY for the whole frame and gets the new byte on a retry. Wrong READY replies dropped to zero across 1,610 simulated timing cases. I used SymbiYosys to check when the bridge can deliver a response.

[Architecture](https://github.com/yu-xuan-xu/spi-readback-debugger/blob/main/docs/spi_apb_architecture.svg) · [Fault replay waveform](https://github.com/yu-xuan-xu/spi-readback-debugger/blob/main/docs/spi_fault_replay.png) · [Run the replay](https://github.com/yu-xuan-xu/spi-readback-debugger#see-it-run)

### [FPGA Rhythm Sequencer](https://github.com/yu-xuan-xu/fpga-rhythm-sequencer)

April to May 2026

I started this in my digital logic course because I wanted to edit a rhythm from buttons and see it on a display. The v2 RTL uses one clock and counts a press only after stable TM1638 scans. The hardware video shows the course prototype, and the v2 animation shows a bar played in simulation.

[Course prototype video](https://github.com/yu-xuan-xu/fpga-rhythm-sequencer/blob/main/demo/rhythm_hardware_demo.mp4) · [v2 simulation animation](https://github.com/yu-xuan-xu/fpga-rhythm-sequencer/blob/main/demo/rhythm_demo.gif)

## Work and research

* At Sino Telecom I wrote a reusable SystemVerilog SPI master model and used it to verify register access through a CPLD path to MDIO.
* On the WashU Robotics Drone Team I work on power distribution and designed the v0.3 flight controller PCB in KiCad.
* I develop Python and SCPI tests for CompactDAQ.
* For our cardiac flow reconstruction research, I built a differentiable Doppler operator in PyTorch that models what an ultrasound probe would measure from a 3D blood flow field. I evaluated it across different probe orientations.

## Contact

[LinkedIn](https://www.linkedin.com/in/xuyuxuan/) · [xyuxuan@wustl.edu](mailto:xyuxuan@wustl.edu)
