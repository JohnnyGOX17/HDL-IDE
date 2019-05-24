# HDL-IDE
Accumulation of tools, plugins &amp; configs to turn Vim into a IDE for HDL development

Heavily reliant on [GHDL](https://ghdl.readthedocs.io/en/latest/index.html)

## TODO:
- Create interface to GHDL that can do C cosimulation to provide stdin/stdout access to TBs or design -> go even farther for Ethernet based designs to be able to wrap design into C kernel module that can be accessed via Linux networking subsystem and other local or remote devices (soft-Eth devices)
- Create seperate Vim plugins for:
  + Waveform viewing for TBs (post-mortem like GTKWave or dynamic using signal output during run?) and type support for enumerated types (see `--wave=<out>` in GHDL docs) that can run in CLI (like UTF-8 output) unlike GTKWave and run in Vi split?
  + Full Design Heirarchy Viewer/Browser (see GHDL output of `--disp-tree`), maybe ctag integration?
  + RegMap auto creation/update?
  + Completion/reference checking plugin for YCM & snippets (like how C/C++ operates) to much more easily integrate changes in interfaces
  + Auto testbench generation
- Integrate other FOSS Vim plugins to overall tooling such as:
  + TODO parser
  + Header/license checker
  + Vim ALE checker
  + Snippets for VHDL/verilog completion
  + Other major vi plugins
