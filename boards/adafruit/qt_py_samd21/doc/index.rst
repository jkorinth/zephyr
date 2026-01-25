.. zephyr:board:: adafruit_qt_py_samd21

Overview
********

The Adafruit QT Py SAMD21 is a small, low-cost, versatile board from
Adafruit. It is equipped with an SAMD21 SoC, an on-board RGB Neopixel,
a USB connector, and a STEMMA QT connector. The USB bootloader allows
it to be flashed without any adapter, in a drag-and-drop manner.
Like the other variants of the series it features a header compatible
with Seeed XIAO boards.

Hardware
********
- Single Arm Cortex-M0+ processor running up to 48Mhz
- 32KB on-chip SRAM and 256KB Flash
- 11 GPIO pins
- 9 Analog inputs (12b)
- 1 Analog output, 10b audio
- 1 AREF (optional)
- 4 SERCOM peripherals (UART, SPI, I2C, I2S)
- 9 PWM channels
- USB 2.0 controller (host/device, 12Mbps)
- 13 Programmable I/O (PIO) for custom peripherals
- On-board RGB LED
- 1 Watchdog timer peripheral
- Optional 8-SOIC flash chip

Supported Features
==================

.. zephyr:board-supported-hw::

Pin Mapping
===========

The peripherals of the SAMD21 SoC can be routed to various pins on the board.
The configuration of these routes can be modified through DTS. Please refer to
the datasheet to see the possible routings for each peripheral.

Default Zephyr Peripheral Mapping:
----------------------------------

.. rst-class:: rst-columns

- UART1_TX : PA6
- UART1_RX : PA7
- I2C_SDA : PA16
- I2C_SCL : PA17
- SPI_MISO : PA9
- SPI_MOSI : PA10
- SPI_SCK : PA11

Programming and Debugging
*************************

.. zephyr:board-supported-runners::

Flashing
========

Using UF2
---------

Since it doesn't expose the SWD pins, you must flash the Adafruit QT Py SAMD21 with
a UF2 file. By default, building an app for this board will generate a
:file:`build/zephyr/zephyr.uf2` file. If the QT Py SAMD21 reset by double-click on
the ``RST`` button, it will appear on the host as a mass storage device. The UF2
file should be drag-and-dropped to the device, which will flash the QT Py SAMD21.

.. target-notes::

.. _Getting Started with Raspberry Pi Pico:
  https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-42254-Getting-Started-with-Sam-D21_AP-Note_AT06466.pdf

.. _Primary Guide\: Adafruit QT Py SAMD21:
  https://learn.adafruit.com/adafruit-qt-py
