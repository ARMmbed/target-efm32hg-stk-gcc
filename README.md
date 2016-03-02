# Yotta build target for the EFM32 Happy Gecko SLSTK3400A Starter Kit using GCC

This is a yotta build target for the EFM32 Happy Gecko SLSTK3400A Starter Kit from
Silicon Labs. In order to use this target for your mbed OS applications, select
the target using `yotta target efm32hg-stk-gcc`.

This target defines several board-specific configuration parameters. If you have
built a custom board, you probably don't want to use this target, but rather
create your own target inheriting the Happy Gecko family target `efm32hg-gcc`.
Read more about inheriting targets in [the Yotta documentation](http://yottadocs.mbed.com/tutorial/targets.html#inheriting).

## Board-specific configuration

The `target.json` for this target contains several yotta configuration
parameters in the `/config` object. If you create your own target, you need to supply the
correct values for these parameters in your custom target.

- `/hardware/device` is a string describing the exact part number of the chip on this board
- `/hardware/flash-size` is an integer describing the flash size of the device in kB
- `/hardware/ram-size` is an integer describing the ram size of the device in kB
- `/hardware/clock` gives the oscillator configuration for this board
- `/hardware/pins` maps user-friendly pin names like `LED1` to GPIO pin names
- `/modules/serial/stdio-uart` defines which UART/USART/LEUART peripheral should be used for standard IO (the pins used are defined by `/hardware/pins/STDIO_UART_TX` and `/hardware/pins/STDIO_UART_RX`)
