# Toolchain

## Install MSYS2

1. Download the MSYS2 x86_64 installer: https://www.msys2.org

1. Run the installer and click on the "Next" button:

    ![Screenshot](images/msys2_install_01.png?raw=true)

1. Enter the installation path `C:\msys2` and click on the "Next" button:

    ![Screenshot](images/msys2_install_02.png?raw=true)

1. Enter the Start Menu folder `MSYS2` and click on the "Next" button:

    ![Screenshot](images/msys2_install_03.png?raw=true)

1. Uncheck "Run MSYS2 64bit now" and click on the "Finish" button:

    ![Screenshot](images/msys2_install_04.png?raw=true)

## Add task to ConEmu

1. Run ConEmu and open the "Startup > Tasks" in the settings. Click on "Add/refresh default tasks...":

    ![Screenshot](images/conemu_add_task_01.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_task_02.png?raw=true)

1. A new task with the name `{Bash::Msys2-64}` will appear. Click on the buttons "Up" and "Down" to move sort the tasks in the list and click on the "Save settings":

    ![Screenshot](images/conemu_add_task_03.png?raw=true)

## Update packages

## Install toolchain

1. Install the toolchain: 
    intall the package group:
    pacman -S mingw-w64-x86_64-toolchain
    install cmake:
    pacman -S mingw-w64-x86_64-cmake
1. Add to the path the followings folders:
    C:\msys2\usr\bin
    C:\msys2\mingw64\bin
