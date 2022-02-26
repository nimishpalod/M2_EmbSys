# Description
Overheat Detector is a device which detects the temprature of system and whenever it exceeds the threshold level, it gives indications through buzzers and displays the condition on LCD Screen. It is made using the AVR Microcontroller which is programmed to take analog input from the temprature sensor (thermistor) and compare it with the threshold value and accordingly produce the output. It has huge applications in industrial machinearies and electronic products. 
# Requirements
## High Level Requirements
|ID| Requirements|
|-------|-------|
|HLR1	|System shall detect the temperature|
|HLR2	|The output shall be displayed on LCD Screen|
|HLR3	|Buzzer should produce noise when output is above threshold value|
|HLR4	|System shall reset when temperature again gets normal|
## Low Level Requirements
|High Level ID|	Low Level ID|	Requirements|
|-----------|---------------|--------|
|`HLR1`| LLR1	|Temperature Sensor shall detect the temperature and send input to the system|
|	 | LLR2	|The input shall be compared to the threshold temperature|
|	 | LLR3	|The temperature shall be displayed on LCD Screen|
|`HLR2`| LLR1	|Whenever temperature reaches threshold value, it should display warning message|
|	   |LLR2	|Whenever temperature goes above threshold value, it should display message|
|	   |LLR3	|It shall display temperature at every moment|
|`HLR3` |LLR1	|Buzzer shall work whenever the temperature passes threshold point|
|	   |LLR2	|Buzzer shall stop when the temperature again gets normal|
|`HLR4` |	LLR1|	The system should reset when the temperature get normal|
|	    |LLR2	|The system shall reset automatically|


