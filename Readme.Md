# PlantMate

This is the open source release of the failed Kickstarter project PlantMate. The product was fully built and it does work.

It does have a few fundamental flaws though. I'd like to start with those, since if you do decide to build a unit we'd like you to know what you are getting.

## Known flaws

1. **The 3D prints leak.** Even when printed in ASA they start leaking after a few months (best case). This can be fixed by applying [Dichtol](https://www.3djake.ch/de-CH/diamant-polymer/dichtol-am). It works, but applying it is a real pain — a painter's mask is highly recommended.

2. **The tank siphons itself empty.** If the outlet of the water hose is below the water level inside the tank, it will siphon the water out. So the plants have to be placed above the unit. This heavily hurt our application, since we wanted PlantMate to be a nice addition to the room, and for that it would have to sit on top of furniture.

3. **The soil moisture sensors corrode.** The ones we chose last approximately 8–12 months. If you need something longer lasting, the [Vegetronix sensor](https://vegetronix.com/soil-moisture-sensor) is an excellent choice — we couldn't use it because of the price, otherwise our product would have been $400+.

4. **Noisy AUX input.** The AUX on the PCB hooks directly to the ADC of the ESP32. This causes noise in the soil moisture readings and should be improved.

5. **Infrared water level sensor.** We should have chosen a capacitive sensor (a first draft is open sourced here as well, never tested nor built) or an ultrasonic one.

6. **Cost at scale.** Manufacturing this at scale would be far more expensive than the $199 we charged.

Other than that PlantMate does work and is a viable vacation watering system.

## For Kickstarter backers

If you'd like to build your own, we will set up a page where you can claim your Kickstarter perk. The box would include all of the parts that we bought to build the PlantMate, except for the 3D printed parts. We can even include 1kg of ASA, since we have no use for it. You would have to pay for shipping and taxes.

Let us know if there is interest by contacting us at info@plantup.io.

## Bill of materials

If you're building from scratch, you'll need:

- 5x 5V water pump — the seller we got them from no longer exists.
- Silicone water tube, 3mm ID / 6mm OD, for the internal tubing (approx. 1m, plus however much hose you need to reach your plants).
- 5x [pipe fittings](https://www.alibaba.com/product-detail/W3-9-M8-3-9-nut_1600927209678.html) (W3.9 M8 nut).
- 5V power supply and a USB-C cable.
- PCB — order from JLCPCB using the gerber files.
- 2x 1mm x 15mm metal pins, used as a hinge to attach the lid to the water tank. A paperclip works if needed.
- 4x soil moisture sensor. Any analog output will do, soldered to an AUX connector — check the schematic.
- Optional: Sharp IR sensor GP2Y0A21YK0F. Doesn't work very well, our suggestion is to replace it with an ultrasonic sensor.

## Printing

- Backplate: vertically, no supports, 100% infill.
- Lid: vertically, with supports.
- Water tank: 100% infill, no supports.

We printed everything in white ASA. ASA gives off a very premium feel — our first prototypes were done in PETG, but PETG ends up looking shiny and plasticky.

When printing ASA, cover the printer in a cardboard box, put the print bed all the way down and heat at 100°C for approx. 2h. This makes printing ASA super easy.

## Firmware

Program the PCB using PlatformIO and this installer: https://github.com/sadrirammal/PlantmateTestingFirmware

## Assembly

_Tutorial coming._

## Repository layout

- `electrical/` — PCB files and the water tank sensor.
- `stl/` — files for 3D printing.

## License

Released for personal and non-commercial use. You're explicitly welcome to modify it and build on it — commercial use is not permitted.