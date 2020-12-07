# GRAFCET programmation in ST

Converting a **GRAFCET design to softwarecode** is demonstrated with the GRAFCET described in subchapter 2.

The GRAFCET is programmed in the LAD or FBD programming language in the function block (%FB) with the use of STATIC parameters. STATIC parameters can remeber their status also without voltage if they are configured as retain.

![Siemens ST ](../Ad04/Images/SiemensVARST.jpg)                       |

The programmation is split into **3 parts** which are chronologically programmed in different networks:
-   Initialisation (network 1)
-   Transition-conditions (network 3 ... x)
-   Actions (network x+1 ... last network)

The **GRAFCET prgramming in ST** is submitted to the next rules
-   The use of CASE .. OF .. ELSE control structure which handles the processing of transition-conditions
-   Only the actual step needs to be known
-   The actual step is represented by an STATIC ANY_INT variable (step)
-   The intial value of this variable is the decimal value 0
-   The actual value of this variable corresponds to the active GRAFCET step
-   The initial step is automatically activated the first time the software is downloaded to the PLC; this because the INT number initial value is equal to the decimal value 0
-   Input "iInit" is always present which causes the activation of the initial step on a rising edge of this input
-   Input "iStarted" is always present which is the result of an external start-stop basic circuit signal that gets send to the GRAFCET

![STL ](../Ad04/Images/SiemensST.jpg)
![STL ](../Ad04/Images/SiemensST2.jpg)
![STL ](../Ad04/Images/SiemensST3.jpg)
![STL ](../Ad04/Images/SiemensST4.jpg)

| **Advantages**| **Disadvantages** |
| :---: | :---: |
| Initial step is not activated while the the first download of the program | Complexer programmation than LAD/FBD variant |
| Smaller programmation then LAD/FBD variant | Programmation of AND-convergence is complexer than the LAD/FBD BOOL variant |
| Monitoring of the active steps are easier | Debugging [^3] in ST is harder than in FBD/LAD |

[^3]: Debugging = Searching for (programmation) faults
