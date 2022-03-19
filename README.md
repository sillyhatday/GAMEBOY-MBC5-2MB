# GAMEBOY-FLASHCART-MBC5
A working PCB layout for making your own MBC5 based Gameboy cartridge.

This is a working Gameboy flash cartridge. I've made a few different types of cartridges, but thought this would be the most popular due to being compatible with the InsideGadgets GBxCart RW. I occasionally sell small batches of these once I've got enough together.

The difficulty of making such a device these days is, when the Gameboy was released, the 8-bit era was already on the way out. So 33 years later parts are not readily available. I'm not sure how other people manage to aquire a consistant supply of components.

**EEPROM AM29F016B**

I've found them available from Aliexpress very easily. I got them for just over £1 per chip. These are a 16-bit address and 8-bit data bus EEPROM. The write enable pin is brought to the audio pin on the Gameboy cartridge header. This is compatible with the GBxCart RW. The pin is held to 5v to keep it disabled during usage through a pullup resistor. You can buy 0603 spec 10k resistors or reuse the resistor on an original Nintendo doner PCB. I've not seen any need for this pull up resistor, but I can see it will cause a problem down the line somehow without it. 70 hours into Pokemon Yellow I wouldn't want the EEPROM to get corrupted and loose your save. I'm not sure if the audio pin is held low by the Gameboy, I think it is, so likely there isn't a need for it. You can omit it if you like. You'll use 500uA of current usage.

**SRAM FM18W08**

The SRAM isn't SRAM, its the modern FRAM that was made to replace battery backed SRAM in industrial PLC applications (among other things I'm sure). Once more Aliexpress has these in a small supply. These are the most expensive part of building this, apart from the donor MBC5 chip, depends on where you get the MBC5. The FRAM is available on eBay but the prices are egregious. Definitly do not buy the FRAM from eBay. The FM1808 was discontinued in 2008 and replaced by the FM18W08 which should be available from more reputable suppliers like Mouser and Digikey. The FM1808 is what I have tested, but there should be no reason the FM18W08 shouldn't work.

**Memory Controller MBC5**

This is the most expensive part of the cartridge. That does depend though. I have been able to find a lot of MBC5 based games for £3. You can be more patient and get them a touch cheaper. I've had some for as low as £1. You'll need a heat gun to remove the chip from the board. It can be done with a soldering iron with gentle prising and patience.

**Compatability**

The MBC5 is compatible with all previous MBC chips before it, and so every game should work with an MBC5 chip. It doesn't. It depends if the programmer followed the rules when making their games. Mole Mania wasn't designed for an MBC5 and works perfectly, yet Zelda - Links Awakening doesn't work and crashes when saving. It all depends on where the programmers wrote to adress spaces. The MBC5 has a few more functions built in and a few other quirks (or fixes) that the MBC1 didn't have. So it's hit or miss for non MBC5 games, that said every MBC5 based game should work that fits into the ROM. Large 4MB games will not work as they will not fit onto the 2MB EEPROM. I may may make a 4MB cart in future, but the 4MB EEPROM are so expensive, I don't think it is worth it. I might do the design and just leave it untested and make it open source.

Here is my short list of tested games for the cartridge:

**ROM too big:**
Harry Potter Chamber Secrets
Harry Potter Sorcerers Stone
Dragons Lair
Alone in the Dark
Cannon Fodder
Austin Powers Welcome to my underground
Austin Powers Oh Behave
Perfect Dark
Dragon Warrior 3
Stone Age
Yu-gi-oh Duel Monsters 4
Yu-gi-oh Dark Duel Stories
Tomb Raider
Tomb Raider 2
Tomb Raider Curse of The Sword
Heroic Sword
Jungle Book Mowglis Wild Adventure
Grand Theft Auto
Shantae
Dragon Warrior Monsters 2 - Cobi's Journey
Dragon Warrior Monsters 2 - Tara's Adventure
Donkey Kong Country
Rayman
Mickeys Speedway
Mickeys Racing Adventure
Donald Duck Going Quackers


**Not Working:**
Super Mario Land Six Golden Coins - Major graphical problems
Zelda: Links Awakening - Crashes when saving
Duke Nukem
Game & Watch Gallery 1 & 2
Turok Rage Wars
Tony Hawk Pro Skater 2
Megaman Xtreme 2
International Karate
Dragon Ball z Legendary Super Warriors

**Working:**
Pokemon Yellow
Pokemon Blue
Pokemon Red
Pokemon TPP
Pokemon Gold - No RTC
Pokemon Silver - No RTC
Pokemon Crystal - No RTC
Pokemon Prism V0.94.0237 - No RTC
Pokemon Crystal Clear - No RTC
Pokemon Trading Card
Pokemon Picross
Mole Mania
Wario Land 2
Wario Land 3
Micro Machines V3
Test Drive 6

Feel free to do whatever you wish with this design. I want everyone to enjoy the Gameboy in whatever way they can. If you can't build your own then look out for my cartridges for sale or buy from InsideGadgets. I'm hoping that mine will be cheaper, but they will not be available like InsideGadgets ones will be.
