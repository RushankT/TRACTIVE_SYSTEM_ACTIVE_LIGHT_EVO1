# TRACTIVE_SYSTEM_ACTIVE_LIGHT_EVO1

## Overview

This repository contains the finalized KiCad schematic design for the **Tractive System Active Light (TSAL)** circuit, developed for our Formula Student Electric Vehicle project. The TSAL is a critical safety component used to indicate the presence of high voltage in the tractive system when the vehicle is powered on.

## Project Details

- **Project Name**: TSAL Final Design
- **Team**: Zuura Formula Racing
- **Engineer**: Rushank Talwar, EV Powertrain Lead
- **Tool Used**: KiCad (Recommended version: 6.x or newer)
- **Date**: July 2025

## Functionality

The TSAL circuit complies with Formula Student Electric rules and includes:
- A high-brightness red LED indicator visible from 3 meters.
- Blinking at ≥ 1 Hz when TS voltage > 60 VDC.
- Automatic turn-off when TS voltage < 60 VDC.
- Isolation and safety using optocouplers and fail-safe design.
- Powered by a reliable low-voltage source (e.g., 12V DC).

## File Structure

- `TSAL_final.kicad_sch`: Main schematic file for the TSAL circuit.
- (Optional) Future files: `TSAL_final.kicad_pcb`, BOM, gerber files.

## How to Use

1. **Open Schematic**:  
   Use [KiCad](https://www.kicad.org/) to open the `.kicad_sch` file.
