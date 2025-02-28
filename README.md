# WWG2 Mods for the A4T toolhead and filament cutter
This is my collection of mods for the A4T Toolhead developed by Armchair-Heavy-Industries, toolhead cutter developed by SouthAsh1 and WWG2 (Wrist Watch G2) extruder developed by tetsu97 and modified by bythorsthunder to include a dual filament sensor. 

**Project source links below:**
1. https://github.com/Armchair-Heavy-Industries/A4T
2. https://github.com/bythorsthunder/Voron_Mods/tree/main/Wristwatch_G2_Dual_Filament_Sensor
3. https://github.com/SouthAsh1/A4T-AFC

All licenses are carried over from their respective creators. License information available in the links above.

![image](https://github.com/user-attachments/assets/bcb7041d-fad1-45fc-af9c-316da4620067)


# Modifications overview and rationale:
During my use of the A4T toolhead together with the southash1 developed filament cutter and Wrist Watch G2 extruder I've come across the following limitations, issues and areas for improvement:

1. **Filament path diameter:** The WWG2 filament path was hexagonal, which while OK in principle, is "looser" than the latest circular filament path implemented in the G2E extruder by JaredC01. **Specifically the hexagonal path is up to 2.54mm in diameter vs. 2.1mm in the latest G2E extruder release.** This results in the filament path not being as constrained, which resulted in observable deviations in the PA value between G2E and WWG2. A cross sectional image of the revised filament path can be found below:
![image](https://github.com/user-attachments/assets/ac474656-e653-436c-a221-bdec1227415d)
2. **WWG2 Filament entry point:** The WWG2 mod to include the dual filament sensors results in a **very thin wall between the upper ball bearing and the filament path** and entry point. This results in the filament path deforming when printed. In addition, the filament entry path has a **very shallow taper** where the filament enters the extruder from the top ECAS fitting. This results in slight filament collisions if the filament enters the extruder at a slight angle due to the filament twisting in the feeding tube or curling due to its natural spool curge. **These have been addressed in the modded design by elevating the ECAS mount point by 1mm and agressively tapering the filament entry path.** A cross sectional image of the revised filament entry path can be found below:
![image](https://github.com/user-attachments/assets/e638fa4e-aca6-42a8-ae2d-ce1d71b7b438)
3. **WWG2 Filament exit and A4T direct filament entry path:** The dual filament sensor WWG2 had a very small recess to mount a bowden tube to the filament exit point. While this works well for toolheads that have a large bowden section after the extruder, when used in combination with the A4T AFC toolhead cutter, it resulted in **approximately 2-3mm of bowden tube needed to constrain the filament between the extruder and the A4T AFC extruder mount** adaptor. In addition, that bowden tube recess was again resulting in **thin walls on the WWG2** filament path that were deforming after printing. **Both of these have been addressed in the modded design by removing the bowden recess from both the WWG2 and the A4T extruder mount.** That small bowden tube was uncecessary and has been replaced with a coincident filament path, tapered at the entry of the A4T AFC to allow for proper filament guidance.
![image](https://github.com/user-attachments/assets/4d01bdb4-b7f3-4804-92d1-42126632ad7c)
![image](https://github.com/user-attachments/assets/b0adc37e-c67b-4c3f-a0c7-ec1fba94c6a8)
Please note that the M2 heatset is still needed to guide the filament through to the cutter and is fitted underneath the extruder adaptor filament path, here:
![image](https://github.com/user-attachments/assets/fa32d39c-94a1-4545-967f-58132c1e456e)

Happy printing!


