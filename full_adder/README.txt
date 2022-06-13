To compile and simulate with GHDL manually do the following:
ghdl -a full_adder.vhd
ghdl -a full_adder_testbench.vhd
ghdl -e full_adder_testbench
ghdl -r full_adder_testbench --vcd=full_adder_testbench.vcd

To visually view the waveforms use GtkWave:
gtkwave full_adder_testbench.vcd

Or just run the makefile bxy running:
make
