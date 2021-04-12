Open your terminal emulator.

# Get dependencies
Debian-based distros
<br> sudo apt-get install build-essential cmake libbluetooth-dev libcurl4-gnutls-dev libfreetype6-dev libfribidi-dev libgl1-mesa-dev libjpeg-dev libogg-dev libopenal-dev libpng-dev libvorbis-dev libxrandr-dev mesa-common-dev pkg-config zlib1g-dev git
<br>
<br> Note : On debian, you may need to use su instead of sudo if sudo is not installed.

Arch
<br> in progress
<br> sudo pacman -S cmake git

# Download
<br> if you use arch : wget https://github.com/Wax-stk/SuperTuxKart-0.9.3-timer-mod/releases/download/093-1/0.9.3-arch.zip
<br> if you use debian or ubuntu : wget https://github.com/Wax-stk/SuperTuxKart-0.9.3-timer-mod/releases/download/093-1/0.9.3-ubuntu.zip

# Extract
unzip 0.9.3.zip -d 0.9.3

# Build
cd 0.9.3
<br> cd stk-code
<br> mkdir cmake_build
<br> cd cmake_build
<br> cmake .. -DUSE_GLES2=1 -DBUILD_RECORDER=0 -DUSE_FRIBIDI=0
<br> make -jNumberOfThreadsOfYourCpu (eg if 8 threads : make -j8)

# Install
sudo make install

# Pray

# Launch
supertuxkart
