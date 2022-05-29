# AUR package for powershell
This repo contains an Arch User Repository package for Powershell following the next standard for the installation:

1. App files directory: `/usr/share/powershell`
2. Executable `powershell` directory: `/usr/share/bin/powershell`

* The executable in `/usr/share/bin` is installed as symbolic link to the `powershell` bin inside the app files.

## * Notes

This package proceeds with the installation as described in [Powershell](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-linux?view=powershell-7.2)

This package may differ from the "official" in the AUR repository in the directories used for the installation and the steps used. The purpose of this package and others 
ones in this account is for install all the programs that I used following certain standard (i.e. using `/usr/share/{pkgname}` for app files and `/usr/share/bin/{execname}`
for executable) and in some cases clean the installation steps from some bloat.
