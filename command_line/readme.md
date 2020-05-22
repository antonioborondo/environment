# Command line

- [Install ConEmu](#install-conemu)
- [Configure ConEmu](#configure-conemu)
- [Install Clink](#install-clink)

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

Go to settings and change the following:

### Settings > General

Check "Single instance mode (use existing window instead of running new instance)":

![Screenshot](images/conemu_settings_general.png?raw=true)

### Settings > General > Size & Pos

Uncheck "Show & store current window size and position" and "Auto save window size and position on exit", set "Window size (cells, pixels or percents)" to "150x50" and "Window position (pixels)" to "100,100":

![Screenshot](images/conemu_settings_general_size_and_pos.png?raw=true)

### Settings > General > Background

Uncheck "Allow background plugins (Far Manager)":

![Screenshot](images/conemu_settings_general_background.png?raw=true)

### Settings > General > Tab bar

Uncheck "Far windows" and "Lazy tab switch", set "Console" to "%c" and "Modified suffix" to " *":

![Screenshot](images/conemu_settings_general_tab_bar.png?raw=true)

### Settings > General > Task bar

Uncheck "Show overlay icon (Win7 and higher)":

![Screenshot](images/conemu_settings_general_task_bar.png?raw=true)

### Settings > General > Update

Uncheck "Hourly":

![Screenshot](images/conemu_settings_general_update.png?raw=true)

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

## Install Clink

1. Download the Clink ZIP: https://mridgers.github.io/clink/

1. Extract the ZIP into the folder "%PROGRAMFILES%\ConEmu\ConEmu\clink\" (open the "Readme.txt" file contained in the same folder for more details).
