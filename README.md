# Mini-Desktop-Printer
A Miniature Desktop 3D Printer based off of the DICE 3D printer. 

*Note - This printer is still a WIP. Some parts are incomplete (notably no power input, the enclosure is incomplete, the electronics cooling is not yet implemented, and cable management has not yet been fully implemented)*
*Note also that the model is missing certain components (such as belts and controller board), due to added complexity. These may be added in the future.* 

## Specifications:
 - 210mm x 210mm x ~326mm (X x Y x Z) Outer Dimensions (optional enclosure adds to this)
 - 110mm x 100mm x 100mm Theoretical Build Volume. (These are the physical limits of the design. Actual build volume may vary on implementation)
 - Full Stainless Steel and Aluminum Frame with Minimal Printed Parts.
 - MGN9c X and Y rails, MGN12c Z rails.
 - CoreXY design.
 - Lightweight Direct Drive Extruder
 - Full metal Z-Axis with Leadscrew. Room for Mandala Roseworks Oldham coupler (Will lose Z height, however)
 - Dual 4010 Blower Fans for Part Cooling
 - 3010 Axial Fan for Hotend Cooling.

## Purpose:
 - This printer was designed with the primary goal of being a very fast, very reliable prototyping machine, which would fit on a small space left on my desk.
  - As this printer was intended to sit on my desk, Another goal was quiet operation.

PICTURE GOES HERE
 
## Design Inspiration/Credit
 - This printer was heavily inspired by the [DICE](https://rene-jurack.de/dice/) 3d printer by Rene Jurack.
 - The printer was designed to utilize the [Sherpa Mini Extruder](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) designed by Annex Engineering
 - The Z-axis of this printer was also heavily inspired by the [Voron v0](https://github.com/VoronDesign/Voron-0) (original release, not 0.1)
 - The Toolhead of this printer utilizes a "Mosquito Net" (as coined by Annex Engineering), to reinforce the lower portion of the mosquito hotend heatsink. The concept, and implementation was utilized in this printer, based on measurements from the cad found [Here](https://github.com/Annex-Engineering/Annex_Engineering_PCBs/tree/master/mosquito_net-brace) and [Here](https://github.com/Annex-Engineering/Chhogori-K2-Basecamp-Edition)


