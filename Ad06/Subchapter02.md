# Sensors
## Digital sensor
A **digital sensor** (Ex.:limit switch, inductive sensor, capacitive sensor, tuning fork,...) processes mainly the presence of a product, object, person, etc. It has 2 conditions which indicate wether these products, objects or persons are preset or not.

Functionally seen these sensors monitor:
- The correct automatic process wether or not with the needed delay (example, opening of a door with the help of a photcell after which the door stays open for a bit)
- The protection against defects (example, overflow protection )

One can design a buildblock wherein all the above functionalities are processed. As a Consequently, this buildblock is the software repesentative of a digital sensor.

![S88 Example Digital Sensor ](../Ad06/Images/ObjectDigitalSensor.jpg)

This buildblock belongs to the grop of **control modules** are provided with following functionalities:
-  The module will ensure that the sensor signal (iSen) wether or not delayed with a on-delay(iTON_Time) and/or a off-delay (iTOF_Time) for a correct operation, which then provides the output signal (oSen_TO)
- In case the option alarm (iAL_Option) is enabled, the module will activate an alarm(ioAL_Sen) as soon as the sensor (iSen) is disabled. Taking into account the off-delay(iAL_Time).
- If the sensor(iSen) isn't switched on anymore, the module will tur off the alarm(ioAL_Sen) as soon as it gets reset(iReset)

It is possible with the description to draft a operation scheme for the control module with the name FB_CM_DI_Sensor.

![operation scheme control module FB_CM_DI_Sensor ](../Ad06/Images/OperationschemeCMFB_CM_DI_Sensor.jpg)

This results into a "Function buildblock" which looks like the following images.
| Text | Image |
| --|---|
| FDB example  | ![TIA image of control module FB_CM_DI_Sensor ](../Ad06/Images/TIA-FB_CM_DI_Sensor.jpg)  |
| More simple example  | ![Simple image of control module FB_CM_DI_Sensor ](../Ad06/Images/SimpleFB_CM_DI_Sensor.jpg)  |

## Analog sensors

It is possible to process for example: the current level of a liquid with a **analog sensor** in a programmable manager "sturing". It's needed to convert the number given to the correct SI-unit, this is because the current value isn't given in the correct SI-unit (ex. : mm). A unipolar sensor is only capable of converting a positive signal (ex. 0 .. 20mA, 4 .. 20mA, 0 .. 10 V, ...). A bipolar sensor processes both positive and negative signals (ex. -10V .. + 10 V).

An **control module** for this type sensors has the following tasks:
- Converting the provided number (iSen) which is a mirror of the measured value, to a SI-unit (oX) whereby taking into account with unipolar and bipolar signals (iUniOption) and the max. (iHiLim) en min. (iLoLim) measure range of the analog sensor.
- Making an alarm (ioAL_Sen) in case of a abnormal situation (ex. cablebreak or overcurrent)
- If the abnormal situation is fixed will the module turn off the alarm as soon as it gets resetted (iReset)

![Object of a analog sensor ](../Ad06/Images/ObjectAnalogSensor.jpg)

It is possible with the description to draft a operation scheme for the control module with the name FB_CM_AI_Sensor.

![Operation scheme control module FB_CM_AI_Sensor ](../Ad06/Images/OperationschemeCMFB_CM_AI_Sensor.jpg)

Notice that the operationscheme is drafted for analog sensor that work following the Siemens principal, they have a normal range of 0 .. 27.648 / -27648 .. + 27648.

The endresult is a "Function buildblock" which looks like the following images.

| Text | Image |
| --|---|--
| FDB example  | ![TIA image of control module FB_CM_AI_Sensor ](../Ad06/Images/TIA-FB_CM_AI_Sensor.jpg)  |
| More simple example  | ![Simple image of control module FB_CM_AI_Sensor ](../Ad06/Images/SimpleFB_CM_AI_Sensor.jpg)  |
