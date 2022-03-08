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
* The solar energy can be reused as it is non-renewable resource.
* This also saves money as there is no need to pay for energy used.
* Helps in maximizing the solar energy absorption by continuously tracking the sun.
### Weaknesses
* Very less efficient in rainy season.
* Setup is expensive.
* It requires high maintainance with time to time change.
### Opportunities
* It reduces the number of solar panel as a single one generates more energy.
* In offices and buildings where huge electricity is required.
* This system reduces the cost of setup.
### Threats
* Difficulty in replacement of existing system.
* High maintainance.

# 5W's and 1H
### WHO
* People having businesses
* Government of Country
### WHAT
* Automated Solar Panel with rotation according to the sun's direction
### WHEN
* Whenever more efficiency is required with small setup of solar panel
### WHERE
* The place where need is more but space is less
### WHY
* To reduce the solar panel cost
* To increase the efficiency of generating energy
### HOW
* Just by Setting up this system at the rooftop of the building

# Applications
* These panels can be used to power the traffic streetlights
* These can be used in home to power the appliances using solar power
* These can be used in industries as more energy can be saved by rotating the panel

<hr>

# Design and Architecture

## Block Diagram
![BlockDiagram](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/2_Architecture/BlockDiagramSolar.drawio.png)

## Components Used
* **ATmega328p microcontroller** 
    * This microcontroller belongs to AVR family.  It is an 8-bit controller, contains 32K Bytes of Programmable Flash memory, 1K Bytes of EEPROM and 2K Bytes of SRAM. 
    * It is the main controlling unit which is responsible for making the required action.
    * It is programmed in such a way that it makes the servo motor moves in the direction of LDR with maximum light intensity, which results in turning solar panel in the direction of sun.
    * It also has inbuilt ADC which takes in analog input from the sensors and converts it into binary format so to make it system understandable and make code run for perticular input.
    * It also provides PWM Signal which is required by Servo Motor to work. 
* **Light Sensors** 
    * Light Dependent Resistors or LDRs are the resistors whose resistance values depend on intensity of the light. As the intensity of light falling on the LDR increases, resistance value decreases. In dark, LDR will have maximum resistance. 
    * These LDRs are placed at different directions and are connected to the microcontroller.
    * They will detect the intensity of light and whichever direction the intensity will be maximum, the solar panel will be turned to that direction.
* **Servo Motor**
    * A servo motor is a self-contained electrical device, that rotate parts of a machine with high efficiency and with great precision.
    * Servo motor is used to rotate the solar panel.
    * It requires PWM Signal to move.
* **Solar Panel**
    * Solar panel consists of photovoltaic cells arranged in an order. Photovoltaic cell is nothing but a solar cell. Solar cell is made up of semiconductor material silicon.
    * When a light ray from Sun is incident on the solar cell, some amount of energy is absorbed by this material. The absorbed energy is enough for the electrons to jump from one orbit to other inside the atom. Cells have one or more electric field that directs the electrons which creates current. By placing metal contact energy can be obtained from these cells.
    * For an efficient usage of the solar energy, the Solar panels should absorb energy to a maximum extent. So it is connected to the servo motor which turns its face in the direction of sun. 

## Flow Chart
![FlowChart](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/2_Architecture/FlowChartSolar.drawio.png)

## Circuit Diagram
![CircuitDiagram](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/2_Architecture/SmartSolarCircuitDiagram.png)

* ATmega328p contains inbuilt Analog to Digital Converter(ADC) at the ports 23-28(PC1-PC5). In this project, the 2 LDRs are connected at port 27 and 28. The LDRs sends analog input to the microcontroller, which will be converted to binary using ADC so to make it understandable for microcontroller. The further operations are done with this input according to the program given to microcontroller.
* Servo Motor is connected to pin 17 which provides PWM.
* At pin 9 and 10 which are port PB6 and PB7 which carries Oscillator, a 16MHz Crystal and 2 22pf Capacitors are given for Oscillation.
* 5V power supply is given to the microcontroller at pin 7, at pin 20 and 21 for ADC and to the servo motor.

<hr>

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
| L_03 | When sun is heading towards East | Value of LDR1 = 588Lux, Value of LDR2 = 3Lux | Servo Motor should turn in the direction of LDR1 | SUCCESS |
| L_04 | When sun is heading towards West | Value of LDR1 = 5Lux, Value of LDR2 = 576Lux | Servo Motor should turn in the direction of LDR2 | SUCCESS |

<hr>

# Output Images
#### The Normal Circuit when the supply to the motor is off
![SolarOutput1](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/6_ImagesAndVideos/SolarOutput1.png)
#### When the value of Light Intensity is more for LDR1
![SolarOutput2](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/6_ImagesAndVideos/SolarOutput2.png)
#### When the value of Light Intensity is more for LDR2
![SolarOutput3](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/6_ImagesAndVideos/SolarOutput3.png)
