# 0013-Pico2_LA
Logic analyser variant originally by El Gusman  https://github.com/gusmanb

Please note:  The M3 mounting holes have their PTH set at 3.0mm by mistake when it should be 3.2mm

There will be a rev B of this design in the near future.
The new revision will use programmable (with a capacitor) reset supervisor IC, so
each of the PICO2 modules will have their nRESET inputs released in sequence upon power
connected to the board.
This will ensure the ttyACMx enumerations are in the sequence we want.
Then we can assign ttyACM0 as the Master and ttyACM1 as the first Slave and know
for certain that ttyACM0 references the Master pins on the signal headers.
This saves having to use DMESG to look at this PICO2 was given which ttyACM port.
