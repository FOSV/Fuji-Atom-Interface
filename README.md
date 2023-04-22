# Fuji-Atom-Interface


#   PREMISE   #

The author disclaims all liability for any damage to property and/or persons resulting from the use of the files in this folder.


#   LICENSE   #


This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/4.0/ or send a letter to 
Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.


#    USAGE    #


I designed two versions of the circuit:

	- "V1_Rev2.0" powers the Atom at 3.3V on the appropriate pin
	
	- "V2_Rev1.5" powers the Atom at 5V on the appropriate pin
	
Choose the one you prefer, there is no difference in the final operation.

In the "FABRICATION" folder there two .zip archive of the Gerber files.
(When the site prompts you to upload Gerber files, upload the .zip archive directly).

Speaking of JLCPCB, there are already part numbers related to the LCSC (component supplier for JLCPCB) catalog.

https://jlcpcb.com/

https://www.lcsc.com/

In case a component is not available, replace it with one of equal characteristics.
("Description" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”).

Be careful, this replacement does not apply to the two ICs in the BOM (IC1 and U1)!!!


Components of equal characteristics found in the BOM can be searched for by entering the part number
("Manufacturer Code" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”) at https://octopart.com/

As for the capacitors, do not get stuck on the choice of temperature coefficient on the BOM if you should not find it, but quietly 
choose from these nine values: X5S X5R X5P X6S X6R X6P X7S X7R X7P. (The scale is: from the "worst" X5S, to the best X7P).
