# GAMEBOY-FLASHCART-MBC5
A working PCB layout for making your own MBC5 based Gameboy cartridge.

This is a working Gameboy flash cartridge. I've made a few different types of cartridges, but thought this would be the most popular due to being compatible with the InsideGadgets GBxCart RW.

The difficulty of making such a device these days is, when the Gameboy was released, the 8-bit era was already on the way out. So 33 years later, parts are not readily available. I'm not sure how other people manage to aquire a consistant supply of components.

![Gameboy MBC5 Cart + FRAM V1 1 Front](https://user-images.githubusercontent.com/65309612/164986777-b8135e78-49ff-47f9-9c12-1bee6f389243.jpg)

![Gameboy MBC5 Cart + FRAM V1 1 Rear](https://user-images.githubusercontent.com/65309612/164986783-6f54a3cb-f7f0-4b71-86f0-46bf79b2fc7b.jpg)

![Batch Made](https://user-images.githubusercontent.com/65309612/159160560-ba56514f-a369-4ae1-9265-43d162a6d556.jpeg)


**EEPROM AM29F016B**

I've found them available from Aliexpress very easily. I got them for just over £1 per chip. These are a 16-bit address and 8-bit data bus EEPROM. The write enable pin is brought to the audio pin on the Gameboy cartridge header. This is compatible with the GBxCart RW. The pin is held to 5v to keep it disabled during usage through a pullup resistor. You can buy 0603 spec 10k resistors or reuse the resistor on an original Nintendo doner PCB. I've not seen any need for this pull up resistor, but I can see it will cause a problem down the line somehow without it. 70 hours into Pokemon Yellow I wouldn't want the EEPROM to get corrupted and loose your save. I'm not sure if the audio pin is held low by the Gameboy, I think it is, so likely there isn't a need for it. You can omit it if you like. You'll use 500uA of current usage.

**SRAM FM18W08**

The SRAM isn't SRAM, its the modern FRAM that was made to replace battery backed SRAM in industrial PLC applications (among other things I'm sure). Once more Aliexpress has these in a small supply. These are the most expensive part of building this, apart from the donor MBC5 chip, depends on where you get the MBC5. The FRAM is available on eBay but the prices are egregious. You can get quality versions of the FRAM from reputable suppliers like Mouser and Digikey. The FM1808, FM18W08, FM1808B and FM18L08 all work in this desgin. FM1808 and the FM18L08 are out of production, so any you find will be old stock or poor copies. Bear in mind that the L version is a 3.3v part that is able to stand an extreme of 5v at its input, so I don't suggest using that if possible.

So in my tinkering with all this, I can suggest that you spend £12 per chip for a quality item. Aliexpress and eBay are full of either copies or factory rejected parts. You can find them for around £2 per chip and you get junk. In a batch of 5 from Aliexpress, none of them worked. From another batch, I went through 4 before finding a working one. In the end I went through 8 chips before getting one that works. So 9 chips x £2 is £18 for one working chip. Better off spending the £12 for one.

**Memory Controller MBC5**

This is the most expensive part of the cartridge. That does depend though. I have been able to find a lot of MBC5 based games for £3. You can be more patient and get them a touch cheaper. I've had some for as low as £1. You'll need a heat gun to remove the chip from the board. It can be done with a soldering iron with gentle prising and patience.

It's not hard though, as every basic game out there for the GBC was MBC5 based. So, lots to go at. 

**Compatability** See MBC5-FLASH-COMPAT.TXT for currently tested games

The MBC5 is compatible with all previous MBC chips before it, and so every game should work with an MBC5 chip. It doesn't. It depends if the programmer followed the rules when making their games. Mole Mania wasn't designed for an MBC5 and works perfectly, yet Zelda - Links Awakening doesn't work and crashes when saving. It all depends on where the programmers wrote to adress spaces. The MBC5 has a few more functions built in and a few other quirks (or fixes) that the MBC1 didn't have. So it's hit or miss for non MBC5 games, that said every MBC5 based game should work that fits into the ROM. Large 4MB games will not work as they will not fit onto the 2MB EEPROM. I may may make a 4MB cart in future, but the 4MB EEPROM are so expensive, I don't think it is worth it. I might do the design and just leave it untested and make it open source.


Feel free to do whatever you wish with this design. I want everyone to enjoy the Gameboy in whatever way they can. I have not yet got around to selling any of these.

**CHANGE LOG**
21/01/23
Updated to V1.2. The Board size has been adjusted to better fit into cartridge shells. Also added extra 5v trace.

15/01/23
Updated Readme in the FRAM section and the end section. Cypress is a the newer name for Ramtron, it's definitly a problem with junk parts not Cypress chips. Also added more to the compatability list.

31/05/22 Not a change as such. I've had problems with Cypress branded FRAM. I Haven't determined if it is bad quality or fake chips. Right now, I suggest sticking with Ramtron branded FRAM. All kinds of strange behavior is to be expected.

24/04/22
Noticed a mistake in 5v top plane. Not sure how this hasn't caused problems. Also changed routing of some grounds and 5v traces.

20/03/22
First Revision uploaded. A few hours of testing done, everything worked as expected. Built 10 of these original versions.
