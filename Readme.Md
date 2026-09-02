This is the open source project of the failed Kickstarter project PlantMate. 
The Product was fully built and does function. 

However it does have a few fundamental flaws. I'd like to start with those since if you do decide to build a unit we'd like you to know what you are getting.

1. 3d Prints even when printed with ASA start leaking after a few Months(best case). In order to fix this the chemical dichtol can be applied. https://www.3djake.ch/de-CH/diamant-polymer/dichtol-am?sai=15460&gad_source=1&gad_campaignid=20589295812&gbraid=0AAAAADzcMj8Y7nv_hEgby27vpQDPftoMB&gclid=Cj0KCQjwkt_UBhDMARIsALpnOAyNzg6kM-gktZdZdvaiX6HjJ_EsuXmQmlgduAnM21Dngige3So1tlIaAjuHEALw_wcB it works, however appling it is a real pain, a painters mask is highly recommended.
2. If the outlet of the waterhose is below the waterlevel inside the watertank it will syphon the water out of the tank. so plants must be placed above. This heavily hurt our application since we wanted PlantMate to be a nice addition to the room and to do that it would have to be placed ontop of furniture.
3. Soil Moisture Sensor. The Soil Moisture sensors we chose corrode after approximatly 8-12 months. If a longer lasting sensor is required the https://vegetronix.com/soil-moisture-sensor is an excellent choice however due to its price we weren't able to use it. otherwise our product would have been 400$+.
4. The AUX on The PCB directly hooks to the ADC of the ESP32. This causes noise in the Soil Moisture reading and should be improved.
5. Infra Red sensor to detect waterlevels. We should have chosen a capacitive sensor(first draft also opensourced never tested nor built tho) or an ultrasonic sensor.
6. Manufacturing this at scale would be far more expensive than the 199$ that we charged.

Other than that PlantMate does work and is a viable vacation watering system.

If you'd like to build your own we will setup a page where you can claim your Kickstarter perk. The box would include all of the Parts that we bought to build the PlantMate, except for the 3d printed parts. You would have to pay for shipping and taxes. Let us know if there is interst.

Otherwise the following materials are needed:
- 5x 5v waterpump - the seller we got them from no longer exists.
- 3mm od 6mm id silicone water tube for internal tubing (approx 1m + whatever amount of hose you need to your plants)
- 5 pipe fittings https://www.alibaba.com/product-detail/W3-9-M8-3-9-nut_1600927209678.html?spm=a2756.trade-list-buyer.0.0.401176e99Hz1av
- powersupply 5v and usb c cable.
- PCB (order from JLCPCB using the gerber files)
- 2x 1mm 
- 4x Soil Moisture Sensor. Any analog output will do, soldered to an aux connector, check schematic.
- Optional: Spark ir sensor GP2Y0A21YK0F, doesn't work very well our suggestion is replacing using ultrasonic

Tutorials:
-Program PCB using Platform.io and this installer https://github.com/sadrirammal/PlantmateTestingFirmware (check for passwords in there i think i might have leaked some at some point)
-How to assemble

Printing suggestions:
Print the backplate vertically no supports 100% infil
Print the lit vertically with supports
Print the watertank with 100% infill no supports


Files for the PCB and the Watertank sensor can be found in electrical and files for 3d printing can be found in stl folder. 