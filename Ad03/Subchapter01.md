# HMI programming in Siemens TIA Portal V16
## Introduction

Due to production processes are becoming more and more complex and requirements for machine and plant functionality are increasing, operators need a powerful tool for controlling and monitoring production plants. An HMI system (human-machine interface) represents the interface between man (operator) and process (machine/plant). It is the controller that actually controls the process. Hence, there is an interface between the operator and WinCC (at the HMI device) and an interface between WinCC and the controller.

## Device description

The SIMATIC HMI Basic Panels product line features key and touch panels (operator input via keyboard and touch screen)
SIMATIC HMI Basic Panels cover all requirements described in the previous section.

## Hardware configuration

For a HMI to be correctly used in TIA Portal V16, one will need to make the right hardware configuration. For this to be correct you will need a correct CPU configuration mentioned in M2C3-ADD03.

To add a HMI to a current project you will have to add a new device. This can be done through the 2 views within TIA portal.

| Project View | Portal View |
| :---: | :---: |
|  "New Device"  |  "Devices & network > Add new device" |
| ![TIA Portal Adding HMI](../Ad03/Images/Step1.jpg)  |  ![TIA Portal Adding HMI](../Ad03/Images/Step1-1.jpg) |

The menu that pops up has 3 main options to select between Controllers / HMI / PC systems. For our example we'll be needing the HMI tab:

![TIA Portal Adding HMI](../Ad03/Images/Step2.jpg)

After which you select the desired HMI. HMI > SIMATIC Basic Panel (we'll be using the simulator of TIA Portal, for this example i took the KTP1500 Basic):

![TIA Portal Adding HMI](../Ad03/Images/Step3.jpg)
