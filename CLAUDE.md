# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

GitHub repository: https://github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa

## Project overview

This project is a from-scratch hardware module inspired by [BruceButBetter](https://github.com/Yoursel71/BruceButBetter), a downstream fork of the Bruce firmware built for a hand-built ESP32-S3 Flipper-Zero-like multitool. Louis Havet-Quillivic and Joachim Willner are designing their own PCB rather than replicating the reference design, choosing their own subset of modules (CC1101 sub-GHz, PN532 NFC/RFID, dual NRF24 2.4 GHz radios, Si5351 signal generator, IR transceiver, microSD, buzzer, OLED display).

The repository currently contains only project structure and documentation — no schematic, PCB, or firmware exists yet.

## Development environment

Development does not happen on the local machine. Instead, a PC running Proxmox hosts several Linux VMs: one of them is the actual development environment, and its installed tools are kept under version control. Louis and Joachim connect to that VM via VS Code Remote and use Claude Code there. A separate Linux VM runs Hermes to support development.

## Repository structure

- `docs/` — project documentation, including the initial project description
- `hardware/` — KiCad schematic/PCB files (not yet started)
- `firmware/` — firmware notes / fork of the Bruce firmware (not yet started)
- `notes/` — research notes and sources

All of these directories are currently empty except `docs/`. There are no build, lint, or test commands yet since no hardware or firmware design exists. When work begins in `hardware/` (KiCad) or `firmware/`, update this file with the relevant commands and architecture notes for that subsystem.
