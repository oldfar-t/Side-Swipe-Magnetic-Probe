# Side Swipe v1.5 Magnetic Probe - The $10 Bolt On Magnetic Voron v0.1/v0 Probe Solution!

[![SideSwipe](https://user-images.githubusercontent.com/55677510/130884085-bd4bb34c-789b-4d5f-ac15-f4a48ff2e831.png)](https://youtu.be/MGC7AC8e7SE "SideSwipe")

Currently Supported Printers: Voron v0.1/v0 using MiniAfterburner direct drive hotend
# BOM
I tried to design this project around Voron v0 parts so hopefully many of these are spare parts you have lying around.
- 2 - M3x8 BHCS or SHCS Bolts
- 2 - M3x10 BHCS or SHCS Bolts
- 2 - M3x40 BHCS for Voron MiniAfterburner Mounting
- 2 - M3 Nuts
- 5 - [6mmx3mm Neodymium Magnets](https://www.amazon.com/gp/product/B077K364Z7/ref=ppx_yo_dt_b_asin_title_o00_s01?ie=UTF8&psc=1)
- 1 - [Omron Mouse Microswitch](https://www.amazon.com/dp/B00HPL57JQ/?coliid=I2L344Q2DNJEAU&colid=WW0P09PQO065&psc=1&ref_=lv_ov_lig_dp_it)
- 1 - [MG90s Hobby Metal Gear Servo Motor](https://www.amazon.com/Maxmoral-Upgraded-Digital-Vehicle-Helicopter/dp/B07NV476P7/ref=pd_lpo_1?pd_rd_i=B07NV476P7&psc=1)
- 1 - [300mm Servo Extension Cable](https://www.amazon.com/gp/product/B01LA9YDEI/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- 1 - [450mm Two conductor wire, I used 24 gauge silicon wire that comes as a strip of 4 strands](https://www.amazon.com/BNTECHGO-Silicone-Ribbon-Flexible-Parallel/dp/B07PMS5KGX/ref=sr_1_5?dchild=1&keywords=24+gauge+silicone+wire+4p&qid=1627635371&sr=8-5)

# Assembly
1. Print all parts using abs, parts are designed with shrinkage in mind. You may need to print the Probe_Mount and Probe_Block with minor supports. I have mine printed at a 0.3mm layer height at 13% infill, but a smaller layer height would work as well.
2. Insert servo connector through hole located in middle of Servo Mount Part then pull wire through.
3. Slot servo side tab into Servo mount with the output shaft closer to the Servo Mount part (See Image Below).
4. Insert M3x8 bolt into hole located on the end of the Servo Mount Part.
5. Insert 2 M3x8 bolts into the mounting holes below servo.
6. Then take the Arm Part and insert and screw in a M3x8 bolt into the hole located on the end between the two prongs.
7. Next press the Arm Part onto the servo output shaft with the text facing upwards, you can also use the screw included with the servo to tighten the arm on but you will need to remove the arm later to calibrate the arm position.
8. Next trim the middle connection on the microswitch flush with the switch body, leaving the two end connections. You will then insert the switch into the Probe Block Part, pressing the switch in so that the connections push through the holes. This is best to be done with a small vise.
9. Bend the switch connections over using a flathead screwdriver.
10. Now insert three 6x3 magnets into the holes of the Probe Block Part, the magnet on the side of the Probe block can be pressed in flush, and the two magnets on top should be pressed so that they are just below the surface of the Block. This can be done by attaching an extra magnet to each to push the magnets further in. Make sure that these two top magnets are facing the same direction.
11. Test the Probe Block with a multimeter on continuity mode by placing the multimeter probes on the top side magnets. The switch is normally closed you you should hear a beep and the beep should stop when pressing the switch.
12. Take your 450mm section of 2 conductor wire and crimp a 3 connection jst connector(refer to wiring diagram).
13. On the other end trim one of the conductors about 8mm shorter than the other and then strip 20mm of insulation from both conductors.
14. Insert the stripped conductors into the holes on the back of the Probe Mount Part, pull all stripped wire through(twisting the wire first helps).
15. Tuck the wire into the cable channel along the back of the Probe Mount.
16. Coil the stripped wire and tuck into the magnet holes so that they lay roughly flat against the bottom of the hole.
17. Press two 6x3 magnets into the holes on the bottom of the Probe Mount ensuring that they are both the same direction, and that they are oriented such that the Probe Block attaches to the Probe Mount. These magnets should not be pressed until they are flush. The magnets should both be proud of the surface by about 0.5mm.
18. Attach the Probe Block to the Probe Mount and test continuity at the JST connector end of the wire. The switch should behave normally closed.
19. Remove the two lower mounting bolts on the face of the MiniAfterburner and using two M3x40 bolts attach the Probe Mount using the now open mounting holes.
22. Before attaching the Side Swipe mechanism to the rail, plug the servo into the mainboard following the wiring diagram and run the SERVO_IN macro. You should then adjust the Arm so that it is in line with the body of the servo. Press the arm into place and attach using screw provided with the servo. Running the SERVO_OUT macro should rotate the servo counterclockwise by 90 degrees.
23. You can then attach the Side Swipe mechanism to the extrusion by first backing the 2 M3x10 screws all the way out and then slide the backet into the extrusion, making sure that the servo wire runs up in the extrusion slot towards the top of the machine and underneath the top horizontal extrusion (It helps to place the machine on its face and remove the right side panel).
24. Before tightening the bracket into place adjust the height of the bracket first so that when the arm is in the extended position, the probe can be picked up properly.
25. The servo wire can be tucked into the bottomside slot of the top horizontal extrusion. You might need to remove the servo wire connector so that you can slide the wires past the rear cover plate into the electronics bay. Reattach the connector and attach the 300mm servo extension or cut and solder the wires so that they can reach the mainboard of the printer.
26. Before reattaching the printer side panel, move the print head so that the Probe Mount can reach the Probe Block when the Arm is in the 90 degree position. Loosen and slide the Side Swipe mechanism until the Probe Block makes contact with the Probe Mount. Keep sliding the Side Swipe until the Arm is level and then tighten the two mounting bolts.
27. You should then wire the servo motor and Probe switch connection according to the wiring diagram.
28. Done! You should be able to run the PROBE_IN and PROBE_OUT macros. You may need to make some adjustments to the macro's positioning depending on your printers exact configuration. This is most easily done by moving the printhead manually and then issuing an M114 command to determine the printhead's position.
![v1 5 Release Render](https://user-images.githubusercontent.com/55677510/130884571-114f16df-11a0-46d8-85a1-845c8b1e6156.png)
![v1 5 thumbnail](https://user-images.githubusercontent.com/55677510/130884609-7332b90d-12a0-497f-891a-ef2e71e9d0ba.JPG)
![Render3](https://user-images.githubusercontent.com/55677510/127622164-c98ef963-63f7-4b12-9a58-14ed6a23e644.JPG)
