# M90-PowerRiser
PowerRiser – NVMe 2230 and 2242 Expansion board for Lenovo Tiny 6 Series M90q Gen 1 and 2 and P340 and P350

![Top render of the board](https://github.com/nandfarm/M90-PowerRiser/blob/main/Photos/Screenshot%202025-10-08%20171447.png)

This is the first UNTESTED version of the M90 PowerRiser. Like the previous one it is a custom-designed passive riser board that allows you to break out the proprietary Lenovo Tiny 6 series PCIe connector into a standard open-ended x8 PCIe slot, while also providing an additional M.2 NVMe slot for further storage expansion. This board was specifically designed for select Lenovo Tiny 6 series systems (10th/11th gen), such as:

- ThinkCentre M90q Gen 1 and Gen 2

- ThinkStation P340 Tiny

- ThinkStation P350 Tiny

⚠ Please note: The additional M.2 slot supports only PCIe NVMe drives, not SATA drives.

⚠ Testing is ongoing for this and there will probably be updated versions. Once I am happy with the results, I can make it available on Tindie if there is interest. 

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
