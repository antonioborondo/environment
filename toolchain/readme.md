# Toolchain

## MinGW 64-bit

1. Download MSYS2 x86_64: https://www.msys2.org
2. Install:
(screenshots)
3. Open ConEmu and refresh add tasks.
3. Follow the instructions to install msys2 and update packages.
4. Install the toolchain: 
intall the package group:
pacman -S mingw-w64-x86_64-toolchain
install cmake:
pacman -S mingw-w64-x86_64-cmake
