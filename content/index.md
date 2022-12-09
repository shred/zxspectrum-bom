# Table of Contents

<div class="toc"><ul>
  <li><a href="index.html">Introduction</a> &ndash; this page</li>
  <li><a href="zxspectrum-bom.html">The Bill of Material</a> &ndash; what you are probably here for</li>
  <li><a href="csv.html">CSV Export</a> &ndash; for Mouser Electronics</li>
  <li><a href="zxspectrum-bom.xlsx">Excel Export</a> &ndash; for your spreadsheet application</li>
  <li><a href="https://github.com/shred/zxspectrum-bom">GitHub Project Page</a> &ndash; feel free to contribute</li>
</ul></div>

# Introduction

This is the Bill of Material for a replica ZX Spectrum 48K Issue 3B. It is optimized for [PABB's ZX Spectrum 48 Issue 3B Redrawn](https://www.pcbway.com/project/shareproject/ZX_Spectrum_48_Issue_3B_Redrawn.html) boards.

## Read Me First!

If you want to build your own ZX Spectrum, be aware that the machine was designed in the early 1980s.

While almost all of the standard components are still available, some components are very rare by now. You will need *all* of the listed components (except of those marked optional). We recommend that you try to get the components marked as <span class="rare">Rare</span> first, so you won't waste your money on standard components if you fail to get all the rare ones.

This bill of material only comprises of the components required for the mainboard itself. For a complete ZX Spectrum replica, you will need:

* This board, fully assembled and tested.
* A ZX Spectrum or ZX Spectrum+ case with keyboard. You can use an original case, but there are also replica cases, faceplates, and key mats in all kind of colors, as well as new keyboard membranes.
* A power supply with correct polarity: 9 V, 1.5 A, 5.5mm/2.1mm barrel plug, **center negative**. Note that most wall power supplies on the market are center positive, and would instantly kill your ZX Spectrum.

If you are new to electronics and soldering, there are easier ways to solder your own ZX Spectrum. For example, there are kits for the [Harlequin 48K](https://www.bytedelight.com/?product_cat=harlequin48) and [Harlequin 128K](https://www.bytedelight.com/?product_cat=harlequin128) clone that include all components and detailed assembly instructions.

## Rare Parts

The easiest way to get these parts is to buy an old or broken ZX Spectrum, and salvage them.

* **ULA**: There are modern ULA replicas like [Retroleum Nebula](http://blog.retroleum.co.uk/electronics-articles/nebula-spectrum-ula-chip-replacement-module/) or [vRetro vLA82](https://vdrivezx.com/vla82/).
* **Z80A**: It is still in production. If you cannot find one in a DIP-40, you can use a Z80 adapter board for other case types. The clock frequency should be 4MHz. Higher frequencies can be used as well, but won't make your ZX Spectrum run faster.
* **4116**: This DRAM type is long out of production, but <abbr title="New Old Stock">NOS</abbr> parts are still available. Alternatively there is an [SRAM module](https://lotharek.pl/productdetail.php?id=267) that replaces all eight 4116 with a single board.
* **4132**: This DRAM is actually a 4164 where one half of the memory turned out to be defective on production. If you get 4132 chips, make sure they are of the same brand and type (e.g. taken from the same ZX Spectrum). It's easier to use 4164 chips as drop-in replacement though, they are still available as <abbr title="New Old Stock">NOS</abbr> parts. You can also mix 4132 and 4164 chips.
* **ROM**: The easiest way is to salvage a ROM from a broken ZX Spectrum. A 27C128 or 27C256 EPROM can be used as replacement, but requires a [modification to the hardware](http://blog.retroleum.co.uk/electronics-articles/how-to-replace-the-rom-of-a-zx-spectrum-with-an-eprom/).
* **LM1889N**: This part is long out of production, but can still be found as <abbr title="New Old Stock">NOS</abbr> part.
* **Transistors**: The original ZTX transistors are out of production, but they all can be replaced with ZTX651 (which is still in production) and standard BC-type transistors. Check the datasheets for the correct orientation! For example, if you use a BC557 as replacement for TR5, the flat side must face in the opposite direction.
* **Coil**: The coil was custom made for Sinclair. There are new coils available on auction platforms sometimes, but they are expensive. The best way is to salvage a coil from a broken ZX Spectrum. If it is defective, [it can be repaired easily](https://shred.zone/cilla/page/458/zx-spectrum-recoiled.html#new-coil). Another alternative is to use the SRAM module mentioned above, which does not need -5V and +12V. You can then leave out the coil, TR4, TR5, D15, D16, and a few capacitors and resistors. Be aware that a few expansions might need these voltages as well, and might not work if you modify your ZX Spectrum that way. You could also use DC/DC converters for generating -5V and +12V, of course.
* **Keyboard Connectors**: They can be found as <abbr title="New Old Stock">NOS</abbr> part from time to time, and otherwise can be salvaged from a broken ZX Spectrum. There are replacement parts in this Bill of Material list that are still in production, however they are not optimal.
* **TV Modulator**: Needs to be reused from a broken ZX Spectrum. However, as most modern TVs don't have a matching input anymore, it can easily be replaced with a [simple RCA connector](https://shred.zone/cilla/page/459/zx-spectrum-chrome.html#composite-mod) to get a composite output ("composite mod"). You could also use an [s-video module](https://github.com/redhawk668/ZX-Spectrum-S-Video), which will enhance the image quality even more ("s-video mod").
* **Beeper**: The speaker should have an impedance of 40Ω, but similar speakers will do as well.
* **7805 and Heatsink**: They should be replaced with a modern DC/DC converter, as it stays cool and does not need a heatsink. Since the original ULA gets pretty warm itself, and cannot be cooled with a heatsink in the original ZX Spectrum case for space reasons, any additional heat source should be avoided.

## Sockets

This Bill of Material also includes sockets for all chips. All sockets are optional, of course. In an original ZX Spectrum, sockets were used as deemed necessary by Sinclair at that time, but usually the ULA was always socketed, and the LM1889N was never socketed.

Generally we recommend to use precision sockets. However, if you are going to use replica parts (e.g. a replica ULA or a memory board), you should check if they fit into precision sockets, and maybe resort to standard sockets.

If you are going to use the Retroleum Nebula as ULA replacement, all nearby chips (IC3, IC4, IC24, IC25) should be soldered directly to the board, as they would collide with the Nebula board otherwise.

If you want to heatsink the original ULA, you might have to solder it directly to the board for space reasons.

## Configuration


* If 4164 memory chips are used, all of these configurations will work, so just pick one.

## Disclaimer

This is not an official list! It was collected and reviewed by Sinclair enthusiasts.

Although we strive to make the information in this project as helpful and accurate as possible, it is provided "as is" and without warranties of any kind either expressed or implied.

In other words: You might spend a lot of money, and end up with a non-functioning board or a cardboard box full of useless components.

**Use at your own risk!**

## Contribute

This list is meant to be a community work. Our goal is to have a canonical list that people can rely on when ordering parts for building an own ZX Spectrum mainboard.

However, this list may not be free of errors. If you have found one, please [open an issue](https://github.com/shred/zxspectrum-bom/issues) or send a patch.

## License

This project is distributed under the terms of [GNU General Public License (GPLv3)](https://www.gnu.org/licenses/gpl-3.0.en.html#content).
