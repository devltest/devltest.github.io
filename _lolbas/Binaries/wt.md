---
Name: wt.exe
Description: Windows Terminal
Author: Nasreddine Bencherchali
Created: 2022-07-27
Commands:
  - Command: wt.exe calc.exe
    Description: Execute calc.exe via Windows Terminal.
    Usecase: Use wt.exe as a proxy binary to evade defensive counter-measures
    Category: Execute
    Privileges: User
    MitreID: T1202
    OperatingSystem: Windows 11
Full_Path:
  - Path: C:\Program Files\WindowsApps\Microsoft.WindowsTerminal_<version_packageid>\wt.exe
Detection:
  - Sigma: https://github.com/SigmaHQ/sigma/blob/add077b8f54474cbfa859cf45a1ca62be5462b0f/rules/windows/process_creation/proc_creation_win_windows_terminal_susp_children.yml
Resources:
  - Link: https://twitter.com/nas_bench/status/1552100271668469761
Acknowledgement:
  - Person: Nasreddine Bencherchali
    Handle: '@nas_bench'
---
