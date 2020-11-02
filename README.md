## Dependencies

- Compiler: [GNU ARM Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)
- SDK: [Texas Instruments MSP432 SDK](https://www.ti.com/tool/download/SIMPLELINK-MSP432-SDK)
- [OpenOCD](http://openocd.org/)

## Setup

- Install the compiler, SDK and the latest commit of OpenOCD for debugging
  - `brew install armmbed/formulae/arm-none-eabi-gcc`
  - `brew install openocd --HEAD`
  
      You may also need to install openocd dependencies: autoconf, automake and texinfo  
  
- Export `GCC_ARMCOMPILER` and `ARM_SDK_HOME` environment variables pointing to the compiler and SDK homes, respectively

## Getting Started

```sh
> git clone git@github.com:caiotavares/arm-first-steps.git
> cd arm-first-steps
> make
> openocd -f board/ti_msp432_launchpad.cfg
```

In another terminal:

```sh
> arm-none-eabi-gdb
> (gdb) target remote :3333
> (gdb) load ./out/hello_world.out
> (gdb) continue
```
