# 🥕 `garduino/embedded`

An embedded rust app powering garden automation. This package targets an **Arduino R4 + Wifi**, an ARM Cortex-M microcontroller.

This project was boostrapped using the [cortex-m-quickstart](https://github.com/rust-embedded/cortex-m-quickstart).

## Stack
 - [cortex-m](https://docs.rs/cortex-m/latest/cortex_m/) for core register definitions and peripheral access.
 - [cortex-m-rt](https://docs.rs/cortex-m-rt/latest/cortex_m_rt/) for initialisation.
 - [panic-halt](https://docs.rs/panic-halt/latest/panic_halt/) for customizing panic behavior in an embedded environment.

## Quickstart

### First-Time Setup
```bash
# Grab the beta toolchain
rustup default beta

# Grab the chip's build target
rustup target add thumbv7em-none-eabihf
```

### Building
```bash
cargo build
```

## Background

The UNO R4 contains an R7FA4M1AB3CFM#AA0 processor, or in short, an RA4M1. This is an ARM Cortex M4 that will run at up to 64 MHz, with 256 kB of flash and 32 kB SRAM. The instruction set is ARMv7-M Thumb and it includes hardware floating point, which will be orders of magnitude faster than doing floating point math on the Uno R3.

## Process & Procedure

### Flashing

*WIP*

## Resources

Check out:
 - [The Embedded Rust Book](https://rust-embedded.github.io/book).

## TODO
- [] Enter memory region information into the `memory.x` file.

``` console
$ cat memory.x
/* Linker script for the STM32F303VCT6 */
MEMORY
{
  /* NOTE 1 K = 1 KiBi = 1024 bytes */
  FLASH : ORIGIN = 0x08000000, LENGTH = 256K
  RAM : ORIGIN = 0x20000000, LENGTH = 40K
}
```

