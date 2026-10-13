# EV Battery Charging Techniques: CC, CV, CC–CV, and CT–CV

## Overview

This project explores and compares different charging techniques for lithium-ion batteries used in electric vehicles (EVs). It includes MATLAB/Simulink models and project presentation materials for four charging strategies:

- **CC — Constant Current**
- **CV — Constant Voltage**
- **CC–CV — Constant Current–Constant Voltage**
- **CT–CV — Constant Temperature–Constant Voltage**

The project focuses on charging time, battery voltage and current behavior, and temperature during charging. It also investigates how temperature-aware control can improve charging safety and performance.

## Problem Statement

Design and simulate battery-charging systems using different charging methods, then compare their charging behavior to understand the trade-offs between charging speed, thermal performance, and safe operation.

## Objectives

- Compare the charging time of different charging methods.
- Observe battery voltage and current profiles during charging.
- Examine battery temperature behavior, including surface and internal temperature where modeled.
- Understand the risks and limitations of charging without suitable voltage or thermal control.
- Evaluate the potential benefits of temperature-aware CT–CV charging.

## Charging Methods

### 1. Constant Current (CC)

The charger supplies a constant current while battery voltage rises. This can provide a fast initial charge, but current-only control does not by itself prevent the battery voltage from exceeding its safe limit. Practical systems require voltage limits and protective controls.

### 2. Constant Voltage (CV)

The charger maintains a fixed voltage while charging current decreases as the battery approaches full charge. Depending on the starting state of charge and model settings, charging can take longer.

### 3. Constant Current–Constant Voltage (CC–CV)

Charging begins with a constant-current stage. When the battery reaches its voltage limit, the charger switches to constant-voltage operation and current gradually tapers down. This is a widely used lithium-ion charging approach because it balances charging speed with voltage control.

### 4. Constant Temperature–Constant Voltage (CT–CV)

The charging current is adjusted based on battery temperature during the initial stage to help manage thermal behavior. When the battery reaches its voltage limit, control transitions to constant-voltage charging. The project materials describe monitoring internal and surface temperature using a thermal model.

## Repository Contents

The main project folder contains:

```text
CT-CV/
├── CC.slx.zip
├── CC_CV_NEW.slx.zip
├── CTCV_NEW.slx.zip
├── cv_NEW.slx.zip
├── charging techniques for Ev batteries.pdf
└── charging techniques for Ev batteries.pptx
```

- `CC.slx.zip` — compressed Simulink model for Constant Current charging.
- `cv_NEW.slx.zip` — compressed Simulink model for Constant Voltage charging.
- `CC_CV_NEW.slx.zip` — compressed Simulink model for CC–CV charging.
- `CTCV_NEW.slx.zip` — compressed Simulink model for CT–CV charging.
- `charging techniques for Ev batteries.pdf` — project report/presentation export.
- `charging techniques for Ev batteries.pptx` — editable presentation slides.

The repository also includes a copy of the PDF in its top-level folder.

## Requirements

- MATLAB
- Simulink
- Any additional MATLAB/Simulink toolboxes or libraries required by the models

The exact MATLAB release and toolbox requirements have not been specified. If a model reports missing blocks or libraries, check its diagnostics and install or replace the required components.

## How to Use

1. Download or clone this repository.
2. Extract the repository archive.
3. For the selected model, extract its corresponding `.slx.zip` file.
4. Open MATLAB and navigate to the extracted model directory.
5. Open the resulting `.slx` file in Simulink.
6. Review model parameters and battery limits before running a simulation.
7. Run the simulation and inspect available plots for current, battery voltage, charging time, and temperature.
8. Repeat with the other models under comparable initial conditions and battery settings for a fair comparison.

**Important:** The model files are provided as ZIP archives containing Simulink files. Extract the nested ZIP before opening the `.slx` model in Simulink.

## Results Reported in the Project Materials

The accompanying presentation reports the following comparison:

| Charging method | Reported charging time | Reported temperature rise |
|---|---:|---:|
| CC | 61 minutes | Not specified |
| CV | 104 minutes | Not specified |
| CC–CV | 91 minutes | 6.5 °C |
| CT–CV | 80 minutes | 6.5 °C |

According to these reported results, CT–CV takes less time than CC–CV in the presented simulation. These values are taken from the project presentation and may depend on the model parameters, battery configuration, initial state of charge, and simulation conditions. Re-run the models to verify the results before using them for formal comparisons.

## Expected Observations

- CC charging keeps current approximately constant while voltage increases.
- CV charging holds voltage approximately constant while current decreases.
- CC–CV transitions from constant-current charging to constant-voltage charging.
- CT–CV adds temperature-aware current control before transitioning to constant-voltage charging.
- Charging time and temperature behavior should be compared using the same battery and simulation assumptions.

## Safety Note

This repository is intended for modeling and educational simulation. It is not a validated battery-management system or a charger design ready for real hardware. Do not use the models alone to set real battery charging limits. Actual battery systems require chemistry-specific voltage/current limits, temperature sensing, fault handling, and appropriate protection hardware.

## References

The project presentation lists these IEEE paper titles as references:

- *A Closed-Loop Constant-Temperature Constant-Voltage Charging Technique to Reduce Charge Time of Lithium-Ion Batteries*
- *Performance Analysis of the Lithium-Ion Batteries using CT-CV Charging Technique*

Please add complete author, publication, year, DOI, or URL details when available.

## Contributors

The project presentation credits:

- Siddhartha Porika
- Ankit Verma
- Midatana Dhileep
- Pankaj Kumar
- Sathvik Rathod

