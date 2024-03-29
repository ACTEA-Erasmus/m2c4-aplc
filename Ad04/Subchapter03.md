# GRAFCET programming in LAD/FBD using BOOL
_____________________________________
Converting a **GRAFCET design to software code** is demonstrated with the GRAFCET described in subchapter 2.

The GRAFCET is programmed in the LAD or FBD programming language in the function block (%FB) with the use of STATIC parameters. STATIC parameters can remember their status without the PLC being powered on if they are configured to retain.

![Interface variables ](../Ad04/Images/SiemensVarLAD.jpg)

The programming is split into **3 parts** which are chronologically programmed in different networks:
-   Initialization (network 1)
-   Transition-conditions (network 3 ... x)
-   Actions (network x+1 ... last network)

The **GRAFCET programming in LAD/FBD with BOOL** follows the next rules
-   Each step is repesented by an unique BOOL variable
-   This variable is an ARRAY of BOOL starting with 0 and ending with max. step number
-   In case the corresponding variable is TRUE, the step will be active
-   Input "iInit" is always present which causes the activation of the initial step on a rising edge of this input
-   Input "iStarted" is always present which processes the result of an external start-stop basic circuit

![FBD  ](../Ad04/Images/SiemensiInitLAD.jpg)
![FBD  ](../Ad04/Images/SiemensFBD.jpg)
![FBD  ](../Ad04/Images/SiemensFBD2.jpg)
![FBD  ](../Ad04/Images/SiemensFBD3.jpg)
![FBD  ](../Ad04/Images/SiemensFBD4.jpg)
![FBD  ](../Ad04/Images/SiemensFBD5.jpg)
![FBD  ](../Ad04/Images/SiemensFBD6.jpg)

| **Advantages** | **Disadvantages** |
| :---:          | :---:             |
| Simplicity (1 step = 1 variable) | Initial step is not activated during the first download of the program |
|                                | Monitoring of active steps is complicated        |
