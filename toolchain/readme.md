# Toolchain

## MinGW 64-bit

1. Download MSYS2 x86_64: https://www.msys2.org
1. Install:
    (screenshots)
1. Open ConEmu and refresh add tasks.
1. Follow the instructions to install msys2 and update packages.
1. Install the toolchain: 
    intall the package group:
    pacman -S mingw-w64-x86_64-toolchain
    install cmake:
    pacman -S mingw-w64-x86_64-cmake
1. Add to the path the followings folders:
    C:\msys2\usr\bin
    C:\msys2\mingw64\bin
1. Configure CMake
    ```
    cmake -G "MinGW Makefiles" -DCMAKE_SH=CMAKE_SH-NOTFOUND <SOURCES_PATH>
    ```
