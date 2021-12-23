# Main Controller for UT22

By: Benjamin Liang, University of Toronto Formula SAE Racing Team Electrical Member

The University of Toronto Formula SAE Racing Team (UTFR) is a formula student design team affiliated with the University of Toronto. In this article, we will explore the main controller for UT22, the team’s car for competition in 2022. This PCB controls the car’s power distribution, powertrain signals, sensor data acquisition, cooling system, and battery management system.

![image](https://user-images.githubusercontent.com/82067858/147109720-74ea52db-8d4e-44a3-a0c4-77e4b8366732.png)

This controller and article were made in collaboration with JLCPCB (https://jlcpcb.com/RAT). Founded in 2006, JLCPCB (https://jlcpcb.com/RAT) is a leading global PCB manufacturer with over 15 years of experience providing the best customer experience through the rapid production of highly reliable and cost-effective PCBs.

![image](https://user-images.githubusercontent.com/82067858/147109743-40eabf92-b9cf-4ee2-92ed-464ab6ecb206.png)

Controller Design

The controller design is centered around an Atmega 2560 as the primary MCU (microcontroller unit) connected to an Atmega 328 as the secondary MCU. The Atmega 2560 is responsible for controlling the car’s eFuses (electronic fuses) in the power distribution system, battery management system, sensor data acquisition, inverter communication, dash lights and cooling system. The Atmega 328 is dedicated to processing drive critical signals such as brake and accelerator pedal positions and wheel speed data for traction control.

![image](https://user-images.githubusercontent.com/82067858/147109778-b2a0bc5e-d762-4b36-9f88-aa8d48592cd6.png)

The power distribution architecture within the board consists of power coming directly from the car’s LiPo battery some of which is regulated to 12V, 5V, and 3V. The unregulated power distribution as well as the 12V, and 5V regulators are shown below.

![image](https://user-images.githubusercontent.com/82067858/147109803-79dc60cd-afc9-4ca3-91ab-e7819ea7deaa.png)

Almost all power supplied to offboard components are protected by mechanical fuses, or eFuses that are controlled by the Atmega 2560. The mechanical fuse holders are shown in the figure above for the MTR_PUMP_HSD (motor coolant pump high side drive) and INV_PUMP_HSD (inverter coolant pump high side drive). Five of the controllers 12V eFuses are shown below.

![image](https://user-images.githubusercontent.com/82067858/147109826-ce5cedbf-e468-4543-a8c1-559c8e2f5450.png)

The controller also includes two CAN (controller area network) modules consisting of a CAN controller and transceiver used for communication with other nodes within the car’s data acquisition architecture.

![image](https://user-images.githubusercontent.com/82067858/147109843-5fb27407-0c7e-4e90-a4fc-2a6fb99a728c.png)

PCB Design
Altium Designer, a PCB and electronic design application was used to design the main controller. The controller circuits were created by placing the required components on schematics and wiring them together in the required configuration. Each component is assigned a footprint that represents the physical dimensions of the component. Once the designer is satisfied with the PCB layout, the footprints are then routed in the exact manner shown in the schematics. The project can then be saved and the Gerber files exported.

![image](https://user-images.githubusercontent.com/82067858/147109863-4891238d-ed5f-416d-b2e9-f25141fa08cc.png)

PCB Ordering

The main controller was ordered from JLCPCB (https://jlcpcb.com/RAT) for quick, reliable, and cost-effective manufacturing. This ordering process is extremely simple and consists of the following four quick steps:
1.	Export Gerber files from Altium
2.	Click on the quote now button on the JLCPCB (https://jlcpcb.com/RAT) website
3.	Upload the Gerber files and double-check the PCB in the Gerber viewer then
4.	Click save to cart, select your shipping and pay.

JLCPCB (https://jlcpcb.com/RAT) automatically detects all the PCB specifications, and fills out the order form for you.
