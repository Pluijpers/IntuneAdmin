# IntuneAdmin

## Preparation
**Installer for multiple files**
1. Create an **install.ps1** that performs and **fully silent** installation and returns exit code 0 (zero) for success non-zero for errors.
2. Create an **uninstall.ps1** that performs a **fully silent** removal of the application and returns exit code 0 (zero) for success and non-zero for errors.
3.	Organize install.ps1, uninstall.ps1 and application installer(s) in a single folder.
4. Package with the [Intune Win32 Content Prep Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool) into a single .intunwin file.
5. After generation, you’ll have a ready-to-upload .intunewin package file.

**Installer for single file**
1. Simply package the .msi or .exe with the [Intune Win32 Content Prep Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool) into a single .intunwin file, which allows you to use:
   - Install command: ```msiexec /i "YourApp.msi" /qn /norestart```
   or ```YourApp.exe /verysilent /norestart```
   - Uninstal command: ```msiexec /x "YourApp.msi" /qn /norestart```
   or ```"%ProgramFiles%\YourApp\uninst.exe" /verysilent```

# Create Windows App
App type: Windows app (Win32)

## App Information
|Setting|Value|
|:---|:---|
|Name	
|Description||
|Publisher||
|App Version||
|Category||
|Show in Company Portal||
|Information URL||
|Privacy URL||
|Developer||
|Owner||
|Notes||
|Logo||


## Program
|Setting|Value|
|:---|:---|
|Install command| ""|	
|Uninstall command| ""|	
|Installation time required (mins)|20|
|Allow available uninstall|Yes|
|Install behavior|System|
|Device restart behavior|No specific action|
|Return codes||	


## Requirements
|Setting|Value|
|:---|:---|
|Check operating system architecture | Yes, install on x64 system |
|Minimum operating system | 1903 |
|Disk space required (MB) | [None] |
|Physical memory required (MB) | [None] |
|Minimum logical processors required | [None] |
|Minimum CPU speed required (MHz) | [None] |
|Configure additional requirement rules | [None] |

## Detection Rules
|Setting|Value|
|:---|:---|
|Rules format|Manually configure detection rules|
|Type|Registry|
|Key path||	
|Value Name|Version|
|Detection method||	
|Operator|Greater than or equal to|
|Value||
|Associated with a 32-bit app on 64-bit clients|No|

---

|Setting|Value|
|:---|:---|
|Rules format|Manually configure detection rules|
|Script file||
|Run script as 32-bit process on 64-bit clients|No|
|Enforce script signature check and run script silently|No|
