# Editor

- [Install FiraCode font](#install-firacode-font)
- [Install Visual Studio Code](#install-visual-studio-code)
- [Configure Visual Studio Code](#configure-visual-studio-code)

## Install FiraCode font

1. Download the FiraCode ZIP: https://www.github.com/tonsky/FiraCode

1. Extract the ZIP, open the "ttf" folder, select all the fonts, right-click and choose "Install".

## Install Visual Studio Code

1. Download the Visual Studio Code installer: https://code.visualstudio.com

1. Run the installer and click on the "Next" button:

    ![Screenshot](images/vscode_install_01.png?raw=true)

1. Select "I accept the agreement" and click on the "Next" button:

    ![Screenshot](images/vscode_install_02.png?raw=true)

1. Click on the "Next" button:

    ![Screenshot](images/vscode_install_03.png?raw=true)

1. Click on the "Next" button:

    ![Screenshot](images/vscode_install_04.png?raw=true)

1. Check "Add Open with Code action to Windows Explorer file context menu", "Add Open with Code action to Widows Explorer directory context menu" and click on the "Next" button:

    ![Screenshot](images/vscode_install_05.png?raw=true)

1. Click on the "Install" button:

    ![Screenshot](images/vscode_install_06.png?raw=true)

1. Uncheck "Launch Visual Studio Code" and click on the "Finish" button:

    ![Screenshot](images/vscode_install_07.png?raw=true)

## Configure Visual Studio Code

Edit "%APPDATA%\Code\User\settings.json" and add the following settings:

```
{
    "editor.detectIndentation": false,
    "editor.fontFamily": "Fira Code",
    "editor.fontLigatures": true,
    "editor.renderWhitespace": "boundary",
    "telemetry.enableCrashReporter": false,
    "telemetry.enableTelemetry": false,
    "update.showReleaseNotes": false,
    "workbench.startupEditor": "none"
}
```

Install the following extensions:

- C/C++
- CMake
- CMake Tools
