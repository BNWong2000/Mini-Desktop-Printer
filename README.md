# Mini-Desktop-Printer
A Miniature Desktop 3D Printer based off of the DICE 3D printer. 



*Note - This printer is still a WIP. Some parts are incomplete (notably no power input, the enclosure is incomplete, the electronics cooling is not yet implemented, and cable management has not yet been fully implemented)*
*Note also that the model is missing certain components (such as belts and controller board), due to added complexity. These may be added in the future.* 

I am happy to answer any questions relating to this printer. The best way to contact me is my discord: TKDonuts#5741

<img src="/Pictures/ISO-view.PNG" alt="Printer View"/>

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
 - I also wanted a 100x100x100 build volume, as it is generally the sweet spot for most of what I print. 
 
## Design Inspiration/Credit
 - This printer was heavily inspired by the [DICE](https://rene-jurack.de/dice/) 3d printer by Rene Jurack.
 - The printer was designed to utilize the [Sherpa Mini Extruder](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) designed by Annex Engineering
 - The Z-axis of this printer was also heavily inspired by the [Voron v0](https://github.com/VoronDesign/Voron-0) (original release, not 0.1)
 - The Toolhead of this printer utilizes a "Mosquito Net" (as coined by Annex Engineering), to reinforce the lower portion of the mosquito hotend heatsink. The concept, and implementation was utilized in this printer, based on measurements from the cad found [Here](https://github.com/Annex-Engineering/Annex_Engineering_PCBs/tree/master/mosquito_net-brace) and [Here](https://github.com/Annex-Engineering/Chhogori-K2-Basecamp-Edition)

*This Printer was Designed in Fusion 360.*

## Design Choices

### Why build this printer? Why not build the DICE or Voron or some other printer?
There were several reasons I decided to design this printer. Firstly, designing printers is fun, and I've taken this partially as a learning opportunity, to sharpen my CAD skills with a more complex project then what I'm typically used to. 
Secondly, may of the other printer's didn't quite satisfy my needs for a desktop 3d printer. 

 - The DICE looks like a great printer, but it is relatively dated, and didn't quite meet my build volume requirements. My original intention was to redesign the parts to meet this, however, I decided instead to rebuild each part from the ground up (as modifying the existing parts had some issues). 
 - The Voron v0 is also a nice printer, but I didn't agree with come of the design choices (notably mgn7s, printed parts making up the frame, nema 14s)
 - The TinyM checked some of these boxes, however it still had printed frame parts, and when scaled down, wasn't nearly as space efficient. 

### Toolhead Design
The toolhead probably took the longest to design, both because I was learning how to design decent part cooling ducts, and I was working on optimized the cooling and belt routing as much as possible. The DICE printer had a belt holder solution which (to my knowledge) essentially required the user to glue in the belts. This was largely due to the belt path/routing. By changing that, I was able to avoid this issue.

<img src="/Pictures/Toolhead ISO.PNG" alt="Toolhead Isometric"/>
<img src="/Pictures/Toolhead-Rear.PNG" alt="Toolhead Rear"/>

The v0 and DICE had somewhat lackluster cooling solutions for both the hotend and part cooling. With my design, I managed to squeeze in dual 4010 blower fans for part cooling, as well as a 3010 axial fan with an unconstricted flow path for hotend cooling (This combined with a genuine mosquito should yield no problems with heat creep.) 

<img src="/Pictures/Toolhead-Cross-Section.PNG" alt="Part Cooling Cross Section"/>

<img src="/Pictures/Unconstricted HE cooling.PNG" alt="Uncontricted Hotend Cooling"/>

At the moment, the toolhead is only designed for a genuine mosquito hotend. Clone mosquitos may fit, however many are not compatible with the mosquito net shown in figure 4. I can really only recommend the genuine mosquito (plus you'll be supporting the original designers). 

<img src="/Pictures/Mosquito-Net.PNG" alt="Mosquito Net"/>

### Gantry Design 

<img src="/Pictures/Gantry-ISO.PNG" alt="Gantry Isometric"/>

The gantry was also somewhat of a challenge. I took elements of the DICE gantry, but modified the pathing on the XY Joiners to allow for the aforementioned toolhead belt holders to be easier to design.

<img src="/Pictures/Belt-Path-A.PNG" alt="Belt Path A"/>
<img src="/Pictures/Belt-Path-B.PNG" alt="Belt Path B"/>

At the moment, the gantry only has the space to accomodate F623 Bearings for idlers. This is a major downside, as it could lower the theoretical life of the belts. As it stands, there is no solution that can maintain the space efficiency, so for now, this is the most likely part that I forsee failing prematurely. It may be possible to replace them with 16T pulleys, however the bearings on those pulleys are significantly smaller, and tend to fail even sooner than the belts would. 

### Z Axis

<img src="/Pictures/Z-View-One.PNG" alt="Z axis view 1"/>
<img src="/Pictures/Z-View-Two.PNG" alt="Z axis view 2"/>

The Z axis was also a challenge. The original plan was to do a belted z axis, however space contraints prevented this from being a viable option. It is subject to re-evaluation at a later date. For now, this utilizes a single leadscrew driven Z, which is further geared down by a ratio of 2:1.

The z-axis bed carriage was also designed with enough space for the Mandala Roseworks [Oldham Leadscrew Wobblers](https://www.mandalaroseworks.com/shop/railcore/oldham-leadscrew-wobblers) to be installed, albeit with some loss in z-height. These should counteract the artifacts present from bent or wobbly leadscrews. 

The bed carriage is also fully metal, and designed to be very stiff. This should hopefully counteract any potential for wobble at the front of the bed, due to the cantilevered design.






