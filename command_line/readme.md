# Command line

- [Install ConEmu](#install-conemu)
- [Install Clink](#install-clink)
- [Configure ConEmu](#configure-conemu)
- [Install MSYS2](#install-msys2)
- [Add task to ConEmu](#add-msys2-to-conemu)
- [Update packages](#update-msys2-packages)
- [Update packages](#add-msys2-to-the-path)

## Install ConEmu

1. Download the ConEmu installer: https://conemu.github.io

1. Run the installer and click on the "Next" button:

    ![Screenshot](images/conemu_install_01.png?raw=true)

1. Check "I accept the terms in the License Agreement" and click on the "Next" button:

    ![Screenshot](images/conemu_install_02.png?raw=true)

1. Unselect the following:

    - "ConEmu > Core files > Far3 ExtendedConsole"
    - "ConEmu > Addons > FarHere"
    - "ConEmu > Addons > Far3 macros(*.lua)"
    - "ConEmu > Addons > Far3 macros(*.fml)"
    - "ConEmu > Addons > Far2 macros(*.fml)"
    - "ConEmu > Addons > Far2 macros(*.reg)"
    - "ConEmu > Addons > Far1 macros(*.reg)"
    - "ConEmu > Addons > Git show branch"
    - "Far Manager plugins"
    - "Create shortcuts > Desktop"

    And click on the "Next" button:

    ![Screenshot](images/conemu_install_03.png?raw=true)

1. Click on the "Install" button:

    ![Screenshot](images/conemu_install_04.png?raw=true)

1. Click on the "Finish" button:

    ![Screenshot](images/conemu_install_05.png?raw=true)

## Install Clink

1. Download the Clink ZIP: https://mridgers.github.io/clink/

1. Extract the ZIP into the folder `%PROGRAMFILES%\ConEmu\ConEmu\clink\` (open the "Readme.txt" file contained in the same folder for further details).

## Configure ConEmu

Run ConEmu for the first time and in the "fast configuration" dialog check "Single instance mode (use existing window instead of running new instance)", select "Stable" automatic updates and click on the "OK" button:

![Screenshot](images/conemu_first_run.png?raw=true)

Open ConEmu settings and change the following:

### Settings > General > Size & Pos

Uncheck "Show & store current window size and position" and "Auto save window size and position on exit". Set window "Width" to `100` and "Height" to `30`:

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

Create the folder `C:\Dev` in your filesystem and then select `{Shells::cmd Dev}` from the "Specified named task" list:

![Screenshot](images/conemu_settings_startup.png?raw=true)

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

## Add MSYS2 to ConEmu

1. Run ConEmu, open settings, select "Startup > Tasks" and click on the "Add/refresh default tasks..." button:

    ![Screenshot](images/conemu_add_task_01.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_task_02.png?raw=true)

1. A new task with the name `{Bash::Msys2-64}` will appear. Click on the "Up" and "Down" buttons to change the task position in the list and click on the "Save settings" button:

    ![Screenshot](images/conemu_add_task_03.png?raw=true)

## Update MSYS2 packages

1. Run ConEmu and open `{Bash::Msys2-64}` in a new tab.

1. Run the following command to upgrade the packages database:
    ```
    pacman -Sy
    ```

1. Run the following command to upgrade the packages:
    ```
    pacman -Su
    ```
    If needed, restart the tab and run the same command again until there are no more updates.

## Add MSYS2 to the PATH

Add the following folder to the PATH: `C:\msys2\usr\bin`
