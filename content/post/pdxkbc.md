---
title: "PDXKBC"
date: 2019-05-22T00:03:27-07:00
---

![Assembled Badge](/pdxkbc/assembledbadge.jpg)

If you're reading this blog post, you probably got one of the PDX KBC (Portland Keyboard Club) badges I designed,
either at a PDXKBC meetup, SMKmeetup, or at DEF CON. This blog post will go over the materials and tools you need to build
the badge, as well as how to flash the firmware and put it together!

## Bill of Materials

![Materials](/pdxkbc/materials.jpg)

- Badge and Case PCBs (free!)
- 4x M3 10+6mm Brass Male-Female Spacers, 4x M3 6mm Screws, 4x M3 Nuts (I bought [a kit off eBay](https://www.ebay.com/itm/120Pcs-M3-Male-Female-Brass-Standoff-Spacer-PCB-Board-Hex-Screws-Nut/282780247495?ssPageName=STRK%3AMEBIDX%3AIT&_trksid=p2057872.m2749.l2649) for $7.50)
- 1x 5v Arduino Pro Micro (I bought [one off eBay](https://www.ebay.com/itm/Leonardo-Pro-Micro-ATmega32U4-5V-16MHz-Development-Board-Micro-USB-for-Arduino/202698426249?hash=item2f31c48789:g:QdQAAOSw5uVc9sE9) for $5.95)
- 6x 1N4148 Diodes (again, [off eBay](https://www.ebay.com/itm/100-x-1N4148-Diodes-DO-35-Switching-Signal-4148-USA-SELLER-Free-Shipping/223296541119?ssPageName=STRK%3AMEBIDX%3AIT&_trksid=p2057872.m2749.l2649), for $3.29)
- 4x Bumpers (I found these at a Safeway for like... $4? They're abought 3mm tall and 12mm in diameter)
- 6x PCB Mount Switches (I bought 10 [Kailh Pro Burgundy](https://novelkeys.xyz/collections/switches/products/kailh-pro-switches?variant=3747975954472) switches from NovelKeys for $6.20 shipped)
- 6x 1u Keycaps (Search Aliexpress, eBay, etc, for 1u DSA PBT blank keycaps, [here](https://www.aliexpress.com/item/MP-1U-DSA-keys-PBT-Blank-Keycap-Mixded-Color-Cherry-MX-switch-keycaps-for-Wired-USB/32847751930.html?spm=2114.search0104.3.2.63f84c52MoNBJT&ws_ab_test=searchweb0_0,searchweb201602_3_10065_10130_10068_10547_319_10546_317_10548_10545_10696_10084_453_454_10083_10618_10307_537_536_10059_10884_10887_321_322_10103,searchweb201603_53,ppcSwitch_0&algo_expid=35b5db04-7693-4f2a-b3fe-0b345b5c973c-0&algo_pvid=35b5db04-7693-4f2a-b3fe-0b345b5c973c&transAbTest=ae803_4) are some for like $7.11)

So the total is ~$35 if you're not buying in bulk.

## Tools

You'll need:

- A decent soldering iron, and solder (I recommend the [Hakko FX888D](https://www.hakko.com/english/products/hakko_fx888d.html) but a much cheaper one will do)
- A phillips screwdriver (I recommend whatever one is within arms reach)
- Flush cutters (something like [this](https://www.ebay.com/itm/Electrical-Cutting-Pliers-Wire-Cable-Jewelry-Cutter-Side-Snips-Flush-Plier-5/291958929654?hash=item43fa1bb8f6:m:mMi3VSjd2tnhs-XyAesnyZQ))

## Assembly

1. Bend your diodes as shown
![Bent Diode](/pdxkbc/bentdiode.jpg)
2. Place your diodes with the black stripe on the diode facing the white stripe on the PCB, slightly bend the legs to prevent the diode from falling out
![Placed Diode](/pdxkbc/placeddiode.jpg)
![Diodes](/pdxkbc/diodes.jpg)
3. Solder the diodes. Here's a guide to soldering if you're new:
{{< youtube J5Sb21qbpEQ >}}
4. Trim the diode legs with flush cutters
![Trimmed Diodes](/pdxkbc/trimmeddiodes.jpg)
5. Place and solder the lower four switches
![Lower Four Switches](/pdxkbc/fourswitches.jpg)
6. Tack on the two pin headers, fiddle with them until they're straight and the pro micro fits on
![Tacked Header](/pdxkbc/tackedheader.jpg)
![Test Fit](/pdxkbc/testfit.jpg)
7. Solder the pin headers
![Soldered Headers](/pdxkbc/solderedheaders.jpg)
8. Solder the top two switches
![Soldered Top Two Switches](/pdxkbc/twoswitches.jpg)
9. Solder the pro micro onto the headers
![Soldered Pro Micro](/pdxkbc/solderedpromicro.jpg)
10. At this point, you can flash the pro micro. On Linux:
{{< highlight bash >}}
git clone git@github.com:qmk/qmk_firmware.git
cd qmk_firmware
util/linux_install.sh
sudo make pdxkbc:default:avrdude
# short the RST and GND pins on the pro micro when prompted
{{< / highlight >}}
11. Test the keyboard, the default keymap is:
{{< highlight c >}}
const uint16_t PROGMEM keymaps[][MATRIX_ROWS][MATRIX_COLS] = {
    [0] = LAYOUT(
      PDXKBCREDDIT, PDXKBCDISCORD,
      BADGELIFE,    HACKTHEPLANET,
      KC_VOLU,      KC_VOLD
    ),
};
{{< / highlight >}}
12. Bolt and screw on the spacers, install the bumpers. You're done!
13. Post on twitter, and don't forget to @fharding0!