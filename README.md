## Dune - microcontroller HAL done right

### What is it?

It's always a good idea to hide hardware details like access to registers or sending bytes over bus into a nice high-level API like gpio_set, uart_send and so on. Unfortunately projects aim to achieve that goal (STM32Cube HAL, Arduino, you name it) just fail drastically:

+ They usually adapted only to one specific MCU, like STM32 or AVR - api is either too much detailed, or not enough detailed;
+ They're bloated - and do a lot of checks in runtime that are not really required, and occupy kilobytes of ROM (and sometimes RAM!)
+ Drivers for other components like sensors or displays are usually not supported at all, and you have to rely on third party libraries.

So we exactly address those 3 problems.

### License

GPL for now.
