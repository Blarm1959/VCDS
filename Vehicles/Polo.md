# Volkswagen Polo

## Confirmed identity

- Model: 2022 UK Volkswagen Polo Life
- Chassis: AW-VW27 (2Q0)
- VIN: WVWZZZAWZNU044942
- Initial scan mileage: approximately 21,060 km
- VCDS: 26.3.0
- Interface: genuine Ross-Tech HEX-V2
- A5 front-sensor module: 2Q0 980 653 C

## Baseline faults

- 09 BCM — B14D1 54 — window regulator missing calibration/basic setting
- 17 Instruments — U1110 — BAP_Audio communication interrupted; frequency 4
- 17 Instruments — U1110 — BAP_BCME communication interrupted; frequency 1
- 5F Infotainment — B1067 13 — rear-right bass speaker open circuit; frequency 4; terminal-30 voltage 11.5 V in freeze-frame

Modules reported OK included:

- 03 ABS
- 10 Park/Steer Assist
- 13 ACC
- 44 Steering Assist
- A5 Front Sensor Driver Assist

## Lane Assist

The Polo has genuine A5 Lane Assist hardware.

Recorded coding change:

```text
Byte 9: 9E -> 9F
```

Purpose:

Change Lane Assist startup behaviour from always active to **Last Setting**.

Result:

- accepted by the vehicle
- tested successfully
- no SFD problem reported
- unrelated to the four pre-existing baseline faults
- baseline faults were not cleared as part of this change

## Source chats

Exact archived chat names confirmed from the user's ChatGPT archive:

- `VW Polo Lane Assist setup`
- `Polo Lane Assist Disable`
