NinjaFuge
==========

![logo](https://raw.githubusercontent.com/hisashin/NinjaFuge/master/markdown/image/ninja_transparent_500x412.png)

![photo](https://raw.githubusercontent.com/hisashin/NinjaFuge/master/markdown/photo/closed1_500x667.jpg)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6wPBDhJhW8Q" frameborder="0" allowfullscreen></iframe>

Opensource ([CC BY-NC-SA 2.5](https://creativecommons.org/licenses/by-nc-sa/2.5/)) centrifuge with cover sensor and lock. Derived from [F.Lab's one](http://www.instructables.com/id/3D-Printed-DIYbio-Mini-Centrifuge/).

- [Frequently asked questions](#faq)
- [What we changed](#change)
- [Please note before making](#note)
- [Bill of material](#bom)
- [Wirings](#wire)
- [Source code](https://github.com/hisashin/NinjaFuge/blob/master/sourcecode/NinjaFuge/NinjaFuge.ino)
- [Assembly instructions](#assembly)

### <a name="faq"></a>FAQ

- How much?

	I made at $20 from junks. If you buy everythings new in Japan, total parts price is $75 now.

- How fast?

	12,000RPM in my case by connecting 12V adapter to cheapest ($10) 1000KV (that means +1000RPM per 1V) motor. You can make faster one if you can use higher voltage or faster motor. Do not exceed absolute maximum voltages of motor, ESC and microcontroller.

### <a name="change"></a>Changelogs

- 2017 Aug 7 : Changes from [F.Lab's one](http://www.instructables.com/id/3D-Printed-DIYbio-Mini-Centrifuge/)
	- Enclosure is changed from 3d printing to acrylic lasercut. because I think printing takes too long time and easier to get fail.
	- Added magnet to cover and reed switch to base. so that it can stop rorating when cover is opened.
- 2017 Aug 8 : Add safety lock
	- I don't know how to brake motor and it takes seconds to stop rorating. That means it's still not safe perfectly. 
	Small servo motor should be added to lock the cover while rotating.

### <a name="note"></a>Notes before making

- Any hinge around you can be used but yours will not be same as mine. Don't forget to change holes on both cover_back and base_back to yours.
- Similar minor changes will be required for other parts like motor, variable resistor and switch. If you use bigger Arduino, basement should be wider.

### <a name="bom"></a>Bill of material

- Lasercut 3mm acrylic parts with [this](https://github.com/hisashin/NinjaFuge/blob/master/lasercut/NinjaFuge_3mm_clear.pdf).
- 3d printed [rotor](https://github.com/hisashin/NinjaFuge/blob/master/3dprint/stl/NinjaFuge_F.lab_Rotor.stl) and [motor base](https://github.com/hisashin/NinjaFuge/blob/master/3dprint/stl/NinjaFuge_motor_holder.stl) with any material.
- Some heat shrinkable tubes with different diameters are useful to protect solderings.
- Small microcontroller like [Arduino Nano](https://store.arduino.cc/usa/arduino-nano) ($22), [Arduino Pro Mini](http://www.sparkfun.com/products/11113) ($10) or anything you like. If you can make Arduino with [Arduino](https://www.arduino.cc/en/Tutorial/ArduinoISP) or [AVRISP mkII](http://www.atmel.com/tools/avrispmkii.aspx), single [ATmega328](https://www.digikey.jp/product-detail/ja/microchip-technology/ATMEGA328P-PU/ATMEGA328P-PU-ND/1914589) ($2.2) is enough. In any case, these pins are required.
	- 1 analog input for tune
	- 1 digital input to catch [interrupt](https://www.arduino.cc/en/Reference/AttachInterrupt) of reed switch
	- 2 digital output for ESC and door lock servo. VCC should be connected to them too. Refer [Wirings](#wire).
- Parts for enclosure. Polycarbonate screws with plastic spacers are enough.
	- 29 M3 10mm screws
	- 8 M3 nuts
	- 4 M3 25mm spacer (both female) for base
	- 3 M3 100mm spacer (both female) for cover
	- To hold door lock servo, I used
		- 2 M2 8mm screws
		- 2 M2 nuts

- Are you living in Japan as me? Good. No need to change lasercut design if you use them.

	- [Brushless motor and ESC kit](https://www.amazon.co.jp/gp/product/B01MTCBO7D/ref=oh_aui_detailpage_o09_s00?ie=UTF8&psc=1)
	- [Small servo to lock door]()
	- [Variable resistor](http://akizukidenshi.com/catalog/g/gP-00246/)
	- [Nob for resistor](http://akizukidenshi.com/catalog/g/gP-00246/)
	- [Single circuit locker switch](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=3A8K-4BFY)
	- [Neodymium magnet](http://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-4VZZ)
	- [Reed switch](http://akizukidenshi.com/catalog/g/gP-03676/)
	- [Hinge](https://hands.net/goods/4991807041906/)
	- [4 rubber foot if you want](http://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=6AZE-JELC)
	- [DC jack](http://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-0HMZ)
	- [12V AC adapter](http://akizukidenshi.com/catalog/g/gM-06961/)
		- 5A might be too much but 1A wasn't enough.

- If not, it would be cheaper to find items similar to above list around you and move [holes](https://github.com/hisashin/NinjaFuge/blob/master/lasercut/NinjaFuge_3mm_clear.pdf) a little for each of them.

### <a name="wire"></a>Wirings

![diagram](https://raw.githubusercontent.com/hisashin/NinjaFuge/master/markdown/image/diagram.png)

### <a name="assembly"></a>Assembly instructions

- Need to make latest model from scratch taking photos or movies to document here. Anyone want to do that?
