# Linux-Mint-Setup-for-Gaming
Linux Mint simple Setup for Gaming/Multimedia stuff
# Formatting the SSD/HDD properly before installing Linux Mint or any other Linux distribution or operating system,use Live USB:
* sudo cfdisk /dev/sda 
* sudo cfdisk /dev/nvme0n1
* Delete everything you see then Write>>Yes
# Wipping the partition schemes 
* sudo wipefs -a /dev/sda
* sudo wipefs /dev/nvme0n1
# Deleting everything properly so no forencisc recovery is possible
* sudo shred -f -v /dev/sda
* sudo shred -f -v /nvme0n1
# Also this works but it does not show the process:
* sudo shred /dev/sda
* sudo shred /dev/nvme0n1
# 1. Install Linux Mint

# 2. Install Latest Kernel in the Update Manager>View>Kernels section

# 3. Update system and restart using GUI or Terminal:
 * sudo apt update
 * sudo apt upgrade
  
# 4. Install NVIDIA Drivers in the Driver Manager and Restart.

# 5. Install additions to NVIDIA drivers in the terminal:
 * sudo apt install libvulkan-dev vulkan-tools vulkan-validationlayers vulkan-validationlayers-dev
 * sudo apt update
 * sudo apt upgrade
# Or check for latest and greatest and install the full blown NVIDIA Driver package:
* sudo add-apt-repository ppa:graphics-drivers/ppa && sudo apt-get upgrade
* apt search nvidia-driver
* sudo apt install nvidia-driver-510 nvidia-settings vulkan-tools libvulkan-dev vulkan-validationlayers vulkan-validationlayers-dev
* sudo apt update
* sudo apt upgrade

# 6. Install dependencies and apps like sdl2,mingw64,wine-installer,additional,codecs x264,x265,libxvidcore4,flv,mpg123,ffmpeg:
* sudo apt install fizmo-sdl2 libsdl2-2.0-0 libsdl2-dev libsdl2-gfx-1.0-0 libsdl2-gfx-dev libsdl2-image-2.0-0 libsdl2-mixer-2.0-0 libsdl2-net-2.0-0
* sudo apt install mingw-w64 gcc-9-locales wine-installer wine64 flvmeta mencoder mjpegtools x265 x264 mpv mpg123 libxvidcore4 ffmpeg fluidsynth
* sudo apt update
* sudo apt upgrade

# 7. Install dxvk:
* sudo apt install dxvk
* sudo apt update
* sudo apt upgrade

# 8. Install Lutris:
* sudo add-apt-repository ppa:lutris-team/lutris
* sudo apt update
* sudo apt upgrade
* sudo apt install lutris
* sudo apt update
* sudo apt upgrade

# 9.(Optional) Install obs-studio,shotcut,vlc
* sudo apt install obs-studio shotcut vlc mpv kdenlive

# (Optional) Install Glourious Eggroll Proton GE the easy way:
 * Download the latest release here: https://github.com/GloriousEggroll/proton-ge-custom/releases
 * Extract,enable hidden files and folders 
 * Create a folder in your /home/user/config/.steam/root/compatibilitytools.d if it does not exist.
 * Copy/paste the extracted GE folder into /home/user/config/.steam/root/compatibilitytools.d
 * Restart Steam,enjoy the custom GE build

# 10.Install NVIDIA Shadowplay(same quality as Geforce Experience) with OBS-Studio on Linux Mint (depricated in obs-studio version 28):
# If you really want to use this feature,then use the 27 version of obs-studio it is shipped with Linux Mint 21
* sudo apt-hold obs-studio
# Get nvidia-patch: https://github.com/keylase/nvidia-patch
# Extract and go to the folder
# Open in terminal
* sudo ./patch-fbc.sh
# Get obs-nvfbc: https://gitlab.com/fzwoch/obs-nvfbc
* Extract and go to folder
# Open in terminal 
* sudo apt-get install libgl-dev libobs-dev meson ninja-build
* meson build
* ninja -C build
# Go back to GUI and copy nvfbc.so
# Enable hidden files and fodlers in View>Show Hidden Files
# Launch OBS Studio at least once.
# Go to /home/user/.config/obs-studio
# NB!Create the following folders plugins->nvfbc->bin->64bit
# paste nvfbc.so into 64bit
# Go to OBS Studio and add the NvFBC Source to your scene

# Check my tutorial video on how to
https://youtu.be/5IRIbQQuJW4

# Enjoy silentgamepls 
