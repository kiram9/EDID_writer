EDID_writer
===========

Arduino based EDID writer for DVI and VGA ports

Apr 2011 Kieran Levin kiram9@yahoo.com 
If you want to modify some data scroll down and modify the bytes in command 'c'
Then load from display - change custom bytes, generate checksum, write to save values back(r,c,g,w)
See also http://en.wikipedia.org/wiki/Extended_display_identification_data
Help Commands:
  r=read hex
  b=read binary
  l=load binary from serial(gets 128 bytes of binary data from serial then returns)
  w=write
  d=displaybuffer(binary)
  e=print detailed info
  g=generatechecksum
  t=check checksum
  c=change custom bytes (compiled in)
Connection 
Arduino         VGA   DVI
Analog 4(Data)  12    7  
Analog 5(Clk)   15    6
DIO 2           14          
Power5V         9      14
GND             11     15

This allows reading, some parsing, and reprogramming of select PIC 128byte eeproms commonly used in projectors and other displays
