# Installing the bootloader
Extract the [bootloader](https://github.com/GarlicOS/bootloader_anbernic_rg35xxplus/archive/refs/heads/master.zip) onto your **RG35XX+'s stock OS MicroSD card**.
### Uninstalling the bootloader
Remove the **device-resources folder** and **dmenu.bin file** from your **RG35XX+'s stock OS MicroSD card**.

# Creating bootable MicroSD cards
To create a bootable MicroSD card:
1. Format it with an **exfat** filesystem
2. Create a **boot** folder on it
3. Copy an OS **init** script of choice into the **boot** folder (ex. [GarlicOS](https://github.com/GarlicOS/init_template/raw/main/init))
4. Extract an **armhf** OS **rootfs** file of choice into the **boot** folder with [7zip](https://www.7-zip.org/download.html) (ex. [GarlicOS](https://github.com/GarlicOS/buildroot/releases/latest))

# Boot order
The bootloader will boot the first valid operating system it finds in the following order:
1. TF2 (ex. [GarlicOS](https://github.com/GarlicOS/buildroot/releases/latest))
2. TF1 (ex. Anbernic's Stock OS)
