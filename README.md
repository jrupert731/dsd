# Digital System Design

* GHDL Quick Start Guide

https://ghdl.readthedocs.io/en/latest/using/QuickStartGuide.html

ghdl -a hello.vhdl

ghdl -e hello_world

ghdl -r hello_world

* Half Adder

ghdl -a ha.vhdl

ghdl -a ha_tb.vhdl

ghdl -e ha_tb

ghdl -r ha_tb

ghdl -r ha_tb --vcd=ha.vcd

gtkwave ha.vcd
