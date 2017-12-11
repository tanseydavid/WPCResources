Testing WPC CPU on the Bench Testing WPC CPU on the Bench Hot
Written by terryb     March 16, 2013    	Skill Rating: Advanced    	0Add
Important Warning

You wouldn't buy some hair clippers and then cut your wife's hair, so why take the same approach to soldering? Quality repair shops won't take hacked boards, so if you damage the board--which is likely if you don't have advanced soldering skills, years of experience and the proper equipment--you'll be out from $200-$400 for a replacement.
With a little knowledge and equipment it's possible to test just about every circuit on a WPC-89, WPC-S or WPC-95 board on the bench.  This article will walk you through setting up a simple test fixture and testing the CPU board. 

Keep in mind that replacing circuit board components requires advanced soldering skills and proper equipment.

While this article is intended to cover all WPC era CPU boards (WPC-89, WPC-S and WPC-95), there may be some minor differences between generations.  For example, position of the component/connector on the board or different component identifiers (WPC-95). 

Unless otherwise stated all information in this article is in regards to a WPC-89 board with the diagnostic game ROM installed.

Before Starting

Before you pull the CPU board out and start troubleshooting it's a good idea to make sure that is where your problem lies.  While sometimes it will be obvious the CPU board is the problem, other times it's not so clear.
Image Gallery

Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
Testing WPC CPU on the Bench
For example if the board won't boot, it is possible for other boards to pull down a voltage or data line and cause this problem.  Disconnect all cables from the CPU except J210 (power to the board), turn the game on and watch the LED's (discussed later) to see if the board boots up properly.

You will also want to check the 5 and 12 volt supplies at the board before moving to the bench.

Test Equipment

In addition to the test fixture described below you will need some additional equipment.  At a minimum you will need a logic probe and a DMM.  It is also helpful to have a second logic probe with a pulser, which will allow you to pulse a circuit with one probe and monitor the output with the other. 

Although you can get away without it, an oscilloscope comes in extremely handy.  My personal recommendation for a low cost scope, but still with plenty of functionality and very high customer reviews, is the Rigol DS1102E 100MHz  2-channel digital oscilloscope (see Image 1).  You can pick one up at Saelig for $399.

Note: Some logic probes will give slightly different LED indications than as described in this document.  Check your manual if you're not sure.  Also, don't forget to connect the red clip on your probe to 12 volts and set the TTL/CMOS switch to CMOS when taking switch matrix (12 volt) readings.

Some IC test clips, jumper cables and mini-grabbers will also make your life a lot easier.  While not necessary, the Switch Matrix Tester from Siegecraft comes in handy (see references for info on all of their products).

There are several instances where you will need to jumper across two connectors, or to ground.  In order to protect the CPU board from damage install a 1N4004 diode in the jumper.  This diode takes the place of the diode that would normally be in the circuit (switch matrix and dedicated switches).

I typically cut a mini-grabber jumper in half, install the diode and put heat-shrink tubing over the leads.  Leave the band on the diode exposed since you will need that for orientation.  Note: If you install the jumper backwards when testing nothing bad will happen, but your test will fail.

You absolutely need a PLCC puller to remove ASIC's without damage.  In regards to the u-shaped chip pullers I think they do more damage than just using two small flat-head screwdrivers when removing IC's.

I also recommend using the Williams diagnostic EPROM's.   The images can be downloaded from Planetary Pinball and burned onto an EPROM. They are available for WPC Alphanumeric, WPC Dot Matrix, WPC-S and WPC-95.  Not all game software will utilize every circuit on the board so by using the diagnostic EPROM we know all circuits will be tested. 

And last, but not least, you will need the CPU schematic.  In addition you will need to have access to the datasheet's for some of the IC's (they can all be found on the web).  Here's the datasheet for an LS245, which shows the internal circuitry of the chip and typically provides a Truth Table that shows the correlation between inputs and outputs. 

This comes in extremely handy when troubleshooting a circuit.

Just Google the name of the IC and the word datasheet.  Not all datasheets, and there are multiple for any given chip, will have this information so you may have to search a little.  In general I find the Motorola datasheets to be the best.

Test Fixture

The first thing you will need is a power supply with 5 volts and 12 volts at 5 amps each.  This is sufficient for testing the CPU board, but additional voltages and/or higher current may be needed for testing other boards.  This test fixture will work for all WPC boards.

I'm using a HAPP video game switching power supply, but you could instead use an old computer power supply.

You can jumper the voltages to the board or create a power cable using some 18 gauge wire and a .156, 7 pin IDC connector (see Image 2).  Wire the pins as follows and connect to J210 on the CPU board.

Pins 1 and 3 - ground
Pin 2 - key
Pins 4 and 5 - 5 volts
Pins 6 and 7 - 12 volts
Additionally it's a good idea to fuse the 5 and 12 volts sources.  Use an inline fuse holder with a 5 amp fuse for the 5 volt line and a 3/4 amp fuse for the 12 volt line.  Technically the fuse for the 5 volts could be lower (3 amps, for example) since we're only powering the logic circuits on the CPU board.

If your power supply does not have an on/off switch (as is the case with the HAPP supply) add an inline switch to the power cord.

For a more advanced test fixture, see the references.

CPU Overview

The CPU is the brain of your pinball game and has four large chips that do most of the work (see Image 3).  From top to bottom on the CPU board are the CPU (Motorola 6809), game ROM, memory chip and ASIC.  All except the memory chip are installed in sockets from the factory.

The EPROM (also called game ROM) is game specific and can range in size (capacity) from 512KB to 8MB (see the info below on CPU jumpers).  The EPROM's are erasable and can be burned with a new image to upgrade to the latest version of software for a specific game.  The ROM images are available at ipdb.org or Planetary Pinball (Williams/Bally).   Diagnostic ROM's are also available at Planetary Pinball.

The large square chip is the ASIC, which is custom made for Williams and no longer manufactured.  The ASIC manages most of the boards input/output functions.  You can still find some NOS (new-old-stock) ASIC's out there, but they will soon be impossible to find.

For some reason ASIC's do not use the same convention for numbering pins as other chips.  Pin 1 is in the middle of one side and indicated by a small dot on the case of the chip.  See Image 4 for more info.

The bottom third of the board is the circuitry for the switch matrix and dedicated switches.

The CPU board sends data to the audio, display and power driver boards through buffers and the large ribbon cables.

The watch-dog or blanking circuit prevents any solenoids, motors, etc. from being energized before the CPU has successfully completed its boot cycle.

WPC-S and WPC-95 games also have a PIC (programmable integrated circuit) security chip, which is game specific.  When swapping a CPU board between games the game ROM and the PIC chip must stay with the correct game.  The PIC chip has an embedded serial number which is displayed briefly when the game is turned on.

NOTE: You can purchase the PIC chip at Shifted Bit or one of the major online pinball parts retailers (remember they are game specific).  The code is not available to burn your own.

The board has three diagnostic LED's that indicate the status of the board (covered in-depth later).

Board Versions

There are six versions of the WPC board set: WPC Alphanumeric, WPC Dot Matrix, WPC Fliptronics, WPC DCS, WPC Security and WPC-95.  For more detailed information, including which boards where shipped in which games, see WPC Board Versions.  In general these test procedures will work for all WPC boards although the chip designators may vary between WPC-89 and WPC-95 boards.

CPU Jumpers

Early WPC games (Funhouse, Bride of Pinbot and possibly more) were jumpered for a 512KB or 1MB EPROM.  These boards cannot be used in newer games unless the jumper setting is changed to handle the larger size EPROM's (2MB-8MB).

The jumper, a zero ohm resistor, is located to the right of the EPROM.  For a 512KB or 1MB chip the jumper should be in the W2 position and for 2MB, 4MB or 8MB chips it should be in the W1 position.  In Image 5 you can see the white resistor in the W1 position.

The CPU also has jumper (or DIP switch) settings for the system language.  If you lose your settings this is the language the game will boot in.  Here's a good article at Flippers.be that covers the language settings if you need to change them.  The settings are also listed in the front of the game's manual.

Jumpwers W13 and W14 should always be installed.

Initial Inspection

The first thing I do with any board is a visual inspection.  I check for burnt spots from overheated components, previous repair work and the quality thereof, cold solder joints, broken traces and damage from leaking batteries.  It's a good idea to do this evaluation using some form of magnification, and back-lighting the while checking traces really helps (see Image 15).

Anytime I see jumpers or other indications of lifted traces, pads or damaged through-holes (usually as the result of a chip being replaced) I check continuity using a DMM.  You want to check from the IC pin, for example, to the trace (you can use a sharply pointed test probe to push through the green solder mask) or the component the trace goes to.  For through-hole damage, check continuity from one side of the board to the other.

See Image 6 for a very typical example of the kind of board repair I come across.  The individual destroyed several through-holes while replacing the IC and then added jumpers to bypass the damage.  If you look closely at the pins on the second chip from the bottom you can see where the solder didn't flow through the board.

In order to get the switch matrix to work I had to press down on the chip.

If you're an experienced solderer you'll want to repair any previous sub-standard work.  Although I do recommend getting the board working before cleaning up old work.  If you're not up to doing board rework and have no desire to tempt fate, just repair what is needed to get the board working (or better yet, send the board out for repair).

At the same time make sure that all chips are properly seated.

Power-On Test

The three diagnostic LED's will indicate the status of the CPU as it boots.  The top LED (D19) indicates the status of the blanking circuit and should come on immediately when the CPU is powered up and then go off after about 3 seconds, and stay off  The middle LED (D20) should start flashing when D19 goes out and indicates the CPU is running.  The bottom LED (D21) should be on all of the time and indicates that 5 volts is present.

See Image 7 for the location of the diagnostic LED's.

The diag LED's are also used to indicate some board failures.  This information is provided in the front of the game manual and excerpted below.  All tests presume the supply voltages (5 volts and 12 volts) are good.  Also note that when you turn off power to the board all 3 LED's will glow dimly indicating that the LED's are good.

D20 blinks once -- U6 game ROM bad (G11 on WPC-95).
D20 blinks twice -- U8 CMOS RAM bad.
D20 blinks three times -- U9 ASIC chip bad (WPC-89) or PIC security chip bad (U22 on WPC-S or G10 on WPC-95).
D20 never blinks --  Check D19 status: If it's on the CPU will not boot.  If it's off check the game ROM.
Note: You can get a flashing D20 even if 12 volts is missing at the board, but the board won't work properly.  It is also possible to get a flashing D20 when the board has data or address line problems.  I just worked on a board where most of the address lines were 3 volts instead of 5, but the LED indicated the board had booted.

Testing the CPU

Blanking Problems (D19)
Dead CPU
Data/Address Line Problems
Check Fuses F114 and F115
Switch Matrix Problems
Dedicated Switch Problems
I/O Problems
Blanking Problems

If D19 doesn't turn off the CPU will not boot.  First check pin 3 of U21 (blanking signal from the ASIC), which should be high. If it is high and D19 doesn't turn off then there is likely a problem with the amplifier chips, either U21 or U5.  If it is low then the signal from the ASIC chip is bad indicating a problem with the ASIC, the 6809 processor or one of the clock circuits.

You can test the 8MHz and 32Khz clock signals (see Image 8) at pins 34 and 35 on the CPU.  These signals come from pins 81 and 82 on the ASIC.  If one or the other is missing check the clock inputs to the ASIC at pins 55 and 70.  If either input is missing check crystal X1 (32Khz) or crystal X2 (8Mhz), as appropriate, and their associated circuitry.

Dead CPU

It doesn't happen often on WPC games, but sometimes nothing happens when you power up the CPU.  You have 5 volts and 12 volts at the board, the D21 LED is on (5 volts), but D19 (blanking) and D20 don't even blink. 

Do a thorough visual inspection.
Check all previous board work.
Look for cracked or broken traces, pads and through-holes.
Check any questionable areas with a DMM.
Look for battery damage.
Check the ROM jumpers.
Reseat the ASIC.
Check the pins on the ASIC while it's removed.
Reseat the game ROM and CPU.
You can check the checksum of the game ROM with a ROM programmer.
Check reset and IRQ.
Pin 37 of the CPU (U4) is the reset and should be low when the board is powered on and then go high (5 volts).
If it never goes high the probable culprit is U10.
Pin 3 of the CPU is the IRQ and is normally high with fast low pulses.
Check 8MHz and 32Khz clock signals.
Check pins 34 and 35 on the CPU for the clock signals (the ASIC provides these clocks).
Although it's rare, a bad ASIC or CPU socket can keep the game from booting.
The CPU will typically not boot if any address or data lines are missing.
See the following section for more information.
Data/Address Line Problems

The CPU board has a single address bus and single data bus that connect the ASIC, CPU, ROM, RAM, buffers, flip-flops, etc.  There are 16 address lines (A0 through A15) and eight data lines (D0 through D7).  A bus structure has a one to many relaionship.  In other words, one address/data line will go to multiple IC's.   Therefore, with the exceptions noted below, A0 on any chip will have conductivity to A0 on any other chip.

It is important to note that not all chips on the bus use all of the address or data lines.  For example, U1 only uses A0 through A4 and U2 only uses A5 through A12.  These differences, and there are many more that I have not listed, are important to note because it will aid in troubleshooting situations where one or more address lines are being pulled low.

There are a couple of exceptions where dedicated address lines exist that are not part of the bus.  There are five address lines (A14 through A19) that go between the ROM and the ASIC and two address lines (A13 and A14) that go between the RAM and the ASIC.  These lines will not have conductivity to any other address lines even if they have the same identifier (for example, A14).

The two most common causes of data or address line problems are cracks in one or more traces or a component pulling the line down.

In the case of a cracked trace the address or data line, A0 for example, will show activity on some components, but not all.  If a line is being pulled low then all of the components on the bus that use that address or data line will show no activity (or a low signal).

Cracked traces typically occur because EPROM's are replaced with the board in the game.  This flexes the board and results in damage to the traces.  The break will often occur at the point where a trace is soldered to a pad so check thoroughly.

I prefer to use an oscilloscope or logic probe to test the address/data lines at each component to narrow down the problem.  All address and data lines should have activity as shown in Image 9, with a minimum of 4 volts peak to peak.

The next step is then a visual inspection to identify the damaged trace.

If you don't have an oscilloscope you can use a DMM in continuity mode to test conductivity between the data and address lines on each component.  This is rather tedious, but it will get the job done.

If you have low, or zero volt, address or data lines on all components that use that line, the problem is caused by a component pulling down the circuit.  For example if D0 reads 0 volts at all test points then any component that uses D0 could be the cause. Remember that all data and address lines don't go to all components on the bus, so this may help you narrow down the problem.

Without expensive test equipment this type of problem be very difficult to isolate.  Often the only choice is to start swapping components, removing non-essential components (buffers, flip-flops, etc.) or cutting traces until the problem goes away.

You can also, but not always, verify this issue by testing the resistance between each data/address line and ground (with the board un-powered).  The problematic line will either read a dead short or a much lower resistance. 

One other quick test is to bend up the lead for the suspect data/address line on the CPU and then test it for activity.  The risk of course is that you break a pin if you're not careful, or it was already weak.  If there is no activity then the CPU is bad, if there is activity then continue to isolate other components. 

Note: You can power the board without a game ROM installed and the CPU will run without a program.  It will execute all NOP's (non-operative instructions) and cycle through all addresses.  The data lines will not be active in this situation, but you can check to see if the ROM is pulling down a line.

In addition to the ASIC, ROM, RAM or CPU pulling down a line, the problem can be with one of the buffers or flip-flops.  I have seen U1 or U2 pull down address lines and U3, U7 or U12 pull down data lines.

Sometimes installing the board in a game or a WPC test fixture with the display and peripheral boards active will provide more information.

Check Fuses F114 and F115

First a little background.  Switch 24 in the switch matrix does not exist.  Instead there is a diode mounted on the coin door interface board across column 2 and row 4.  If the CPU does not see this closed switch it presumes there is a problem with the 12 volts and the error is displayed.

The error message can be caused by blown fuses, a problem with the 12 volt circuit or switch matrix issues.  If you are getting this error while the board is in the game and there is 12 volts at the CPU, then the problem lies with the switch matrix.  See the section below for troubleshooting the switch matrix.

Switch Matrix Problems

The switch matrix columns are pulsed (normally high, 12 volts, with very fast pulses going low--see Image 10) so troubleshooting them requires an oscilloscope or logic probe.  For more info on the switch matrix operation see Switch Matrix - Theory and Troubleshooting.

Image 11 shows the switch matrix diagram from an Addams Family.  Note: J206 and J207 (column drives) are electrically the same and the connector may go to either one.  The same is true of the two switch row connectors, J208 and J209.

Switch matrix problems on the CPU are typically indicated by an entire row or column not working.  There are times though when CPU problems can cause very odd behavior of the switch matrix . For example, when one switch is closed, the entire row of switches indicates closed.  This is caused when the column is shorted low.

You can test the eight column drives with an oscilloscope or logic probe.  If testing with a logic probe the yellow LED (pulse) will be on, the red (high) will be very bright and the green (low) will be dim.  This is because the pulses are very fast, normally high and pulsed low (0 volts).

If any or all of the pins are not pulsed, check the input to the ULN-2803 (U20, pins 1-8).  Since U20 is an inverter the green led on your logic probe will be bright and the red dim.  If the inputs are good, but the outputs are not (pins 11-18, which are connected directly to J207 and J206 and will read the same) then U20 is defective. 

If there is a problem with the inputs to U20 then the problem is most likely the LS374SC (U14).  Be aware that it is common for the column circuitry to have been damaged by a high voltage (solenoids, etc.) being applied to the switch matrix.  If this has happened it is likely both U20 and U14 have been blown.

Note: Some games (for example Creature from the Black Lagoon) do not use all 8 column drivers and the unused ones won't be pulsed.  You can check using the switch matrix diagram in the manual to see if all columns are used (this is why I use a diagnostic ROM).

In order to test the row circuitry we'll need our jumper with the diode installed (see Image 12).  The end of the jumper with the banded side of the diode should be placed on the column side.  Attach the jumper to J207 pin 1 (after it has been verified good) and the other end to J209 pin 1.  When column 1 is pulsed we will now see the pulse on row 1.

Note: You can also use the Siegecraft switch matrix tester discussed earlier instead of a jumper.

Looking at the CPU schematic we can see that row 1 is connected to U18 (LM339) at pin 11, with the output at pin 13, which then goes to U13 (74LS240).  Using your logic probe or oscilloscope check pin 11 for a pulse.   If there is no pulse then check resistor R51 and diode D3.

If there is a pulse at pin 11, then check pin 13.  If there is a pulse at pin 11 and none at pin 13 then U13 is defective.

Since the output of U13 is data there is no way to test it without a logic analyzer.  If the board is having row problems while in the game and everything else tests good then you can assume U13 is defective.

Move the jumper to row 2 and check the circuit in the same way.  Continue through all the rows (U19 is used for rows 5 through 8).

Direct Switches

The return side of the dedicated switch circuit works the same as the row (return) circuit in that it senses when the line goes low.  There is no column circuit since the switch provides a path to ground instead (see Image 13). 

Attach the jumper to J205, pin 1 and the banded side of the diode to ground (see Image 14). 

Looking at the CPU schematic we can see that row 1 is connected to U17 (LM339) at pin 5, with the output at pin 2, which then goes to U17 (74LS240).  Using your DMM check pin 5, which should be low.   If it is not low then check resistor R50 and diode D15.

If pin 5 is low, then check pin 2.  If pin 5 is low and pin 2 is not low, then U17 is defective.

Since the output of U15 is data there is no way to test it without a logic analyzer.  If the board is having direct switch problems while in the game and everything else tests good then you can assume U15 is defective.

Continue to test the other direct switch circuits.  Note that U16 is used for direct switches 5 through 8.

I/O Problems

Input/output circuits process data to and from other boards (video, sound, etc.) and use buffers to prevent cross-talk and interference.  The CPU board has 5 buffer chips: U1, U2, U3, U7 and U12, which can occasionally go bad.  Random problems with the sound, video or driver board are all indicative of buffer or ribbon cable problems.

Note: The diagnostic game ROM seems to have a lot less I/O activity than a standard game ROM.  Therefore when troubleshooting I/O problems it is best to use the latter.  In my case I typically use an Addams Family ROM.

The following table provides the chip ID, type of chip, whether it is unidirectional or bidirectional, if it processes addresses or data, what the enable signal is and which I/O connector is used..

Buffer	Chip	Bidirectional	Adr/Data	Enable	I/O
U1	74LS244	No	Address	IOEN	J202
U2	74LS244	No	Address	IOEN	J201
U3	74LS245	Yes	Data	IOEN	J202
U7	74LS244	No	Data	DISEN	J204
U12	74LS240	No	Data	DREN	J211
The unidirectional buffers need a low on pin 1 and 19 to enable data flow.  Pins 1 and 19 are tied together externally from the chip and each pin controls half of the buffers.  While there is always data on the input pins, the buffer only passes data through to the output when pin 1/19 is low.

First verify that pin 1/19 are being pulsed low.  Note: Depending on I/O activity and your scope settings it can be difficult to catch the pulses on pins 1/19, and also on the output pins.  So give it a few seconds before deciding there is no activity.

Note: If you are using a non-DMD game or diagnostic ROM, you will not be able to test U7 since it is the buffer for the alpha-numeric display.  If you are using an alpha-numeric game or diagnostic ROM, you will not be able to test U2 since it is the buffer for the dot matrix display. 

You can also get tricky and use pin 1 as the trigger for your scope when looking at the buffer outputs.

If an input pin has activity (2, 4, 6, 8, 11, 13, 15 and 17). the associated output pin (18, 16, 14, 12, 9, 7, 5, and 3, respectively) should also show activity .  For example if pin 2 has activity, when pin 1/19 goes low, pin 18 should have activity, although less than it's input pin.  See the LS240 datasheet for more info.

There is one bidirectional chip (U3), which passes data in one direction if pin 1 and pin 19 are both low and in the opposite direction if pin 1 is high and pin 19 is low.  See the LS245 datasheet for more info.  You can test it using the pin configuration in the data sheet and the method described above.  Just remember the inputs and outputs swap based on the signals at pin 1 and 19.

While testing the buffers as described is a good test, it is not a definitive test.  If the buffer tests bad, it is bad, but if it test good it may in reality have problems when under load (the other boards connected).  I have seen cases where the buffer voltages where soft, meaning they worked fine with no load, but did not work when under load.

Tags
logic probe
CPU
WPC-89
WPC-95
WPC-S
oscilloscope
Reference 1
Electronics Tutorial - Test Equipment
Reference 2
Building a WPC Test Fixture
Latest Listings

Pad and Trace Repair
Category: Board Rework and Test
When it comes to pad and trace repair the two common solutions are copper foil or jumpers. Both...
Repairing WPC Dot Matrix Controller
Category: Board Rework and Test
Display problems are typically the result of failing DMD's, bad ribbon cables or connectors, a cable installed one pin...
Building a WPC Test Fixture
Category: Board Rework and Test
As my Dad would say, there are several ways to skin a cat. So while this may not...
Board Rework Standards
Category: Board Rework and Test
While it's not always feasible for a hobbyist to adhere to industry standards in regards to board rework, it...
Circuit Board Updates
Category: Board Rework and Test
While I'm not a huge proponent of upgrading circuit boards (in most cases I find very little benefit versus...
Micro-Blasting Circuit Boards
Category: Board Rework and Test
The two primary reasons for micro-abrasive blasting a pinball circuit board are to remove the green solder mask (commonly,...
