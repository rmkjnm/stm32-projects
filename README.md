# stm32-projects
My STM32 Nucleo projects
first project 
# BlinkLED - STM32L433 Project

This project is for blinking an LED using the STM32L433 microcontroller, created using STM32CubeIDE.

## Folder Structure

- `Core/` – Contains application code (main.c, stm32xx_it.c, etc.)
- `Drivers/` – CMSIS and HAL driver files
- `blink-led/Blinkled.ioc` – STM32CubeMX configuration file
- `STM32L433RCTXP_FLASH.ld` – Linker script

## Build Instructions

1. Open STM32CubeIDE.
2. Import the project using `File > Open Projects from File System`.
3. Select the `blink-led` folder.
4. Build the project (`Project > Build All`).
5. Flash it to your STM32 board (`Run > Debug`).

## Notes

- This project excludes the `Debug/` directory from version control.
- Make sure to regenerate code if `.ioc` is updated.


blink led for 1s
here we can change our time set for led to blink 
in this board ld4 is user contolled PB13 is the pin for control gpiooutput

