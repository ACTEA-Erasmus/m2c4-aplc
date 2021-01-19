# The Pick and Place Project
_____________________________________
-   The [first goal](../Ex02/Subchapter03.md) is to program a GRAFCET
-   The [second goal](../Ex02/Subchapter04.md) is to program a Flowchart
-   The [second goal](../Ex02/Subchapter05.md) is to deliver a working program

Back to the [project scope](../Ex02/Subchapter03.md)

## Goal 1: To program a GRAFCET
_____________________________________

**Step 1:**

Open the previous exercise Ex2-PickAndPlace.
```javascript
Filename : Ex2-PickAndPlace.ap16
```

**Step 2:**

Remove the function block that we previously ported into TIA.
```javascript
Functionblock : FB-P_PickAndPlace
```
**Step 3:**

Copy/download the included .zal file named. Make a new subfolder into automation called "Library"(If it doesn't exist already). Copy the file into:
```javascript
Filename : S88 GRAFCET.zap16
Destination : \Documents\Automation\Library
```
**Step 4:**

Open the archive as we did in Ex02. Here you'll find a template of a GRAFCET under "Master Copies" called "FB-P_GRAFCET". Drag this into your TIA portal project.

**Step 5:**

Rename the block to FB-P_PickAndPlace.

*Remark: The previous block "FB-P_PickAndPlace" in "FC_EM_PnP" will be red, to fix this right click on the block and press "Update block call".*

**Step 6:**

Program the following GRAFCET into FB-P_PickAndPlace.
![GRAFCET](../Ex03/Images/GRAFCET.jpg)
