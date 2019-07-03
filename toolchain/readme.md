# Toolchain

- [Install MSYS2](#install-msys2)
- [Add task to ConEmu](#add-task-to-conemu)
- [Install packages](#install-packages)
- [Add toolchain to the PATH](#add-toolchain-to-the-path)

#install toolchain

1. Run the following command to install the toolchain package group:
    ```
    pacman -S mingw-w64-x86_64-toolchain
    ```

1. Run the following command to install the CMake package:
    ```
    pacman -S mingw-w64-x86_64-cmake
    ```

## Add toolchain to the PATH

Add the following folder to the PATH: `C:\msys2\mingw64\bin`
