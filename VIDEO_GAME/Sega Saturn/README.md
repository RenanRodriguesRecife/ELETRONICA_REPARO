
Sega Saturn/Hardware revisions

**Motherboards:** Note that the changes are all evolutionary unless noted. If one revision, for example, integrates two ICs into one, all following ones have that too unless noted.

Board types used in Model 1: VA0 to 3

Board types used in Model 2: VA2 to 15

- **VA0:** Launch units, very first revision. CD Block is on a daughterboard, power supply mounted on top ("Type A"). Power led, access led, on/off and reset buttons, and the CD Tray open/close sensor are all separate. Uses ENR-007B drives (on some later units, ENR-007D). Very rarely they may have a Hitachi drive instead (JA00292).

- **VA1:** marked as "VA" on the motherboard, "VA1" on the controller board. Power supply is now bottom mounted ("Type B"). Every previous sub-board is now integrated to the motherboard, except the controller ports which are separated. This includes the CD Tray sensor which is now a very tall switch on the motherboards. Uses ENR-007D drives.

- **VA2 & 3:** Same form factor as VA1, but there are small changes to accompany the different CD Drive. The controller board is also a little different from VA1. VA2 is marked as VA SG, and VA3 is marked as VA SD. Type B power supply and ENR-011A drive. VA2 uses SG RAM for the main memory, VA3 uses SD RAM (hence their markings). You'll notice that even revisions will all use SG RAM and the following odd one will use SD RAM, but the boards themselves are otherwise identical.

- **VA4 & 5:** Exactly the same as VA2 and 3, respectively, but in a model 2 case. The only difference is that a few components are removed (access led, memory reset button, resistor leading to both of them), since they are not used on model 2s anymore. Type B power supply, ENR-011A drive. Note that some model 2s are still marked as VA2 or 3 by the serial number, but they also have those components removed, perhaps some manufacturers failed to get the memo.

**VA6 to 9:** Entirely new form factor, everything is in a single board from now on. Uses a new PLL chip (CY2292SC-45). Power supply has a different pinout ("Type C"). Uses ENR-013A drive. Some units may have a Sanyo 610-6185-30 drive instead.

  -  VA6 & 7 has the CD Block reduced to a single IC from the previous two, VA8 & 9 has them still separated.
  
  - VA6 & 8 uses SG RAM, VA 7 & 9 uses SD RAM.
  
  - VA9 seems to be using a much later design and is almost exclusive to PAL units, the only exception being the Hi-Saturn MMP-11. It also uses the old type PLL chip (315-5746, aka Hitachi HD49422).
  
- **VA10 to 15:** uses HQA-001A drive, sometimes rarely a Sanyo 610-6294-30 or a Sanyo 610-6473-30 instead. Sound block is now integrated to a single IC instead of two. Type C power supply.

  - VA10 uses SG RAM, VA11 & 13 & 15 uses SD RAM.
  
  - VA11 has a small extra daughter board to fix some design error. The function of that board is unknown.
  
  - VA11+ boards have a different form factor DAC, VA10 uses the old one.
  
  - VA12 and 14 were never produced. They would have been SG RAM counterparts to VA13 and 15. They may have been produced in extremely low quantities, so low that they haven't been spotted, but it is doubtful
  
  - VA15 integrates the two SH-2 main cpus into a single IC.
  
Note: the integrated sound block has a bug in certain 68000 commands, this might be the same bug as the Genesis 3 suffers from as that one also has an integrated 68000 made by Yamaha. The result is that certain games are incompatible with these boards. The Japanese only releases of Space Harrier and Outrun are the only two that come to mind, and both have received second pressings that eliminate this bug and work in all machines equally. Metal Slug is rumored to be incompatible, but this appears to be false.

### PAL Motherboards

**PAL Motherboards** (only the main differences are listed, otherwise see above): All PAL boards use different region & video output jumpers when compared to ntsc machines and use a 17.7344 Mhz master clock (NTSC units use 14.31818 Mhz). They also replace the c-sync output of the a/v out with a 9v connection, intended for SCART auto switching. On VA7+ boards, there is an extra power supply pin added to the entire machine just for that. C-sync is still there, just not wired into the a/v out, it can be restored with modding very easily (in case you are interested, the test point for c-sync is TP4 near the a/v out, on the bottom of the board).

  - **VA0 PAL** - has extra jumpers to set the master clock divider (JP18 & 19), functional but unpopulated 50/60hz switch on the back (SW4).
  
  - **VA1 PAL** - unpopulated 50/60hz switch on the back (SW4). There is a design snafu however, as it is still connected to the master clock divider select pin. Therefore the switch does not work on its own, you have to cut or raise+ground the PLL pin 1 for the switch to work.
  
  - **VA3 PAL** - has extra jumpers to set the master clock divider (JP20 & 21), functional but unpopulated 50/60hz switch on the back (SW4).
  
  - **VA5 PAL** - same as VA3 PAL.
  
  - **VA7 PAL** - chronologically, this board was designed after VA9, likely to use up remaining stock of certain parts. Unlike NTSC boards, this still uses the old Hitachi PLL (315-5746), and its pin 1 is interconnected to the pal/ntsc and 50/60hz selection pins on the video encoder and the VDP2. So, for installing 50/60hz switches, you have to separate those accordingly. Has an extra fifth power supply pin for the a/v out (for SCART auto selection).

  - **VA9** - same notes apply as for VA7 PAL. This is an odd board in that it has no NTSC equivalent. Only the model 2 Hi-Saturn MMP-11 used VA9 boards, and they used the exact same boards as PAL machines, not counting the different jumper setup, master clock, power supply, etc.

  - **VA13 PAL** - Has an extra fifth power supply pin for the a/v out (for SCART auto selection), but otherwise it seems to be identical to the NTSC boards.
  
It should be noted that no PAL board ever used SGRAM. The cause of this is unknown. Of course, the cause of using SGRAM in the first place is also unknown (and up to speculation - possible causes for both points include contractual obligations, shortage of one specific part, or a very good deal on SGRAM that made it worth to design two of each motherboards).

**Power supplies:**

- **Type A** is for VA0 units, is mounted to the top, pinout is GND, GND, 3.3V, 5V, (empty pin), 9V. (5 pins total)

- **Type B** is for VA 1 to 5 units, bottom mounted, pinout is GND, GND, 3.3V, 5V, 9V. (5 pins total)

- **Type C** is for VA6+ units, bottom mounted, pinout is GND, GND, 5V, 5V (4 pins total).

PAL units use a 5-pin variant of Type C power supplies, where the extra fifth pin is a 9V used exclusively in the a/v connector (for SCART auto switching). Later Asian units (that have a 220v power supply) most likely use that type of power supply too, with the 5th pin just not connected. In fact there are some USA and Asian machines that had a hole for the fifth pin but it was not connected to anything. The moniker "Type A/B/C" is coined by the service manuals.

# continuar aqui

CD Drives:

20pin, VA0-1:
JVC ENR-007B EMW10447-003E
JVC ENR-007B EMW10447-004E
JVC ENR-007D EMW10447-005E
JVC ENR-007D EMW10447-006E
Hitachi JA00292
These are all 20pin units. The Hitachi drive is rarely found in Japanese units, most commonly on early Hi-Saturns. They also seem to be exclusive to the SKC-1000 and SKC-1000C. There is a small difference in the microcontrollers used between ENR-007B and D.

21pin, VA 2-5:
JVC ENR-011A EMW10589-002
JVC ENR-011A EMW10589-003
These are the so-called 64pin drives. The -002 one seems to be used only in model 1s and the -003 only in model 2s, but it seems they are exchangeable.

21pin, VA6-9:
JVC ENR-013A EMW20035-002 610-6185-20
Sanyo 610-6185-30
The JVC drive is most often referred to as the 32pin drive. The Sanyo drive may or may not come with an extra Trap Board, its function is unknown at this point.

21pin, VA10-15:
JVC HQA-001A HQ100002-002 610-6294-20
Sanyo 610-6294-30
Sanyo 610-6473-30
Same as the above ones, but they all lack an oscillator and have a white border on the edges of the PCB. The Sanyo drive does not always comes with a trap board apparently.

Optical pickups used:

for EVERY JVC drive: Optima-6
for the Hitachi drive: HOP-6
for Sanyo drives: SF-P101 is used in the 610-6185-30.
As you can see, there are three different Sanyo drives, from two different type of drive families. Modchip guides seem to take them all under the same umbrella, and that's why one guide may not work with one of the Sanyo drives (as it was meant for the other type).

Special Saturn units: note: all production numbers are ESTIMATED FROM THE SERIAL NUMBERS. They may not be entirely accurate.

"This Is Cool" Skeleton Saturns: exact same as the normal Japanese units, except for the shell and the boxing, and they came with transparent controllers as well. They had VA13 and VA15 motherboards inside. VA13 seems to have been in the HST-0020 Special Campaign Original machines, while the VA15 ones were in HST-0021 models. These were among the last Saturns ever produced. The HST-0020s were made in late 1997, and the VA15 ones in 1998. They were all made by Seiyo Denshi. Estimated production based on the serials seen: ~30,000 to ~40,000. There is a rumor that made its way to Wikipedia stating that these units were made for the USA market, but this is false, no USA Skeleton machine exists. The only American skeleton unit was the Brazilian Tectoy model, which was most likely a rebranded Derby Stallion Skeleton unit.
Derby Stallion Skeleton Saturns: exact same as the normal Japanese units, except for the shell and the boxing. In contrast to the other Skeleton units, these had a lighter and greener transparent case and no "this is cool" logo. They were all VA15 boards, and the HST-0022 package they were sold as was the very last Saturn bundle Sega released. They were all made by Sanwa Denki in 1998, but released much later in 1999 to promote the Derby Stallion game software. Estimated production based on the serials seen: at least ~12,000, might be as much as ~30,000.
Victor V-Saturn: exact same as the normal Japanese units, the only difference is the BIOS rom, the case color, and the brand. They used pretty much every type of motherboard and are quite common. Based on the serials, there are ~70,000 model 1 units and ~140,000 model 2 units produced, and they have been in production from the very start (November 1994) to the very end (July 1998).
Hitachi Hi-Saturn: exact same as the normal Japanese units, the only difference is the BIOS rom, the case color, and the brand. They used VA0, VA1 and VA2 boards for the MMP-1, MMP-1-1 and MMP-1-2 units (model 1) and VA9 for MMP-11 units (model 2). They also had a Video CD card included, as they were meant to be multimedia units, sold for A/V enthusiasts. The case color was unique only for the top, the bottom of the case was a normal black one, like in USA and PAL machines. Produced: ~5,500 (MMP-1), ~2,000 (MMP-1-1), ~11,000 (MMP-1-2), ~10,000 (MMP-11). Note that due to the low production number, these estimates are not very accurate, they may have been thousands more units produced.
Hitachi Hi-Saturn NAVI (MMP-1000NV): A specialized unit with an external power supply, karaoke controls (voice cancellation DSP and microphone inputs), GPS, optional LCD display, video input for optional TV Tuner, and lots of other things. They used a unique motherboard most likely based on VA1 or VA2/3 boards. The CD Drive is a huge cusotm board that houses all the extra audio functions. Optical pickup is unknown, presumed to be a Hitachi type. Has no RGB out, but it can be modded back in fairly easily. Produced from 1995 November to at least 1996 January, number of units produced is unknown, and hard to estimate as they are rarely seen. The highest serial on record of is 1416, so ~1,500 produced units seems plausible. A guesstimate given by nfggames is ~2,000 units produced.
Samsung Saturn: a machine released in South Korea under the Samsung brand. There are a lot of rumors about what is inside these, but all units that have been seen opened up were all completely stock Japanese VA1 motherboards (171-7006C 837-11613-01), had everything intact, with only the region jumpers and the BIOS rom being different. The region is set to 2 for Korea, and the BIOS version states v1.02a and looks like the USA/PAL version rather than the Japanese one. The bios has a unique quirk that when it is set to the default region-2, the Japanese language option is disabled. The power supply is unique in that it accepts 110v-220v. Some units were packaged with a region converter cartridge and a game. Units produced: unknown, probably ~3,000-4,000, but there might have been a lot more.
Asian / HK units: these were again normal Japanese units, with different boxing only, and a 200-240v power supply. These units all have their model numbers end in -07. Not much to say about these, their boxes were in English instead of Japanese. They are a nice option if you live in PAL land but want a 60hz machine without modding, as their 220v power supply makes voltage converters unnecessary. They had counterparts for almost every Japanese boxed release. Known motherboards are VA0, 1, 3, 5, 7, 13, and 15. The last few units came with Video CD cards preinstalled, and had a red "Video CD" label on the console and the boxing had unique yellow colors instead of white.
Korean units: not to be confused with the Samsung Saturn. These were Sega branded model 2s, model number MK-80200A-08. They are similar in appearance to the US model 2s, but with the Japanese-style Sega Saturn logo instead of the western-style logo. They were made in 1997 and distributed by Kama Entertainment, use VA13 boards, region is set to 1 for Japan, the BIOS version states v1.01, and the power supply is 220v.
Tectoy Sega Saturn: sold in Brazil by Tectoy, these units were essentially rebranded USA units at first (both model 1 and 2), then Japanese white units, and lastly Derby Stallion Skeleton Saturns. All these units had a few internal modifications: custom power supplies were added, all serial numbers were removed, the region was changed to region 4 for USA when necessary, and units were fitted to output PAL-M signal. This sometimes included changing the master clock to 14.302446 Mhz, but sometimes they only added a separate sub-board with an oscillator, and fed the clock input directly to the video encoder, leaving the default 14.318 Mhz master clock in place. Since all serials were removed, it is impossible to guess how many of these were made.
Sunseibu SGX: a unit that was apparently used as a hotel kiosk with a coin based timer system, and could house multiple game CDs inside which were selectable. There is not enough info on this, but the one internal screenshot seen has suggested that it used a VA SG or VA SD type board.
SKC: short for Sega Karaoke Commander, this was a Denon/Columbia built dedicated Karaoke machine with multiple audio/video outputs, multiple microphone inputs, dedicated high quality mixers and DSPs, a modem, a SCSI hard drive, and connections for an optional CD Changer that could house ~50 discs, and for a coin counter. The unit connected to the internet and to download midi-esque song data + lyrics, and other updates such as latest news, ads, weather forecasts, etc. You could then select a song to play (even queue up multiple ones), and show off your karaoke skills for a few coins. It is assumed that the CD Changer could be filled with discs and then the system could double as a jukebox, but this is unknown. It could also play Saturn games, but with no battery backups and cart connectors, this function was limited - and it is unknown how it would've functioned with the coin input. Internally the machine uses mostly Denon boards, a Roland DSP board, and a Saturn board based on a VA0, but labelled as "Commander" instead, with its own BIOS. The machine has no RGB out, but has 4-6 Composite and S-video outputs, perhaps driving all of them at the same time. There was a later revision called SKC-1000C which reduced the huge amount of boards inside. The main motherboard on that one was labelled "Commander C", and included the full Saturn hardware, the hard drive controller, and the ROM board (those were separate on the SKC-1000).


Fonte:

- https://segaretro.org/Sega_Saturn/Hardware_revisions - (2022/10)
