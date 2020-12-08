## Software model following ANSI/ISA-88

### The different parts

The ANSI/ISA-88 norm or the **S88 software model** is a norm that describes how a machine/installation (batch)process can be subdivided in different parts.

The advantage of this is that one big problem[^1] will be divided in different smaller partialproblems; smaller problems are often easier to solve than bigger problems. A strategy will be developed for each small partialproblem that will cause the bigger problems to disapear one by one.


[^1]: Within (proces)automation is this commonly the automation of an entire machine/installation.
The S88 software model divides a machine/installation proces in 3 big parts:

-   The physical part

-   The procedure part

-   The recept part

![S88 Software Design ](../Ad06/Images/S88_Softwaredesign.jpg)

Because the S88 software model is very abstract and expanded we will be using a very simple form in this course:


-   The backspine is the physical part

-   The procedure part gets integrated in the physic part.

-   The recept part won't be applied

This means that the software buildblocks only get designed for the processing of the physic part or only the procedure part.
The buildblocks will exhange information between each other.

The following chapters describe different buildblocks that are included in the software library. The operation of each individual buildblock is explained with the use of a operation scheme with the following symbols:

| **Symbol** | **Description**                                                                                                             |
|-------------|------------------------------------------------------------------------------------------------------------------------------|
|     ![AND port ](../Ad06/Images/AND.jpg)        | AND port                                                                                                                    |
|     ![OR port ](../Ad06/Images/OR.jpg)        | OR Port                                                                                                                     |
|      ![Not connection ](../Ad06/Images/NOT-connection.jpg)       | NOT connection                                                                                                               |
|        ![OR port ](../Ad06/Images/OR.jpg)     | Connection                                                                                                                   |
|     ![TON ](../Ad06/Images/TON.jpg)        | Risedelay                                                                                                              |
|        ![TOF ](../Ad06/Images/TOF.jpg)     | Drop-off delay                                                                                                             |
|      ![Time pulse ](../Ad06/Images/TP.jpg)       | Time Puls                                                                                                                     |
|             | A collection of instructions that together a combination basiccircuit form (in this case the start-stop circuit)  |
|       ![Positive flank ](../Ad06/Images/Pflank.jpg)      | Positive flank signal                                                                                                       |
|        ![Negative flank ](../Ad06/Images/Nflank.jpg)     | Negative flank signal                                                                                                       |

The operationscheme gets drawn up so that every incoming signal is as far to the left as possible and all output signals are to the right. Connections are wether or not drawn with dotted lines (with crossing lines) to avoid confusion.
