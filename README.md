# Fuji-Atom Interface for [HomeSpan](https://github.com/HomeSpan/HomeSpan) and [ESPHome](https://github.com/esphome/esphome)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

## Introduction 

The purpose of this project, thanks to [HomeSpan](https://github.com/HomeSpan/HomeSpan) or [ESPHome](https://github.com/esphome/esphome), is to be able to control your Fuji-Electric Air Conditioning internal unit from [HomeKit](https://en.wikipedia.org/wiki/HomeKit) or [Home Assistant](https://www.home-assistant.io/).

This is a simple interface between 3-wire remote control of a Fuji-Electric internal unit and an Atom Lite (ESP32 based) device.

This interface was inspired by this project: [Unreality's repo](https://github.com/unreality/FujiHK).

***You need to connect this interface in parallel with remote control.***

### Curiosity
[This](https://community.home-assistant.io/t/fujitsu-ac-heat-pump-integration-via-esphome-esp32/407610/80?u=fosv) is the first prototype I shared on [Home Assistant Community](https://community.home-assistant.io/).

## Platform

The tested version, so called [Atom Lite](https://shop.m5stack.com/collections/m5-controllers/products/atom-lite-esp32-development-kit), can be purchased on the offical site.

There also is a new version, [AtomS3 Lite](https://shop.m5stack.com/products/atoms3-lite-esp32s3-dev-kit), available for purchase on the official site.

***Pease note, I have not tested this interface on the new version, I only notice that the power pins are unchanged and the pin-matching between the Atom Lite and the AtomS3 Lite is:***
* ***G22 (Atom Lite) -> G5 (AtomS3 Lite)***
* ***G19 (Atom Lite) -> G6 (AtomS3 Lite)***

## Files usage

In this repository there are two .zip archives containing the Gerber files, when the JLCPCB site prompts you to upload Gerber files, directly upload the .zip archive you have chosen.

I designed two versions of the circuit:
* **"V1_Rev2.0"** powers the Atom @3.3V on the appropriate pin
* **"V2_Rev1.5"** powers the Atom @5V on the appropriate pin
	
Choose the one you prefer, there is no difference in the final operation.

***I prefer to use **"V2_Rev1.5"** to complain the Atom Lite specifications.***

## Components availability

In case a component is not available, replace it with one of equal characteristics. \
("Description" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”)

***Be careful, this replacement does not apply to the two ICs in the BOM (IC1 and U1)!!!***


Components of equal characteristics found in the BOM can be found by typing the part number on [Octopart](https://octopart.com/). \
("Manufacturer Code" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”)

As for the capacitors, do not get stuck on the choice of temperature coefficient on the BOM if you should not find it, but quietly 
choose from these nine values: X5S X5R X5P X6S X6R X6P X7S X7R X7P. \
(The scale is: from the "worst" X5S, to the best X7P).

## Schematic

![Schematic](https://user-images.githubusercontent.com/80490825/233783775-efdf0b0c-d2d9-4551-94d4-81a8f3df71db.jpg)

## Model

![Immagine 2023-04-22 135723](https://user-images.githubusercontent.com/80490825/233783978-aa935885-1513-4ba5-9345-d3cbda1a8040.png)
![Immagine 2023-04-22 135642](https://user-images.githubusercontent.com/80490825/233783980-d88b5b62-2906-4631-a99a-d100e16ed9ff.png)
