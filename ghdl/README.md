# GHDL Open-Source Simulator by Tristan Gingold

* [Getting Started With VHDL on Windows (GHDL & GTKWave)](https://www.youtube.com/watch?v=H2GyAIYwZbw) by Nerdy Dave

* [Getting Started With VHDL on Linux (GHDL & GTKWave)](https://www.youtube.com/watch?v=dvLeDNbXfFw) by Nerdy Dave

* [Download GHDL](https://github.com/ghdl/ghdl/releases)

* [Download GTKWave](https://sourceforge.net/projects/gtkwave/files)

* Extract Zip files, edit Environment Variables | Path

* For macOS
```sh
$ cd Downloads
$ mv ghdl-0.37-macosx-mcode /usr/local
$ cd
$ PATH=$PATH\:/usr/local/ghdl-0.37-macosx-mcode/bin ; export PATH
$ echo $PATH
... :/usr/local/ghdl-0.37-macosx-mcode/bin: ...
```

## [Hello, World](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program)

* [GHDL Quick Start Guide](https://ghdl.readthedocs.io/en/latest/using/QuickStartGuide.html)

* Clone 'dsd' repository, make and change directory to a new 'vhdl' directory, copy vhdl code to the current directory '.'
```sh
$ git clone https://github.com/kevinwlu/dsd.git
$ mkdir vhdl
$ cd vhdl
$ cp ~/dsd/hello.vhdl .
```
* GHDL options: help, version, analyze, elaborate, run
```sh
$ ghdl -h
$ ghdl -v
$ ghdl -a hello.vhdl
$ ghdl -e hello_world
$ ghdl -r hello_world
```
## [Adder](https://en.wikipedia.org/wiki/Adder_(electronics))

### Half Adder
```sh
$ cp ~/dsd/ha.vhdl .
$ cp ~/dsd/ha_tb.vhdl .
$ ghdl -a ha.vhdl
$ ghdl -a ha_tb.vhdl
$ ghdl -e ha_tb
$ ghdl -r ha_tb --vcd=ha.vcd
```
### [Full Adder](http://ghdl.free.fr/ghdl/A-full-adder.html)
```sh
$ cp ~/dsd/adder.vhdl .
$ cp ~/dsd/adder_tb.vhdl .
$ ghdl -a adder.vhdl
$ ghdl -a adder_tb.vhdl
$ ghdl -e adder_tb
$ ghdl -r adder_tb --vcd=adder.vcd
```
## [Flip-flop](https://en.wikipedia.org/wiki/Flip-flop_(electronics))

### [D Flip-flop](https://electronicstopper.blogspot.com/2017/07/d-flip-flop-in-vhdl-with-testbench.html)
```sh
$ cp ~/dsd/dff.vhdl .
$ cp ~/dsd/dff_tb.vhdl .
$ ghdl -a dff.vhdl
$ ghdl -a dff_tb.vhdl
$ ghdl -e dff_tb
$ ghdl -r dff_tb --vcd=adder.vcd
```
### [T Flip-flop](https://electronicstopper.blogspot.com/2017/07/t-flip-flop-in-vhdl-with-testbench.html)
```sh
$ cp ~/dsd/tff.vhdl .
$ cp ~/dsd/tff_tb.vhdl .
$ ghdl -a tff.vhdl
$ ghdl -a tff_tb.vhdl
$ ghdl -e tff_tb
$ ghdl -r tff_tb --vcd=adder.vcd
```
## [Multiplexer](https://en.wikipedia.org/wiki/Multiplexer)

### [4-to-1 Multiplexer](https://allaboutfpga.com/vhdl-4-to-1-mux-multiplexer)
```sh
$ cp ~/dsd/mux.vhdl .
$ cp ~/dsd/mux_tb.vhdl .
$ ghdl -a mux.vhdl
$ ghdl -a mux_tb.vhdl
$ ghdl -e mux_tb
$ ghdl -r mux_tb --vcd=adder.vcd
```
### [1-to-4 Demultiplexer](https://allaboutfpga.com/vhdl-code-for-1-to-4-demux)
```sh
$ cp ~/dsd/demux.vhdl .
$ cp ~/dsd/demux_tb.vhdl .
$ ghdl -a demux.vhdl
$ ghdl -a demux_tb.vhdl
$ ghdl -e demux_tb
$ ghdl -r demux_tb --vcd=adder.vcd
```
## Wave Viewer: GTKWave Based on [GTK](https://en.wikipedia.org/wiki/GTK)

[Download latest version](https://sourceforge.net/projects/gtkwave/files/)

GTKWave > File > Open New Tab > vhdl >

ha.vcd

adder.vcd

dff.vcd

tff.vcd

mux.vcd

demux.vcd