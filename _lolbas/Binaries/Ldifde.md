---
Name: Ldifde.exe
Description: Creates, modifies, and deletes LDAP directory objects.
Author: 'Grzegorz Tworek'
Created: 2022-08-31
Commands:
  - Command: Ldifde -i -f inputfile.ldf
    Description: Import inputfile.ldf into LDAP. If the file contains http-based attrval-spec such as thumbnailPhoto:< http://example.org/somefile.txt, the file will be downloaded into IE temp folder.
    Usecase: Download file from Internet
    Category: Download
    Privileges: Administrator
    MitreID: T1105
    OperatingSystem: Windows Server with AD Domain Services role,  Windows 10 with AD LDS role.
Full_Path:
  - Path: c:\windows\system32\ldifde.exe
  - Path: c:\windows\syswow64\ldifde.exe
Code_Sample:
  - Code:
Detection:
  - IOC:
  - Analysis:
  - Sigma:
  - Elastic:
  - Splunk:
  - BlockRule:
Resources:
  - Link: https://twitter.com/0gtweet/status/1564968845726580736
Acknowledgement:
  - Person: Grzegorz Tworek
    Handle: '@0gtweet'
---
