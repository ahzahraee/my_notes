CMSIS core
**device.h**
- provided by the device manufacturer (*e.g. stm32u5g9xx.h*) for access to device peripherals
- interrupt numbers
- some compiler specific definitions (*#if defined (__ICCARM__)
  #pragma language=extended*)
- processor and core related definitions (*e.g.  #define __FPU_PRESENT             1U        /* FPU present */*)
- device specific peripheral related definitions and address map
**startup_device.s**
- provided by the device manufacturer (*e.g. startup_stm32u5g9xx.s*) for device startup
- specific to the compiler
- refers to variables defined in the linker script
- implements the NVIC interrupt vector
- every ISR is implemented as a weak function and can be reimplemented in the application
**system_device.c**

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTkwODAzMTAzMV19
-->