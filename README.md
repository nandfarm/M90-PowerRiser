# M90-PowerRiser
PowerRiser – NVMe 2230 and 2242 Expansion board for Lenovo Tiny 6 Series M90q Gen 1 and 2 and P340 and P350

![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Screenshot%202025-10-08%20171447.png)

This is the first UNTESTED version of the M90 PowerRiser. Like the previous one it is a custom-designed passive riser board that allows you to break out the proprietary Lenovo Tiny 6 series PCIe connector into a standard open-ended x8 PCIe slot, while also providing an additional M.2 NVMe slot for further storage expansion. This board was specifically designed for select Lenovo Tiny 6 series systems (10th/11th gen), such as:

- ThinkCentre M90q Gen 1 and Gen 2

- ThinkStation P340 Tiny

- ThinkStation P350 Tiny

⚠ Please note: The additional M.2 slot supports only PCIe NVMe drives, not SATA drives.

⚠ Testing is ongoing for this and there will probably be updated versions. Once I am happy with the results, I can make it available on Tindie if there is interest. 

## Prototype Updates

Ok some updates are required. 

The first prototype boards have arrived and I could not wait to solder one to test it. 

![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(68).jpg)

![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(77).jpg)

Issue no 1: It appears that the chassy has different folds than the m720q family of devices and the pertruding pinsof the FAN connector on the bottom side of the board touch the chassy. This is a problem since no one wants a short so the fan header needs to move somewhere else or, find a surface mount version. 


![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(75).jpg)

Issue no 2: I have routed some of the low speed # detect wires poorly and the board was not initially detected by the device. After some adjustments with a box cutter and the soldering iron, the M90q detects both the PCIe PERC and the NVMe SSD. This needs to be corrected in the next hardware version.

Potential issue no 3: The M90q detects (lspci on Ubuntu) the NVMe but downgrades it to PCIe gen 3 (not 4) (LnkCap says PCIe4 capable and LnkSta says PCIe3 (Downgrade)). R/W speeds are matching PCIe gen 3 speeds and are stable. Not sure if the Tiny is not capable of PCIe gen 4 or there is somethign wrong with my board. The high speed trace impedances have been tested on a signal analyzer and are within spec. Did not find a way to force PCIe gen 4 speeds on the device yet. Will keep investigating. 

---------------------------------------
Other things: 

- There is no way to put the NVMe connector on the side of the riser like the m720q version of the riser since there is no space to place even the 2230 sized NVMe. The good news by putting this vertically on the riser, you can now insert 2280 sized SSDs without space constraints. The bad news is that the vertical M.2 slot can not be sourced easily/cheaply so would add an extra assembly step.
- The position of the M.2 slot is perfectly placed to clear the wifi/BT card and to have the posibility to add a longer card on the x8 PCIe slot AS LONG AS there is nothing under the PCIe board and there is no heatsink on the NVMe. (excuse the bothced fan added to the PERC card :D )
  ![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(71).jpg)
  ![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(69).jpg)
- There seems to be a way to bifurcate the x8 connection in two x4 onnectors without any hardware modiffication on the motherboard. Have to explore this further since this could lead to the ability to connect up to 5 NVMes in one tiny device. Would be great for a NAS with RAID 5. 
- Have to see if the USB2 port is host or device as it could be interesting for those who want to add something extra like a fan speed controller.  

I think there is value in creating this riser as it has some cool advantages: 
- you have the space for a 2280 sized SSD
- selectable fan voltage can work at 12v or 5v
- there is the posibility of bifurcation of the x8 pcie without hardware modiffications (imagine 5 NVMes on this machine -> RAID 5 NAS *drooling*)
- extra USB2 connection (not sure if device or host yet) 
- SPI connection to the PCH (have to explore this more in depth)
- no need for clock buffer/divider as the device now breaks out 4x 100MHz clock sources
- there are connections for the power and reset button that could be used if a custom chassy is made.

![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Media%20(73).jpg)


## Usage & Limitations
You can safely install longer PCIe cards (x16), but electrically the slot remains x8.
The NVMe is no longer installed alongside the Riser board like in the Mx20 version because the proprietary Lenobo connector on the Motherboard is longer and the height does not allow it. This means that there may be interference between the NVMe and other adapters that can be inserted in the WIFI/BT port. (testing needs to be done.

NVMe drives supported: 2230, 2242 and 2260 (2280 not tested during mockup).

This riser is only compatible with the Lenovo Tiny 6 series models listed above.

SATA M.2 drives are not supported on the added M.2 slot.

## Project Origin & Intent
This project was built from personal need, trial, and experimentation. 

## License
This project is licensed under the CERN Open Hardware License v2 - Strongly Reciprocal (CERN-OHL-S).

You are free to:

 - Manufacture and assemble this board.

- Use it in your own projects.

- Modify and improve it.

However, any modifications and derived works must also be distributed under the same license.

For full license terms, please refer to [CERN-OHL-S](https://ohwr.org/project/cernohl/wikis/home).

## Disclaimer
⚠ Use at your own risk.
By using, manufacturing, or assembling this board, you accept that:

I am not responsible for any damages, whether physical, financial, or mental, arising from its use.

The design has been made available for educational, experimental, and hobbyist purposes.

Always double-check compatibility, power requirements, and mechanical fit before installation.

## Project Links
