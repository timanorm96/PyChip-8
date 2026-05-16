# PyChip-8

A lightweight, hardware-accurate CHIP-8 emulator written in Python using the Pygame library. This project emulates the core architecture of the vintage 1970s interpretative programming language, providing a foundation for running retro arcade classics like Pong, Tetris, and Space Invaders.

## Features

- **Accurate CPU Cycle Emulation**: Implements the classic Fetch-Decode-Execute pipeline.
- **Memory & Register Mapping**: Mimics 4KB of RAM, 16 general-purpose 8-bit registers, and standard CHIP-8 font sets.
- **XOR Graphics**: Implements the original $64 \times 32$ monochrome display system using Pygame with customizable scaling.
- **Subroutine Stack**: Full support for nested calls and returns via an internal call stack.

## Architecture Overview

The emulator replicates the fundamental components of the CHIP-8 virtual computer:

* **Memory (RAM)**: 4096 bytes, where the first 512 bytes (`0x000`–`0x1FF`) are reserved for system fonts, and the program ROM is loaded at `0x200`.
* **Registers**: 16 8-bit data registers ($V0$ to $VF$), where $VF$ doubles as a carry/collision flag, alongside a 16-bit index register ($I$).
* **Timers**: 60Hz Delay and Sound timers for gameplay pacing and audio cues.

## Prerequisites

Make sure you have Python 3.x and Pygame installed on your machine.

```bash
pip install pygame

Getting Started

    Clone this repository to your local machine:
    Bash

    git clone [https://github.com/yourusername/PyChip-8.git](https://github.com/yourusername/PyChip-8.git)
    cd PyChip-8

    Run the emulator by passing the path to a CHIP-8 ROM file as a command-line argument:
    Bash

    python chip8.py path/to/your/rom.ch8
