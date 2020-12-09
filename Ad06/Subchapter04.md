# Analog sensors

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
