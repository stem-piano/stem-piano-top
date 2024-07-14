# Hybrid MIDI Digital Piano

Check this page regularly for updates.

## Project is Active

New pianos, features, capabilities, and enhancements could be added in the future. These changes could impact the hardware, firmware, software, or the mechanical structure.

See the following file for project state:

https://github.com/gzweigle/DIY-Grand-Digital-Piano/blob/main/STATUS.md.

## Experience

It is recommended to have some experience with software and electronics projects.

## Known Issues

Take a look at any pending hardware changes or known problems before building boards or playing the piano:

https://github.com/gzweigle/DIY-Grand-Digital-Piano/issues

## Headphone and Audio System Safety

An external light source can trigger the sensors and cause one or many loud notes to play. Shield the sensors from light.

Also, although unlikely, problems or bugs with the piano could cause multiple (even all 88) notes to play at the maximum MIDI volume level unexpectedly. This could happen even if the piano is not in use. See example from a *stem piano* video:

https://youtu.be/gNeLMGaxmG0?t=173

Before playing, powering up, or using the piano in any way, please verify with another MIDI program as source that volume and all other parameters are acceptable in the event of any piano problem, including as described above. Also, check for external light triggers before increasing volume.

## Teensy USB and External Power

The Teensy 4.1 shorts its USB power connection and its +5 volt power pin. Please see this information from the Teensy 4.1 manufacturer:

https://www.pjrc.com/teensy/external_power.html

The recommended option following PJRC instructions for cutting the 5V pad on the Teensy 4.1 before using or powering the piano.

It is possible to power *stem piano* circuit boards through the USB and without a separate +5 volt power connection. This setup is great for debugging. However, when *stem piano* has all 88 key sensors connected, the total current draw will exceed the capability of an external computer that is trying to power the board through a USB cable connected to the Teensy 4.1.

## Power Supply Protection

Use power supplies that include short-circuit (overcurrent), overvoltage, thermal, and all other protection for safety. This includes the USB power source.

Some boards include places to install fuses and some may not. Fuses require design and coordination with external power sources. See each circuit board documentation.

Some boards include low dropout voltage regulators (LDO). The LDO should include short-circuit protection. See the *bill_of_materials* files in hardware directories.

## Exposed Connections

Instructions are not provided for circuit board or piano enclosures.

Shield the circuit boards from physical access.

Some pins on the circuit boards are at power level and some are at ground level. Be careful not to accidentally connect them together. For example, do not place or use anything conductive near the circuit boards.

Use a nonconductive instrument for moving the configuration switches.

Be careful with placing anything near or around the circuit boards, or with anything related to the circuit boards that are accessible to others.

The boards are low-voltage (five volts and below) but portions could under unexpected or unforseen circumstances get hot. Keep the circuit boards clear of any materials.

## EEPROM

The nonvolatile EEPROM Teensy memory wears out after approximately 100,000 writes. Under normal use this limit is sufficient. A firmware or hardware problem could result in excessive writes. Therefore, use caution if modifying firmware or hardware related to the EEPROM. At startup some firmware (depending on debug setting) displays total lifetime writes.

## Static Sensitive Parts

Be careful when soldering, assembling and using the electronic parts. Electrostatic Discharge (ESD) can damage components. An ESD damaged component could cause an intermittent failure that is very difficult to debug.

## Lead Free

Recommend lead free for everything.

## it is all: As Is

See licenses.