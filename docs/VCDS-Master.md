# VCDS – Amalgamated Chat Record

Version: 1.0.3 working master  
Purpose: single maintainable record of VCDS / Golf / Polo information recovered from earlier ChatGPT conversations.

This file replaces the earlier PDF as the preferred editable master for GitHub.

---

## 1. Source chats used

### Earlier current chats already amalgamated

These exact chat names were previously confirmed from the user's ChatGPT sidebar and were incorporated into the VCDS master record before they disappeared from the current-chat list:

- `Investigate VCDS Faults`
- `Enable PY66CUC Extra`
- `Golf App Connect Activation`
- `VCDS Scan Without Licence`
- `VW Golf Fault Analysis`

Their useful VCDS/Golf content has been carried into this master record.

### Current working chat

The current visible VCDS-related chat is:

- `VDCS 1`

This is the working consolidation/project-maintenance chat and should be retained while the VCDS repository is still being updated.

### Archived chats

The following exact archived chat names are VCDS/Polo-related:

- `VW Polo Lane Assist setup`
- `Polo Lane Assist Disable`

Their relevant Polo details are incorporated into this master record, including the confirmed vehicle identity, baseline faults and Lane Assist coding change.

### Current screenshot review

A fresh review of the visible current-chat and archived-chat lists found no other chat titles clearly related to:

- VCDS / VDCS
- Volkswagen / VW
- Golf
- Polo

Therefore the two archived Polo chats above are the only remaining old VCDS/VW/Polo/Golf source chats visible outside the current `VDCS 1` working chat.

### Important note about older descriptive labels

Earlier drafts used descriptive labels such as:

- `Golf Android Auto`
- `VW Golf VCDS Fault Investigation`
- `VW Polo - VCDS Fault Investigation`
- `Use VCDS On S23`
- `Golf Lane Assist / coding-adaptation investigation`

These were not all exact sidebar/archive chat titles and must not be used as the deletion list.

The exact titles confirmed from the user's own ChatGPT screens are the titles listed above.

---

## 2. Deletion caution

Before deleting any of the source chats, check whether they contain unique attachments that have not yet been saved into the VCDS repository, especially:

- raw VCDS Auto-Scans
- screenshots
- CSV adaptation maps
- Advanced Identification exports
- coding screenshots
- supplier/order information
- infotainment screenshots
- fault freeze-frame data

This Markdown file preserves the consolidated textual conclusions, but it does not automatically preserve every original attachment from an old chat.

---

# 3. Current VCDS setup

## Interface

- Genuine Ross-Tech HEX-V2
- 10-VIN version
- USB interface

## Software

- VCDS 26.3 / 26.3.0
- Full VCDS runs on Windows

## Phone

- Samsung Galaxy S23
- Android

The existing HEX-V2 does **not** run full VCDS directly on Android.

The practical arrangement is:

```text
Car
  ↓
HEX-V2
  ↓
Windows laptop running VCDS
  ↓
Optional remote control from Samsung S23
```

A USB-C adaptor does not turn the S23 into a supported VCDS host.

HEX-NET has network/browser functionality, but it is different Ross-Tech hardware and is not required for the existing HEX-V2 setup.

Generic Android Bluetooth OBD applications are not equivalent to full VCDS.

---

# 4. General VCDS working rules

Before coding, adaptation changes or fault clearing:

1. Run and save a complete Auto-Scan.
2. Preserve relevant freeze-frame information.
3. Save Advanced Identification where useful.
4. Save adaptation maps for affected control modules where appropriate.
5. Record the original value before making a change.
6. Make one logical change at a time where practical.
7. Test the result.
8. Rescan.
9. Record whether the change was retained or reverted.

Do not perform a blanket **Clear All DTCs** before preserving the starting condition.

Preferred diagnostic sequence:

```text
Scan
→ Save
→ Investigate
→ Clear only where useful
→ Drive/test
→ Rescan
```

Do not make speculative coding changes simply because an adaptation or coding option appears to be available.

---

# 5. Volkswagen Golf Mk7

## Vehicle identity

- Registration: `PY66 CUC`
- Model: Volkswagen Golf Mk7
- Model year: 2017 / 66 plate
- Engine: 1.6 TDI BlueMotion
- Engine code: `CXXB`
- VIN: `WVWZZZAUZHP544636`
- Earlier Auto-Scan mileage: approximately `198,202 km` / `123,157 mi`
- Earlier scan work recorded no AdBlue/SCR

---

## Known installed control modules

The earlier Golf Auto-Scan included:

- `01` Engine
- `03` ABS Brakes
- `08` Auto HVAC
- `09` Central Electrics
- `10` Park/Steer Assist
- `13` Auto Distance Regulation / ACC
- `15` Airbags
- `16` Steering Wheel
- `17` Instruments
- `19` CAN Gateway
- `42` Driver Door
- `44` Steering Assist
- `52` Passenger Door
- `5F` Information Electronics

No `A5` front-camera module was present in the scan.

---

# 6. Golf driver-assistance conclusions

## ACC

Address `13` is present.

The Golf therefore has ACC radar/control.

## Steering Assist

Address `44` is present.

The steering system is EPS and can provide requested steering torque.

However, the presence of EPS by itself does **not** mean the vehicle has Lane Assist.

## Lane Assist

No `A5` front camera was present.

Therefore genuine Lane Assist cannot be enabled on this Golf by VCDS coding alone.

Additional hardware would be required before genuine Lane Assist could be provided.

---

# 7. Golf parking system

Address `10` was identified as:

- J446
- Part number: `5Q0 919 294 K`
- Component: `PARKHILFE 8K`

This is the normal 8-sensor front/rear ParkPilot system.

It provides:

- front parking sensors
- rear parking sensors
- parking display in the infotainment system

It is **not** self-steering Park Assist / PLA.

The Golf should therefore not be described as having automatic self-parking unless later hardware evidence proves otherwise.

---

# 8. Golf historical fault investigation

The following fault codes were recovered from earlier work.

These are **historical observations**, not a statement that the faults are still currently present.

| Module | Fault | Recovered detail |
|---|---|---|
| 01 Engine | P2000 | NOx catalyst/trap efficiency below threshold; intermittent/not confirmed |
| 01 Engine | P0562 | System voltage too low; intermittent/not confirmed |
| 01 Engine | P16C7 | Heater support pump locked; intermittent/not confirmed |
| 09 Central Electrics | B147A18 | Key 2 current low |
| 09 Central Electrics | B1330F5 | Alarm activation; intermittent/confirmed |
| 13 ACC | U1123 | Predictive route-data error; intermittent/confirmed; frequency 254; first recorded at about 182,443 km on 10 Jan 2026 |
| 17 Instruments | B2010 | No basic setting; confirmed; frequency 1; recorded about 182,360 km on 9 Jan 2026 |
| 5F Infotainment | No faults | Module 5F was fault-free in the baseline scan |

The original diagnostic work was initially treated as read-only.

Before clearing future faults, preserve:

- complete Auto-Scan
- fault status
- freeze-frame information where available

---

# 9. Golf coding and adaptation investigation

Areas previously investigated included:

- exterior lighting
- daytime running lights
- rear wiper behaviour
- parking sensors
- manoeuvre braking
- adaptive cruise control
- instrument cluster behaviour
- infotainment
- mirrors
- windows

Modules identified for adaptation-map capture included:

- `09`
- `10`
- `13`
- `17`
- `42`
- `52`

The agreed approach was to wait until physically at the vehicle, preserve baselines, then work interactively through only the wanted changes.

No speculative Golf coding changes from that investigation are recorded here as completed.

---

# 10. Golf MIB2 / Discover Media

Previously recorded infotainment details:

- Discover Media / MIB2
- Part number: `3Q0 035 874 B`
- Hardware: `H30`
- Software: `0359`
- Component recorded as `MU-S-ND-ER`
- Dataset: `V03935247LK 0001`
- Previously identified software train: `MST2_EU_VW_ZR_P0359T`

The Samsung Galaxy S23 is used with applications including Waze.

---

# 11. Golf App-Connect investigation

The App-Connect screen displayed an activation message requiring an activation key / dealer contact.

The user wanted to use the Samsung S23, including Waze, on the Golf screen and ideally to use Android Auto wirelessly.

## Key conclusion

VCDS coding alone cannot create or install a missing genuine Volkswagen App-Connect FEC/SWaP entitlement.

The genuine Volkswagen activation route discussed was associated with:

- part number `5G0 054 830 A`
- activation through Volkswagen diagnostic systems / ODIS

VCDS remains useful for:

- identifying module 5F
- reading coding
- reading adaptations
- checking configuration
- diagnostics
- checking whether entitlement/configuration is present

But VCDS cannot manufacture the missing genuine licence entitlement.

Earlier work also recorded:

- an `adphex` CSV adaptation backup with about 61 lines
- a readable adaptation-map CSV
- a specialist-oriented log involving `IDE04329`
- confirmation that App-Connect entitlement was absent

A specialist had indicated they could perform the activation.

An earlier price recorded for the activation document/part was approximately `£147.85 including VAT`; this was a historical price at the time and should not be treated as current without checking.

Unofficial SD-card patching methods were investigated but are not part of the preferred documented configuration.

---

# 12. Volkswagen Polo

## Confirmed vehicle information

From the archived Polo VCDS chats:

- Model: 2022 UK Volkswagen Polo Life
- Chassis: `AW-VW27 (2Q0)`
- VIN: `WVWZZZAWZNU044942`
- Initial scan mileage: approximately `21,060 km`
- VCDS: 26.3.0
- Interface: genuine Ross-Tech HEX-V2
- A5 front-sensor module: `2Q0 980 653 C`

This corrects the earlier assumption that the Polo details had not been recovered.

---

# 13. Polo baseline faults

The earlier Polo baseline included the following faults.

These had not been cleared when they were recorded.

| Module | Fault | Recovered detail |
|---|---|---|
| 09 BCM | B14D1 54 | Window regulator missing calibration/basic setting |
| 17 Instruments | U1110 | BAP_Audio communication interrupted; frequency 4 |
| 17 Instruments | U1110 | BAP_BCME communication interrupted; frequency 1 |
| 5F Infotainment | B1067 13 | Rear-right bass speaker open circuit; frequency 4; terminal-30 voltage 11.5 V in freeze-frame |

Modules reported OK included:

- `03` ABS
- `10` Park/Steer Assist
- `13` ACC
- `44` Steering Assist
- `A5` Front Sensor Driver Assist

---

# 14. Polo Lane Assist work

The Polo had genuine A5 Lane Assist hardware.

The recorded coding change was:

```text
Byte 9
9E → 9F
```

Purpose:

Change Lane Assist startup behaviour from always active to:

```text
Last Setting
```

The change was:

- accepted by the vehicle
- tested successfully
- not blocked by SFD
- unrelated to the four pre-existing baseline faults

Those baseline faults were not cleared as part of the Lane Assist coding change.

---

# 15. Polo archived chat sources

The exact archived chat names visible in ChatGPT are:

- `VW Polo Lane Assist setup`
- `Polo Lane Assist Disable`

These should be treated as the source chats for the Polo Lane Assist material above.

Before deleting them, check for:

- raw Auto-Scan text
- screenshots
- before/after coding screenshots
- adaptation maps
- any unique notes not yet copied into the repository

---

# 16. Current-chat source review

The exact current chat names visible in ChatGPT and identified as relevant are:

## Investigate VCDS Faults

Used for Golf diagnostic/fault work.

Before deleting, check for:

- full raw Golf Auto-Scan
- freeze-frame data
- screenshots
- any exported scan files

## Enable PY66CUC Extra

Used for Golf coding/adaptation investigation and possible feature changes.

Before deleting, check for:

- coding screenshots
- adaptation map files
- before/after values
- any features considered but not yet transferred here

## Golf App Connect Activation

Used for:

- MIB2 identification
- App-Connect investigation
- activation route
- supplier/specialist information
- S23 / Waze use

Before deleting, check for:

- screenshots of the App-Connect activation screen
- supplier links or order details
- adaptation CSV files
- MIB2 screenshots

## VCDS Scan Without Licence

Used for VCDS scan/setup discussions and diagnostic workflow.

Before deleting, check for any:

- scan files
- interface screenshots
- licensing/setup screenshots

## VW Golf Fault Analysis

Used for analysis of Golf faults and interpretation of scan data.

Before deleting, check for:

- original Auto-Scan text
- fault freeze-frame information
- screenshots
- detailed diagnosis that may not yet be represented here

---

# 17. Recommended GitHub repository structure

Suggested structure:

```text
VCDS/
│
├── README.md
├── docs/
│   └── VCDS-Amalgamated-Chat-Record.md
│
├── Vehicles/
│   ├── Golf-Mk7/
│   │   ├── README.md
│   │   ├── Scans/
│   │   ├── Adaptation-Maps/
│   │   └── Changes/
│   │
│   └── Polo/
│       ├── README.md
│       ├── Scans/
│       ├── Adaptation-Maps/
│       └── Changes/
│
├── Procedures/
│   ├── Baseline-Before-Changes.md
│   └── S23-Remote-Use.md
│
└── Research/
    └── MIB2-AppConnect.md
```

The repository should distinguish clearly between:

- current confirmed configuration
- historical observation
- proposed change
- change actually made

---

# 18. Change-record format

For every significant VCDS change record:

- date
- vehicle
- control module
- original setting
- new setting
- reason for change
- outcome
- retained or reverted

Where possible, retain the associated:

- before scan
- after scan
- adaptation map
- screenshot

---

# 19. Project workflow

This project follows the standard PowerShellTools workflow.

Create/clone the GitHub repository first.

Then, from:

```powershell
C:\WDL\GitHub\PowerShellTools
```

run:

```powershell
.\ProjectCreate.ps1 VCDS
```

PowerShell 7 (`pwsh`) is the standard shell.

Ongoing updates use PSTP Change Packages.

From:

```powershell
C:\WDL\GitHub\VCDS
```

release with:

```powershell
.\PSTP.ps1 Release -Zip
```

The first release line is:

```text
v1.0.1
```

Release-managed files such as `release.json` and `build-info.json` remain under PSTP control.

---

# 20. Current status

This Markdown file is now the preferred editable replacement for the earlier PDF.

The next repository update should incorporate the corrected Polo information and the exact current/archive source-chat names recorded here.

Once all unique attachments from the source chats have also been saved into the VCDS repository, the old source chats can be considered for deletion.

---

# 21. Final chat-cleanup review

Fresh screenshots of the current and archived ChatGPT lists were reviewed after VCDS v1.0.2.

## Current chats

The only VCDS/VW/Polo/Golf-related current chat still visible is:

- `VDCS 1`

Keep this chat for now because it is the active VCDS consolidation and repository-maintenance conversation.

## Archived chats

The only VCDS/VW/Polo/Golf-related archived chats still visible are:

- `VW Polo Lane Assist setup`
- `Polo Lane Assist Disable`

Their relevant textual information is now represented in this master record.

Before deleting either archived chat, confirm there are no unique raw VCDS scans, screenshots or other attachments in the chat that have not been copied into the GitHub repository.

No other visible current or archived chat title in the supplied screenshots appears related to VCDS, Volkswagen, Golf or Polo.
