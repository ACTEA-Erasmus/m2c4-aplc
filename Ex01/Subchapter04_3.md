# The Crane Project
_____________________________________
## Overview
-   The [first goal](Ex01/Subchapter04_1.md) is to add ProfiNET based devices
-   The [second goal](Ex01/Subchapter04_2.md) is to add Profibus based devices
-   The [third goal](Ex01/Subchapter04_3.md) is to add Drives

Back to the [project scope](Ex01/Subchapter04.md)

## Goal 3: to add Drives

**Step 1:** Search for the correct GSD file for the following device:
```javascript
Control Techniques Commander C300
```

**Step 2:** Link the drive to the PLC

![Networkview](../Ex01/Images/Networkdrive.jpg)

**Step 3:** Add some inputs and inputs into the drive (4IN words & 4OUT words). These words are necessary to create communication through status words & control words.

**Step 4:** Compile the entire project and check for errors

__Normal functionallity__
- TIA compiles the project without issues
