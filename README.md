# WWG2 Mods for the A4T toolhead and filament cutter
This is my collection of mods for the A4T Toolhead (developed by Armchair-Heavy-Industries) cutter developed by SouthAsh1 and WWG2 (Wrist Watch G2) extruder developed by tetsu97 and modified by bythorsthunder to include a dual filament sensor. 

**Project source links below:**
1. https://github.com/Armchair-Heavy-Industries/A4T
2. https://github.com/bythorsthunder/Voron_Mods/tree/main/Wristwatch_G2_Dual_Filament_Sensor
3. https://github.com/SouthAsh1/A4T-AFC

All licenses are carried over from their respective creators. License information available in the links above.

![image](https://github.com/user-attachments/assets/bcb7041d-fad1-45fc-af9c-316da4620067)


# Modifications overview and rationale:
During my use of the A4T toolhead together with the southash1 developed filament cutter and Wrist Watch G2 extruder I've come across the following areas for improvement:

1. **Filament path diameter:** The WWG2 filament path was hexagonal, which while OK in principle, is "looser" than the latest circular filament path implemented in the G2E extruder by JaredC01. **Specifically the hexagonal path is up to 2.54mm in diameter vs. 2.1mm in the latest G2E extruder release.** This results in the filament path not being as constrained, which resulted in observable deviations in the PA value between G2E and WWG2. A cross sectional image of the revised filament path can be found below:
![image](https://github.com/user-attachments/assets/ac474656-e653-436c-a221-bdec1227415d)

2. **WWG2 Filament entry point:** The WWG2 mod to include the dual filament sensors results in a **very thin wall between the upper ball bearing and the filament path** and entry point. This results in the filament path deforming when printed. In addition, the filament entry path has a **very shallow taper** where the filament enters the extruder from the top ECAS fitting. This results in slight filament collisions if the filament enters the extruder at a slight angle due to the filament twisting in the feeding tube or curling due to its natural spool curge. **These have been addressed in the modded design by elevating the ECAS mount point by 1mm and agressively tapering the filament entry path.** A cross sectional image of the revised filament entry path can be found below:
![image](https://github.com/user-attachments/assets/e638fa4e-aca6-42a8-ae2d-ce1d71b7b438)

3. **WWG2 Filament exit and A4T direct filament entry path:** The dual filament sensor WWG2 had a very small recess to mount a bowden tube to the filament exit point. While this works well for toolheads that have a large bowden section after the extruder, when used in combination with the A4T AFC toolhead cutter, it resulted in **approximately 2-3mm of bowden tube needed to constrain the filament between the extruder and the A4T AFC extruder mount** adaptor. In addition, that bowden tube recess was again resulting in **thin walls on the WWG2** filament path that were deforming after printing. **Both of these have been addressed in the modded design by removing the bowden recess from both the WWG2 and the A4T extruder mount.** That small bowden tube was uncecessary and has been replaced with a coincident filament path, tapered at the entry of the A4T AFC to allow for proper filament guidance.
![image](https://github.com/user-attachments/assets/4d01bdb4-b7f3-4804-92d1-42126632ad7c)
![image](https://github.com/user-attachments/assets/b0adc37e-c67b-4c3f-a0c7-ec1fba94c6a8)
Please note that the M2 heatset is still needed to guide the filament through to the cutter and is fitted underneath the extruder adaptor filament path, here:
![image](https://github.com/user-attachments/assets/fa32d39c-94a1-4545-967f-58132c1e456e)

4. **WWG2 M3x20 and M3x25 screws mod:** The stock WWG2 main body requires M3x20 and M3x18 screws. I have discovered that the M3x20 is barely long enough to make it fully through the square nut. Also they do not extend all the way through to the holes underneath the nut, somewhat reducing stability. In this mod, the WWG2 front plate has been modified to allow for the use of M3x20 and M3x25 screws
![image](https://github.com/user-attachments/assets/6ecad1c6-b28b-471d-ad77-fcab9195cef5)


5. **Reinforced blade holder:** While the stock design works well with PLA and ABS, when cutting fiber reinforced material (eg. PPA CF, PET CF) it tends to crack at infront of the lever bushing. The reinforced blade holder thickens that area allowing for more walls to be extruded, reducing the opportunity for cracks to appear.
 
![IMG_5974](https://github.com/user-attachments/assets/3b3d6572-b265-49c4-9e4d-eca69250475d)

![image](https://github.com/user-attachments/assets/345353c7-1f5d-451f-8070-a7200ec02cb0)

6. **Updated WWG2 THB mount:** Updated THB mount for the XOL carriage with the rear support screw now able to be used again.
![image](https://github.com/user-attachments/assets/4e6f4df2-8ceb-48b9-8136-46b23af80ab4)

7. **Experimental: Updated cowling with enhanced support for the G2 extruder gearbox:** What I have noticed is that the extruder is now mounted a bit higher up compared to the stock A4T hotend. This allows the WWG2 extruder room to "vibrate" as the extruder rear plate is unsupported vs. the stock A4T where the extruder is supported by the housing of the A4T. I have updated the cowling to extend the rear mounting plate to support the underside of the WWG2 resulting in slightly improved IS results.

 ![image](https://github.com/user-attachments/assets/870a98f4-bfc0-406b-a941-385d4468e6e3)

 ![image](https://github.com/user-attachments/assets/72ebd062-16fd-47b8-a996-202e3f0aad2d)

Please note that you will need to use supports in the slicer to print the extended support area. Apologies my CAD skills are not good enough to do this natively! Also as this is experimental, I have ony updated the Revo XOL cowling as that is the one my printer is using!

![image](https://github.com/user-attachments/assets/e68ef452-8e8e-40b3-a4cc-49976f11fba0)


# Assembly tips
As the filament paths are now tigther than the original designs (2.1mm in diameter) you may need a 2mm drill bit to ream them out slightly if they are too tight for filament to pass through easily.

The **WWG2 extruder has shrinkage compensation for ABS like materials already built in** the base design, from which these mods are derived from. So in theory you shouldnt need to scale the parts.

The **A4T AFC parts do not have shrinkage compensation baked in the CAD**, so you'll need to apply your material shrinkage compensation as per the base design instructions.

Happy printing!


