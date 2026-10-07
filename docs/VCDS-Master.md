# VCDS Master Record

Version: 1.0.1

This is the authoritative project record for VCDS work on the family Volkswagen vehicles.

## Current diagnostic setup

- Genuine Ross-Tech HEX-V2
- 10-VIN version
- VCDS 26.3 / 26.3.0
- Full VCDS runs on Windows
- Samsung Galaxy S23 can be used to remote-control the Windows laptop, but the HEX-V2 does not run full VCDS directly on Android

## Vehicles currently in scope

1. 2017 Volkswagen Golf Mk7 1.6 TDI BlueMotion
2. Wife's Volkswagen Polo

The Golf is documented in detail from earlier scans and investigations.
The Polo is known to be intended for use with one HEX-V2 VIN slot, including possible Lane Assist work, but its exact year, engine, VIN and control-module configuration have not yet been recovered from the prior chats. These must be recorded from the car or a future Auto-Scan rather than guessed.

## Core rule before any VCDS change

Before coding, adaptation or fault clearing:

1. Save a complete Auto-Scan.
2. Save relevant freeze-frame information.
3. Save Advanced Identification where useful.
4. Save adaptation maps for affected modules where appropriate.
5. Record the original setting before changing it.
6. Make one logical change at a time where practical.
7. Test the result.
8. Record whether the change was retained or reverted.

Do not clear all faults before preserving the starting scan.

Preferred diagnostic sequence:

Scan -> save -> investigate -> clear only where useful -> drive/test -> rescan

## Repository structure

- `docs/` - master project notes
- `Vehicles/` - vehicle-specific records
- `Scans/` - saved VCDS Auto-Scans
- `Adaptation-Maps/` - baseline and later maps
- `Changes/` - coding/adaptation change records
- `Procedures/` - repeatable operating instructions
- `Research/` - investigations and unresolved ideas

The project must distinguish:
- current confirmed configuration
- historical observation
- proposed change
- change actually made

This avoids old investigations being mistaken for current configuration.
