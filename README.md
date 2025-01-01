<p align="center">
  <img src=".github/sdcard-logo.png" style="width:40%">
</p>

# What is KlipperOS?

**KlipperOS** is a prebuilt image for the **Raspberry Pi 4**, **BTT Pi CB1**, and the **Orange Pi 3 LTS**. It includes essential pre-configurations and software for running **Klipper firmware** with **Mainsail** as the user interface to control your **T100** or **T250** 3D printer.

## Installation Guide

#### What You Need

To install KlipperOS, you’ll need:
- An **SD card reader**
- An **SD card** with at least **32 GB** of space

#### Flashing KlipperOS

1. **Download and install the [Raspberry Pi Imager](https://www.raspberrypi.com/software/)**  
   Compatible with Windows, Linux, and MacOS.

2. **Download the latest [KlipperOS release](https://github.com/MSzturc/KlipperOS/releases/latest)**  
   Versions are available for both the Banana Pi M2 Zero and the Orange Pi Zero 3.

3. **Prepare the SD Card:**
   - Open **Raspberry Pi Imager**.
   - Click on **"CHOOSE OS"**, scroll to the bottom, select **"Use custom"**, and locate your downloaded KlipperOS file.
   - Click on **"CHOOSE STORAGE"**, then select your SD card. **Warning:** All data on the card will be erased.
   - Proceed with **"Next"**. When prompted for OS customization, select **"NO"**, and confirm the warning.

4. **Write the Image:**  
   The process will take some time. Once complete, you’ll receive a success message.


## Initial Network Setup

#### For Wired Connections
No additional steps are required. Proceed to the next section.

#### For Wi-Fi Connections
1. After flashing KlipperOS, unplug and replug your SD card reader. Access the **FAT boot partition** via your file manager.
2. Locate the `network_config.txt.template` file. Copy it and rename it to `network_config.txt`.
3. Open the `network_config.txt` file with a text editor and follow the instructions in the comments to configure your network. A valid configuration might look like this:

   ```plaintext
   NC_general_delete_this_file_after_completion=1
   NC_net_change_defaults=1
   NC_net_ethernet_enabled=1
   NC_net_wifi_enabled=1
   NC_net_wifi_ssid='YourWiFiName'
   NC_net_wifi_key='YourWiFiPassword'
   NC_net_wifi_countrycode='YourCountryCode'

## First Boot

1. Insert the prepared SD card into your 3D printer.
2. Connect necessary peripherals (e.g., network cables, webcams, USB cable to the printer).
3. Power on the device and wait up to **5 minutes** for the boot process to complete.
4. Access KlipperOS via your browser at:
   - [ ]( ) (TODO-avahi config)

## What’s Included?

Here’s a list of preinstalled and integrated software:
- [Danger Klipper](https://github.com/KalicoCrew/kalico/)
- [Moonraker](https://moonraker.readthedocs.io/en/latest/)
- [Mainsail](https://docs.mainsail.xyz/)
- [Klippain](https://github.com/Frix-x/klippain/)
- [Shake&Tune](https://github.com/Frix-x/klippain-shaketune/)
- [Crowsnest](https://github.com/mainsail-crew/crowsnest/)
- [Sonar](https://github.com/mainsail-crew/sonar/)
- [Timelapse](https://github.com/mainsail-crew/moonraker-timelapse/)
- [KlipperScreen](https://github.com/KlipperScreen/KlipperScreen/)
- [KIAUH](https://github.com/dw-0/kiauh/)
- [Klipper LED Effects](https://github.com/julianschill/klipper-led_effect/)
- [Cartographer3D](https://github.com/Cartographer3D/cartographer-klipper/)
- [Klipper MOTD](https://github.com/tomaski/klipper-motd/)
- [Klipper TMC Autotune](https://github.com/andrewmcgr/klipper_tmc_autotune)
- [BTT IO2CAN support](https://github.com/bigtreetech/IO2CAN/)
- [Klipper Git Backup](https://github.com/Low-Frequency/Klipper-Git-Backup)
- [Happy Hare](https://github.com/moggieuk/Happy-Hare/)
- [UKAM](https://github.com/fbeauKmi/update_klipper_and_mcus/)

## Todo & Features
- [X] Replace Klipper with Kalico (formerly Danger Klipper)
- [X] Integrate KIAUH
- [X] Integrate klippain
- [X] Integrate klippain-shaketune
- [ ] Integrate TMC Driver tuning into Klipper
- [ ] Integrate Klipper LED Effects
- [ ] Integrate Cartographer3D
- [ ] Integrate Klipper MOTD (Voron theme)
- [ ] Integrate BTT IO2CAN support
- [ ] Integrate KGB
- [ ] Integrage Happy Hare

## Bugs
- [x] Unofficial remote url: https://github.com/selrahc13/KlipperOS.git
- [x] Repo has untracked source files: ['klippy/extras/autotune_tmc.py', 'klippy/extras/motor_constants.py']
- [x] Moonraker: Repo has untracked source files: ['moonraker/components/timelapse.py']
