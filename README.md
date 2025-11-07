# LMH Team

This is the deliverables for LMH team for the CHORAS workshop at ASSA. 

In `assets` you will find the following:
1. `IR_DE.wav`: Impulse response from DE
2. `IR_DG.wav`: Impulse response from DG
3. `t30_DE.csv`: T30 results from DE
4. `DG_modes.csv`: Frequencies of first 5 modes from DG 
5. T30 results from DG (still work in progress)
6. `notes.txt` for feedback and issues.

## Members

- Lauri
- Maciej
- Hossein

## Process

- We started with the shoebox and the default material settings.
- We tried DE with small charachteristich lenght ~0.1 and it was very slow.
- We then moved to custom materials for ceiling and floor.
- We also did cutom material for glass.
- We tried to consider desks and chairs as part of the floor properties.
- In the end, we had two types of glass, a cutom wall, a custom ceiling, and a custom floor.

## Input settings

For reproducibility of your results we would like to know what inputs you used to complete your simulations.

### Geometry

We did use [Room2215_withAbs.obj](https://github.com/choras-org/ASSA_Workshop/blob/main/Geometries/Room2215_withAbs.obj) from CHORAS repository.

### Source position

- x: 9.5
- y: 4.5
- z: 1.7

### Receiver position

- x: 2.5
- y: 3
- z: 1.4

### Surfaces

We used the following custom materials:
- Double Glazzed Window, 0.15, 0.15, 0.05, 0.03, 0.03, 0.02, 0.02
- Plasticboard, 0.15, 0.15, 0.01, 0.06, 0.04, 0.04, 0.05
- 500hz custom wall, 0.06, 0.06, 0.11, 0.6, 0.57, 0.63, 0.64
- Micro Celing, 0.86, 0.86, 0.94, 0.65, 0.77, 0.76, 0.75
- Floor boards on joist floor, 0.15, 0.15, 0.2, 0.1, 0.1, 0.1, 0.1

Material properties:
- Surface [1]: single pane of glass > 4mm
- Surface [2]: single pane of glass > 4mm
- Surface [3]: double glazzed window
- Surface [4]: double glazzed window
- Surface [5]: single pane of glass > 4mm
- Surface [6]: single pane of glass > 4mm
- Surface [7]: double glazzed window
- Surface [8]: plasticboard
- Surface [9]: plasticboard
- Surface [10]: Acoustic ceiling (rockwool), 40 mm , 100 kg/m3, suspended 200 mm
- Surface [11]: Acoustic ceiling (rockwool), 40 mm , 100 kg/m3, suspended 200 mm
- Surface [12]: plasticboard
- Surface [13]: 500hz custom wall
- Surface [14]: 500hz custom wall
- Surface [15]: Micro Celing
- Surface [16]: Floor boards on joist floor
- Rest of the surfaces: _material name_

### Settings

These are the DE and DG settings:
- DE

```json
{
  "sim_len_type": "edt",
  "de_ir_length": 0.5,
  "de_c0": 343,
  "edt": 35,
  "de_lc": 1
}
```

- DG

```json
{
  "dg_freq_upper_limit": 300,
  "dg_c0": 343,
  "dg_rho0": 1.213,
  "dg_ir_length": 0.5,
  "dg_poly_order": 4,
  "dg_ppw": 2,
  "dg_cfl": 1
}
```

## 3 proposals for improving CHORAS

For proposa, issues, and feedback, check our feedback note in `notes.txt`.
