# Verilog Notes
Notes r.e learning Verilog

--------------------------------------------------------------------------------------------

## How to run a testbench using iverilog/VVP

#### Compile testbench

$ iverilog -o <test_bench_name>.vpp test_component_x.v  

#### Run testbench
$ vvp <test_bench_name>.vpp  

#### Add VCD waveform output to testbench file (.v)
```initial
 begin
    $dumpfile("waveform_output.vcd");
    $dumpvars(0, <wire/reg to capture>);
 end
```

#### View testbench
vvp <test_bench_name>.vvp -lxt2  
gtkwave dump.lxt  

--------------------------------------------------------------------------------------------

## Some simulation commands:

$finish - exits the simulation and gives control back to the operating system.
$stop - suspends the simulation and puts a simulator in an interactive mode.
