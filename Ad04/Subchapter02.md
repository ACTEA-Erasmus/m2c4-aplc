# Designing of a GRAFCET in IEC 60848
## GRAFCET diagram

| **Symbol**| **Description** |
|:---:      |:---             |
|![Grafcet Diagram](../Ad04/Images/GRAFCET_Diagram.jpg) | A GRAFCET diagram is a collection of steps, actions, transitions, connections, etc. which form a complete diagram. The collection of all elements is surrounded by a rectangle. |
|![Input Variables](../Ad04/Images/Input_variables.jpg) | **Input variables** are on the left with an incoming arrow <p><p>__Example__: "Initial step activation" and "installation started" inputs <p> ![Input Variables Example](../Ad04/Images/Input_variablesEx.jpg)                                                                                                    |
|![Output Variables](../Ad04/Images/Output_variables.jpg)| **Output variables** are located on the right with an outgoing arrow. <p><p>__Example__: "Forward" and "Backward" output signals.<p> ![Output Variables Example](../Ad04/Images/Output_variablesEx.jpg)                                                                                                                        |
|"*" | A **comment** clarifies the working of certain parts and is written between double quotation marks, whereby the asterisk symbol gets replaced by the description.<p><p>  __Example__: Stop a drain  pump if the level is too low. <p> ![Comments](../Ad04/Images/Comments.jpg)                               |

## Step
A **step** displays a defined condition of the sequential process. A step is either **Active** or **Not Active**.

On a certain moment during the sequential proces:
-   Is a step active or not active
-   The set of active steps determines the state of the process
-   The GRAFCET determines which step or steps can become active

| **Symbol** | **Descpription** |
| :---:      | :----            |
|![Step](../Ad04/Images/Step.jpg)       | A **step** is shown as a square with an unique label. For practical reasons the most commonly used label are numbers which replaces the asterisk symbol.<p><p> __Example__: Step 2 <p>       ![Step Example](../Ad04/Images/Step_2.jpg) |
| ![Initial Step](../Ad04/Images/Initial_Step.jpg) | The **initial step** characterizes the initial situation and is displayed as a double square. In case of the initial step being active, all other steps in the GRAFCET won’t be active.<p><p> __Example__: Step 0 <p><p> ![Initial Step Example](../Ad04/Images/Initial_StepEx.jpg) |
| ![Enclosed Step](../Ad04/Images/Enclosed_Step.jpg) | An **enclosed step** means that this step contains other steps. If the conditions after the enclosed step are TRUE, we will proceed to the next step and all internal steps will be inactive.<p><p> It is allowed that an enclosed step contains multiple GRAFCET diagrams, but the enclosed internal steps can only be assigned to one enclosed step. |
| ![Enclosed Initial Step](../Ad04/Images/Enclosed_Initial_Step.jpg)       | An **enclosed initial step** means that this step has multiple internal steps that participate in the initial condition.<p><p> The enclosed initial step contains minimum one internal initial step and can contain multiple GRAFCET diagrams. |
| ![Macro Step](../Ad04/Images/Macro_Step.jpg) | A **macro step** means that this step has multiple internal steps. We can describe it as an independent piece of software. A macro is not designed as standalone software, it’s meant to support a different piece of software. <p><p> The internal steps always start with a source step and always end with an end step. Only in the case of the end step being active can the macro exit. Unlike an enclosed step, a macro contains a maximum of one GRAFCET diagram and the asterisk symbol gets replaced by one unique label that can deviate from step labels, in numbered order. |
| ![Active Step](../Ad04/Images/Active_Step.jpg) |  In case that an **active step** needs to be displayed, this will be done by placing a point under the label.|

## Connections
| **Symbol** | **Description** |
| :---:      | :---            |
| ![Connectionelements](../Ad04/Images/Connectionelements.jpg) | Connections are lines in the network that connect steps. |
| ![Horizontal Connectionelements](../Ad04/Images/ConnectionelementsHorizontal.jpg) | Both horizontal and vertical lines are allowed. <p><p>Diagonal lines are to be avoided. They are allowed, but only to clarify. |
| ![Flow Connection](../Ad04/Images/FlowConnection.jpg) | The flow of a connection is always from top to bottom.<p><p> The use of arrows is allowed in case of clarification. |
| ![Disconnected](../Ad04/Images/Disconnect.jpg) | If a directed link has to be broken (for example for complex charts or when a chart covers several pages) the number of the destination steps and the number of the page on which it appears, shall be indicated. <p><p>__Example__: Reference to step 12 on page 2<p><p> ![Disconnected Example](../Ad04/Images/DisconnectEx.jpg)|

## Transition
| **Symbol** | **Description** |
| :---:      | :---            |
| ![Condition](../Ad04/Images/Condition.jpg) | A transition between two steps is indicated by a horizontal line right through the connection line. <p><p> The transition-condition is active if the previous step is active. <p><p> Between 2 steps one condition is allowed. |
| ![Condition Horizontal](../Ad04/Images/Condition_Horizontal.jpg) | It’s allowed to use vertical transitions for graphical reasons. |
| ![Transition Condition](../Ad04/Images/Transition_Condition.jpg) | Each transition contains a condition. This is a mathematical boolean expression composed by variables, they replace the asterisk symbol. The result of a transition-condition is TRUE or FALSE. <p><p>The transition-condition is always at the right of the transition. <p><p> __Example__: Start button AND stop button <p><p>![Transition Condition Example](../Ad04/Images/Transition_ConditionEx.jpg) |
| ![Transition Number](../Ad04/Images/Transition_Number.jpg) | The transition may have an unique designation ( ) at the left of the transition.<p><p> __Example__: Label 6 <p><p>![Transtion Number Example](../Ad04/Images/NumberingEx.jpg) |
| ![Always TRUE](../Ad04/Images/Always_TRUE.jpg) | A transition condition that is always TRUE is displayed with the underscored expression 1. |
| ![Step Status](../Ad04/Images/Step_Status.jpg) | The status of a step (active or not active) can be added in a transition-condition with the capital letter "X".<p><p> The asterisk symbol will be replaced by a label of the step.<p><p> __Example__: Step variable of step 7 |       |  |
| ![Increasing Flank](../Ad04/Images/Increased_Flank.jpg) | An upward arrow in the transition-condition means that it is only TRUE the moment the variable changes from FALSE to TRUE. <p><p>__Example__: The transition-condition is TRUE on a rising edge of the "Door is Open" sensor OR if the "Door Limit switch" is activated. ![Increasing Flank Example](../Ad04/Images/Increased_FlankEx.jpg)   |   |   |
| ![Decreasing Flank](../Ad04/Images/Decreasing_Flank.jpg)| A downward arrow in the transition-condition means that it is only TRUE the moment the variable changes from TRUE to FALSE.<p><p> __Example__: The transition condition is TRUE on a decreasing flank of the pallet fotocel.<p><p>![Decreasing Flank Example](../Ad04/Images/Decreasing_FlankEx.jpg) |
| ![Comparison Instruction](../Ad04/Images/Comparison_Instructionjpg.jpg)| A **comparison** is noted between [ ].<p><p> The asterisk symbol gets replaced with a comparison.<p><p>  The result of a comparison instruction is TRUE or FALSE. <p><p>__Example__: The transition-condition is TRUE in case the actual pressure is higher than 5,0 bar. <p><p> ![Comparison Instruction Example](../Ad04/Images/Comparison_InstructionEx.jpg) |
|![Time Condition](../Ad04/Images/Time_Condition.jpg) | A variable that is time dependent is displayed with the **/** symbols (TON / variable / TOF). <p><p> Hereby, the transition-condition is TRUE after an on-delay and stays TRUE with an off-delay. It is allowed to simplify the notation by removing the off-delay in case this isn’t used. <p><p>__Example__: The transition condition is TRUE 2 s after the iSen is TRUE  and stays 5s TRUE after iSen becomes FALSE.<p> ![Time Condition Example 1](../Ad04/Images/Time_VariableEx.jpg) <p><p>__Example__: 3 s after step 4 is activated the transition-condition becomes TRUE and step 5 will be activated.<p><p>![Comparison Instruction](../Ad04/Images/Time_ConditionEx.jpg)
| ![Source Transition Condition](../Ad04/Images/Source_Transition_Condition.jpg)  |  A **source transition-condition** is a transition-condition without previous steps. Each time the transition condition is TRUE, the next step will be activated. It is recommended to provide a transition condition with a rising or dropping flank to avoid the activation of the next step. <p><p>__Example__:The initialization step 0 will be activated on a rising flank from the initialization input signal.<p><p>     ![Source Transition Condition Example](../Ad04/Images/Source_Transition_ConditionEx.jpg) |
|  ![End Transition Condition](../Ad04/Images/End_Transition_Condition.jpg) |  An **end transition-condition** is a transition-condition where no steps follows. Each time the transition condition is TRUE, the upwards steps will be disabled.  <p><p>__Example__:  Sequence with initialization of a sourcestep where all steps get activated ![End Transition Condition Example](../Ad04/Images/End_Transition_ConditionEx.jpg)|
  Explanation symbolic image
  -	iInit = digital input – GRAFCET initialise
  -	iStarted = digital input – Result of a start-stop circuit
  -	iSen1 = digital input – Sensor 1
  -	iSen2 = digital input – Sensor 2

## Action
| **Symbol** | **Description** |
| :---:      |:---             |
| ![Action](../Ad04/Images/Action.jpg) | An **action** is assigned to a step and gets illustrated by a rectangle which is connected to that step with a horizontal line.<p><p> It is allowed to use multiple actions in the same step, if each of them have their own rectangle.<p><p> **Allowed multiple actions:** ![Action Example](../Ad04/Images/ActionEx.jpg) |
| ![Action Label](../Ad04/Images/Action_Label.jpg) | Each action has an action label which clarifies the executed task.<p><p> The label is written in the rectangle where the asterisk symbol is replaced by a variable.<p><p> A **continue action** will have the status of the variable TRUE the moment the corresponding step is active. All other moments the action is FALSE.<p><p>__Example__: The pump action is TRUE on step 4 and FALSE on step 5<p><p> ![Action Label Example](../Ad04/Images/Action_LabelEx.jpg) |
| ![Memory Action](../Ad04/Images/Memory_Action.jpg) | A **memory action** has a specific value assigned to a variable which gets stored. The asterisk symbol gets replaced by a variable and the \# symbol gets replaced by a (mathematical) value, formula, .... . <p><p>__Example__: The lamp gets activated in step 7, is still activated in step 8 and turns off in step 9. The internal variable "sX" is increased by 1 in step 8.<p><p> ![Memory Action](../Ad04/Images/Memory_ActionEx.jpg) | ![Conditional Action](../Ad04/Images/Conditional_Action.jpg) | A **conditional action** gets the status TRUE in case of the corresponding step being active and the assigned actioncondition is TRUE. <p><p>__Example:__ The disapproval lamp lights up in case the amount of disapproved parts are bigger then 3 in case step 5 is active. ![Conditional Action Example](../Ad04/Images/Conditional_ActionEx.jpg) |
| ![Conditional Action Example Time Dependent](../Ad04/Images/Conditional_Action_TimeDependant.jpg) | A time dependent **conditional action** is displayed with the / symbols. The action is TRUE after an on-delay and stays TRUE with an off-delay. It is allowed to simplify the condition by removing the off-delay in case this isn't used. <p><p>__Example__: 2s after "iSen" becomes TRUE valve A+ will be activated. 5s after "iSen" become FALSE valve A+ will be deactivated if step 9 is activated.![Conditional Action Example Time Dependent Example](../Ad04/Images/Conditional_Action_TimeDependantEx1.jpg) <p><p>__Example__: 3s after step 4 is activated the OK lamp lights up.<p><p>![Conditional Action Example Time Dependent Example](../Ad04/Images/Conditional_Action_TimeDependantEx2.jpg) |
| ![Memory Action Activation](../Ad04/Images/Memory_ActionActivation.jpg) | It is possible to run a memory action with the activation of a step. This is indicated with an upwards arrow. <p><p>__Example__: With the activation of step 8 the formula will be ran. <p><p>![Memory Action Activation](../Ad04/Images/Memory_ActionActivationEx.jpg) |  | ![Memory Action Deactivation](../Ad04/Images/Memory_ActionDeactivation.jpg) | It is possible to run a memory action with the deactivation of a step. This will be shown as a downwards arrow. |   |
Explanation of the used symbols:
-	oPump = digital output – Activation of a pump
-	oLmp = digital output – Activation of a lamp
-	oLmpOK = digital output – Activation of an OK lamp
-	oVlvA_1 = digital output – Activation of Valve A+
-	sX = static variable X
-	sNumNOK = static variable – Amount of NOK parts

## Structures
| **Symbol** | **Description**  |
| :---:      | :-----           |
| ![Sequence](../Ad04/Images/Sequence.jpg) |A **sequence** is a series of steps where each step contains max. one transition-condition.<p><p> The sequence is active if at least one step of the sequence is active. The sequence is inactive when all steps are inactive. |
| ![ Loop Sequence](../Ad04/Images/LoopSequence.jpg) | A simple **loop sequence** is a sequence of steps whereby each step contains max. one transition-condition and where the last step is connected to the first step. |
| ![ Sequence With Source Step](../Ad04/Images/SequenceWithSourceStep.jpg) | A **sequence with source step** has a step without previous transition- condition. <p><p>__Example__: Sequence with a initializing sourcestep.<p><p> ![ Sequence With Source Step Example](../Ad04/Images/SequenceWithSourceStepEx.jpg) |
| ![ Sequence With End Step](../Ad04/Images/SequenceWithEndStep.jpg) | A **sequence with end step** has a step where there are no transition- conditions after it. An end step (and a source step) are necessary with macros. |
| ![ Forward Sequence Jump](../Ad04/Images/ForwardSequenceJump.jpg) | It is possible to jump to a step with a **forward sequence skip**.<p><p> Notice that between 2 steps only one transition is allowed. |
| ![ Backwards Sequence jump](../Ad04/Images/BackwardsSequenceJump.jpg)       | It is possible to loop back with a **backwards sequence skip**. This makes it possible to repeat a sequence.<p><p> Notice that between 2 steps only one transition is possible. |
| ![ OR-Convergence](../Ad04/Images/OR-Convergence.jpg) | Using a **OR-convergence** makes it possible to choose between different sequences where between 2 steps only one transition is allowed. The designer needs to make sure that both sequences can't be activated at the same time. <p><p>__Example__: In the GRAFCET version A it is possible to activate both step 4 and 5. This can happen when "iSen1" and "iSen2" have the status TRUE and in the moment step 3 is active. In the GRAFCET version B it isn't possible due to the extended transition-condition.<p><p>![ OR-Convergence Example](../Ad04/Images/OR-ConvergenceEx.jpg) |
| ![ AND-Convergence ](../Ad04/Images/AND-Convergence.jpg) | A **AND-convergence** allows to activate parallel sequences at the same time. They will be started after a starting transition.<p><p> An startind AND-convergence is showed by means of a double line after the starting transition.<p><p> Once the parallel sequence is activated both sequences will run seperatly from each other.<p><p> An AND-convergence gets back ends if all the parallel end steps are active and the ending transition-condition is TRUE. An ending AND-convergence is showed by a double line before the ending transition. |

## Function rules
The **function of a GRAFCET** is in general step by step.
If a step is active and the transition condition(s) are met than the next step will be activated. If the next step gets activated the previous step will be deactivated immediately.

It is possible that the status of the different transtion-conditions the fucntion of a GRAFCET seems not to run step by step. It is the task of the designer to avoid that functions which can cause an unstable function of actions.

| **Function** | **Description** |
| :---         | :---            |
| ![ Non transient action ](../Ad04/Images/TransitionFunction.jpg) | A **non transient action**  will run step by step.<p><p> Situation: Step 4 active, iSen1 = iSen2 = Isen3 = FALSE <p><p> Function: iSen1 (1) is TRUE which activates step 5 and deactivates step 4. |
| ![ Transient Function ](../Ad04/Images/TransientFunction.jpg) | With a **transient action** the steps won't run step by step.<p><p> Situation Step 4 active, iSen1 = iSen3 = FALSE iSen2 = TRUE <p><p>Function: iSen (1) is TRUE which causes step 5 to be activated and step 4 gets deactivated. Because iSen3 (2) is true, step 6 will inmediatly be activated and step 5 will be deactivated.<p><p> Disadvantage: In case we use an action instead of a memory action, it is possible that the assigned actions of a transient step are not or transient executed (= unstable function).|
|       ![ And Convergence ](../Ad04/Images/ANDFunction.jpg)        | An **AND-convergence** parallel sequences will be started in case the previous transition condition is TRUE.<p><p> Situation 1: If step 1 is active and transition conditoin iGestart is TRUE then step 2 and 4 will be activated.   <p><p> Situation 2: Once the parallel sequences are activated they will run separatly.<p><p> Situation 3: Step 9 gets activated in case step 3 and step 6 are active and in case the transition-condition "iSen1.iSen2" is TRUE. |

## Example
The next example shows a GRAFCET for the functionality of a conveyor belt. A box is displaced 5x times from start to end before it stops. After this operation it is necessary to restart the installation.
<p><p>

![ Conveyor belt ](../Ad04/Images/ConveyorbeltEx.jpg)

<p><p>
The GRAFCET has the name FB_PE_BeltFwBw:

-   FB = GRAFCET will be programmed in a function block (FB)
-   PE = This part is a procedure element according ANSI/ISA S88 standard
-   BeltFwBw = Conveyor belt forwards & backwards

The conveyor belt is **started and stopped** by means of a start button and a stop button. The functionality of these buttons is not included in the GRAFCET but gets executed by an external start-stop basic circuit. The result of this start-stop basic circuit will be linked with the GRAFCET input variable "iStarted".
<p><p>
![ Start Stop exaple ](../Ad04/Images/StartStopEx.jpg)
<p><p>
Each time the stop button is pressed the conveyor belt will immediatly stop. When the start button is pressed again, the conveyor and GRAFCET continues where they ended.
<p><p>
![ Conveyorbelt GRAFCET ](../Ad04/Images/ConveyorbeltGRAFCET.jpg)
<p><p>
The **photocell** sensors on the conveyor belt detects the presence of the box when the infrared beam between photocell and reflector is interrupted. The status of the photocells (%I) is linked with the GRAFCET input variables "iSenFw" and "iSenBw".
<p><p>
![ Processing Sensors ](../Ad04/Images/ProcessingSensors.jpg)
<p><p>
Controlling the conveyor belt forwards and backwards will be determined by step 1 and step 2 on condition that the installation is started.
<p><p>
![ Controlling the conveyorbelt ](../Ad04/Images/UpwardsEx.jpg)
<p><p>
The effective **control of the conveyor belt** happens by the GRAFCET output variables "oBeltFw" and "oBeltBw" which are linked to the contactors (%Q) and the conveyor belt motor (asynchronous motor).<p><p>

![ Processing of contactors ](../Ad04/Images/ProcessingContactors.jpg)

Counting of the **number of backward and forward movements** is controlled by the internal INT variable "i". This variable is an internal function block parameter of the type STATIC. This makes it possible to remember the condition of variable "i" also without voltage (=retentive). <p><p>

![ Variable example ](../Ad04/Images/IncreasingVariableEx.jpg)
<p><p>
Increasing the variable "i" is executed in step 3, after which step 1 gets activated because there is a loop sequence between step 3 and step 1 but only if the value of the variable "i" is less than the decimal value 5. Noticed that the increasing of the variable "i" is only executed on the moment that step 3 is activated (rising edge). This is to prevent wrongly increasing the value of the variable in case step 3 is active longer the one PLC cycle.

In case the box went 5x backwards and forward this will be displayed with a green OK lamp. This lamp (%Q) is connected with the GRAFCET output variable "oOk". Now the installation needs to be stopped with the stop button before the installation can restart.
<p><p>

 ![ Lamp Processing ](../Ad04/Images/ProcessingLamp.jpg) ![ Lamp Processing ](../Ad04/Images/ProcessingLamp2.jpg)

<p><p>
It is possible to **initialize** the GRAFCET. This is the activation of the initial step (step 0) by using GRAFCET input variable "iInit". All the other active steps get deactivated. The initialising is only activated on the rising edge of "iInit".
<p><p>
![iInit Grafcet Example ](../Ad04/Images/iInitGRAFCET.jpg)

You could choose to initialize the installation in case you press the start and stop button simultaneously for 5 seconds or more.

![Activating iInit Grafcet Example ](../Ad04/Images/ActivatingiInitGRAFCET.jpg)
