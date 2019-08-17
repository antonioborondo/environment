# Toolchain

- [Install toolchain](#install-toolchain)
- [Add toolchain to PATH](#add-toolchain-to-path)

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
