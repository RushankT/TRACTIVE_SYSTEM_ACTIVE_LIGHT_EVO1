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
- Green Light Turns on when TS voltage < 60 VDC.
- Isolation and safety using optocouplers and fail-safe design.
- Powered by a reliable low-voltage source (e.g., 12V DC).

## File Structure

- `TSAL_final.kicad_sch`: Main schematic file for the TSAL circuit.
- (Optional) Future files: `TSAL_final.kicad_pcb`, BOM, gerber files.

## Relevant Rules

EV4.10 Tractive System Active Light

EV4.10.1 The vehicles must include a single TSAL that must indicate the TS status. The TSAL must
not perform any other functions. A TSAL with multiple LEDs in one housing is allowed.


EV4.10.2 The TSAL itself must have a red light, flashing continuously with a frequency between 2 Hz
and 5 Hz and a duty cycle of 50%, active if and only if the LVS is active and the voltage
across any DC-link capacitor exceeds
• 60VDC or 50VACRMS
• Half the nominal TS voltage
whichever is lower.


EV4.10.3 The TSAL itself must have a green light, continuously on, active if and only if the LVS is
active and ALL of the following conditions are true:
• All AIRs are opened.
• The pre-charge relay, see EV5.7.2, is opened.
• The voltage at the vehicle side of the AIRs inside the TSAC does not exceed 60VDC
or 50VACRMS.


EV4.10.4 The mentioned voltage detection must be performed inside the respective TS enclosure.



EV4.10.5 The mentioned states of the relays (opened/closed) are the actual mechanical states. The
mechanical state can differ from the intentional state, i.e. if a relay is stuck. Any circuitry
detecting the mechanical state must meet EV5.6.2.


EV4.10.6 The voltage detection circuit of the red light and the relay state and voltage detection circuit
of the green light must be independent. Any plausibility check between both lights is not
allowed. A TSAL state with both lights simultaneously active might occur and must not be
prevented.


EV4.10.7 The TSAL must:
• Be located lower than the highest point of the main hoop and including the mounting
within the rollover protection envelope, see T1.1.15.
• Be no lower than 75mm from the highest point of the main hoop.
• Not be able to contact the driver’s helmet in any circumstances.


EV4.10.8 The entire illuminated surface of the TSAL must be clearly visible:
• Except for angles less than 10° which are blocked by the main hoop.
• From a point 1:60m vertically from ground level, within 3m horizontal radius from
the TSAL.
• In direct sunlight.


EV4.10.9 The TSAL and all needed circuitry must be hard-wired electronics. Software control is not
permitted.


EV4.10.10 A green indicator light in the cockpit that is easily visible even in bright sunlight and clearly
marked with “TS off” must light up if TSAL green light is on, see EV4.10.3.


EV4.10.11 Signals influencing the TSAL and the indicator according to EV4.10.10 are SCS, see T11.9.
The individual safe state of each of the TSAL lights is off. The TSAL has an active indication
of the absence of failures (continuous green illumination) and thus the red light must not be
illuminated for a visible check, see T11.9.5.


EV4.10.12 The TSAL’s red light voltage detection circuit, see EV4.10.2, does not need to detect an
open circuit, as required by T11.9, when no voltage is present. A plausibility check must not
be implemented.


EV4.10.13 The TSAL’s green light relay state detection circuit, see EV4.10.3, does not need to detect an
open circuit, as required by T11.9, when the intentional state of the used (auxiliary) contact
is opened. A plausibility check using the intentional relay state must be implemented in a
way that the TSAL’s green light stays off after the open circuit is detectable.


EV4.10.14 The TSAL’s green light voltage detection circuit, see EV4.10.3, does not need to detect an
open circuit, as required by T11.9, when no voltage is present. A plausibility check using
the intentional relay states must be implemented in a way that the TSAL’s green light stays
off after the open circuit of the accumulator voltage detection circuit is detectable.


EV4.10.15 The latching required by EV4.10.13 and EV4.10.14 must not be triggered during normal
operation conditions and must only be reset by power cycling the LVS.
