---
redirect_from: "/sbc/odroid_xu4"
---

## Odroid XU4

![Odroid XU4](https://wiki.odroid.com/lib/exe/fetch.php?tok=ad1940&media=https%3A%2F%2Fdn.odroid.com%2Fhomebackup%2F%2F201506171531272562.jpg)

Odroid XU4 is single board computer designed by South Korean company Hardkernel.

### Features

| Processor |	Samsung [Exynos5 Octa ARM](exynos_5422) Cortex™-A15 Quad 2Ghz and Cortex™-A7 Quad 1.3GHz CPUs |
| --------- | -------------------------------------------------------------------------------- |
| Memory 	| 2Gbyte LPDDR3 RAM at 933MHz (14.9GB/s memory bandwidth) PoP stacked |
| 3D Accelerator |	Mali-T628 MP6(OpenGL ES 3.0/2.0/1.1 and OpenCL 1.1 Full profile) |
| Video 	| supports 1080p via HDMI cable(H.264+AAC based MP4 container format) |
| Video Out |	Standard Type A HDMI connector |
| Audio 	| Instead of On-board Audio codec, There is I2S Expansion Port(CON11) |
| USB3.0 Host |	SuperSpeed USB standard A type connector x 2 port, Max Load: total 2Amp for two USB 3.0 host ports |
| USB2.0 Host |	High Speed standard A type connector x 1 ports, Max Load: 500mA/port |
| Storage (Option) | 	MicroSD Card Slot, eMMC module socket : eMMC 5.0 HS4000 Flash Storage |
| Gigabit Ethernet LAN |	10/100/1000Mbps Ethernet with RJ-45 Jack ( Auto-MDIX support) |
| Serial console port |	Serial UART uses 1.8 volt interface. Molex 5268-04a(2.5mm pitch) is mounted on the PCB |
| RTC (Real Time Clock) backup battery connector | Molex 53398-0271 1.25mm pitch Header, Surface Mount, Vertical type (Mate with Molex 51021-0200) |
| Power | 	5V 4A Power |
| PCB Size | 	83 x 58 x 20 mm approx. |

### Hardware

Board schematics rev 2.0 [PDF](https://dn.odroid.com/5422/ODROID-XU4/Schematics/XU4_MAIN_REV0.2_20191126.pdf)

#### Block Diagram

![Odroid XU4 with Exynos 5422 structure](https://wiki.odroid.com/lib/exe/fetch.php?w=900&tok=effd4c&media=https%3A%2F%2Fdn.odroid.com%2Fhomebackup%2F201506191222574523.png)

#### Board Layout

![Odroid XU4 Board Layout](https://wiki.odroid.com/_media/odroid-xu4/hardware/xu4_detail.jpg?w=980&tok=460969)

#### Connectors

GPIO DC Electrical Characteristics (VDD = 1.80V)

| Parameter 	                 | Min 	     | Max 	    | Unit |
| ------------------------------ | --------- | -------- | ---- |
| Vih (High-level input voltage) | 	0.7 x VDD| 	VDD+0.2 |	V  |
| Vil (Low-level input voltage)  | -0.2 	 | 0.3 x VDD| 	V  |
| dV (Hysteresis voltage) 	     | 0.15 	 |	        |   V  |

#### Serial Console Port (UART)

```
_____UART____
|Pin 4 - GND|
|Pin 3 - RXD|
|Pin 2 - TXD|
|Pin 1 - VCC|
\___________|

1.8V LVTTL interface
Pin 1 : 1.8Volt output from XU4 board for the reference voltage for USB-UART board.
```

##### CON 10 - 30pin GPIO header - 2x15 pins

| Default  Pin State |	GPIO & Export No |	Net Name |	Pin Number | Pin Number |	Net Name |	GPIO & Export No |	Default Pin State |
| :----------------: | :---------------: | :-------: | :---------: | :--------: | :--------: | :---------------: | :----------------: |
| - 	             | - 	             | 5V0 	     | 1           | 2          |	GND 	 | -                 | 	-                 |
| I 	             | XADC0AIN_0 	     | ADC_0.AIN0| 3 	       | 4 	        | UART_0.CTSN| 	GPA0.2 (#173) 	 | I(PUDN)            |
| I(PUDN) 	         | GPA0.3 (#174) 	 | UART_0.RTSN| 	5 	   | 6  	    | UART_0.RXD |	GPA0.0 (#171) 	 | I(PUDN)            |
| I(PUDN) 	         | GPA2.7 (#192) 	 | SPI_1.MOISI| 	7 	   | 8 	        | UART_0.TXD |	GPA0.1 (#172) 	 | I(PUDN)            |
| I(PUDN) 	         | GPA2.6 (#191) 	 | SPI_1.MISO | 	9 	   | 10 	    | SPI_1.CLK  | 	GPA2.4 (#189) 	 | I(PUDN)            |
| I(PUDN) 	         | GPA2.5 (#190) 	 | SPI_1.CSN | 	11 	       | 12 	    | PWRON 	 | Input Range (1.8V ~ 5V)|  	I         |
| I(PUDN) 	         | GPX1.5 (#21) 	 | XE.INT13  | 13 	       | 14 	    | I2C_1.SCL  | 	GPB3.3 (#210) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX1.2 (#18) 	 | XE.INT10  | 	15 	       | 16 	    | I2C_1.SDA  | 	GPB3.2 (#209) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX1.6 (#22) 	 | XE.INT14  | 	17 	       | 18 	    | XE.INT11 	 | GPX1.3 (#19) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX2.6 (#30) 	 | XE.INT22  | 	19 	       | 20 	    | XE.INT20 	 | GPX2.4 (#28) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX2.5 (#29) 	 | XE.INT21  | 	21 	       | 22 	    | XE.INT23 	 | GPX2.7 (#31) 	 | I(PUDN)            |
| I 	             | XADC0AIN_3 	     | ADC_0.AIN3|  23 	       | 24 	    | XE.INT17 	 | GPX2.1 (#25) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX1.7 (#23) 	 | XE.INT15  | 	25 	       | 26 	    | XE.INT16 	 | GPX2.0 (#24) 	 | I(PUDN)            |
| I(PUDN) 	         | GPX3.1 (#33) 	 | XE.INT25  | 	27 	       | 28 	    | GND 	     | - 	             | -                  |
| - 	             | - 	             | VDD_IO(1.8V)|  	29 	   | 30 	    | GND 	     | - 	             | -                  |

##### CON 11 - 12pin GPIO Header - 2x6 pins

| Default Pin State |	GPIO & Export No |	Net Name |	Pin Number | Pin Number |	Net Name | GPIO & Export No  |	Default Pin State |
| :---------------: | :----------------: | :-------: | :---------: | :--------: | :--------: | :---------------: | :----------------: |
| - 	            | - 	             | 5V0 	     | 1 	       | 2 	        | GND 	     | - 	             | -                  |
| - 	            | - 	             | VDD_IO(1.8V)|  	3 	   | 4 	        | I2C_5.SDA  | 	GPA2.2 (#187) 	 | I(PUDN)            |
| I(PUDN) 	        | GPX3.2 (#34) 	     | XE.INT26  | 5 	       | 6 	        | I2C_5.SCL  | 	GPA2.3 (#188) 	 | I(PUDN)            |
| I(PUDN) 	        | GPZ.0 (#225) 	     | I2S_0.SCLK| 7 	       | 8 	        | GND 	     | -                 | -                  |
| I(PUDN) 	        | GPZ.1 (#226) 	     | I2S_0.CDCLK|  	9 	   | 10 	    | I2S_0.SDO  | 	GPZ.4 (#229) 	 | I(PUDN)            |
| I(PUDN) 	        | GPZ.2 (#227) 	     | I2S_0.LRCK|  	11 	   | 12 	    | I2S_0.SDI  | 	GPZ.3 (#228) 	 | I(PUDN)            |

### Software

#### Linux Images

- Latest Ubuntu 18.04.3 Official [images](https://odroid.in/ubuntu_18.04lts/XU3_XU4_MC1_HC1_HC2/) ([download](https://odroid.in/ubuntu_18.04lts/XU3_XU4_MC1_HC1_HC2/ubuntu-18.04.3-4.14-mate-odroid-xu4-20190929.img.xz),[MD5SUM](https://odroid.in/ubuntu_18.04lts/XU3_XU4_MC1_HC1_HC2/ubuntu-18.04.3-4.14-mate-odroid-xu4-20190929.img.md5sum))
- [Armbian](armbian) Images:
  - Ubuntu 20.04 based Armbian Focal ([torrent](https://redirect.armbian.com/odroidxu4/Focal_legacy_xfce.torrent))
  - Debian 10 based Armbian Buster ([torrent](https://redirect.armbian.com/odroidxu4/Buster_legacy.torrent))

### References

1. [ODROID Wiki - Odroid XU4](https://wiki.odroid.com/odroid-xu4/odroid-xu4)
2. [Hardkernel Official Web Site - ODROID](https://www.hardkernel.com)
3. [ODROID XU4 Schematics](https://dn.odroid.com/5422/ODROID-XU4/Schematics/)
4. [ODROID Wiki - Expansion Connectors](https://wiki.odroid.com/odroid-xu4/hardware/expansion_connectors)
5. [Odroid XU4 - Armbian](https://www.armbian.com/odroid-xu4/)
6. [ODROID Wiki - Hardware](https://wiki.odroid.com/odroid-xu4/hardware/hardware)