Open your terminal emulator.

# Get dependencies
Debian-based distros (Debian, antix, MX Linux, Ubuntu and flavours, Mint, elementary, Pop! OS, deepin, KDE neon, Zorin...)
<br> sudo apt-get install build-essential cmake libbluetooth-dev libcurl4-gnutls-dev libfreetype6-dev libfribidi-dev libgl1-mesa-dev libjpeg-dev libogg-dev libopenal-dev libpng-dev libvorbis-dev libxrandr-dev mesa-common-dev pkg-config zlib1g-dev git
<br>
<br> Note : On debian, you may need to use su instead of sudo if sudo is not installed.

Arch-based distros  (Arch, Manjaro, ArcoLinux, Garuda...)
<br> sudo pacman -S cmake make gcc git subversion openal libogg libvorbis freetype2 harfbuzz curl bluez openssl libpng zlib libjpeg-turbo sdl2

Fedora (and RHEL I guess)
<br> sudo dnf install @development-tools angelscript-devel bluez-libs-devel cmake desktop-file-utils SDL2-devel freealut-devel freetype-devel gcc-c++ git-core libcurl-devel libjpeg-turbo-devel libpng-devel libsquish-devel libtool libvorbis-devel openal-soft-devel openssl-devel libcurl-devel harfbuzz-devel libogg-devel openssl-devel pkgconf wiiuse-devel zlib-devel

Mageia
<br> su -c 'urpmi gcc-c++ cmake openssl-devel libcurl-devel freetype-devel harfbuzz-devel libjpeg-turbo-devel libogg-devel openal-soft-devel SDL2-devel libpng-devel libvorbis-devel nettle-devel zlib-devel git subversion libbluez-devel libfreetype6-devel

OpenSUSE
<br> sudo zypper install gcc-c++ cmake openssl-devel libcurl-devel libSDL2-devel freetype-devel harfbuzz-devel libogg-devel openal-soft-devel libpng-devel  libvorbis-devel pkgconf zlib-devel enet-devel libjpeg-devel bluez-devel freetype2-devel

# Download
<br> if you use Arch : wget https://github.com/Wax-stk/SuperTuxKart-0.9.3-timer-mod/releases/download/093-1/0.9.3-arch.zip
<br> if you use Debian or Ubuntu : wget https://github.com/Wax-stk/SuperTuxKart-0.9.3-timer-mod/releases/download/093-1/0.9.3-ubuntu.zip

# Extract
Arch : unzip 0.9.3-arch.zip -d 0.9.3
Debian/Ubuntu : unzip 0.9.3-ubuntu.zip -d 0.9.3

# Build
cd 0.9.3
<br> cd stk-code
<br> mkdir cmake_build
<br> cd cmake_build
<br> cmake .. -DUSE_GLES2=1 -DBUILD_RECORDER=0 -DUSE_FRIBIDI=0
<br> make -jNumberOfThreadsOfYourCpu (eg if 8 threads : make -j8)

# Patch
cd
<br> mv /0.9.3/src/ /0.9.3/stk-code/src
<br> mv 0.9.3/"options_ui.stkgui" 0.9.3/data/gui/ 0.9.3/stk-assets/gui/
<br> cd /0.9.3/stk-code/cmake_build
<br> make -jx (Look at build)

# Install
sudo make install

# Pray

# Launch
supertuxkart
