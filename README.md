# Fuji-Atom Interface for [HomeSpan](https://github.com/HomeSpan/HomeSpan) and [ESPHome](https://github.com/esphome/esphome)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

## Introduction 

The purpose of this project, via [HomeSpan](https://github.com/HomeSpan/HomeSpan) or [ESPHome](https://github.com/esphome/esphome), is to be able to control your Fuji-Electric Air Conditioning internal unit from [HomeKit](https://en.wikipedia.org/wiki/HomeKit) or [Home Assistant](https://www.home-assistant.io/).

This is a simple interface between 3-wire remote control of a Fuji-Electric internal unit and an Atom Lite (ESP32 based) device.

This interface was inspired by this project: [Unreality's repo](https://github.com/unreality/FujiHK).

### Curiosity
[This](https://community.home-assistant.io/t/fujitsu-ac-heat-pump-integration-via-esphome-esp32/407610/80?u=fosv) is the first prototype I shared on [Home Assistant Community](https://community.home-assistant.io/).

## Platform

The tested version, so called [Atom Lite](https://shop.m5stack.com/collections/m5-controllers/products/atom-lite-esp32-development-kit), can be purchased on the offical site.

There is also a new version, [AtomS3 Lite](https://shop.m5stack.com/products/atoms3-lite-esp32s3-dev-kit), available for purchase on the official site.

***Pease note, I have not tested this interface on the new version, I only notice that the power pins are unchanged and the pin-matching between the Atom Lite and the AtomS3 Lite is:***
* ***G22 (Atom Lite) -> G5 (AtomS3 Lite)***
* ***G19 (Atom Lite) -> G6 (AtomS3 Lite)***

## Files usage

In this repository there are two .zip archives containing the Gerber files, when the JLCPCB site prompts you to upload Gerber files, directly upload the .zip archive you have chosen.

I designed two versions of the circuit:
* **V1_Rev2.0 ->** powers the Atom @3.3V on the appropriate pin
* **V2_Rev1.5 ->** powers the Atom @5V on the appropriate pin
	
Choose the one you prefer, there is no difference in the final operation.

***I prefer to use **V2_Rev1.5** to complain the Atom Lite specifications.***

## Connection

***You need to connect this interface in parallel with remote control.***

## Components availability

In case a component is not available, replace it with one of equal characteristics. \
("Description" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”)

***Be careful, this replacement does not apply to the two ICs: IC1 and U1***


Components of equal characteristics on the BOM can be found by typing the part number on [Octopart](https://octopart.com/). \
("Manufacturer Code" column of the file “Fuji_HK_BOM [Updated on 22-04-2023 h12.10].xlsx”)

As for the capacitors, do not get stuck on the choice of temperature coefficient on the BOM if you should not find it, but quietly 
choose from these nine values: X5S X5R X5P X6S X6R X6P X7S X7R X7P. \
(The scale is: from the "worst" X5S, to the best X7P).

## Bill of Materials

| Manufacturer Code | Description | Designer | Notes | Replaceable |
| ----------------- | ----------- | -------- | ----- | ----------- |
| MCP2025-330E/MD | IC TRANSCEIVER HALF 1/1 8DFN | IC1 | For both designs | N |
| TPS82140SILR | DC DC CONVERTER 0.9-6V | U1 | For both designs | N |
| C2012X5R1C106M085AC | Capacitor 10UF 16V X5R 0805 | C1 | For both designs | Y |
| CL21A226MOQNNNE | Capacitor 22UF 16V X5R 0805 | C2 | For both designs | Y |
| C2012X5R1C106M085AC | Capacitor 10UF 16V X5R 0805 | C3 | For both designs | Y |
| 2176094-7 | Resistor SMD 133K OHM 0.1% 1/4W 0805 | R1 | For both designs | Y |
| **CPF0805B42K2E1** | Resistor SMD 42.2K OHM 0.1% 1/10W 0805 | **R2** | Only for "V1_ Rev2.0" design (sets up the DC/DC converter to 3.3V) | Y |
| **4-2176093-0** | Resistor SMD 24.9K OHM 0.1% 1/4W 0805 | **R2** | Only for "V2_ Rev1.5" design (sets up the DC/DC converter to 5V) | Y |
| RG2012P-103-B-T5 | Resistor SMD 10K OHM 0.1% 1/8W 0805 | R3 | For both designs | Y |
| TNPU0805500RAZEN00 | Resistor SMD 500 OHM 0.05% 1/8W 0805 | R4 | For both designs | Y |
| 150080VS75000 | LED GREEN CLEAR 0805 SMD | L1 | For both designs | Y |
| TSM-105-01-F-SV | Connector HEADER SMD 5POS 2.54MM | J1 | For both designs | Y |
| TSM-104-01-F-SV | Connector HEADER SMD 4POS 2.54MM | J2 | For both designs | Y |
| S3B-ZR-SM4A-TF(LF)(SN) | Connector HEADER SMD R/A 3POS 1.5MM | J3 | For both designs | Y |

## Schematic

![Schematic](https://user-images.githubusercontent.com/80490825/233783775-efdf0b0c-d2d9-4551-94d4-81a8f3df71db.jpg)

## Model

![Immagine 2023-04-22 135723](https://user-images.githubusercontent.com/80490825/233783978-aa935885-1513-4ba5-9345-d3cbda1a8040.png)
![Immagine 2023-04-22 135642](https://user-images.githubusercontent.com/80490825/233783980-d88b5b62-2906-4631-a99a-d100e16ed9ff.png)
