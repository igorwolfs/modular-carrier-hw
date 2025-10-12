# FPGA Choice
In our board we would want an FPGA, which connects to the CPU-board.

This should handle any high-speed data incoming from analog front-ends or sensors, and repackage them into a format the CPU or other peripherals on the main-board in a way the CPU can handle.

On top of that it can provide the necessary debug info, communicate over a FIFO2USB2.0-IC.

## Main requiremenets
### Multiplier
- Optional, not explicitly necessary unless we'll go with some heavy data-processing

### LUT's
- Enough to do some simple repackaging of data, and perhaps sample-dropping or filtering
- Enough to form a FiFo interface with the USB2.0 IC, and send data to this IC 
	- Coming from a parallel bus connection connected to the CPU-board
	- Coming from the ADC bus

### Clock speed
- Should have a clock speed that can handle 60 MHz of 10-bit data coming through

### Programmable
- Should be programmable and configurable with free tools

### IO's
- More than 100 IO's
	- 11 per ADC (22)
	- 20 for the USB parallel data bus
	- 16 for the fifo

### Flash
Good to have but not rquired, we'll try making sure to have an external flash somewhere else anyways.

## FPGA Choices
### FPGA 1: LCMXO2-4000HC-4TG144C
- TQFP144 package
#### LUT's
Has enough LUT's to repackage data

#### Multipliers
- No multiplier

#### Clock speed
- 2 edge-clocks for high-speed IO interfaces


#### Programmable
- Over serial SPI / JTAG / I2C
	- Even I2C (amazing)
- It even has on-chip flash memory

### IO's
- 144 IO's (114 usable pins)

### Internal flash
- 256 kbits

# MachXO2-4000

## Symbol + footprint check



# Examples
## Reddit
- https://www.reddit.com/r/PrintedCircuitBoard/comments/1f73iwi/review_request_lattice_machxo2_system_on_module/

