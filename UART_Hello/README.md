# UART_Hello - STM32L433 Nucleo-64

This project demonstrates basic UART (serial) communication on the STM32L433 Nucleo-64 board using STM32CubeIDE.

## 🧠 Objective

Transmit the message `"Hello from Manoj\n"` continuously over UART so it can be read by a terminal (like PuTTY or screen) on your PC.

## 📦 Project Structure

- `Core/`: Contains `main.c`, startup code, and HAL initialization.
- `Drivers/`: HAL and CMSIS drivers.
- `UART_Hello.ioc`: STM32CubeMX configuration file.
- `Debug/`: Build output directory.
- `STM32L433RCTXP_FLASH.ld`: Linker script.
- `UART_Hello Debug.launch`: Debug configuration for STM32CubeIDE.

## 🔌 UART Pin Mapping (LPUART1)

| Signal     | STM32 Pin | Nucleo Label | Connected To      |
|------------|-----------|--------------|-------------------|
| TX         | PA2       | ARD_D1       | ST-Link Virtual COM Port |
| RX         | PA3       | ARD_D0       | ST-Link Virtual COM Port |

Use `/dev/tty.usbmodem*` on macOS or `COMx` on Windows.

## 🛠️ Build & Flash Instructions

1. Open the project in **STM32CubeIDE**.
2. Build the project: **Project > Build Project**.
3. Connect your board via USB.
4. Flash: **Run > Debug**.

## 📟 Test the Output

- Open a terminal emulator:
  - macOS: `screen /dev/tty.usbmodemXXXX 115200`
  - Windows: PuTTY on the correct COM port at `115200 baud`

You should see:
 Hello from Manoj repeated
