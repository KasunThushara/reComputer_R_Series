# reComputer R Series


<p align="center"><img src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/01.png" alt="pir" width="400" height="auto"/></p>

<p align="center"><a href="https://www.seeedstudio.com/Seeeduino-XIAO-Pre-Soldered-p-4747.html" target="_blank"><b><strong>🖱️ Buy Now</strong></b></a></p>

The reComputer R1000 edge IoT controller is built on the high-performance Raspberry Pi CM4 platform, featuring a quad-core A72 processor with a maximum support of 8GB RAM and 32GB eMMC. Equipped with dual Ethernet interfaces that can be flexibly configured, it also includes 3 isolated RS485 channels supporting BACnet, Modbus RTU, Modbus TCP/IP ,and KNX protocols. With robust IoT network communication capabilities, the R1000 series supports multiple wireless communication options including 4G, LoRa®, Wi-Fi/BLE, allowing for flexible configurations to serve as corresponding wireless gateways. This controller is well-suited for remote device management, energy management, and various other scenarios in the field of smart buildings.

---
# Table of Contents

- [reComputer R Series](#recomputer-r-series)
- [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Hardware Overview](#hardware-overview)
  - [Mainboard Overview](#mainboard-overview)
  - [Power Diagram](#power-diagram)
    - [2-Pin Power terminal](#2-pin-power-terminal)
    - [POE (optional)](#poe-optional)
    - [Power Consumption](#power-consumption)
    - [Power On and Power Off](#power-on-and-power-off)
  - [Block Diagram](#block-diagram)
    - [IIC Diagram](#iic-diagram)
  - [Interfaces](#interfaces)
    - [LED Indicator Status](#led-indicator-status)
    - [Buzzer](#buzzer)
    - [RS485](#rs485)
    - [Boot Switch](#boot-switch)
    - [USB](#usb)
    - [SIM Slot](#sim-slot)
    - [SSD Slot](#ssd-slot)
    - [Mini-PCle Slot](#mini-pcle-slot)
    - [Reset Hole](#reset-hole)
    - [Ethernet RJ45](#ethernet-rj45)
    - [HDMI](#hdmi)
    - [RTC](#rtc)
    - [Watchdog](#watchdog)
  - [These steps will help you test and ensure the functionality of the watchdog timer on your system.](#these-steps-will-help-you-test-and-ensure-the-functionality-of-the-watchdog-timer-on-your-system)
  - [Optional Interfaces and Modules](#optional-interfaces-and-modules)
    - [Wi-Fi/BLE](#wi-fible)
      - [Connect WiFi](#connect-wifi)
      - [Connect bluetooth devices](#connect-bluetooth-devices)
    - [4G Module](#4g-module)
    - [LoRa® Module](#lora-module)
      - [WM1302 SPI Module](#wm1302-spi-module)
      - [WM1302 USB Module](#wm1302-usb-module)
    - [Zigbee Module](#zigbee-module)
      - [To test Zigbee communication with two Zigbee modules, follow these steps:](#to-test-zigbee-communication-with-two-zigbee-modules-follow-these-steps)
    - [PoE](#poe)
    - [SSD](#ssd)
    - [Encryption Chip TPM 2.0](#encryption-chip-tpm-20)
    - [UPS](#ups)
    - [DSI \& Speaker](#dsi--speaker)
  - [Additional Resources](#additional-resources)





## Features

<table align="center">
  <tbody>
    <tr>
      <td style="width: 35.4622%;">Parameter</td>
      <td colspan="2" style="width: 63.1933%;">Description</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Hardware Spec</strong></td>
    </tr>
    <tr>
      <td style="width: 35.4622%;">Product Series</td>
      <td style="width: 31.5967%;">R10xx-10</td>
      <td style="width: 31.5966%;">R10xx-00</td>
    </tr>
    <tr>
      <td>CPU</td>
      <td colspan="2">Raspberry Pi CM4, Quad-core Cortex-A72@ 1.5GHz</td>
    </tr>
    <tr>
      <td>Operating System</td>
      <td colspan="2">Raspbian, Debian</td>
    </tr>
    <tr>
      <td>RAM</td>
      <td colspan="2">1GB/2GB/4GB/8GB</td>
    </tr>
    <tr>
      <td>eMMC</td>
      <td colspan="2">8GB/16GB/32GB</td>
    </tr>
    <tr>
      <td colspan="3"><strong>System Spec</strong></td>
    </tr>
    <tr>
      <td>Input</td>
      <td colspan="2">2-pin Terminal Block</td>
    </tr>
    <tr>
      <td>PoE(as powered device)</td>
      <td colspan="2">IEEE 802.3af Standard 12.95W PoE*</td>
    </tr>
    <tr>
      <td>Supply Voltage(AC/DC)</td>
      <td colspan="2">12~24V AC/9~36V DC</td>
    </tr>
    <tr>
      <td>Overvoltage Protection</td>
      <td colspan="2">40V</td>
    </tr>
    <tr>
      <td>Power Consumption</td>
      <td colspan="2">Idle:2.88W; Full Load:5.52W</td>
    </tr>
    <tr>
      <td>Power Switch</td>
      <td colspan="2">No</td>
    </tr>
    <tr>
      <td>Reboot Switch</td>
      <td colspan="2">Yes</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Interface</strong></td>
    </tr>
    <tr>
      <td rowspan="2">Ethernet</td>
      <td colspan="2">1 x 10/100/1000 Mbps(supports PoE*)</td>
    </tr>
    <tr>
      <td colspan="2">1 x 10/100 Mbps IEEE802.3/802.3u</td>
    </tr>
    <tr>
      <td rowspan="2">USB</td>
      <td colspan="2">2 x USB-A 2.0 Host</td>
    </tr>
    <tr>
      <td colspan="2">1 x USB-C 2.0 (For flashing OS)</td>
    </tr>
    <tr>
      <td>RS485</td>
      <td colspan="2">3 x 3-pin Terminal Block (isolated)</td>
    </tr>
    <tr>
      <td>HDMI</td>
      <td colspan="2">1 x HDMI 2.0</td>
    </tr>
    <tr>
      <td>SIM Card Slot</td>
      <td colspan="2">supports Standard SIM Card</td>
    </tr>
    <tr>
      <td>M.2 Slot</td>
      <td colspan="2">supports M.2 NVMe SSD</td>
    </tr>
    <tr>
      <td>LED</td>
      <td colspan="2">6 x LED indicators</td>
    </tr>
    <tr>
      <td>Buzzer</td>
      <td colspan="2">1</td>
    </tr>
    <tr>
      <td>Reset Button</td>
      <td colspan="2">1</td>
    </tr>
    <tr>
      <td>DSI(reserved)</td>
      <td colspan="2">supports LCD*(on board within the enclosure)</td>
    </tr>
    <tr>
      <td>Speaker(reserved)</td>
      <td colspan="2">supports Microphone*(on board within the enclosure)</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Wireless Communication</strong></td>
    </tr>
    <tr>
      <td>Wi-Fi 2.4/5.0 GHz</td>
      <td style="width: 31.5967%;">On-chip Wi-Fi*</td>
      <td style="width: 31.5966%;">No</td>
    </tr>
    <tr>
      <td>BLE 5.0</td>
      <td>On-chip BLE*</td>
      <td>No</td>
    </tr>
    <tr>
      <td>LoRa®</td>
      <td colspan="2">USB LoRa®/SPI LoRa®*</td>
    </tr>
    <tr>
      <td>4G Cellular</td>
      <td colspan="2">4G LTE*</td>
    </tr>
    <tr>
      <td>Zigbee</td>
      <td colspan="2">USB Zigbee*</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Standards</strong></td>
    </tr>
    <tr>
      <td rowspan="3">EMC</td>
      <td colspan="2">ESD: EN61000-4-2, Level 3</td>
    </tr>
    <tr>
      <td colspan="2">EFT: EN61000-4-4, Level 2</td>
    </tr>
    <tr>
      <td colspan="2">Surge: EN61000-4-5, Level 2</td>
    </tr>
    <tr>
      <td rowspan="4">Certification</td>
      <td colspan="2">CE, FCC</td>
    </tr>
    <tr>
      <td colspan="2">TELEC</td>
    </tr>
    <tr>
      <td colspan="2">RoHS</td>
    </tr>
    <tr>
      <td colspan="2">REACH</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Ambient Conditions</strong></td>
    </tr>
    <tr>
      <td>Ingress Protection</td>
      <td colspan="2">IP40</td>
    </tr>
    <tr>
      <td>Operating Temperature</td>
      <td colspan="2">-30~70 °C</td>
    </tr>
    <tr>
      <td>Operating Humidity</td>
      <td colspan="2">10~95% RH</td>
    </tr>
    <tr>
      <td>Storage Temperature</td>
      <td colspan="2">-40~80 °C</td>
    </tr>
    <tr>
      <td colspan="3"><strong>Others</strong></td>
    </tr>
    <tr>
      <td>Supercapacitor UPS</td>
      <td colspan="2">SuperCAP UPS LTC3350 Module*</td>
    </tr>
  </tbody>
</table>

---
## Hardware Overview

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/02.png" /></div>

## Mainboard Overview

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/03.png" /></div>

## Power Diagram

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/04.png" /></div>

The reComputer R1000 supports three power supply options: AC, DC terminal and PoE port. By default, the reComputer R1000 is powered through the AC/DC terminal (Official regional power adapter SKU:110061505/110061506), while **the PoE power supply(PoE module, SKU:110991925) is optional**. This provides flexibility in power supply selection and allows for easy integration with various power sources.

### 2-Pin Power terminal

<div align="center"><img width={300} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/powerplug.png" /></div>

The reComputer R1000 is supplied with a nominal AC voltage of 12~24 V or DC voltage of 9~36V. The power supply is connected via the 2-pin power terminal block connector. To ground the reComputer R1000, the ground wire can be secured to the screw located at the top left corner of the power terminal.

### POE (optional)

With the PoE module installed, the ETH0 port of reComputer R1000 can support PoE power supply, providing a convenient and efficientway to power the device over Ethernet. This option simplifies the installation process and reduces the amount of cabling required, making it an ideal solution for applications with limited power sources or where power outlets are not readily available.

* PoE input: Range 44~57V; Typical 48V 
* PoE output: 12V, 1.1A Max.

> [!NOTE]
> It's worth noting that the PoE module provided with the reComputer R1000 is compliant with the IEEE 802.3af standard and can provide a maximum power supply of 12.95W. Therefore, if there is a need to connect high-power peripherals such as SSD or 4G modules, the PoE power supply may not be sufficient. In this case, it's recommended to use the AC/DC terminal for power supply instead to ensure stable and reliable operation of the device.

### Power Consumption

Please refer to the table below for the tested power consumption of reComputer R1000 in Seeed Studio's laboratory. Please note that this value is for reference only, as the test methods and environment can result in variations in the results.

| Status   | Voltage | Current | Power Consumption | Description |
|   ---      |    ---    |   ---      |         ---          |        ---    |
|Shutdown  |24V      |  51mA  |    1.224W         | Static power consumption test in shutdown and power-off state.|
|Idle      |24V      |  120mA |    2.88W          | To test the input current when supplying 24V power to the reComputer R1000 device without running any test programs.|
|Full Load |24V      |  230mA  |    5.52W          | Configure CPU to run at full load using the "stress -c 4" command. No external devices connected. |

### Power On and Power Off

The reComputer R1000 does not come with a power button by default, and the system will automatically start up once power is connect- ed. When shutting down, please select the shutdown option in the operating system and wait for the system to fully shut down before cutting off power. To restart the system, simply reconnect to the power.

> [!NOTE]
> Please note that after shutting down, please wait for at least 10 seconds before restarting the system to allow for the internal capacitors to fully discharge.

## Block Diagram

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/05.png" /></div>

###  IIC Diagram

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/06.png" /></div>

To query GPIO mappings and offsets, please use following command:

```bash
cat /sys/kernel/debug/gpio
```
## Interfaces

### LED Indicator Status

The reComputer R1000 features 6 LED indicators that serve to signal the machine's operational status. Please refer to the table below for the specific functions and status of each LED:

| LED Indicator | Color          | Status | Description                                                  |
| ------------- | -------------- | ------ | ------------------------------------------------------------ |
| PWR           | Green          | On     | The device has been connected to power.                      |
|               |                | Off    | The device is not connnected to power.                       |
| ACT           | Green          |        | Under Linux this pin will flash to signify eMMC access.<br /> If any error occurs during booting, then this LED will flash an <br />error pattern which can be decoded using the look up [table on the Raspberry Pi website](https://www.raspberrypi.com/documentation/computers/configuration.html#led-warning-flash-codes). |
| USER          | Green/Red/Blue |        | Need to be defined by user.                                  |
| RS485-1       | Green          | Off    | No data transfer on RS485 channel 1.                         |
|               |                | Blink  | RS485 channel 1 is receiveing or sending data.               |
| RS485-2       | Green          | Off    | No data transfer on RS485 channel 2.                         |
|               |                | Blink  | RS485 channel 2 is receiveing or sending data.               |
| RS485-3       | Green          | Off    | No data transfer on RS485 channel 3.                         |
|               |                | Blink  | RS485 channel 3 is receiveing or sending data.               |

<br/>

the ACT LED blinks in a regular four blink pattern, it cannot find bootcode (start.elf)
If the ACT LED blinks in an irregular pattern then booting has started.
If the ACT LED doesn't blink, then the EEPROM code might be corrupted, try again without anything connected to make sure. For more detail please check the Raspberry Pi forum:
STICKY: Is your Pi not booting? (The Boot Problems Sticky) - Raspberry Pi Forums
For more detail please check the [Raspberry Pi forum](https://forums.raspberrypi.com//viewtopic.php?f=28&t=58151).

In this section we will use the raspi-gpio tool to test with GPIOs, you can use the raspi-gpio help to view the manual:

```bash
raspi-gpio help
```

1. The pin controlling the third LED of reComputer R1000 is gpio20. To get specific GPIO status, Please enter following command in the Terminal :

```bash
raspi-gpio get 20
```

2. Change the state of gpio20:

```
#set current pin state
sudo raspi-gpio set 20 dl
#get the pin state after set
raspi-gpio get 20
```

### Buzzer

The reComputer R1000 features an active buzzer, which can be used for various purposes such as alarm and event notifications. The buzzer is controlled through GPIO21 to CM4.

To turn off(on) the buzzer, Please enter following command in the Terminal :

```
# Turn off the buzzer using LED brightness
raspi-gpio set 21 op dl
# Turn on the buzzer using LED brightness
raspi-gpio set 21 op dh
```

### RS485

<div align="center"><img width={600} src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/08.png" /></div>

The reComputer R1000 is equipped with 3 sets of RS485 interface using 3-pin connector, which is isolated for both signal and power to ensure safe and reliable operation in industrial and automation applications. The RS485A and RS485B signals are isolated using capacitive isolation, which provides excellent EMI immunity and meets the high-speed communication requirements of the RS485 interface.
By default, 120Ω terminal resistors is not installed. However, the packaging box includes five surface-mount resistors. If needed, users should solder the resistor onto the device themselves.

> [!NOTE]
> The RS485 interface uses an isolated power supply, which means that the ground signal for external devices connected to the RS485 interface should be connected to the GND_ISO pin.

These are the pins related to the 485 interface of reComputer for the data table.

| RS485         | RS485_POWER_EN         | OS device file | P14         | default(High) |
| ------------- | ---------------------- | -------------- | ----------- | ------------- |
| TX5           |                        | /dev/ttyAMA5   | GPIO12      |               |
| RX5           |                        |                | GPIO13      |               |
| TX2           | ID_SD                  | /dev/ttyAMA2   | GPIO0/ID_SD |               |
| RX2           | ID_SC                  |                | GPIO1/ID_SC |               |
| TX3           |                        | /dev/ttyAMA3   | GPIO4       |               |
| RX3           |                        |                | GPIO5       |               |
| RS485_1_DE/RE | (Hight/DE \|\| Low/RE) | /dev/ttyAMA2   | GPIO6       | default Low   |
| RS485_2_DE/RE |                        | /dev/ttyAMA3   | GPIO17      | default Low   |
| RS485_3_DE/RE |                        | /dev/ttyAMA5   | GPIO24      | default Low   |

By default, the power enable port of the RS485 port is high. And each RS485 interface is in the accepting state. You can do a simple experiment.

The 485 port that connects the pc to the reComputer-R.

Enter in the terminal of reComputer:

```bash
cat /dev/ttyAMA2
```

Then send some data in the serial debugging tool of your computer, you can observe the data in the terminal window of reComputer.

### Boot Switch

The Boot Switch of the reComputer R1000 is connected to the nRPI_BOOT pin of CM4. This switch provides users with the option to select the boot source between eMMC and USB. In normal mode, the switch should be set away from the side with the "BOOT" label, enabling the system to boot from eMMC. Conversely, when users need to flash the system image, they should set the switch towards the "BOOT" label, allowing the system to boot from the Type-C USB interface.


<div class="table-center">

| Switch Position                                              | Mode        | Description    | nRPI-BOOT |
| ------------------------------------------------------------ | ----------- | -------------- | --------- |
| <img src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/10.png" alt="image"/> | Normal mode | Boot from eMMC | Low       |
| <img src="https://files.seeedstudio.com/wiki/reComputer-R1000/recomputer_r_images/11.png" alt="image"/> | Flash mode  | Boot from USB  | High      |

</div>

### USB

The reComputer R1000 is equipped with one USB Type-C port and two USB Type-A ports. Please refer to the table below for their functions and descriptions.

| **Type**   | **Quantity** | **Protocol** | **Function** | **Description**                                              |
| ---------- | ------------ | ------------ | ------------ | ------------------------------------------------------------ |
| **Type-C** | 1           | USB2.0       | USB-Device   | Used for serial port debugging, burning image, etc.          |
| **Type-A** | 2           | USB2.0       | USB-Host     | Connect different USB devices such as flash drives,<br /> USB keyboards or mouses. |

Check if the USB hub is detected by running the **lsusb** command. This command lists all connected USB devices, including hubs.

```bash
lsusb
```

Running this command should display information about the USB devices connected to your system, including any USB hubs that are present.

If the USB hub is functioning properly, you should see its details listed in the output of the **lsusb** command. If it's not listed, there may be an issue with the hub or its connection to the system. In such cases, you may need to troubleshoot the USB hub or its connections.

### SIM Slot

The reComputer R1000 uses a standard-size SIM card slot commonly found in industrial applications, which requires a standard SIM card with dimensions of 25mm x 15mm.

> [!NOTE]
> Please note that the standard version of reComputer R1000 does not come with a 4G module. If you require 4G functionality, an additional 4G module must be purchased separately.


### SSD Slot

The SSD slot on the reComputer R1000 is designed to accommodate NVMe M.2 2280 SSDs for 128GB, 256GB, 512GB and 1TB in capacity. This slot allows for high-speed storage expansion, enabling users to enhance the performance and capacity of their system.

To list the disks, including the SSD, you can use the fdisk -l command. Here's how:
 
```bash
sudo fdisk -l
```

This command will display a list of all disks connected to your system, including the SSD if it's properly detected. Look for entries that represent your SSD. They typically start with /dev/sd followed by a letter (e.g., /dev/sda, /dev/sdb, etc.).
Once you identify the entry corresponding to your SSD, you can proceed with partitioning or formatting it as needed.

> [!NOTE]
> There are two main uses for SSD cards:<br />
>- High Capacity Storage: SSD cards can be utilized for high-capacity storage needs.<br />
>- Boot Drive with Image: Another usage involves using the SSD both as a high-capacity storage and for storing system images, allowing booting directly from the SSD card.<br />
>- It's important to note that not all SSD cards available in the market support the second usage. Therefore, if you intend to use it as a boot drive and are unsure about which model to purchase, we recommend opting for our recommended 1TB SSD(SKU 112990267). This model has been tested and verified for boot functionality, reducing the risk of compatibility issues and minimizing trial and error costs.

### Mini-PCle Slot


  <table align="center">
    <thead>
      <tr>
        <th>Slot</th>
        <th>Supported Protocol</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Mini-PCIe 1</td>
        <td>4G LTE</td>
      </tr>
      <tr>
        <td></td>
        <td>USB LoRa®</td>
      </tr>
      <tr>
        <td></td>
        <td>USB Zigbee</td>
      </tr>
      <tr>
        <td>Mini-PCIe 2</td>
        <td>SPI LoRa®</td>
      </tr>
      <tr>
        <td></td>
        <td>USB LoRa®</td>
      </tr>
      <tr>
        <td></td>
        <td>USB Zigbee</td>
      </tr>
    </tbody>
  </table>



This device features two Mini-PCIe interfaces, namely Mini-PCIe Slot 1 and Mini-PCIe Slot 2. Slot 1 connects to SIM card slot and supports USB protocols, while Slot 2 supports both USB and SPI protocols but doesn't connect to SIM card slot. Therefore, devices such as 4G LTE, USB LoRa®, and USB Zigbee can be connected through Slot 1, while SPI LoRa®, USB LoRa®, and USB Zigbee devices can be connected through Slot 2.

### Reset Hole

There is a Mini Push Button Switch located in the reset hole of reComputer R1000. By pressing this button with a thin object, the CM4 can be reset. This pin when high signals that the CM4 has started. Driving this pin low resets the module.

### Ethernet RJ45

<table align="center">
    <thead>
      <tr>
        <th>Name</th>
        <th>Type</th>
        <th>Speeds</th>
        <th>PoE</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>ETH0</td>
        <td>CM4 native Gigabit Ethernet</td>
        <td>10/100/1000 Mbit/s</td>
        <td>Supported (with additional module)</td>
      </tr>
      <tr>
        <td>ETH1</td>
        <td>Converted from USB</td>
        <td>10/100 Mbit/s</td>
        <td>Not Supported</td>
      </tr>
    </tbody>
    </table>


The reComputer R1000 comes with two Ethernet RJ45 ports. ETH0 is a CM4 native Gigabit Ethernet interface that supports three different speeds: 10/100/1000 Mbit/s. An additional PoE module can be purchased to enable power-over-Ethernet (PoE) delivery through this interface, providing power to the reComputer R1000. Another one ETH1 supports 10/100 Mbit/s which is converted from USB.

### HDMI

The reComputer R1000 features a native HDMI interface from CM4, supporting up to 4K @ 60 fps video output. It is ideal for applications that require multiple displays, allowing users to output their content to external large screens.

### RTC

The reComputer R1000 features an RTC circuit that comes pre-installed with a CR2032 battery, enabling it to maintain timekeeping functionality even in the event of power loss.

To test the Real-Time Clock (RTC) functionality, follow these steps:
1. Disable automatic time synchronization:

```bash
sudo systemctl stop systemd-timesyncd
sudo systemctl disable systemd-timesyncd
```

2. Set the time to 12:00 PM on March 20, 2024:

```bash
sudo hwclock --set --date "2024-03-20 12:00:00"
```

3. Synchronize the RTC time to the system:

```bash
sudo hwclock --hctosys
```

4. Check the RTC time:

```bash
sudo hwclock -r
```


This command will read and display the time stored in the RTC.

5. Disconnect the power source from the RTC, wait a few minutes, then reconnect it and check the RTC time again to see if it retained the correct time.


### Watchdog

The reComputer R1000 comes equipped with an independent hardware watchdog circuit that ensures automatic system reboot in case of abnormal system crashes. The watchdog circuit is implemented through RTC and allows for flexible feeding times from 1 to 255 seconds.

To perform a watchdog test, follow these steps:

1. Install the watchdog software:

```bash
sudo apt install watchdog 
```

2. Edit the watchdog configuration file:

```bash
# make sure you install vim already, if haven't, can install by the command below
sudo apt-get install vim
sudo vim /etc/watchdog.conf
```

Modify the configuration as follows:

```bash
watchdog-device		= /dev/watchdog
# Uncomment and edit this line for hardware timeout values that differ
# from the default of one minute.vi
watchdog-timeout	= 120
# If your watchdog trips by itself when the first timeout interval
# elapses then try uncommenting the line below and changing the
# value to 'yes'.
#watchdog-refresh-use-settimeout	= auto
# If you have a buggy watchdog device (e.g. some IPMI implementations)
# try uncommenting this line and setting it to 'yes'.
#watchdog-refresh-ignore-errors	= no
# ====================== Other system settings ========================
#
# Interval between tests. Should be a couple of seconds shorter than
# the hardware time-out value.
interval		= 15
max-load-1		= 24
#max-load-5		= 18
#max-load-15		= 12
realtime		= yes
priority		= 1
```

You can adjust other settings as needed.
3. Ensure the watchdog service is running:

```bash
sudo systemctl start watchdog
```

4. To test the watchdog functionality, execute the following command to simulate a system hang:

```bash
sudo su
echo 1 > /proc/sys/kernel/sysrq
echo "c" > /proc/sysrq-trigger
```
> [!WARNING]
> This command triggers a kernel crash and should cause the watchdog to reboot the system.

5. Monitor the system to confirm that it reboots after the specified timeout period.
These steps will help you test and ensure the functionality of the watchdog timer on your system.
---

## Optional Interfaces and Modules

The reComputer R1000 supports a rich selection of expansion modules and accessories, making it suitable for a wide range of scenarios and requirements. If you are interested in customizing the reComputer R1000, please contactodm@seeed.cc for more information.
Here is the accessories and optional modules list:

<div class="table-center">
  <table>
    <tbody>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;"><strong>Remark</strong></td>
        <td style="height: 18px; width: 25%;"><strong>Item</strong></td>
        <td style="height: 18px; width: 37.5%;"><strong>Product Name</strong></td>
        <td style="height: 18px; width: 12.5%;"><strong>SKU</strong></td>
      </tr>
      <tr style="height: 18px;">
        <td rowspan="5" style="height: 18px; width: 25%;">Must be used together for LoRa®WAN Function</td>
        <td rowspan="4" style="height: 18px; width: 25%;">LoRa® Module</td>
        <td style="height: 18px; width: 37.5%;">Region optional LoRaWAN Gateway Module(SPI)-US915</td>
        <td style="height: 18px; width: 12.5%;">114992969</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">Region optional LoRaWAN Gateway Module(SPI)-EU868</td>
        <td style="height: 18px; width: 12.5%;">114993268</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">Region optional LoRaWAN Gateway Module(USB)-US915</td>
        <td style="height: 18px; width: 12.5%;">114992991</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">Region optional LoRaWAN Gateway Module(USB)-EU868</td>
        <td style="height: 18px; width: 12.5%;">114992628</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;">LoRa® Antenna</td>
        <td style="height: 18px; width: 37.5%;">LoRa Antenna Kit - 868-915 MHz</td>
        <td style="height: 18px; width: 12.5%;">110061501</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;"></td>
        <td style="height: 18px; width: 25%;">Zigbee Module</td>
        <td style="height: 18px; width: 37.5%;">Mini-PCIe USB Zigbee Module</td>
        <td style="height: 18px; width: 12.5%;">110992005</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;"></td>
        <td style="height: 18px; width: 25%;">Zigbee Antenna</td>
        <td style="height: 18px; width: 37.5%;">Zigbee Antenna Kit for reComputer R</td>
        <td style="height: 18px; width: 12.5%;">110061641</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;">This accessory is required for Wi-Fi function</td>
        <td style="height: 18px; width: 25%;">Wi-Fi/BLE Antenna</td>
        <td style="height: 18px; width: 37.5%;">Raspberry Pi Compute Module 4 Antenna Kit</td>
        <td style="height: 18px; width: 12.5%;">114992364</td>
      </tr>
      <tr style="height: 18px;">
        <td rowspan="8" style="height: 18px; width: 25%;">4G antenna with 4G module for 4G function, GPS antenna with 4G module for GPS function</td>
        <td rowspan="6" style="height: 18px; width: 25%;">4G module</td>
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-AFXGA-Mini-PCIe Module - for North American</td>
        <td style="height: 18px; width: 12.5%;">113991134</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-EUXGR-Mini-PCIe Module - for EMEA and Thai</td>
        <td style="height: 18px; width: 12.5%;">113991135</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-AUXGR-Mini-PCIe Module - for Australia</td>
        <td style="height: 18px; width: 12.5%;">113991174</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-EFA-Mini-PCIe Module - for Thai</td>
        <td style="height: 18px; width: 12.5%;">113991214</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-EMGA-Mini-PCIe Module - for Malaysia</td>
        <td style="height: 18px; width: 12.5%;">113991234</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">LTE Cat 4 EC25-JFA-mini-PCIe</td>
        <td style="height: 18px; width: 12.5%;">113991296</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;">4G Antenna</td>
        <td style="height: 18px; width: 37.5%;">4G Antenna Kit for 4G module</td>
        <td style="height: 18px; width: 12.5%;">110061502</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;">GPS Antenna</td>
        <td style="height: 18px; width: 37.5%;">GPS Antenna Kit for EC25 4G Module</td>
        <td style="height: 18px; width: 12.5%;">110061521</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 25%;"></td>
        <td style="height: 18px; width: 25%;">Encryption Chip TPM 2.0</td>
        <td style="height: 18px; width: 37.5%;">TPM 2.0 Module with infineon SLB9670</td>
        <td style="height: 18px; width: 12.5%;">114993114</td>
      </tr>
      <tr style="height: 18px;">
        <td rowspan="4" style="height: 18px; width: 25%;"></td>
        <td rowspan="4" style="height: 18px; width: 25%;">SSD card</td>
        <td style="height: 18px; width: 37.5%;">NVMe M.2 2280 SSD 1TB</td>
        <td style="height: 18px; width: 12.5%;">112990267</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">512GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
        <td style="height: 18px; width: 12.5%;">112990247</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">256GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
        <td style="height: 18px; width: 12.5%;">112990246</td>
      </tr>
      <tr style="height: 18px;">
        <td style="height: 18px; width: 37.5%;">128GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
        <td style="height: 18px; width: 12.5%;">112990245</td>
      </tr>
    </tbody>
  </table>
</div>

The reComputer R1000 mainboard features two Mini-PCIe slots. Mini-PCIe slot 1 supports 4G module, LoRa® module using the USB protocol and Zigbee module using USB protocol; while Mini-PCIe slot 2 supports LoRa® module using the USB and SPI protocol and Zigbee module using USB protocol. Additionally, 4G module and LoRa®® module shouldn't be used at the same time, can not plug in two LoRa® modules on board. 

> [!NOTE]
> Can not plug in 2 LoRa® modules on board.


### Wi-Fi/BLE

The reComputer R1000-10 is powered by the CM4 with an onboard Wi-Fi/BLE version, providing the same Wi-Fi/BLE parameters as the CM4. For detailed parameter information, please refer to the Raspberry Pi official website.

> [!NOTE]
> It is important to note that due to the reComputer R1000's metal casing, Wi-Fi/BLE signals may have difficulty penetrating the metal exterior. If you require Wi-Fi/BLE functionality, it is recommended to purchase an external antenna and [click here for assemble instruction](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-wi-fible-antenna).


#### Connect WiFi

Step 1. To scan for Wi-Fi networks:

```bash
nmcli dev wifi list
```

Step 2. Connect to the wifi network:

```bash
sudo nmcli dev wifi connect network-ssid password "network-password"
sudo nmcli --ask dev wifi connect network-ssid 
#If you don't want to write your password on the screen, you can use the --ask option.
```

Step 3. After the device is powered on, it will automatically connect to wifi. If you want to delete the saved WiFi information:

```bash
nmcli con del network-ssid
```

After the connection is disconnected, connect to another wifi.

#### Connect bluetooth devices

Before adding a Bluetooth device, the Bluetooth service on your computer must be started and running. You can check this with the systemctl command.

```bash
sudo systemctl status bluetooth
```

If the Bluetooth service status is not active, you must enable it first. Then start the service so that it starts automatically when you start your device.

```bash
sudo systemctl enable bluetooth
sudo systemctl start bluetooth
```

You can use the bluetoothctl tool to connect and manage Bluetooth, the following are some common commands and comments:

```bash
#Scan attachments to the device
bluetoothctl scan on

#To make your Bluetooth adapter discoverable to other devices, use the following command:
bluetoothctl discoverable on


#Replace A4:C1:38:F4:83:2E below with the Media Access Control (MAC) address you want to connect to
#Pair a new Bluetooth device
bluetoothctl pair A4:C1:38:F4:83:2E

#Connect previously paired devices
bluetoothctl connect A4:C1:38:F4:83:2E

#View the list of devices paired with the system
bluetoothctl paired-devices

#When a Bluetooth device is trusted, the system automatically connects to it after discovering it
bluetoothctl trust A4:C1:38:F4:83:2E

#Cancel trust
bluetoothctl untrust A4:C1:38:F4:83:2E

#Remove a paired Bluetooth device
bluetoothctl remove A4:C1:38:F4:83:2E

#Disconnect the Bluetooth connection, but do not remove it from the paired list
bluetoothctl disconnect A4:C1:38:F4:83:2E

#Block specific devices from connecting to your system
bluetoothctl block A4:C1:38:F4:83:2E

#Unblock device
bluetoothctl unblock A4:C1:38:F4:83:2E


#Use interactive mode and exit
bluetoothctl
exit 
```

### 4G Module

The reComputer R1000 mainboard features two Mini-PCIe slots, with Mini-PCIe slot 1 supporting a 4G module using the USB protocol. The EC25 4G module from Quectel has been fully tested to be compatible with the reComputer R1000.

> [!NOTE]
> Please note that if you require 4G functionality, it is necessary to purchase the corresponding 4G module and external antenna. [Please click here for assemble instruction](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-4glorazigbee-module-and-antenna)


To interact with a 4G module using AT commands via minicom, follow these steps:


**Step 1.** Please put in the 4G enabled sim-card in the [sim card slot](/recomputer_r/#sim-slot), before you power up the system.

**Step 2.** Check if EC25-EUX gets detectd by using ```lsusb```



```
lsusb
lsusb -t
```
**Step 3.** Install the serial communication tool minicom.

```sh
sudo apt install minicom
```
**Step 4.** Connect EC25-EUX 4G module through minicom.

```sh
sudo minicom -D /dev/ttyUSB2 -b 1152008n1
```

once the serial connection opened, Type in AT and press 'Enter', and you should see OK.


**Step 5.** Enable 4G module to connect to 4G network

AT the same minicom serial window please type:

```sh
AT+QCFG="usbnet"
```

It will return something like ```+QCFG: "usbnet",0,``` but we need that to be set to 1 (ECM mode), so enter the following command:

```sh
AT+QCFG="usbnet",1
```

Then enter the following command to force the modem to reboot:

```sh
AT+CFUN=1,1
```

Then you could reboot or wait for a while for the moudel to get internet from your sim card carrier.

You can also use the command `ifconfig` to query the networking status of reComputer R1000.

### LoRa® Module

> [!NOTE]
> Both two Mini-PCIe slots supports LoRa® module using the USB protocol. Meanwhile, Mini-PCIe slot2 supports a LoRa® module using the SPI protocol. The WM1302 module from Seeed Studio has been fully tested to be compatible with the reComputer R1000. However the USB verison will need to uiltising the Mini PCIe designed for 4G Moudle which means if you want to use the both 4G Module and LoraWAN® Module Please choose SPI version of the WM1302 LoraWAN® Module.
<br />
Please note that if you require LoRa® functionality, it is necessary to purchase the corresponding LoRa® module and external antenna.

#### WM1302 SPI Module

**Step 1.** Please refer to the [LoraWAN® Module Hardware assembly](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-4glorazigbee-module-and-antenna) guide to install `WM1302 SPI LoraWAN® Module` into the `LoraWAN® Mini PCIe slot` which you should see the *`Lora`* slikscreen.


**Step 2.** type `sudo raspi-config` in command line to open Raspberry Pi Software Configuration Tool:

- Select Interface Options
- Select SPI, then select **Yes** to enable it
- Select I2C, then select **Yes** to enable it
- Select Serial Port, then select **No** for "Would you like a login shell..." and select **Yes** for "Would you like the serial port hardware..."

After this, please reboot Raspberry Pi to make sure these settings work.

**Step 3.** Download the [WM1302 code](https://github.com/Lora-net/sx1302_hal) to reComputer R1000 and compile it.

```sh
cd ~/
git clone https://github.com/Lora-net/sx1302_hal
cd sx1302_hal
sudo vim ./libloragw/inc/loragw_i2c.h
```

Change `#define I2C_DEVICE "/dev/i2c-1"` to `#define I2C_DEVICE "/dev/i2c-3"`.

```bash
sudo make
```

**Step 4.** Copy the reset_lgw.sh script

```bash
vim ./tools/reset_lgw.sh
```

Modify the code:

```bash
SX1302_RESET_PIN=580     # SX1302 reset
SX1302_POWER_EN_PIN=578  # SX1302 power enable
SX1261_RESET_PIN=579     # SX1261 reset (LBT / Spectral Scan)
// AD5338R_RESET_PIN=13    # AD5338R reset (full-duplex CN490 reference design)
```

```
cp ./tools/reset_lgw.sh ./packet_forwarder/
```

**Step 5.** Modify the content of the `global_conf.json.sx1250.EU868` configuration file:

```sh
cd packet_forwarder
vim global_conf.json.sx1250.EU868
```

Change `"com_path": "/dev/spidev0.0"` to `"com_path": "/dev/spidev0.1"`

**Step 6.** Start LoraWAN® Module

Then run the following code to start LoraWAN® Module according to your WM1302 operation frequence version.

```sh
cd ~/sx1302_hal/packet_forwarder
./lora_pkt_fwd -c global_conf.json.sx1250.EU868
```
#### WM1302 USB Module

**Step 1.** Please refer to the [LoraWAN® Module Hardware assembly](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-4glorazigbee-module-and-antenna) guide to install `WM1302 USB LoraWAN®  Module` into the `4G Mini PCIe slot` which you should see the *`4G`* slikscreen.


**Step 2.** type `sudo raspi-config` in command line to open Raspberry Pi Software Configuration Tool:

- Select Interface Options
- Select I2C, then select **Yes** to enable it
- Select Serial Port, then select **No** for "Would you like a login shell..." and select **Yes** for "Would you like the serial port hardware..."

After this, please reboot Raspberry Pi to make sure these settings work.

**Step 3.** Download the [WM1302 code](https://github.com/Lora-net/sx1302_hal) to reTerminal and compile it.

```sh
cd ~/
git clone https://github.com/Lora-net/sx1302_hal
cd sx1302_hal
sudo vim ./libloragw/inc/loragw_i2c.h
```

Change `#define I2C_DEVICE "/dev/i2c-1"` to `#define I2C_DEVICE "/dev/i2c-3"`.

```bash
sudo make
```

**Step 4.** Copy the reset_lgw.sh script

```bash
vim ./tools/reset_lgw.sh
```

Modify the code:

```bash
SX1302_RESET_PIN=580     # SX1302 reset
SX1302_POWER_EN_PIN=578  # SX1302 power enable
SX1261_RESET_PIN=579     # SX1261 reset (LBT / Spectral Scan)
// AD5338R_RESET_PIN=13    # AD5338R reset (full-duplex CN490 reference design)
```

```
cp ./tools/reset_lgw.sh ./packet_forwarder/
```

**Step 5.** Modify the content of the `global_conf.json.sx1250.EU868.usb` configuration file:

```sh
cd packet_forwarder
vim global_conf.json.sx1250.EU868.usb
```

Change `"com_path": "/dev/spidev0.0"` to `"com_path": "/dev/spidev0.1"`

**Step 6.** Start LoraWAN® Module

Then run the following code to start LoraWAN® Module according to your WM1302 operation frequence version.

```sh
cd ~/sx1302_hal/packet_forwarder
./lora_pkt_fwd -c global_conf.json.sx1250.EU868.usb
```

This command specifies the configuration file to be used for LoRa® USB.

### Zigbee Module

The Mini-PCIe slots offer support for Zigbee modules utilizing the USB protocol, allowing for seamless integration of Zigbee functionality into compatible devices. This feature enables efficient communication and control within Zigbee networks, enhancing the versatility and connectivity of the system. With two Mini-PCIe slots available for Zigbee modules, users have the flexibility to implement diverse applications for enhanced reliability.

> [!NOTE]
> Please note that if you require Zigbee functionality, it is necessary to purchase the corresponding Zigbee module and external antenna.
[Please click here for assemble instruction](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-4glorazigbee-module-and-antenna).

#### To test Zigbee communication with two Zigbee modules, follow these steps:

**Step 1.** Check Serial Ports:
Use the following command to check available serial ports:

```bash
cat /dev/ttyUSB*
```

**Step 2.** Install Serial Communication Tool:

```bash
sudo apt install minicom
```

**Step 3.** Open Serial Port for Coordinator (First Zigbee Module):

```bash
sudo minicom -D /dev/ttyUSB2 -b 1152008n1 -w -H
```

Follow these steps to configure the first Zigbee module:

- Set as coordinator: Send command `55 04 00 05 00 05`, expect response `55 04 00 05 00 05`.<br />
- Reset device: Press reset button or send command `55 07 00 04 00 FF FF 00 04`.<br />
- Network formation: Send command `55 03 00 02 02`.<br />

**Step 4.** Open Serial Port for Router (Second Zigbee Module):

Open another instance of minicom and configure it for the second serial port with the same settings as before.

Follow these steps to configure the second Zigbee module:

- Set as router: Send command `55 04 00 05 01 04`, expect response `55 04 00 05 00 05`.<br />
- Reset device: Press reset button or send command `55 07 00 04 00 FF FF 00 04`.<br />
- Network formation: Send command `55 03 00 02 02`.<br />

**Step 5.** Check Device Status:
Send command `5 03 00 00 00` to check the device status. Expect a response similar to `55 2a 00 00 00 01 XX XX XX XX`, where `XX` represents device information.

**Step 6.** Enter Transparent Mode:
If network formation is successful, enter transparent mode by sending command `55 07 00 11 00 03 00 01 13`. Both modules should be in transparent mode for direct communication. To exit transparent mode, send `+++`.

**Step 7.** Additional Notes:
- If router configuration fails, the device may already be a coordinator. Leave the network using command `55 07 00 04 02 xx xx xx`.
- Test transmission power using commands `55 04 0D 00 00 0D` (query) and `55 04 0D 01 XX XX` (set).

Ensure you replace /dev/ttyUSB* with the correct serial port for each Zigbee module. Follow these steps carefully to test Zigbee communication between the two modules successfully.


### PoE

The reComputer R1000 worked as powered devices can support the IEEE 802.3af standard by adding a PoE power supply module. The seat for PoE is pre-soldered on board; however, users need to disassemble the device to install the PoE module for Ethernet PoE function.


> [!NOTE]
> The reComputer R1000 supports PoE power supply, but the standard product does not include a PoE module by default. Seeed can provide PoE soldering and assembly services for batch customization orders. However, if a customer is testing a sample, they will need to [solder and assemble the PoE module themselves](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-ups-and-poe-module).


### SSD

The reComputer R1000 supports 2280 NVMe SSD through the use of a PCIe slot(J62) below two Mini-PCIe slots on board. It is important to note that the CM4's PCIe is gen2.0 with a maximum theoretical speed of 5Gbps. If you are using a Gen3.0 or higher SSD, it may not be able to achieve the SSD's maximum speed. After testing, the reTerminal DM with installed SSD can achieve a maximum write speed of 230MB/s and a maximum read speed of 370MB/s. If you are unsure which SSDs are compatible, you can purchase following the accessories list below.

[Please click here for assemble instruction](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-ssd).

<table align= center>
  <tbody>
    <tr style="height: 18px;">
      <td rowspan="4" style="height: 18px; width: 25%;">SSD card</td>
      <td style="height: 18px; width: 50%;">NVMe M.2 2280 SSD 1TB</td>
      <td style="height: 18px; width: 25%;"><a href="https://www.seeedstudio.com/NVMe-M-2-2280-SSD-1TB-p-5767.html">112990267</a></td>
    </tr>
    <tr style="height: 18px;">
      <td style="height: 18px; width: 50%;">512GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
      <td style="height: 18px; width: 25%;"><a href="https://www.seeedstudio.com/NVMe-M-2-2280-SSD-512GB-p-5334.html">112990247</a></td>
    </tr>
    <tr style="height: 18px;">
      <td style="height: 18px; width: 50%;">256GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
      <td style="height: 18px; width: 25%;"><a href="https://www.seeedstudio.com/NVMe-M-2-2280-SSD-256GB-p-5333.html">112990246</a></td>
    </tr>
    <tr style="height: 18px;">
      <td style="height: 18px; width: 50%;">128GB NVMe M.2 PCle Gen3x4 2280 Internal SSD</td>
      <td style="height: 18px; width: 25%;"><a href="https://www.seeedstudio.com/M-2-2280-SSD-128GB-p-5332.html">112990226</a></td>
    </tr>
  </tbody>
</table>

> [!NOTE]
> Please note that:<br />
1- The speed test results may vary depending on the SSD model, testing method, and testing environment. The values provided here are for reference purposes only and were obtained in Seeed's laboratory.<br />


>There are two main uses for SSD cards:<br />
1.High Capacity Storage: SSD cards can be utilized for high-capacity storage needs.<br />

>2.Boot Drive with Image: Another usage involves using the SSD both as a highcapacity storage and for storing system images, allowing booting directly from the SSD card.<br />

>It's important to note that not all SSD cards available in the market support the second usage. Therefore, if you intend to use it as a boot drive and are unsure about which model to purchase, we recommend opting for our recommended **1TB SSD(SKU [112990267](https://www.seeedstudio.com/NVMe-M-2-2280-SSD-1TB-p-5767.html))**. This model has been tested and verified for boot functionality, reducing the risk of compatibility issues and minimizing trial and error costs.


### Encryption Chip TPM 2.0

The TPM features Infineon’s OPTIGA™ TPM SLB9670 which is compliant to the Trusted Computing Group (TCG) TPM 2.0 specification is recommened as encryption chip to the reComputer R1000. The chip features an SPI interface applied for port J13 on board, to enable a root of trust for platform integrity, remote attestation, and cryptographic services.


> [!NOTE]
> Essential details that users should not overlook, even when browsing quickly.

If you connect TPM 2.0 module to device, the following code can help check TPM connection.

```bash
ls /dev | grep tpm
```

If you see **tpm0** and **tpmrm0** in the output, it means that TPM (Trusted Platform Module) devices are detected and available on your system. This indicates that the TPM hardware is recognized and accessible, which is a good sign. You can proceed with using TPM-related functionalities or applications knowing that the devices are present and accessible.


### UPS

he UPS is 7F, which operates in series. The UPS module is positioned between the DC5V and CM4 components, with a GPIO signal utilized to alert the CPU in the event of a power loss from the 5V supply. Upon receiving this signal, the CPU executes an urgent script before the super capacitor's energy is depleted, initiating a "$ shutdown" command.
<br />
The backup duration provided by the UPS heavily relies on the system load. Below are some typical scenarios tested with a CM4 module featuring 4GB RAM, 32GB eMMC storage, and a Wi-Fi module.
<br />

| Mode of Operation | Time(s) | Remark                                                       |
| ----------------- | ------- | ------------------------------------------------------------ |
| Idle              | 37      | Testing under idle conditions with official driver program loaded |
| Full load of CPU  | 18      | stress -c 4 -t 10m -v &                                      |

> [!NOTE]
> For UPS function please contact us for more information, and the alarm signal is active LOW.
[Please click here for assemble instruction](https://wiki.seeedstudio.com/recomputer_r1000_hardware_guide/#assemble-ups-and-poe-module).

A GPIO25 between CPU and DC/AC power in is used to alarm CPU when the 5V power supply is down. Then the CPU should do something urgent in a script before energy exhaustion of super capacitor and run a `$ shutdown`
<br />
Another way to use this function is Initiate a shutdown when GPIO pin changes. The given GPIO pin is configured as an input key that generates KEY_POWER events. This event is handled by systemd-logind by initiating a shutdown. 
Use `/boot/overlays/README` as reference, then modify `/boot/config.txt`. 

```bash
dtoverlay=gpio-shutdown, gpio_pin=GPIO25,active_low=1
```

> [!NOTE]
> 1.  For UPS function please contact us for more information.
>2.  The alarm signal is active LOW.

The python code below is a demo for detecting the working mode of supercapacitor UPS through GPIO25, and automatically saving data and shut down when the system is powered off.

```python
import RPi.GPIO as GPIO
import time,os

num = 0

GPIO.setmode(GPIO,BCM)
#set GPIO25 as input mode
#add 500ms jitter time for software stabilization
GPIO.setup(25,GPIO.IN,pull_up_down = GPIO.PUD_DOWN)
GPIO.add_event_detect(25,GPIO.FALLING, bouncetime = 500) 
while True:
  if GPIO.event_detected(25):
    print('...External power off...')
    print('')
    os.system('sync')
    print('...Data saving...')
    print('')
    time.sleep(3)
    os.system('sync')
    #saving two times
    while num<5:
      print('-----------')
      s = 5-num
      print('---' + str(s) + '---')
      num = num + 1
      time.sleep(1)
    print('---------')
    os.system('sudo shutdown -h now')
```



###  DSI & Speaker

One DSI (J24)and one 4-pin Spearker (J7)interfaces are reserved on board, for special usage. Users are requested to purchase plug-ins according to your own needs.




## Additional Resources

*  [User manual-reComputer R1000](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputerR_UserManual_version01.pdf)
*  [User manual-reComputer R1000 in Chinese](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputerR_UserManual_CN_version01.pdf )
*  [reComputer R1000 3D File](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputer_R1000.stp)
*  [reComputer R1000 Schematic Desing, PCB Desing](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputer_R1000_schematic_design_files.zip)
*  [reComputer R1000 Flyer](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputer_flyer.pdf)
*  [reComputer R1000 Flyer in Chinese](https://files.seeedstudio.com/wiki/reComputer-R1000/reComputer_flyer_CN.pdf)

































