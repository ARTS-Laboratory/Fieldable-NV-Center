# v0.1.0
* Working ESR/NMR setup in November 2026.
* Functional Setup with operatations instructions. 

## Documentation

The accompanying PDF was prepared by Angelo Varillas to document his NMR work over the past four to five months. It was created using the video transcript, selected video snapshots, photographs of relevant notebook pages, and additional notes. The lab notebook is also being kept in the lab as a reference.


## Townes: Operation Instruction Videos

Townes is a benchtop NV-center ODMR setup for ESR/NMR and pulsed measurements. These five
videos walk through operating it, from the hardware to writing and running new pulse
sequences. Each video has chapters; the links below jump straight to each one.

| Video | Length | Covers |
|-------|--------|--------|
| [A: Hardware](https://www.youtube.com/watch?v=bWd51GEcrH8) | 13:06 | Optics, bias magnet, microwave I/Q chain, SR400, PulseBlaster |
| [B: First Measurements](https://www.youtube.com/watch?v=OPnI7cuR7Co) | 22:55 | Starting the LabVIEW programs, CW ESR, Rabi |
| [C: Coherence Measurements](https://www.youtube.com/watch?v=aqQHxkeU-ls) | 20:01 | T2 (Hahn echo), XY8 |
| [D: Writing a New Pulse Sequence](https://www.youtube.com/watch?v=5kdYVRmKDM4) | 27:48 | Building a correlation-contrast sequence from scratch |
| [E: Debugging and Running](https://www.youtube.com/watch?v=tKU9IeiQwhY) | 24:52 | Wiring in, debugging on the scope, running scans, T1 and Ramsey |

### A: Hardware – Optics, Magnet, Microwave Chain, and Timing

- [0:00](https://www.youtube.com/watch?v=bWd51GEcrH8&t=0s) Quarter-wave plate: exciting all NV orientations
- [0:31](https://www.youtube.com/watch?v=bWd51GEcrH8&t=31s) ND filter: new 5 mW laser and avoiding detector saturation
- [1:33](https://www.youtube.com/watch?v=bWd51GEcrH8&t=93s) Permanent magnet instead of the coil for NMR
- [2:18](https://www.youtube.com/watch?v=bWd51GEcrH8&t=138s) Microwave I/Q switch chain and getting −X / −Y pulses
- [6:08](https://www.youtube.com/watch?v=bWd51GEcrH8&t=368s) SR400 gated photon counter settings
- [9:08](https://www.youtube.com/watch?v=bWd51GEcrH8&t=548s) Scope channel map, PulseBlaster outputs, and switch power supplies

PulseBlaster bits: 0 MW indicator, 1 AOM, 2 SR400 trigger, 3 I, 4 Q, 7 inhibit.
The LabVIEW programs number channels from 1, so there I = channel 4 and Q = channel 5.

### B: First Measurements – CW ESR and Rabi

- [0:00](https://www.youtube.com/watch?v=OPnI7cuR7Co&t=0s) Starting the LabVIEW programs and running a CW ESR (ODMR) sweep
- [6:48](https://www.youtube.com/watch?v=OPnI7cuR7Co&t=408s) Rabi program layout and scan parameters
- [9:27](https://www.youtube.com/watch?v=OPnI7cuR7Co&t=567s) Placing the SR400 gates and inhibit for a Rabi scan
- [14:52](https://www.youtube.com/watch?v=OPnI7cuR7Co&t=892s) How a pulse sequence steps: manipulate sub-VI, dark time, and inversion
- [18:32](https://www.youtube.com/watch?v=OPnI7cuR7Co&t=1112s) Running a test Rabi scan and averaging (N and passes)

### C: Coherence Measurements – T2 and XY8

- [0:00](https://www.youtube.com/watch?v=aqQHxkeU-ls&t=0s) Speeding up T2 / XY8 scans: sectioning and sampling revivals
- [3:28](https://www.youtube.com/watch?v=aqQHxkeU-ls&t=208s) Setting up and running a T2 (Hahn echo) scan
- [10:51](https://www.youtube.com/watch?v=aqQHxkeU-ls&t=651s) XY8 sequence: setup, gate placement, and dark/bright readout

### D: Writing a New Pulse Sequence in LabVIEW

- [0:00](https://www.youtube.com/watch?v=5kdYVRmKDM4&t=0s) Correlation contrast program and other programs in the repo
- [2:24](https://www.youtube.com/watch?v=5kdYVRmKDM4&t=144s) Step 1: copy a template and build the first half
- [14:44](https://www.youtube.com/watch?v=5kdYVRmKDM4&t=884s) Step 2: second half, −Y pulses, and inhibits

## E: Wiring, Debugging, and Running a New Sequence; T1 and Ramsey
3
- [0:00](https://www.youtube.com/watch?v=tKU9IeiQwhY&t=0s) Step 3: wiring the new sequence into the main VI
- [7:09](https://www.youtube.com/watch?v=tKU9IeiQwhY&t=429s) Step 4: debugging it on the oscilloscope
- [18:40](https://www.youtube.com/watch?v=tKU9IeiQwhY&t=1120s) Starting a long scan: file paths, passes, and sanity checks
- [22:12](https://www.youtube.com/watch?v=tKU9IeiQwhY&t=1332s) T1 and Ramsey programs; ESR vs. Ramsey field sensitivity

### Quick reference

- Always run **NMR Main.vi** first to set the global variables.
- Keep microwave power at **15 dBm or less** with two switches.
- Data file paths must stay on the **desktop**, not inside the GitHub folder.
