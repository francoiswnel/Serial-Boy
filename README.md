# Serial Boy

Serial Boy is a Game Boy Link Cable to Arduino Uno adapter. The main purpose being to connect a Game Boy Pocket Camera to an emulated Game Boy Printer.

![Serial Boy](https://raw.githubusercontent.com/francoiswnel/serial-boy/master/Images/image1.jpg)

![Serial Boy](https://raw.githubusercontent.com/francoiswnel/serial-boy/master/Images/image2.jpg)

# Get the PCB

You can upload the generated CAM job in the output directory to your favourite PCB fab, or you can generate a new CAM job from the project files, or you can use the [shared project on OSH Park](https://oshpark.com/shared_projects/0MKOwrEA). Please note that the version on OSH Park has the pin numbers incorrectly labelled since I had not realised at the time that the serial clock needs to be connected to a pin with hardware interrupt.

# Get the Game Boy Printer emulator

I've forked [mofosyne's Arduino Gameboy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator) project and reconfigured it to work with Serial Boy, since that project assumes that you'll be cutting up a link cable and directly soldering it to Arduino Micro pins. Get the [Serial Boy branch](https://github.com/francoiswnel/arduino-gameboy-printer-emulator/tree/serial-boy) and transfer it to your Arduino Uno.

# Connect your Game Boy to your Arduino

You'll need to solder some pins to the PCB, angled ones will be ideal. Insert the pins into headers 2 to 6 on the Arduino Uno, and connect the link cable to the other end of the PCB. It can fit both ways, so just orient the internal pins with the labels printed on the PCB - you'll see some pins in the cable are missing. Then follow the instructions from the [emulator repository](https://github.com/francoiswnel/arduino-gameboy-printer-emulator/tree/serial-boy).
