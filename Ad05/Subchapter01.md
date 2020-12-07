## Characteristics and defenitions

Controllers is used mainly to control continues processes. Also not continue can be controlled. This way a GRAFCET can in a determined step run the controller as action. We use analog sensors to control analog or digital actuators.

Controllers are defined by several Characteristics which is explained in the tabel below.


| **Definition**         | **abbreviation** | **Description**                                                                                                                                                                                                                                                                                               |
|--------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Process value     | X *PV*        | The value measured by the analog sensor *German naming = Istwert*                                                                                                                                                                                                          |
| Setpoint   | W *SP*        | The value that we want to achieve. *German naming = Sollwert*                                                                                                                                                                                                                   |
| Loop manipulated value      | Y *LMN*       | The result that the actuator that affects the process adjusts *German naming = Regelabweichung*                                                                                                                                                                   |
| Error      | E *ER*        | Difference between measured values and the setpoint *German naming = Stellgrösse*                                                                                                                                                                                                     |
| Hysteresis         | H             | The area wherein a actuator gets turned on and off.                                                                                                                                                                                                                                                      |
| Dead band          | XDo *Db*      | The area in which multiple digital acutators gets turned off. With analog actuators changes the status of the output that isn't in the dead band.H *German naming = Bandbreite*                                                                                                 |
| Dead time         | T0/Tt Td      | The time delay between the change of the loop manipulated value and the change of the measured value. *German naming = Totzeit*                                                                                                                                                     |
| Gain        | Kr *GAIN*     | The proportional action or P-action amplifies the output in proportion to input. The magnitude is determined by the gain factor, which can be positive or negative.                                                                                              |
| Reset time     | TI            | DThe integrating action ensures a constant sum of the error and keeps outputting more signal depending on how long an error exists between measured and desired value. The integrator or I action is characterized by the time response of the integrator  |
| Derivative time | TD            | The D action responds to the rate of change of the error. So only when creating a step will the D action give its contribution to the controller. The differentiating action or D action is characterized by the time response of the differentiator           |


The measure difference is the difference between the loop manipulated value and the measured value.

E=W-X

Notice that the controldifference can have both a positive or a negative value.
