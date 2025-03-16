**Project title:** Vehicle Dashboard by using Can Communication 🚗🚗🚗🚗 


**Description:** Developed Vehicle Dashboard by using can node. I have used 4 node for this project. out of 4 node, 1 node is centralized node. that centralized node is control and monitoring the other 3 nodes real-time activities. Remaining 3 node are receiving and send there real-time data to the centralized node. The Centralized node is connect with one LCD. using LCD display the real time information. using this real-time information we can enhanced safety and enhance vehicle functionality.

👉👉**Note: I developed this projects only for testing purpose and my understanding purpose only. how this protocols are working. these are written and experienced in during my course. I can shared this project with you. And also test my knowledge with microcontrollers.**


Requirements:

Software Requirements: C, Embedded C.

Hardware Requirements: Microcontrollers, CAN transreceiver - MC2551, CAN Controller - MC2515, Fuel Sensor, Analog to digital convertor - MCP3204, LCD, LED, Motor.

Tools: Keil IDE for develop the firmware code, flash Magic for flash the code to controller.


**Explanation:**

Transmit and Receiving Realtime data with help of CAN bus. one centralized node controlling other 3 nodes. centralized node is connect with LCD that node is act as a Vehicle dashboard that will be display real-time activities with help of LCD. Based on user Requirement  the Centralized node send data to other nodes and control the activities. Receiving information from other node by using can network and display the data on LCD. Centralized node Controlling other node with help of Switch.

Node description:
* Node 1 - act as vehicle dashboard it has request data from other node and collect it and display it on LCD.
* Node 2 - act as fuel monitor. it continuously monitoring the fuel level by using capacitive fuel sensor.
* Node 3 - act as a LED Indicator Controller. this node receive the data from node1 and activate and deactivate the LEDs.
* Node 4 - act as Wiper Controller. this node also receive the data from node1. it will analyze the received data based on information it will turn on the wiper and control the wiper with 3 mode of speed. Controlling the 3 mode of speed with help  of PWM.


**Problem faced:**

I working with LCD. The LCD display the message based on real-time activities by triggered by condition(Press Sw). However, after flashing the code to microcontroller. i observed that all message were displayed sequentially on the first line of the LCD. Even though the condition not also met.
	
 Scrolling function issue:
		
  * At begging of my code, i implemented a scrolling effect for displaying my project title.
  * The scrolling function extract string to individual char by char.
  * To achieve this string to char i used increment operator in string to char converting function.
  * Problem faced in scrolling function with handled incorrect string length. 
	
 Rectification:
 
 * I handled within loop incorrect string length in scrolling function. The loop access individual char memory location. it after completing project title length. function fetch nearby memory location. that nearby memory location is next string starting address. i find this and rectify it
