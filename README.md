Download configuration over SPI to DIPSY (a sub-5 USD FPGA board).

Raspberry PI (excerpt from https://github.com/piface/pifacecommon/blob/master/docs/installation.rst):
1. Remove "spi-bcm2708" from the blacklist in /etc/modprobe.d/raspi-blacklist.conf
   or (kernel 3.18 or newer): add dtparam=spi=on to /boot/config/txt
2. Reboot or modprobe spi-bcm2708
3. Pinout on P1:
	25 = GND
	24 = SS (SPI HW)
	23 = SCLK
	22 = RESET
	21 = MISO
	20 = GND
	19 = MOSI
	18 = CDONE
	17 = +3.3V
	16 = SS

Intel Edison Arduino breakout:
1. Update to the latest version as of 2015-09-05.
2. Pinout on J1B1:
	 8 = RESET
	 9 = DONE
	10 = SS
	11 = MOSI
	12 = MISO
	13 = SCK

Beaglebone (tested on revision A3):
1. Update to the latest Debian image.
2. Pinout on P9
	1,2 = GND
	3,4 = +3.3V
   Pinout on P8
	 8 = RESET
	10 = SS
	12 = DONE
	14 = MOSI
	16 = SCK
