     MicroPython - Python for microcontrollers           

 [![](./MicroPython - Python for microcontrollers_files/Mlogo_138wh.png)MicroPython](http://micropython.org/) Toggle navigation

*   [DOWNLOAD](https://micropython.org/download)
*   [DOCS](https://docs.micropython.org/)
*   [DISCORD](https://micropython.org/discord)
*   [DISCUSSIONS](https://github.com/orgs/micropython/discussions)
*   [WIKI](https://github.com/micropython/micropython/wiki)
*   [STORE](https://store.micropython.org/)

MicroPython
===========

<div style="background-color:rgba(0, 0, 0, 0.0470588); text-align:center; vertical-align: middle; padding:40px 0;">
<a href="/donate">DONATE</a>
</div>

MicroPython is a lean and efficient implementation of the [Python 3](http://www.python.org/) programming language that includes a small subset of the Python standard library and is optimised to run on microcontrollers and in constrained environments.

The MicroPython [pyboard](https://micropython.org/pyboard) is a compact electronic circuit board that runs MicroPython on the bare metal, giving you a low-level Python operating system that can be used to control all kinds of electronic projects.

MicroPython is packed full of advanced features such as an interactive prompt, arbitrary precision integers, closures, list comprehension, generators, exception handling and more. Yet it is compact enough to fit and run within just 256k of code space and 16k of RAM.

MicroPython aims to be as compatible with normal Python as possible to allow you to transfer code with ease from the desktop to a microcontroller or embedded system.

[TEST DRIVE A PYBOARD](http://micropython.org/live) [BUY A PYBOARD](https://store.micropython.org/) [USE MICROPYTHON ONLINE](https://micropython.org/unicorn)

Proper Python with hardware-specific modules
============================================

MicroPython is a full Python compiler and runtime that runs on the bare-metal. You get an interactive prompt (the REPL) to execute commands immediately, along with the ability to run and import scripts from the built-in filesystem. The REPL has history, tab completion, auto-indent and paste mode for a great user experience.

MicroPython strives to be as compatible as possible with normal Python (known as CPython) so that if you know Python you already know MicroPython. On the other hand, the more you learn about MicroPython the better you become at Python.

In addition to implementing a selection of core Python libraries, MicroPython includes modules such as "machine" for accessing low-level hardware.

import pyb

\# turn on an LED
pyb.LED(1).on()

\# print some text to the serial console
print('Hello MicroPython!')

←

Example 1 / 7

→

The pyboard
===========

[![pyboard v1.1](./MicroPython - Python for microcontrollers_files/pybv11-persp.jpg)](https://micropython.org/static/pyboard)

The pyboard is the official MicroPython microcontroller board with full support for software features. The hardware has:

*   STM32F405RG microcontroller
*   168 MHz Cortex M4 CPU with hardware floating point
*   1024KiB flash ROM and 192KiB RAM
*   Micro USB connector for power and serial communication
*   Micro SD card slot, supporting standard and high capacity SD cards
*   3-axis accelerometer (MMA7660)
*   Real time clock with optional battery backup
*   24 GPIO on left and right edges and 5 GPIO on bottom row, plus LED and switch GPIO available on bottom row
*   3x 12-bit analog to digital converters, available on 16 pins, 4 with analog ground shielding
*   2x 12-bit digital to analog (DAC) converters, available on pins X5 and X6
*   4 LEDs (red, green, yellow and blue)
*   1 reset and 1 user switch
*   On-board 3.3V LDO voltage regulator, capable of supplying up to 250mA, input voltage range 3.6V to 16V
*   DFU bootloader in ROM for easy upgrading of firmware

[Visit the store to order!](https://store.micropython.org/)

[![pyboard quick reference](./MicroPython - Python for microcontrollers_files/pybv10b-pinout.jpg)](http://docs.micropython.org/en/latest/pyboard/quickref.html)

Watch MicroPython in action
===========================

Completely free, open source software
=====================================

![MicroPython is open-source](./MicroPython - Python for microcontrollers_files/opensource.jpg)

MicroPython is written in C99 and the entire MicroPython core is available for general use under the very liberal [MIT license](https://github.com/micropython/micropython/blob/master/LICENSE). Most libraries and extension modules (some of which are from a third party) are also available under MIT or similar licenses.

You can freely use and adapt MicroPython for personal use, in education, and in commercial products.

MicroPython is developed in the open on GitHub and the source code is available at [the GitHub page](https://github.com/micropython/micropython), and on the [download page](https://micropython.org/download). Everyone is welcome to contribute to the project.

Code: state-of-the-art and highly robust
========================================

MicroPython employs many advanced coding techniques, and lots of tricks to maintain a compact size while still having a full set of features.

Some of the more notable items are:

*   highly configurable due to many compile-time configuration options
*   support for many architectures (x86, x86-64, ARM, ARM Thumb, Xtensa)
*   extensive [test suite](https://github.com/micropython/micropython/tree/master/tests) with over 590 tests, and more than 18,500 individual testcases
*   [code coverage](https://micropython.org/resources/code-coverage/) at 99.2% for the core and at 98.5% for the core plus extended modules
*   fast start-up time from boot to loading of first script (150 microseconds to get to boot.py, on PYBv1.1 running at 168MHz)
*   a simple, fast and robust mark-sweep garbage collector for heap memory
*   a MemoryError exception is raised if the heap is exhausted
*   a RuntimeError exception is raised if the stack limit is reached
*   support for running Python code on a hard interrupt with minimal latency
*   errors have a backtrace and report the line number of the source code
*   constant folding in the parser/compiler
*   [pointer tagging](https://github.com/micropython/micropython/blob/master/py/mpconfig.h#L93-L147) to fit small integers, strings and objects in a machine word
*   transparent transition from small integers to big integers
*   support for 64-bit NaN boxing object model
*   support for 30-bit stuffed floats, which don't require heap memory
*   a cross-compiler and frozen bytecode, to have pre-compiled scripts that don't take any RAM (except for any dynamic objects they create)
*   multithreading via the "\_thread" module, with an optional global-interpreter-lock (still work in progress, only available on selected ports)
*   a native emitter that targets machine code directly rather than the bytecode virtual machine
*   inline assembler (currently Thumb and Xtensa instruction sets only)

Online resources
================

You can learn more about MicroPython and keep up-to-date with developments via the following resources:

*   subscribe to [the newsletter](https://micropython.org/newsletter)
*   read [the documentation](http://docs.micropython.org/)
*   join the community at [the forum](http://forum.micropython.org/)
*   submit bug reports, and follow and join in development [on GitHub](https://github.com/micropython/micropython)

[![pyboards on parade](./MicroPython - Python for microcontrollers_files/colourhousings.jpg)](https://store.micropython.org/#/products/HOUSING-OB-1)

[Take me to the store!](https://store.micropython.org/)

### MicroPython

*   [Home](https://micropython.org/)
*   [Discord](https://micropython.org/discord)
*   [Discussions](https://github.com/orgs/micropython/discussions)
*   [Wiki](https://github.com/micropython/micropython/wiki)
*   [GitHub](https://www.github.com/micropython)

### Resources

*   [Tutorials](http://docs.micropython.org/en/latest/pyboard/tutorial/index.html)
*   [Documentation](http://docs.micropython.org/)
*   [Download](https://micropython.org/download)

### Contact

*   [Contact us](https://micropython.org/contact)
*   [IRC](irc://freenode/micropython)
*   [Twitter](http://twitter.com/micropython)
*   [Facebook](http://www.facebook.com/micropython)
*   [Privacy Policy](https://micropython.org/privacypolicy)
*   [Terms & Conditions](https://micropython.org/termsandconditions)

A project by [Damien George](http://dpgeorge.net/)

© 2014-2023 George Robotics Limited
