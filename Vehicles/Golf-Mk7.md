# Volkswagen Golf Mk7

## Identity

- Registration recorded in prior VCDS work: PY66 CUC
- Model year: 2017
- Volkswagen Golf Mk7
- Engine: 1.6 TDI BlueMotion
- Engine code: CXXB
- VIN: WVWZZZAUZHP544636
- Earlier Auto-Scan mileage: approximately 198,202 km

## Known installed control modules from earlier Auto-Scan

- 01 Engine
- 03 ABS Brakes
- 08 Auto HVAC
- 09 Central Electrics
- 10 Park/Steer Assist
- 13 Auto Distance Regulation / ACC
- 15 Airbags
- 16 Steering Wheel
- 17 Instruments
- 19 CAN Gateway
- 42 Driver Door
- 44 Steering Assist
- 52 Passenger Door
- 5F Information Electronics

No A5 front camera was present in the scan.

## Driver-assistance conclusions

### ACC

Address 13 is present, so the car has ACC radar/control.

### Steering Assist

Address 44 is present and was recorded as EPS with scan status OK 0000.

The steering system can provide requested steering torque, but this does not by itself provide Lane Assist.

### Lane Assist

No Address A5 front camera was present.

Therefore Lane Assist cannot be enabled on this Golf by VCDS coding alone.

Hardware would be required before coding could provide genuine Lane Assist.

### Parking system

Address 10 was identified as:

- J446
- Part number: 5Q0 919 294 K
- Component: PARKHILFE 8K

This is the normal 8-sensor front/rear ParkPilot system.

It provides:
- front parking sensors
- rear parking sensors
- infotainment parking display

It is not self-steering Park Assist / PLA.

Do not describe the Golf as having automatic self-parking unless later hardware evidence shows otherwise.

## Historical fault codes

Earlier work recorded the following fault codes:

- P2000
- P0562
- P16C7
- B147A
- B1330
- U1123
- B2010

These are historical observations only.

Do not assume they are currently present.

Module 5F was previously recorded as fault-free.

Before clearing future faults, preserve:
- complete Auto-Scan
- fault status
- freeze-frame information where available

## Areas previously investigated

- exterior lighting
- daytime running lights
- rear wiper behaviour
- parking sensors
- manoeuvre braking
- adaptive cruise control
- instrument cluster
- infotainment
- mirrors
- phone integration
- App-Connect
