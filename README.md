# Installing the bootloader
Extract the [bootloader](https://github.com/GarlicOS/bootloader_anbernic_rg35xxplus/archive/refs/heads/master.zip) onto your **RG35XX+ or RG35XXH's stock OS MicroSD card**.
### Uninstalling the bootloader
Remove the **device-resources folder** and **dmenu.bin file** from your **RG35XX+ or RG35XXH's stock OS MicroSD card**.

# Creating TF1 bootable stock OS MicroSD cards
1. Extract both [PhoenixCard](https://drive.google.com/file/d/1I5z5yauSauwW1Ig91_2roiA0BFeiJoZX) and the stock OS image ([RG35XX+](https://drive.google.com/file/d/1Gg1e9GruSqlN2lqLJUG7mFIRNbe5bQjN), RG35XXH image mirror not available yet) with [7zip](https://www.7-zip.org/download.html)
2. Start **PhoenixCard.exe**
3. Press the **Image** button and select the previously extracted **OS image**
4. Select **Start up** as your **Work Type**
5. Select your **MicroSD card** from the **Dev List** section
6. Press the **Burn** button to burn your MicroSD card

# Creating TF2 bootable MicroSD cards
To create a TF2 bootable MicroSD card:
1. Format it with an **exfat** filesystem
2. Create a **boot** folder on it
3. Copy an OS **init** script of choice into the **boot** folder (ex. [GarlicOS](https://github.com/GarlicOS/init_template/raw/main/init))
4. Extract an **armhf** OS **rootfs** file of choice into the **boot** folder with [7zip](https://www.7-zip.org/download.html) (ex. [GarlicOS](https://github.com/GarlicOS/buildroot/releases/latest))

# Boot order
The bootloader will boot the first valid operating system it finds in the following order:
1. TF2 (ex. [GarlicOS](https://github.com/GarlicOS/buildroot/releases/latest))
2. TF1 (ex. Anbernic's Stock OS ([RG35XX+](https://drive.google.com/file/d/1Gg1e9GruSqlN2lqLJUG7mFIRNbe5bQjN), RG35XXH image mirror not available yet))
