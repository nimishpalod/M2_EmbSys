# Test-Plan
## High Level Test Plan
| ID | Description | Input | Output | Status |
|----|-------------|-------|--------|--------|
| H_01 | Light Dependent Resistor 1 | Light intensity Value | Expected analog value in Lux | SUCCESS |
| H_02 | Light Dependent Resistor 2 | Light intensity Value | Expected analog value in Lux | SUCCESS |
| H_03 | Resistor | Restrict the flow | Restrict the flow of current | SUCCESS |
| H_04 | Capacitor | Work as an Oscillator | Used in Oscillation | SUCCESS |
| H_05 | Servo Motor | LDR with maximum intensity value | Rotate in the LDR's direction | SUCCESS |

## Low Level Test Plan
| ID | Description | Input | Output | Status |
|----|-------------|-------|--------|--------|
| L_01 | Servo Motor should turn in the direction of LDR1 | Value of LDR1>LDR2 | Turned in the direction of LDR1 | SUCCESS |
| L_02 | Servo Motor should turn in the direction of LDR2 | Value of LDR2>LDR1 | Turned in the direction of LDR2 | SUCCESS |
| L_03 | When sun is heading towards East | Value of LDR1 = 588Lux
Value of LDR2 = 3Lux | Servo Motor should turn in the direction of LDR1 | SUCCESS |
| L_04 | When sun is heading towards West | Value of LDR1 = 5Lux
Value of LDR2 = 576Lux | Servo Motor should turn in the direction of LDR2 | SUCCESS |
