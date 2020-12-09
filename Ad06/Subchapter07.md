# Valve

A valve is used to power compressed air or hydraulic actuators (ex. compressed air cylinder). The combination of a valve and actuator has a specific funcionality:
- Monostable power circuit: In case there is a loss of power the actuator will automatically take its residual state (ex. single-acting compressed air cylinder)
- Bistable power circuit: In case there is a loss of power the actuator will keep the last position (ex. double-acting compressed air cylinder)
- Monostable control circuit:  In case there is a loss of power in the control circuit the valve will automatically take its residual state (ex. 3/2 valve with spring return)
- Bistable control circuit: In case there is a loss of power in the control circuit the valve will automatically keep its last state (ex. 5/2 valve with electromagnetic control on both sides)

A **control module** for a valve will be build without taking into account the already existing functions of the combination valve - actuator. The control module will work following the bistable process.

**Why would you use a monostable valve and cylinder?**

During the design of a machine/installation one needs to ask themselves: What can go wrong during a unexpected event? How do i take care of potential risk to a human? Following the machine guidelines, no moving part of the machine or no single object that is held by the machine can be dropped or ejected. (2006/42/EG,2006)

Unexpected events like for example a fire, an accident, an earthquake, a flood, etc. can cause interruptions in the control- and/or power circuits. The interruption of these circuits can cause dangerous situations.

_Example_

Because of a fire in a technical room, the air compressor stopped working which has the side effect that there is no more compressed air. A robot that moves part of +/- 2 kg on highspeed is equipped with a pneumatic grabber "grijper". There is the danger that in case the compressed air falls away on the moment the robot moves at high speed, that the robot lets go of the object and basically trows away the object. This has the potential to hurt humans that work near the robot.

In this situation one choses a monostable compressed air cylinder with spring return, this will keep the grabber "grijper" to remain closed in case the compressed air falls away.

The functionality of this type control module:
- The control module will work following a bistable principal;
-  - In case the thinkprocess asks to activate the "+" side of the valve (iAut_1) the control module will do this (oVen_1) and it will keep the condition in case the thinkprocess doesn't ask for it anymore, until the "-" side gets activated
-  - In case the thinkprocess asks to activate the "-" side of the valve (iAut_0) the control module will do this (oVen_0) and it will keep the condition in case the thinkprocess doesn't ask for it anymore, until the "+" side gets activated
- The control module will only change the condition of the electromagnetic control in case this is allowed (Enable)
- If the hand mode is active (iModeHand) the control module ignores the thinkprocess signals (iAut_1 & iAut_0) and sends the valve (oVen_1 & oVen_0) commands based off the hand signals (iHand_1 & iHand_0)

It is possible with the description to draft a operation scheme for the control module with the name FB_CM_Valve

![Operationscheme for a valve ](../Ad06/Images/OperationschemeFB_CM_Vlv.jpg)

The endresult is a "Function buildblock" which looks like the following images.

| Text |Image |
| :---:      | :----            |
| FDB example  | ![TIA image of control module FB_CM_Valve](../Ad06/Images/TIA-FB_CM_Valve.jpg)  |
| More simple example  | ![Simple image of control module FB_CM_Vavle ](../Ad06/Images/SimpleFB_CM_Valve.jpg)  |
