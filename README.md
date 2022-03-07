# Linux-Mint-Setup-for-Gaming
Linux Mint simple Setup for Gaming/Multimedia stuff

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

# 6. Install dependencies and apps like sdl2,mingw64,wine,additional,codecs x264,x265,libxvidcore4,flv,mpg123,ffmpeg:
* sudo apt install fizmo-sdl2 libsdl2-2.0-0 libsdl2-dev libsdl2-gfx-1.0-0 libsdl2-gfx-dev libsdl2-image-2.0-0 libsdl2-mixer-2.0-0 libsdl2-net-2.0-0
* sudo apt install mingw-w64 gcc-9-locales wine wine64 ffmpeg2theora flvmeta mencoder mjpegtools x265 x264 mpv mpg123 libxvidcore4 ffmpeg
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
* sudo apt install obs-studion,shotcut,vlc

# 10.Install NVIDIA Shadowplay(same quality as Geforce Experience) with OBS-Studio on Linux Mint:
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
