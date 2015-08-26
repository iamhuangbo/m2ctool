m2ctool
============================
A basic tool to assist in debugging i2c devices on MRAA based systems. This tool uses the MRAA library to implement functionality
similar to that found in the i2ctool set. 

Testing 
============================
Tested on:
Intel Edison on Mini-breakout (bus 1 can be read with i2ctools, m2ctool can read 1 and 6)
Intel Edison on Arduino (bus 6)
Intel Galileo (bus 0)

Limitations
===========================
Currently only support for reading words is implemented.

Dependencies
===========================
This tool requires the minimist package. 

To install globally : 
	npm install -g minimist 


Installation:
==========================
Copy or move m2ctool.js to m2tool somewhere on your path. 

Set permissions on m2ctool -- chmod u+x m2ctool to make executable
 
Usage
=========================
m2ctool -- a tool to scan i2c buses on MRAA based systems\n
Some device info:\n
Intel Edison on mini-breakout board can use i2c bus 1 and 6\n
Intel Edison on Arduino board can use i2c bus 6\n
Intel Galileo can use i2c bus 0\n

Use of this script is at your own risk\n

Topic help is avaialble -- mctools help '<scan|dump|get|set>'\n
scan for devices on an i2c bus\n
usage -- m2ctool scan '<bus number>'\n

dump  the registers of a device\n
usage -- m2ctool dump '<bus number>' '<device address>' '<optional -s -l>'\n
where -s is swap byte order and -l is the number of registers to return (255 default)\n
example -- m2ctool dump 6 0x18 -s -l13\n

get the value a register of a device\n
usage -- m2ctool get '<bus number>' '<device address>' '<register address>' '<optional -s>'\n
where -s is swap byte order

set the value of a device register\
usage -- m2ctool set '<bus number>' '<device address>' '<register address>' '<data>'\n
data should be in hexadecimal format


 App Files
---------------------------
* m2ctool.js
* package.json
* README.md

License Information Follows
---------------------------
The MIT License (MIT)

Copyright (c) 2015, m2ag.labs

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.