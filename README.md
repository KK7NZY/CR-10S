# CR-10S
Marlin 2.0.x firmware configuration with BLTouch and EZR Struder.

### Upgrade Parts
- [SeeMeCNC EZR Struder](https://www.seemecnc.com/products/ezrstruder)
- [Capricorn Bowden PTFE Tubing](https://www.filastruder.com/collections/e3d-spare-parts-and-accessories/products/capricorn-ptfe-tubing)
- [Creality 3D Printer BL Touch Auto Bed Leveling Sensor Kit](https://www.amazon.com/gp/product/B0859T6JVC/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&psc=1)
- [Befenybay Upgrade 2020 Profile X-axis Synchronous Belt Tensioner](https://www.amazon.com/gp/product/B087YWMHM2/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)
- [Befenybay Upgrade Y-axis Synchronous Belt Tensioner](https://www.amazon.com/gp/product/B07XQH1FPN/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)

### 3DMN Z-Offset Callibration Instructions
  1. Home 3D printer
  2. `M851 Z0` - Reset Z0Offset
  3. `M500` - Store setting to eeprom
  4. `M501` - Set active parameters
  5. `M503` - Display Active Parameters
  6. `G28 Z` - Home Z Axis
  7. `G1 F60 Z0` - Move nozzle to true 0 offset
  8. `M211 S0` - Switch off soft endstops
  9. Move nozzle towards bed slowly until the paper can barely move
  10. Take note of the Z on the printer display (take that number and add the measurment of the calibration sheet or device used)
  11. `M851 Z X.XX` (X.XX being your z offset achieved)
  12. `M211 S1` - Enable Soft Endstops
  13. `M500` - Save settings to Eeprom
  14. `M501` - Set Active Parameters
  15. `M503` - display current settings

### Resources
**Videos**:
 - [Installing the BLTouch on the CR-10S](https://www.youtube.com/watch?v=fPUXS1lFPYQ)
 - [Calibrating Z-Offset With A BLTouch Bed Levelling Probe](https://youtu.be/y_1Kg45APko)

**Firmware**:
  - [Marlin](https://marlinfw.org/meta/download/)
  - [TH3D Unified Firmware Package](https://support.th3dstudio.com/hc/en-us/articles/360043293452-TH3D-Unified-Firmware-Package)
