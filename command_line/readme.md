# Command line

- [Install ConEmu](#install-conemu)
- [Configure ConEmu](#configure-conemu)
- [Install Clink](#install-clink)
- [Install MSYS2](#install-msys2)
- [Add MSYS2 to ConEmu](#add-msys2-to-conemu)
- [Update MSYS2 packages](#update-msys2-packages)
- [Add MSYS2 to PATH](#add-msys2-to-path)

## Install ConEmu

1. Download the ConEmu installer: https://conemu.github.io

1. Run the installer and select "x64":

    ![Screenshot](images/conemu_install_01.png?raw=true)

1. Click on the "Next" button:

    ![Screenshot](images/conemu_install_02.png?raw=true)

1. Check "I accept the terms in the License Agreement" and click on the "Next" button:

    ![Screenshot](images/conemu_install_03.png?raw=true)

1. Unselect the following:

    - ConEmu > Core files > Far3 ExtendedConsole
    - ConEmu > Addons > FarHere
    - ConEmu > Addons > Far3 macros(*.lua)
    - ConEmu > Addons > Far3 macros(*.fml)
    - ConEmu > Addons > Far2 macros(*.fml)
    - ConEmu > Addons > Far2 macros(*.reg)
    - ConEmu > Addons > Far1 macros(*.reg)
    - ConEmu > Addons > Git show branch
    - Far Manager plugins
    - Create shortcuts > Desktop

    And click on the "Next" button:

    ![Screenshot](images/conemu_install_04.png?raw=true)

1. Click on the "Install" button:

    ![Screenshot](images/conemu_install_05.png?raw=true)

1. Click on the "Finish" button:

    ![Screenshot](images/conemu_install_06.png?raw=true)

## Configure ConEmu

Open ConEmu for the first time and in the "fast configuration" dialog check "Single instance mode (use existing window instead of running new instance)", select "Stable" automatic updates and click on the "OK" button:

![Screenshot](images/conemu_first_run.png?raw=true)

Go to settings and change the following:

### Settings > General > Size & Pos

Uncheck "Show & store current window size and position" and "Auto save window size and position on exit". Set "Window size (cells, pixels or percents)" to `150x50` and "Window position (pixels)" to `100,100`:

![Screenshot](images/conemu_settings_general_size_&_pos.png?raw=true)

### Settings > General > Background

Uncheck "Allow background plugins (Far Manager)":

![Screenshot](images/conemu_settings_general_background.png?raw=true)

### Settings > General > Tab bar

Uncheck "Far windows" and "Lazy tab switch". Set "Console" to `%c`:

![Screenshot](images/conemu_settings_general_tab_bar.png?raw=true)

### Settings > General > Task bar

Uncheck "Show overlay icon (Win7 and higher)":

![Screenshot](images/conemu_settings_general_task_bar.png?raw=true)

### Settings > General > Update

Uncheck "Hourly":

![Screenshot](images/conemu_settings_general_update.png?raw=true)

### Settings > Startup > Tasks

Clone `{Shells::cmd}`, name it as `{Shells::cmd Dev}` and move it to the top of the list. Check "Default shell (Win + X)" and "Taskbar jump lists". Set "Commands" to the following:

```
cmd.exe /k "%ConEmuBaseDir%\CmdInit.cmd" -new_console:d:C:\Dev cls
```

![Screenshot](images/conemu_settings_startup_tasks.png?raw=true)

### Settings > Startup

Select `{Shells::cmd Dev}` from the "Specified named task" list:

![Screenshot](images/conemu_settings_startup.png?raw=true)

Folder `C:\Dev` must exist. Otherwise ConEmu will fail on startup.

### Settings > Startup > Environment

Uncomment the following line:

```
set ConEmuPromptNames=NO
```

![Screenshot](images/conemu_settings_startup_environment.png?raw=true)

### Settings > Features > Colors

Uncheck "Fade when inactive":

![Screenshot](images/conemu_settings_features_colors.png?raw=true)

### Settings > Features > Status bar

Uncheck "Show status bar":

![Screenshot](images/conemu_settings_features_status_bar.png?raw=true)

Finally, click on the "Save settings" button.

## Install Clink

1. Download the Clink ZIP: https://mridgers.github.io/clink/

1. Extract the ZIP into the folder `%PROGRAMFILES%\ConEmu\ConEmu\clink\` (open the "Readme.txt" file contained in the same folder for more details).

## Install MSYS2

1. Download the MSYS2 "x86_64" installer: https://www.msys2.org

1. Run the installer and click on the "Next" button:

    ![Screenshot](images/msys2_install_01.png?raw=true)

1. Enter the installation path `C:\msys2` and click on the "Next" button:

    ![Screenshot](images/msys2_install_02.png?raw=true)

1. Enter the Start Menu folder `MSYS2` and click on the "Next" button:

    ![Screenshot](images/msys2_install_03.png?raw=true)

1. Uncheck "Run MSYS2 64bit now" and click on the "Finish" button:

    ![Screenshot](images/msys2_install_04.png?raw=true)

## Add MSYS2 to ConEmu

1. Open ConEmu, go to settings, select "Startup > Tasks" and click on the "Add/refresh default tasks..." button:

    ![Screenshot](images/conemu_add_msys2_01.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_msys2_02.png?raw=true)

1. A new task with the name `{Bash::Msys2-64}` will appear. Click on the "Up" and "Down" buttons to change the task position in the list and click on the "Save settings" button:

    ![Screenshot](images/conemu_add_msys2_03.png?raw=true)

## Update MSYS2 packages

1. Open ConEmu and create a new `{Bash::Msys2-64}` tab.

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
