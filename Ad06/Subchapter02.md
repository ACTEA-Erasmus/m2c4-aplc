# Physical part - Control modules
**Control modules** are software blocks that
  - Process sensor inputsingals (%I)
  - Activate / control output signals (%Q)

This way an control module gets represented of a certain type actuator or sensor and by preference gets included in the software library.
Control modules are preferably progammed in "Function buildblocks" whereby, The TAG-naming gets expanded with the letters CM.

_Examples_
| Tag | Processing of a digital sensor  |
|--|---|
| FB_CM_DI_Sensor |  Processing of an digital sensor |
| FB_CM_AI_Sensor | Processing of an analog sensor |
| FB_CM_ASM_1R1S	| Controlling an asynchronous motor with 1 speed and 1 rotating direction   |
| FB_CM_ASM_2R1S	   | Controlling an asynchronous motor with 1 speed and 2 rotating directions    |
| FB_CM_Valve   | Controlling of an (pressurised air) valve  |
| FB_CM_Relay   | Controlling of a relay |
| FB_CM_Lamp  | Controlling of a (LED) lamp  |
