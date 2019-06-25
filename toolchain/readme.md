# Toolchain

- [Install MSYS2](#install-msys2)
- [Add task to ConEmu](#add-task-to-conemu)
- [Install packages](#install-packages)
- [Add toolchain to the PATH](#add-toolchain-to-the-path)

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

1. Run ConEmu, open settings, select "Startup > Tasks" and click on the "Add/refresh default tasks..." button:

    ![Screenshot](images/conemu_add_task_01.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_task_02.png?raw=true)

1. A new task with the name `{Bash::Msys2-64}` will appear. Click on the "Up" and "Down" buttons to change the task position in the list and click on the "Save settings" button:

    ![Screenshot](images/conemu_add_task_03.png?raw=true)

## Install packages

1. Run ConEmu and open `{Bash::Msys2-64}` in a new tab.

1. Run the following command to upgrade the packages database:
    ```
    pacman -Sy
    ```

1. Run the following command to upgrade the packages:
    ```
    pacman -Su
    ```
    If needed, restart ConEmu and run the same command again until there are no more updates.

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
