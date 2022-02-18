# Comparison of Cortex-M Architectures

*Most information here taken from https://en.wikipedia.org/wiki/ARM_Cortex-M*

## M0

- **ARM Architecture Version**: ARMv6-M
- **Pipeline**: 3-Stage
- **Comp Arch**: von Neumann
- Optimised for physical silicon die size + cost
- Supports Thumb-1 and some of Thumb-2

## M0+

- **ARM Architecture Version**: ARMv6-M
- **Pipeline**: 2-Stage
- **Comp Arch**: von Neumann
- Superset of M0
- Optional MTB (micro trace buffer)
- Optional MPU (memory protection unit)

## M1

- **ARM Architecture Version**: ARMv6-M
- **Pipeline**: 3-Stage
- **Comp Arch**: von Neumann
- Optimized core especially designed to be loaded into FPGA chips.

## M3

- **ARM Architecture Version**: ARMv7-M
- **Pipeline**: 3-Stage + branch speculation
- **Comp Arch**: Harvard
- All Thumb instructions
- H/W divide
- Saturation arithmetic
- Optional MPU (memory protection unit)

## M4

- **ARM Architecture Version**: ARMv7E-M
- **Pipeline**: 3-Stage + branch speculation
- **Comp Arch**: Harvard
- Essentially M3 + DSP
- DSP: MAC + SIMD
- Optional FPU
- Optional MPU (memory protection unit)

## M7

- **ARM Architecture Version**: ARMv7E-M
- **Pipeline**: 6-Stage + branch speculation
- **Comp Arch**: Harvard
- High performance, ~2x efficiency of M4
- Superscaler
- 64-Bit Instruction + Data buses
