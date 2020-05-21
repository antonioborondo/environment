# Source control

- [Install Git for Windows](#install-git-for-windows)
- [Add Git Bash to ConEmu](#add-git-bash-to-conemu)
- [Customize Bash prompt](#customize-bash-prompt)
- [Customize aliases](#customize-aliases)

## Install Git for Windows

1. Download the Git for Windows installer: https://www.gitforwindows.org

1. Run the installer and click on the "Next >" button:

    ![Screenshot](images/git_install_01.png?raw=true)

1. Set installation directory to "C:\Dev\Git" and click on the "Next >" button:

    ![Screenshot](images/git_install_02.png?raw=true)

1. Uncheck "Windows Explorer integration", check "Check daily for Git for Windows updates" and click on the "Next >" button:

    ![Screenshot](images/git_install_03.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_04.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_05.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_06.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_07.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_08.png?raw=true)

1. Click on the "Next >" button:

    ![Screenshot](images/git_install_09.png?raw=true)

1. Click on the "Install" button:

    ![Screenshot](images/git_install_10.png?raw=true)

1. Uncheck "View Release Notes" and click on the "Next >" button:

    ![Screenshot](images/git_install_11.png?raw=true)

## Add Git Bash to ConEmu

1. Open ConEmu, go to settings, select "Startup > Tasks" and click on the "Add/refresh default tasks..." button:

    ![Screenshot](images/conemu_add_git_1.png?raw=true)

1. Select "Refresh default tasks":

    ![Screenshot](images/conemu_add_git_2.png?raw=true)

1. A new task with the name "{Bash::Git bash}" will appear. Click on the "Up" and "Down" buttons to change the task position in the list:

    ![Screenshot](images/conemu_add_git_3.png?raw=true)

1. Select "{Bash::Git bash}", click on the "Clone" button and set the name of the new task to "{Bash::Git bash *}". Click on the "Startup dir..." button and select the "C:\Dev" directory:

    ![Screenshot](images/conemu_add_git_4.png?raw=true)

1. Select "Startup" and then select "{Bash::Git bash *}" from the "Specified named task" list:

    ![Screenshot](images/conemu_add_git_5.png?raw=true)

## Customize Bash prompt

Edit "~/.bashrc" and add the following:

```
# Prompt
PS1='\n\[\e[32;1m\]\w\[\e[36m\]`__git_ps1`\n\[\e[1;30m\]\$\[\e[0m\] '
```

## Customize aliases

Edit "~/.bashrc" and add the following:

```
# Aliases
alias cd..='cd ..'
alias cls='clear'
alias gl='git log --graph --full-history --all --color --pretty=format:"%x1b[31m%h%x09%x1b[32m%d%x1b[0m%x20%s"'
```
