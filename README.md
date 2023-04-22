# Fuji-Atom Interface for [HomeSpan](https://github.com/HomeSpan/HomeSpan) and [ESPHome](https://github.com/esphome/esphome)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

## Introduction 

This interface was inspired by this project: [Unreality's repo](https://github.com/unreality/FujiHK).

This is a simple interface between 3-wire remote control of Fuji-Electric internal unit and an Atom Lite (ESP32 based) device.

***You need to connect this interface in parallel with remote control.***

## Platform

The tested version can be purchased here on the [M5Stack Store on AliExpress](https://it.aliexpress.com/item/1005003299215808.html?gps-id=pcStoreLeaderboard&scm=1007.22922.271278.0&scm_id=1007.22922.271278.0&scm-url=1007.22922.271278.0&pvid=224e7336-f02f-437a-9968-e8bd99935065&_t=gps-id%3ApcStoreLeaderboard%2Cscm-url%3A1007.22922.271278.0%2Cpvid%3A224e7336-f02f-437a-9968-e8bd99935065%2Ctpp_buckets%3A668%232846%238112%231997&pdp_npi=3%40dis%21EUR%218.79%218.79%21%21%21%21%21%40211b801816821634937488779e9747%2112000025086683331%21rec%21IT%21&spm=a2g0o.store_pc_home.smartLeaderboard_6000640622359.1005003299215808&gatewayAdapt=glo2ita).

The new AtomS3 Lite version is available for purchase on the [Official Store](https://shop.m5stack.com/products/atoms3-lite-esp32s3-dev-kit).

***Pease note, I have not tested this interface on the new version, I only notice that the power pins are unchanged.***

## Files usage

I designed two versions of the circuit:
* **"V1_Rev2.0"** powers the Atom @3.3V on the appropriate pin
* **"V2_Rev1.5"** powers the Atom @5V on the appropriate pin
	
Choose the one you prefer, there is no difference in the final operation.

***I prefer to use **"V2_Rev1.5"** to complain the Atom Lite specifications.***

In this repository there are two .zip archives containing the Gerber files.
When the JLCPCB site prompts you to upload Gerber files, directly upload the .zip archive you have chosen.

## Components availability

In case a component is not available, replace it with one of equal characteristics.
("Description" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”).

***Be careful, this replacement does not apply to the two ICs in the BOM (IC1 and U1)!!!***


Components of equal characteristics found in the BOM can be found by entering the part number
("Manufacturer Code" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”) on [Octopart](https://octopart.com/).

As for the capacitors, do not get stuck on the choice of temperature coefficient on the BOM if you should not find it, but quietly 
choose from these nine values: X5S X5R X5P X6S X6R X6P X7S X7R X7P. (The scale is: from the "worst" X5S, to the best X7P).

## Schematic

![Schematic](https://user-images.githubusercontent.com/80490825/233783775-efdf0b0c-d2d9-4551-94d4-81a8f3df71db.jpg)

## Model

![Immagine 2023-04-22 135723](https://user-images.githubusercontent.com/80490825/233783978-aa935885-1513-4ba5-9345-d3cbda1a8040.png)
![Immagine 2023-04-22 135642](https://user-images.githubusercontent.com/80490825/233783980-d88b5b62-2906-4631-a99a-d100e16ed9ff.png)
