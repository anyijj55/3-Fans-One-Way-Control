One-Way Fan Control System 

PLC Ladder Logic Description 

The PLC-based control system is designed to manage the operation of three fans (Fan1, Fan2, and Fan3) with the following sequence of operations: 

Start Sequence: 

Fan2 cannot be started unless Fan1 is running. 

Fan3 cannot be started unless Fan2 is running. 

Stop Sequence: 

Stopping must begin with Fan3, followed by Fan2, and then Fan1. 

Safety and Interlocks 

Interlocks: 

Fan1 and Fan3 cannot start unless Fan2 is running. 

Fan3 must stop before Fan2, and Fan2 must stop before Fan1. 

Emergency Stop: 

Include an emergency stop button (NC) to immediately de-energize all fan contactor coils, overriding the normal stop sequence. 

Fault Handling: 

Monitor fan status feedback for faults (e.g., motor overload or failure). 

If a fault is detected, stop all fans in the correct sequence and trigger an alarm. 

 

System Components 

Inputs: 

Start Button (NO - Normally Open): Initiates the start sequence. 

Stop Button (NC - Normally Closed): Initiates the stop sequence. 

Fan1, Fan2, and Fan3 Status Feedback (from motor contactors or sensors): Indicates whether each fan is running or stopped. 

Outputs: 

Fan1 Contactor Coil: Controls the operation of Fan1. 

Fan2 Contactor Coil: Controls the operation of Fan2. 

Fan3 Contactor Coil: Controls the operation of Fan3. 

PLC: 

The PLC processes the input signals and executes the control logic to manage the start and stop sequences of the fans. 

Safety and Interlocks 

Interlocks: 

Fan2 cannot start unless Fan1 is running. 

Fan3 cannot start unless Fan2 is running. 

Fan3 must stop before Fan2, and Fan2 must stop before Fan1. 

 

Sequence Summary 

Start Order: Fan1 → Fan2 → Fan3 

Stop Order: Fan3 → Fan2 → Fan1 

Further Design Considerations 

Timers: 

Use timers to introduce delays between start/stop sequences if required (e.g., to allow fans to reach full speed before starting the next fan). 

HMI Integration: 

Integrate an HMI (Human-Machine Interface) to provide operators with real-time status of the fans and control options. 

Manual Override: 

Include manual override options for maintenance purposes, allowing individual fans to be started/stopped independently (if necessary). 

Emergency Stop: 

Include an emergency stop button (NC) to immediately de-energize all fan contactor coils, overriding the normal stop sequence. 

Fault Handling: 

Monitor fan status feedback for faults (e.g., motor overload or failure). 

If a fault is detected, stop all fans in the correct sequence and trigger an alarm. 

 

 

 
