# Description
In today's world it has become a necessity to use the renewable resources for making energy since the applications and users have increased, the need for electricity has grown by times. The best source of renewable energy is Solar Energy. Now a days solar panels are becoming more popular. Solar panel absorbs the energy from the Sun, converts it into electrical energy and stores the energy in a battery. The position of the Sun with respect to the solar panel is not fixed due to the rotation of the Earth. For an efficient usage of the solar energy, the Solar panels should absorb energy to a maximum extent. So this project aims to collect the maximum energy from the sun. 

# Requirements
## High Level Requirements
| ID | Description |
|------|-----------|
| HLR_01 | The system shall detect the light intensity |
| HLR_02 | The system shall continuously move in the direction of sun |
| HLR_03 | The system shall absorb the solar energy |
| HLR_04 | The solar panel shall charge the batteries with sunlight |

## Low Level Requirements
| HLR ID | ID | Description |
|----|--------|-------------|
| `HLR_01` | LLR_01 | Their shall be more than one Light Sensors (LDRs) |
|        | LLR_02 | The resistance of LDRs should get changed with the intensity of light |
|        | LLR_03 | The resistance value shall be given to the microcontroller in binary format |
| `HLR_02` | LLR_04 | The system shall compare the intensity on the basis of different LDR values |
|        | LLR_05 | The servo motor shall move in the direction where the intensity is more |
|        | LLR_06 | The servo motor shall be provided with a PWM signal |
| `HLR_03` | LLR_07 | Solar panel shall absorb solar light |
|        | LLR_08 | The energy from sun shall be converted to electrical energy |
| `HLR_04` | LLR_09 | The electrical energy shall be used to store the energy for the battery |
|        | LLR_10 | The electrical energy shall be used directly for different purposes |

# SWOT Analysis
### Strengths

### Weaknesses

### Opportunities

### Threats