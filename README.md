Initially this was to document all the mods that I've done on my ender 3 since 2020.

## Intentions with the modifications

### Why this exists?

Creality Ender 3 has been a gamechanger in the 3d printing community, whether you like to admit it or not. But, the downside (and maybe
a good thing) with it has been its mod-ability / upgradability.

Although you can mod an ender 3 into a switchwire, but that really defeats the purpose of it being an "ender 3", specially because of taking the
core-xz route. This repo exists mainly to showcase an ender 3, that could be modded (somewhat) easily, and somewhat defying its End-Of-Life amidst
being in the Voron / BambuLab / AMS / CoreXY era.

The mods done here keeps the main spirit of ender 3 alive, but add enhancements and quality of life improvements in the era of high speed, highly reliable
3d printers. Also, the mods here are a bit opinionated on the fact too not overdo it, because you can always buy a Bambulab / Voron / new gen Creality printers for cheap.

In short, this mod is to make Ender 3 a highly reliable, no-headache machine that keeps up with (most of the) state of the art in 3d printing.

## Mods

1. Klipper (offcourse)
2. Dual Z axis
3. Flexible PEI bed
4. Silicon Bed Spacers
5. BTT smart filament sensor
6. Bottom PSU mount
7. Tall legs
8. Inset display mount
9. BTT Manta E3EZ + CM1 Board
10. Sprite Pro Extruder (12.5mm3)
11. Spriteburner Mod (with 5010 fan)
12. Bimetal Heatbreak
13. Hardened Steel Nozzle
14. Klipper!! (offcourse)
15. Linear X Axis Rails
16. Linear Z Axis Rails
17. BTT Eddy ( you'll need to buy a right angle usb connector to fit it in the E3EZ port unless you want to mod the mainboard enclosure ) (doing the [z-offset](https://github.com/bigtreetech/Eddy?tab=readme-ov-file#z-offset))
18. Nozzle wiper
19. Ceramic Hotend for Sprite Pro Extruder (28.5mm vs 32mm3)
20. Eddy-NG
    
## Recommended Accessories

1. Fiament Dryer
2. Crafting Knife
3. ADXL sensors

## Future plans ?

1. Webcam feed
2. Obico server
3. Linear Y axis rails ( Only if Klipper gets native support for strain gauge )
4. Load Cell based Z Offset on Hotbed (Can be based on PRtouch on Ender 3v3 se/ke )
5. ✅ BTT Eddy
6. ✅ Linear Z axis rails (actually this seem to be more important than Y axis, because Z v-slot wheels seems to loosen up due to added weight, and needs to be tightened as a regular maintenance every few months) 


## Mods on order of priority

### Phase 1 - Reliable Printing
1. Silicon Bed Spacers
2. BiMetal Heatbreak
3. CR-Touch

### Phase 2 - Klipper
1. BTT Manta E3EZ + CB1 Board
2. Sprite Pro Extruder
3. Flexible ~~PEI~~ PEZ (cold) Buildplate

### Phase 3 - Speed
1. Hardened Steel Nozzle
2. Spriteburner Mod (5010 fan version)
3. Dual Z mod
4. Bottom PSU Mount
5. BTT Eddy

### Phase 4 - Quality
1. Linear X axis rails
2. Linear Z axis (essential for reducing z axis v slot wheel loosening issue)

### Phase 4.1 - Extra set 01 - Quality of Life
1. BTT filament sensor (turned out to be less harm than help, as it puts tension in the filament and causes first layer issues)
2. Filament dryer
4. Y axis linear rails (it really improves print quality, but I am waiting for linear rails compatible with load cell sensors)
5. BTT eddy

### Phase 4.2 - Manual Filament Swap
1. Nozzle Cleaner (was exteremely helpful, it was custom designed with silicon brush in mind, will share the stl and design files)
2. Custom manual swap g-codes

### Phase 4.3 - Multimaterial & Multitooling (skipped)
1. Voron Stealthburner
2. Stealthburner easy tool change mod (need to design)
3. BigTreeTech VVD (Might need to upgrade the toolhead to stealthburner)
4. [Happy-Hare](https://github.com/moggieuk/Happy-Hare) based MMU, most probably [3MS](https://3ms.3dcoded.xyz/) for multimaterial printing

>> I've done a good deal of research on this by now, the MMU setup takes away the "soul" of this project.
>> MMUs are too complicated and comes with a lot of bagage.
>> However the best solution I think would be 3MS, but I'd like to change the extruder, and design a custom filament feeder, might take some
>> inspiration from Bambulab's [AMS gear feeding system](https://www.reddit.com/r/BambuLab/comments/12x65pt/hopefully_grinding_ams_gears_doesnt_turn_into_a/), but
>> not entirely.
>> The feeder (or extruder) has to engage only when a filament is being fed or retracted, so it needs a central gear for torque deliver, and two levered gears,
>> with ratched mechanismto engage or disengage it in its direction.
>> Finally to comply with the cleanliness / tidyness of the project, the AMS has be able to be disconnected both physically and at software level easily.
>> First solution being to keep the power and usb cable in a cable wrap, and female USB and power connectors coming from the printer.
>> Second solution should be well kept klipper segments that can be commented out and disabled easily.
>>
>> Still, I think this solution is too much far fetched, not worth the trouble in the short run, but I am keeping notes if I build an AMS in future. I barely
>> need to print anything multi-color; it creates too much waste, and when I do, its gonna be only few swaps, so I am happy with the current semi-manual-auto-clean
>> setup, and it should be more than enough for 99% single color prints that I do. I't best to focus on my other project to work on something that i'll barely use.

### Phase 5 (2025) - Stealthburner
The goal in 2025 now is to keep the printer alive. While most of the things by now are in open ecosystem, but it seems like the toolhead has been discontinued by creality,
although it lasted for a while, and had great accessories. I can still make this run for 3-4 years atleast, but the toolhead itself is sort of a bottleneck for many future
things to come.

Stealthburner is an easy choice, its cheap to build, cheap to maintain, and will ensure that I can buy parts for cheap. And I already have a mount for it after the linear rail
upgrade. Also, seems like all the cheap ceramic hotends are using E3D-style groove mounts. Although I have no intention to do the MMU upgrade right now, but atleast this upgrade
will open up that door "easily", I dont have to custom design the parts as much (although I don't completely hate that process, specially now as the printer is working so reliably)

## Phase 5.1 Live Z offset with Eddy-NG
This is the final straw to make the printer "worry free".
This also means we'll be changing our Klipper to be [Kalico](https://github.com/KalicoCrew/kalico) for easy maintenance.
It will create worry free Z-Offset Calculation with eddy probe and a bit of sensorless homing.
Check out [Eddy-NG](https://github.com/vvuk/eddy-ng) for more info.
--- updates
Seems like this will be in the mainline firmware sometime soon (when it's stable) according to [this](https://github.com/bigtreetech/Eddy/issues/43) github issue. With that update,
I'll have no more nozzle digging the bed, and zero manual z-offset calibration.

### 2024 updates

- BTT eddy (recommended to buy a flat usb 3 angle connector because the mcu enclosure box doesn't leave much room left for connecting anything on the USB ports)
- PEZ (Polyurea) build plate
- ceramic hotend
- custom nozzle wiper mount
- conditional turn off of filament sensor at layer 0-2 and turn on at layer 3
- custom cable organizer

### 2025 updates

- Z axis linear rails
- Nozzle Wiper v2
- Height Adjustable mount for eddy

I've been thinking about endgame this year, and the endgame mod should incorporate as many open source mods as possible, with projects like voron, to keep the machine futureproof,
as well as to make it compatible with multimaterial system like BTT VVD.

I also wanted to incorporate a laser head / CNC (as we have linear rails now), but I haven't found any viable open source projects to
pick up for the mod right now. I was inspired by some of the early printers like Creality CP-01 and Snapmaker. Even wanted to have a rolling bed, like in creality CR-30.
But more I am modding it, more I am realizing the importance of not trying to make it too complicated.

The problem with all in one devices is, it ends up being mediocre in all things. I've also felt myself hitting the ceiling of FDM printing while trying to design and print intricate things
for watches. I might even cancel out the plan to upgrade the toolhead.

The only reason why my wish to create an all-in-one device has popped up again, might be due to the release of Bambulab H2D, which excited me for a bit, specially because of the prospect
of an all in one machine with Bambulab's software-hardware integration. But then again, the toolchanges aren't automatic. And I'd rather buy a larger X1C, Makera Carvera, Cricut and laser
cutter/ engravers separately (also throw in a high-res resin printer/ UV printer; anything that helps in desktop manufacturing/ prototyping).

#### Discontinuation of Sprite Extruder

Although I wanted to skip the Stealthburner toolhead, as Sprite Extruder is more than enough, but its "almost" unavoidable as Sprite Extruder has reached end of life in 2025. I will consider a Stealthburner
mod sometime in future. Thankfully due to X-Axis linear rails, this seems to be quite possible, also opening up the possibility of other toolheads like cnc and laser. Only gripe here is, Stealthburner is a lot more expensive than Sprite Extruder pro, and you're not getting much more. Sprite Extruder kit comes at around 45$ (kit + mount + carriage) where stealthburner kit can go for anywhere between $80 - $150.

---

#### Random tip if you are using BTT Eddy
Please ensure that your cable isn't coiled or any coiled cable is nearby. The Eddy comes with a rather long cable, don't coil it up for cable management; it creates Electro-Magnetic noise, and causes a frequent disconnects
from Eddy. If possible cut it short and resolder the cable socker (its easier to resolder the JST end).

#### Thoughts on future upgrades
The printer seem to be future proofed because of usage of many open/ community approved parts used in the build. Definitely this printer can be updated with MMU and other optional toolheads like, Laser / CNC/ Plotter / Cutter,
but all those seem to be fairly unnecessary upgrades for this printer. I didn't even bother to upgrade the Y axis V-Wheels to linear rails, because it doesn't help much.
The main philosophy of this mod, is to make a highly reliable workhorse of a 3d printer, that requires low maintenance; and that has been pretty much achieved. Any additions that diminish the reliability or maintenance will not be considered.

## Past Mods

- CR Touch (replaced with BTT Eddy)
