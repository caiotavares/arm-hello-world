## Dependencies

- Compiler: [GNU ARM Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)
- SDK: [Texas Instruments MSP432 SDK](https://www.ti.com/tool/download/SIMPLELINK-MSP432-SDK)
- Burner: [Uniflash](https://www.ti.com/tool/download/UNIFLASH)

## Setup

- Install the compiler, SDK and OpenOCD for debugging
  - `brew install armmbed/formulae/arm-none-eabi-gcc`
  - `brew install openocd`
- Export `GCC_ARM_HOME` and `ARM_SDK_HOME` environment variables pointing to the compiler and SDK homes, respectively
- Install the flash burner `Uniflash` and setup the burn settings for the board, go to `Standalone Command line tool` and export a binary with the selected configurations.
- Export `ARM_BURNER` environment variable with the exported binary above

## Getting Started

```sh
> git clone git@github.com:caiotavares/arm-first-steps.git
> cd arm-first-steps
> make
> ./burn ./out/hello_world.out
```

## Example Summary

This demo software demonstrates a basic blink LED example on the MSP-EXP432P401R LaunchPad development kit.

## Example Usage

Upon running the demo, the device toggles LED1 on the LaunchPad

## Application Design Details

* No-RTOS
  * Clock System is left with default setting, MCLK = 3 MHz.

