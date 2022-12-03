# VSDHDP
VSDHDP

# Day 0
Checking yosys

![](Day0/yosys.PNG)

Checking ngspice

![](Day0/ngspice.PNG)

Checking sta

![](Day0/sta.PNG)

Checking iverilog

![](Day0/iverilog.PNG)

Checking gtkwave

![](Day0/gtkwave.PNG)

# Day 1 - Introduction to Verilog RTL design and Synthesis

Run iverilog and gtkwave on good_mux.v

![](Day1/good_mux.PNG)

Run yosys
```
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```

![](Day1/yosys1.PNG)

Read verilog file and run synth
```
yosys> read_verilog good_mux.v
yosys> synth -top good_mux
```

![](Day1/yosys2.PNG)

Run abc - generate the gate netlist

```
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show
```
Loos like libs contain cell mux

![](Day1/yosys3.PNG)


