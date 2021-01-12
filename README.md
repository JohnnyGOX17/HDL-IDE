# HDL-IDE

Accumulation of tools, plugins and configs to turn Vim into a IDE for HDL development and in general, make HDL development that much quicker and easier.

Heavily reliant on [GHDL](https://ghdl.readthedocs.io/en/latest/index.html)

## TODO:
- Overall design like https://github.com/TerosTechnology/vscode-terosHDL
- Create interface to GHDL that can do C cosimulation to provide stdin/stdout access to TBs or design -> go even farther for Ethernet based designs to be able to wrap design into C kernel module that can be accessed via Linux networking subsystem and other local or remote devices (soft-Eth devices)
- Create seperate Vim plugins for:
  + Waveform viewing for TBs (post-mortem like GTKWave or dynamic using signal output during run?) and type support for enumerated types (see `--wave=<out>` in GHDL docs) that can run in CLI (like UTF-8 output) unlike GTKWave and run in Vi split?
    * Look at using a Python TUI like https://github.com/mingrammer/python-curses-scroll-example which parses VCD files, displays UTF-8 symbols as signal values/transitions, and can have Vim keybindings for scolling/zooming:
      - https://github.com/yne/vcd
      - https://pypi.org/project/pyvcd/
      - https://pypi.org/project/vcdvcd/
      - https://pypi.org/project/pyDigitalWaveTools/
  + Full Design Heirarchy Viewer/Browser (see GHDL output of `--disp-tree`), maybe ctag integration?
  + RegMap auto creation/update?
    - Look into integrating with [Kactus2](http://funbase.cs.tut.fi/) and https://github.com/olofk/ipyxact for general IP-XACT interoperability
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
- Document setup and how to use integrated flow like already contributed parts:
  + ALE + GHDL
  + ctags to jump between definitions/entities easily
