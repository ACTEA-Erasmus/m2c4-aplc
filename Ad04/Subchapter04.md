# GRAFCET programming in LAD/FBD using INT

Converting a **GRAFCET design to software code** is demonstrated with the GRAFCET described in subchapter 2.

The GRAFCET is programmed in the LAD or FBD programming language in the function block (%FB) with the use of STATIC parameters. STATIC parameters can remember their status without the PLC being powered on if they are configured to retain.

![Siemens VAR ](../Ad04/Images/SiemensVarINT.jpg)

The programming is split into **3 parts** which are chronologically programmed in different networks:
-   Initialization (network 1)
-   Transition-conditions (network 3 ... x)
-   Actions (network x+1 ... last network)

The **GRAFCET programming in LAD/FBD with INT** follows the next rules
-   Only the actual step needs to be known
-   The actual step is represented by an STATIC INT variable (step)
-   The initial value of this variable is the decimal value 0
-   The actual value of this variable corresponds to the active GRAFCET step
-   The initial step is automatically activated the first time the software is downloaded to the PLC; this is because the INT number initial value is equal to the decimal value 0
-   Input "iInit" is always present which causes the activation of the initial step on a rising edge of this input
  - Input "iStarted" is always present which processes the result of an external start-stop basic circuit

![INT ](../Ad04/Images/SiemensINT1.jpg)
![INT ](../Ad04/Images/SiemensINT2.jpg)
![INT ](../Ad04/Images/SiemensINT3.jpg)
![INT ](../Ad04/Images/SiemensINT4.jpg)
![INT ](../Ad04/Images/SiemensINT5.jpg)
![INT ](../Ad04/Images/SiemensINT6.jpg)

| **Advantages** | **Disadvantages** |
| :---:          | :---:             |
| Initial step is activated during the first download of the program | More complex, advanced programming then with LAD/FBD BOOL method |
| Monitoring of active steps is easier | Programming of AND-convergence is more complex then with LAD/FBD BOOL variant |
