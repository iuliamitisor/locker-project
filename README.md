# Digital Locker System for Basys 3 FPGA

## Features
- **Button-controlled locker access**: Users interact with the locker system through a button interface.
- **Digilent keyboard input**: Users can enter an access code using a Digilent Pmod KYPD.
- **LED status indicators**: The system uses LEDs to indicate locker status.
- **State management**: Implements registers and counters to control access logic.
- **Modular design**: Built using multiple VHDL components for easy modification and expansion.

## Project Structure
- `top.vhd` - The top-level entity integrating all components.
- `SR_register.vhd` - Shift register used in the design.
- `counter_modulo_8.vhd` - A counter module for internal logic.
- `decoder.vhd` - Gathers input from the Digilent Pmod KYPD.
- `load_register.vhd` - A register for storing input values.
- `mpg.vhd` - Handles mechanical pulse generation.
- `ssd.vhd` - Seven-segment display driver to view code entered using the keypad.
- `Basys3_Master.xdc` - FPGA constraints file for Basys 3 board.

## Hardware Requirements
- **Digilent Basys 3 FPGA Board**
- **Digilent Pmod KYPD: 16-button Keypad**: For entering access codes
- **Software**: Xilinx Vivado (for synthesis and implementation)

## How to Use
1. Open the project in Xilinx Vivado.
2. Assign FPGA pins using `Basys3_Master.xdc`.
3. Synthesize, implement, and generate the bitstream.
4. Load the bitstream onto the Basys 3 FPGA.
5. Use the Digilent Pmod KYPD to enter the access code and control the locker system.
6. Observe the LED indicators for system status.
