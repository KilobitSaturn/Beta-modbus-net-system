# Beta-modbus-net-system
Project with two PLCs via MODBUS/RS485 (COM2): one master and one slave. The slave measures temperature using a thermocouple and sends it to the master; both exchange analog voltage values ​​and digital states (switches/LEDs) via input registers, holding registers, discrete inputs, and coils, with display on HMIs.

# Activity
This work aims to develop and validate an industrial communication system using the **MODBUS** protocol over an **RS485** network, integrating two Programmable Logic Controllers (PLCs) configured in a master-slave architecture. The proposal involves the practical implementation of fundamental concepts of industrial automation, serial communication, and variable mapping in industrial networks.

In this activity, one of the PLCs is configured as a **MODBUS master**, while the other acts as a **MODBUS slave**, being physically interconnected through COM2/RS485 ports using cables with RJ45 connectors. The system must allow bidirectional exchange of digital and analog data between the two controllers, correctly using the register types of the MODBUS standard.

The slave PLC is responsible for measuring the temperature using a thermocouple connected to its appropriate input. This value must be processed internally, correctly scaled (considering a full-scale value of 30000 for analog inputs), and displayed on its Human-Machine Interface (HMI) with two decimal places and the appropriate unit. Furthermore, the slave must receive the voltage value measured at the master's analog input via MODBUS and display it on its own HMI.

In turn, the master PLC must measure its own analog input (also with a full-scale value of 30000), convert the value to actual voltage, display it on its HMI, and simultaneously read the temperature value acquired by the slave, also displaying it correctly formatted with units and two decimal places.

Analog communication must utilize the functions of reading **Input Registers** and writing **Holding Registers**, while digital communication must employ reading **Discrete Inputs** and writing **Coils**. Thus, when a switch (digital input) is activated on one of the PLCs, the command must traverse the MODBUS network and activate the corresponding LED (digital output) on the other PLC, ensuring cross-control between the workstations.

A key aspect of the project is the prior planning of the communication strategy, including the organized definition of the variable map, MODBUS addressing, association with internal operands (as in MasterTool), and structured documentation of the implemented logic.

In general, the work consolidates knowledge in instrumentation, industrial communication, analog signal scheduling, HMI integration, and distributed systems organization, simulating a real-world industrial network application widely used in the automation sector.
