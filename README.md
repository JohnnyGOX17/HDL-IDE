# HDL-IDE

Accumulation of tools, plugins &amp; configs to turn Vim into a IDE for HDL development

Heavily reliant on [GHDL](https://ghdl.readthedocs.io/en/latest/index.html)

## TODO:
- Create interface to GHDL that can do C cosimulation to provide stdin/stdout access to TBs or design -> go even farther for Ethernet based designs to be able to wrap design into C kernel module that can be accessed via Linux networking subsystem and other local or remote devices (soft-Eth devices)
- Create seperate Vim plugins for:
  + Waveform viewing for TBs (post-mortem like GTKWave or dynamic using signal output during run?) and type support for enumerated types (see `--wave=<out>` in GHDL docs) that can run in CLI (like UTF-8 output) unlike GTKWave and run in Vi split?
  + Full Design Heirarchy Viewer/Browser (see GHDL output of `--disp-tree`), maybe ctag integration?
  + RegMap auto creation/update?
    - Look into integrating with [Kactus2](http://funbase.cs.tut.fi/) and https://github.com/olofk/ipyxact
  + Completion/reference checking plugin for YCM & snippets (like how C/C++ operates) to much more easily integrate changes in interfaces
    - LSP using GHDL, kind of like what [vim-hdl](https://github.com/suoto/vim-hdl) was starting to do?
  + Auto testbench generation
- Integrate other FOSS Vim plugins to overall tooling such as:
  + TODO parser
  + Header/license checker
  + Vim ALE checker
  + Snippets for VHDL/verilog completion
  + Other major vi plugins
  + HDL linting/code formatting to prettier -> https://github.com/prettier/prettier
- Document setup and how to use integrated flow
  + ALE + GHDL
  + ctags to jump between definitions/entities easily
