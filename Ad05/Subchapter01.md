## Characteristics and defenitions

Controllers are used mainly to control continuing processes. Also non continuing can be controlled. This way a GRAFCET can run t he controller as action in a determined step. We use analog sensors to control analog or digital actuators.

Controllers are defined by several Characteristics which are explained in the table below.


| **Definition**         | **Abbreviation** | **Description**                                                                                                                                                                                                                                                                                               |
|--------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Process value     | X *PV*        | The value measured by the analog sensor *German name = Istwert*                                                                                                                                                                                                          |
| Setpoint   | W *SP*        | The value that we want to achieve. *German name = Sollwert*                                                                                                                                                                                                                   |
| Loop manipulated value      | Y *LMN*       | The result that the actuator that affects the process adjusts *German name = Regelabweichung*                                                                                                                                                                   |
| Error      | E *ER*        | Difference between measured values and the setpoint *German naming = Stellgrösse*                                                                                                                                                                                                     |
| Hysteresis         | H             | The area wherein an actuator gets turned on and off.                                                                                                                                                                                                                                                      |
| Dead band          | XDo *Db*      | The area in which multiple digital acutators get turned off. With analog actuators the status of the output that isn't in the dead band changes.H *German name = Bandbreite*                                                                                                 |
| Dead time         | T0/Tt Td      | The time delay between the change of the loop manipulated value and the change of the measured value. *German name = Totzeit*                                                                                                                                                     |
| Gain        | Kr *GAIN*     | The proportional action or P-action amplifies the output in proportion to input. The magnitude is determined by the gain factor, which can be positive or negative.                                                                                              |
| Reset time     | TI            | The integrating action ensures a constant sum of the error and keeps outputting more signals depending on how long an error exists between the measured and desired value. The integrator or I action is characterized by the time response of the integrator  |
| Derivative time | TD            | The D action responds to the rate of change of the error. So only when creating a step will the D action give its contribution to the controller. The differentiating action or D action is characterized by the time response of the differentiator           |


The measure difference is the difference between the loop manipulated value and the measured value.

E=W-X

Notice that the control difference can have a positive or a negative value.
