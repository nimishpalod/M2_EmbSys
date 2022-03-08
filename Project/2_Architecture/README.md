# Design

## Flow Chart
![FlowChart](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/2_Architecture/FlowChartSolar.drawio.png)

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

## Circuit Diagram
![CircuitDiagram](https://github.com/nimishpalod/M2_EmbSys/blob/nimish/Project/2_Architecture/SmartSolarCircuitDiagram.png)

* ATmega328p contains inbuilt Analog to Digital Converter(ADC) at the ports 23-28(PC1-PC5). In this project, the 2 LDRs are connected at port 27 and 28. The LDRs sends analog input to the microcontroller, which will be converted to binary using ADC so to make it understandable for microcontroller. The further operations are done with this input according to the program given to microcontroller.
* Servo Motor is connected to pin 17 which provides PWM.
* At pin 9 and 10 which are port PB6 and PB7 which carries Oscillator, a 16MHz Crystal and 2 22pf Capacitors are given for Oscillation.
* 5V power supply is given to the microcontroller at pin 7, at pin 20 and 21 for ADC and to the servo motor.