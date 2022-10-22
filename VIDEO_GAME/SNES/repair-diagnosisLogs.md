# Nintendo Super System (and SNES) repair/diagnosis logs

## Main Nintendo Super System Page

# Table of contents

- Troubleshooting Tips

- Super System motherboard repair log

- CPU failures

- PPU failures

- "What-if" failures


# Nintendo Super System / SNES troubleshooting tips

- If working on a Nintendo Super System (arcade) motherboard, be sure to use a V3 BIOS (I've seen several faulty boards wouldn't boot to the menu on V1 or V2, even though the menu circuitry was fine)

- Again, on the Nintendo Super System, be sure to check the +5V at the board and adjust. The stability of the system doesn't seem very sensitive to an exact voltage, but there is no voltage regulator (like the SNES), so the entire SNES circuitry will be running directly from the +5V from the power supply. If the voltage is adjusted too high, it's likely to significantly shorten the life of the chips (possibly the cause of some of the failures I came across).

- A bad CPU seems to be the most common failure, and has many different symptoms (see specific failures below)

- My experience is that PPU1, PPU2, and VRAM failures don't affect game logic, just the display of the game (though in some cases will cause certain games not to boot). So, for example if the Mario Kart track looks bad and it thinks you're off the track and Lakitu keeps picking you up, it's likely a CPU problem (or possibly WRAM)... but if the game still plays fine, I'd suspect a PPU problem (though you can have CPU problems that don't affect gameplay).

- Statistics: While working with Super System and SNES motherboards, I came across 24 bad CPUs, 4 bad PPU1s, 4 bad PPU2s, 1 bad APU, and no bad WRAMs or VRAMs... if you suspect either a bad CPU or WRAM, I'd say odds are better that the CPU is bad.

- A bad CPU can cause controller problems. I'd check the obvious first (wiring, controllers, etc. on the Super System, and swap the controller, ports, ribbon on the SNES), though if that all checks out, some controller problems I've encountered from CPUs include dead controls and buttons seemingly connected together (press one button and multiples show as pressed).

- A bad APU can cause the system to not boot (not the most likely cause, but it's easy to swap on boards with the sound module).

- I highly recommend making/borrowing/buying a Burn-In test cart (described <a href="https://tcrf.net/SNES_Burn-In_Test_Cart">HERE</a> ). Even when other games won't boot, many times it'll boot, test the hardware, and tell you which tests failed. It won't necessarily tell you the bad chip, but you can make educated guesses from the results.

<img src=".assets/test.jpg">

Fonte: https://www.projectvb.com/nss/logs.htm#whatif
