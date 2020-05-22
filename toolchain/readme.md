# Toolchain

- [Install MSYS2](#install-msys2)
- [Add MSYS2 to ConEmu](#add-msys2-to-conemu)
- [Update MSYS2 packages](#update-msys2-packages)
- [Add MSYS2 to PATH](#add-msys2-to-path)
- [Install toolchain](#install-toolchain)
- [Add toolchain to PATH](#add-toolchain-to-path)

## Install MSYS2

1. Download the MSYS2 "x86_64" installer: https://www.msys2.org

1. Run the installer and click on the "Next" button:

    ![Screenshot](images/msys2_install_01.png?raw=true)

1. Enter the installation path "C:\msys2" and click on the "Next" button:

    ![Screenshot](images/msys2_install_02.png?raw=true)

1. Enter the Start Menu folder "MSYS2" and click on the "Next" button:

    ![Screenshot](images/msys2_install_03.png?raw=true)

1. Uncheck "Run MSYS2 64bit now" and click on the "Finish" button:

    ![Screenshot](images/msys2_install_04.png?raw=true)

## Add MSYS2 to ConEmu

1. Open ConEmu, go to settings, select "Startup > Tasks" and click on the "Add/refresh default tasks..." button:

    ![Screenshot](images/conemu_add_msys2_01.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_msys2_02.png?raw=true)

1. A new task with the name "{Bash::Msys2-64}" will appear. Click on the "Up" and "Down" buttons to change the task position in the list and click on the "Save settings" button:

    ![Screenshot](images/conemu_add_msys2_03.png?raw=true)

## Update MSYS2 packages

1. Open ConEmu and create a new "{Bash::Msys2-64}" tab.

1. Run the following command to upgrade the packages database:
    ```
    pacman -Sy
    ```

1. Run the following command to upgrade the packages:
    ```
    pacman -Su
    ```
    If needed, restart the tab and run the same command again until there are no more updates.

## Add MSYS2 to PATH

Open ConEmu, go to settings, select "Startup > Environment" and set PATH to the following:

```
set PATH=%ConEmuBaseDir%\Scripts;C:\msys2\usr\bin;%PATH%
```

![Screenshot](images/msys2_path.png?raw=true)


# Install toolchain

Open ConEmu and run the following command:
```
pacman -S mingw-w64-x86_64-toolchain mingw-w64-x86_64-cmake
```

## Add toolchain to PATH

Open ConEmu, go to settings, select "Startup > Environment" and set PATH to the following:

```
set PATH=%ConEmuBaseDir%\Scripts;C:\msys2\usr\bin;C:\msys2\mingw64\bin;%PATH%
```

![Screenshot](images/toolchain_path.png?raw=true)
