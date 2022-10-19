# Dragon-Beta
Reverse engineered PCB of the never-released 1984 Dragon Beta machine from Dragon Data

## ackground
The Dragon Beta was a machine in development at the time of Dragon Data's demise in 1984. Only two boards are known to still exist - although one of those has not been verified for over ten years. The one board which remains is in the care of the Dragon Data archive at http://www.dragondata.co.uk. It is this latter board which has formed the basis for this current reverse engineering project. Richard, from the Dragon Data archive had made some very clear photographs of his Dragon Beta board before, during and after it's restoration. That board was returned to working order, but understandably Richard was not keen to continually use such a rare piece of computing history.

Initially, and somewhat secretly, I (John Whitworth) began to trace the circuitry using Paint Shop Pro and KiCad. That is, I'd have the high quality images of the desoldered PCB on the screen, and would slowly build the circuit in KiCad, whilst drawing coloured bold lines over board traces that I'd already dealt with on the schematic in KiCad. The process took, in all, about 6 months.

During that time, as I started to feel less like it was an impossible mission, I revealed to a gradually larger and larger group exactly what I was doing.

## Development

It's ended up being a very closely knit Facebook Messenger team who have come together to actually get this board working - mainly Phill Harvey-Smith, Richard Harvey, Mike Miller and myself. The original boards I ordered had a few mistakes on them. Some Vcc and GND pins not connected on ICs, as well as one of the select pins on the 74LS138, which is used to drive many devices on the board.

I managed to get my board built really quickly, and it came up with the OS9 is loading screen - but nothing else happened. At this point, Phill also built his board, and we were to start diagnosing the issues together. In reality, there was very little actually wrong with the board as it was made. Just the aforementioned power connections, the LS138 configuration, and the fact that I'd missed a little Dragon Data bodge on the back, which was a 4.7K pull-up resistor on one of the expansion port control lines. This was effectively throwing an interrupt request spuriously, and stopping the machine from running. Mike has been a huge support to me throughout all of this, being my sounding board for many issues. I lost count of the amount of logic analyser images and videos I sent him!

## Improvements and Addons

Many of the components used on the Dragon Beta are really obsolete - to the point of being almost unobtainable. Phill has gone to great lengths to create some really good add-on boards which can be used to replace the archaic SRAM chips that handle paging, as well as replacing the 32 DRAM chips which provided the original 256K. These are replace by a small daughterboard. He has also created a 512KB expansion RAM which plugs into the expansion port and effectively takes the machine to 768K of RAM.

Another archaic part of the Beta was it's use of the original Sony 26-pin floppy drive connector. This is different to the Amstrad 26-pin connector. Phill has put together a 26-pin to 34-pin connector, which allows the connection of normal floppy disk drives.

The last area for now is improvements to the keyboard interface. The original Dragon Beta used a matrix scanned keyboard. As with many other old machines, Phill put together a PS/2 keyboard adapter, and now has a USB keyboard and mouse adapter (yes, the Dragon Beta had a mouse - it also had a lightpen - but we will likely leave that back in 1984!)

## Board Revision

The boards which are available at this repository are the slightly updated ones, which contain some ease-of-use modifications. Some of those are to allow Phill's add-on components to be plugged in more easily (e.g. header pins for control signals etc.), whilst others are about completing the expansion port wiring up, and adding a few useful control signals to that as well.
