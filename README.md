# GAMEBOY-FLASHCART-MBC5 2MB

A working PCB layout for making your own MBC5 2MB based Gameboy cartridge. Final version fully tested. Unless there is an issue that comes up, then consider this complete.

>[!NOTE]
>If you are looking for a first cartridge to build yourself, then this is it.

## ⚪ Game Compatibility

[COMPATIBILTY LIST](MBC5-FLASH-COMMPAT.txt)

Nearly all Gameboy colour games used this memory mapper. It can address up to 8MB of game storage and up to 128KB of game save storage. This one only using 2MB of ROM and 32KB of RAM. 95% of GBC games using this mapper are within this range. Most 8KB save files should work fine on the 32KB chip also. 

Earlier games from the DMG should work, Nintendo kept each revision of mapper compatible with the previous (for the most part). So long as programmers followed Nintendos suggestions when developing. Mole Mania wasn't designed for an MBC5 and works perfectly, yet Zelda - Links Awakening doesn't, it crashes when saving.

>[!WARNING]
>This cart will not work properly for real time clock games. This means games like Pokemon G/S/C.

## 📷 Photos

<img width="800" height="450" alt="mbc5x3" src="https://github.com/user-attachments/assets/155773fb-53d9-461e-be3d-257cc47a1bf0" />

![IMG_5662](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-2MB/assets/65309612/d1c8e6ab-e6d2-49b6-afda-699cef6fa9b4)
![IMG_5668](https://github.com/sillyhatday/GAMEBOY-FLASHCART-MBC5-2MB/assets/65309612/448fb447-8838-43ae-a5bb-0fa0a498bef3)

<img width="600" height="631" alt="mbc5" src="https://github.com/user-attachments/assets/0c3836ba-9024-4461-85ec-8c33ab2983c0" />

## 🟣 Bill of materials:

>[!IMPORTANT]
>When ordering PCBs, be sure to order in 0.8mm thickness with gold plating!

| Part | Quantity |
|--------------|----|
| 29F016 Flash | x1 |
| FM1808 or FM18W08* | x1 |
| MBC5 | x1 |
| SN74LVC1G332DBVR | x1 (OPTIONAL) |
| 10K 0603 resistor | x2 |
| 0.1uF 0603 capacitor | x4 |

**FM18L08 will work but is not suggested*

### 💻 EEPROM 29F016B <br>
I've found them available from Aliexpress very easily. Lately the prices of these have risen. Once available for about £1 per chip are not £1.60 per chip. These are a 16-bit address and 8-bit data bus EEPROM. The write enable pin is brought to the audio pin on the Gameboy cartridge header. This is compatible with the GBxCart RW. The pin is held to 5v to keep it disabled during usage through a pullup resistor.

### 🐏 FRAM FM1808 <br>
These are expensive. Current prices are €11.90 from Mouser. They are available for much less on Aliexpress, for the same price you can get 5 - 10. These are known to be ***extremely*** unreliable. You are likely buying factory rejects that don't fully work or meet the speed rating. In a batch of 5 from Aliexpress I got, none of them worked. Another 10 I got, I went through 4 before finding a working one. In the end I went through 8 chips before getting one that works. The cost of 9 dodgy chips was more than one from Mouser.

### ❔ Memory Controller MBC5 <br>
You used to be able to go on eBay and find trash games for €3 easily, some deals I've had as low as €1. I could go on eBay and grab one or two of them per week. They seem to have gone up and the best deals are about €5 now. You'll need a hot air station to remove the chip from the board.

## CHANGE LOG <br>
| Date | Notes |
| ---- | ----- |
| 30/11/23 | Last update was not final. This should hopefully be final. More tastful logo design on the cart now. I've spend ages making sure the holes in the PCB are the same as factory Nintendo PCB. They should actually fit in Nintendo shells now with the small top locating pin. Nothing more to add now. I've actually got some of these on order for myself. Last ones I had made were V1.2 |
| 08/05/23 | Big update. Added OR gate for better MBC1 compatibility, which can be bypassed if not desired. Moved nearly every trace to reduce vias and improve appearance. Likely final update unless there is a problem. |
| 08/04/23 | Changed fill edge limits to right values for new KiCad version. Changed Sillyhatday rear label to be more subtle. |
| 10/03/23 | Updated the top edge cut drill hole. Doesn't quite fit in shells with the top stud properly. It should now, but is untested. |
| 05/03/23 | Update to V1.4. Changed some tiny errors in trace routing, invisible but bugged me. Changed MBC and ROM footprints to standard library footprints. |
| 07/02/23 | Updated to V1.3. Adjusted some trace routes for a better looking board. Added missing capacitor value to board for C4. Added many games to compatibility list. |
| 21/01/23 | Updated to V1.2. The Board size has been adjusted to better fit into cartridge shells. Also added extra 5v trace. |
| 15/01/23 | Updated Readme in the FRAM section and the end section. Cypress is a the newer name for Ramtron, it's definitly a problem with junk parts not Cypress chips. Also added more to the compatability list. |
| 31/05/22 | Not a change as such. I've had problems with Cypress branded FRAM. I Haven't determined if it is bad quality or fake chips. Right now, I suggest sticking with Ramtron branded FRAM. All kinds of strange behavior is to be expected. |
| 24/04/22 | Noticed a mistake in 5v top plane. Not sure how this hasn't caused problems. Also changed routing of some grounds and 5v traces. |
| 20/03/22 | First Revision uploaded. A few hours of testing done, everything worked as expected. Built 10 of these original versions. |

## Links

🏷️ NextStopPlease Labels: https://nextstopplease.square.site/ <br>
📷 NextStopPlease Insta: https://www.instagram.com/nxt.stop.please/ <br>
🛍️ Inside Gadgets Shop: https://shop.insidegadgets.com <br>
📎 Inside Gadgets GitHub: https://github.com/insidegadgets <br>
📷 Inside Gadgets Insta: https://www.instagram.com/inside.gadgets <br>
🖇️ Bytendo Mods GitHub: https://github.com/bytendomods <br>
🐭 Bucket Mouse: https://github.com/Bucket-Mouse <br>
🛒 Natalie Shop: https://nataliethenerd.com/ <br>
🤓 Natalie GitHub: https://github.com/natalie-lang/natalie <br>

## ⚖️ License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License. You are able to copy and redistribute the material in any medium or format, as well as remix, transform, or build upon the material for any purpose (even commercial) - but you must give appropriate credit, provide a link to the license, and indicate if any changes were made.
