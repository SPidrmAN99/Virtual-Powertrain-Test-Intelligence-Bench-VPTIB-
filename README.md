# Virtual Powertrain Test & Intelligence Bench (VPTIB)

> **Project status: PLANNING PHASE**  
> VPTIB is currently being scoped. The capabilities below describe the intended project; they are not implemented or validated yet.

VPTIB is a planned software platform for exploring engine-dyno testing and ECU behaviour without requiring a physical car. It will connect a simplified virtual engine and dynamometer model to configurable control logic, repeatable test procedures, signal logging, fault injection, and analysis tools.

The project is intended as an educational and engineering portfolio project. Simulated outputs will be identified as simulations and will not be presented as measurements from a real engine.

## Project goals

- Create repeatable virtual engine test runs under configurable RPM and load conditions.
- Explore how ECU fuel and ignition control strategies affect modelled engine behaviour.
- Log and visualize test signals such as RPM, torque, throttle, fuel rate, and selected temperatures or pressures.
- Inject sensor and actuator faults and evaluate detection logic.
- Use AI to help summarize and compare runs, with results traceable to the underlying data.

## Planned modules

### 1. Virtual engine dyno

A simplified engine plant and dynamometer model will support steady-state points, RPM sweeps, and step tests. Planned outputs include torque and power curves, with optional modelled fuel consumption and environmental adjustments.

### 2. ECU fuel and ignition control

A configurable controller will use simulated engine speed and load to select fuel and ignition commands. Runs will compare control maps or strategies against stated objectives such as torque response or modelled fuel use.

### 3. Sensor and actuator fault detection

The test bench will support simulated signal faults such as noise, bias, dropouts, and stuck readings. Detection results will be presented as items for investigation, not as definitive diagnoses of a real engine fault.

### 4. Dyno test automation and data analysis

Users will be able to define repeatable tests, record run configuration and signal data, generate performance plots, and flag incomplete or inconsistent runs.

### 5. AI-assisted run analysis

An AI feature is planned to answer questions about recorded runs, summarize comparisons, highlight unusual signal windows, and draft reports. Numerical calculations and pass/fail checks should remain deterministic and auditable; AI summaries should link back to supporting signals and values.

### 6. Optional hardware-in-the-loop (HIL)

HIL is a possible later extension after the virtual plant and controller are established. It would require suitable real-time simulation and hardware, and is outside the initial software-only scope.

## Proposed workflow

```text
Configure test → Run virtual dyno and engine → Apply ECU control
                         ↓
                 Log and validate signals
                         ↓
             Analyze, compare, and visualize
                         ↓
               AI-assisted report (planned)
```

## Development roadmap

- [ ] **Planning:** define scope, model assumptions, requirements, and initial toolchain.
- [ ] **Virtual plant:** implement a documented engine and dyno model.
- [ ] **Test runner:** add repeatable sweep, steady-state, and step tests with run logging.
- [ ] **ECU prototype:** implement and compare basic fuel and ignition control strategies.
- [ ] **Fault scenarios:** inject selected sensor and actuator faults and evaluate detection.
- [ ] **Analysis interface:** add plots, run comparisons, and exportable reports.
- [ ] **AI assistant:** add evidence-linked summaries over saved run data.
- [ ] **HIL exploration:** assess feasibility after the simulation-only version is usable.

## Proposed tools

The toolchain is still to be decided. MATLAB/Simulink is a candidate for modelling and control development; Python may support data processing, automation, and the user interface. Toolbox availability and final architecture will be confirmed during planning.

## Scope and limitations

- This project begins as a **simulation**, not a real engine dyno or production ECU.
- Model behaviour depends on documented assumptions and parameter values.
- Without measurements from a physical engine, simulated results cannot validate a specific engine or calibration.
- The project is not intended to provide safety-critical control or instructions for operating real engine hardware.

## Repository status

The repository is in the **planning phase**. Implementation details, model fidelity, and the final software stack may change as the design is developed.

## Project link

[View the VPTIB repository](https://github.com/SPidrmAN99/Virtual-Powertrain-Test-Intelligence-Bench-VPTIB-)