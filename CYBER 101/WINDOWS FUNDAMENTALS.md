•The file system used in modern versions of  Windows  is the New Technology File System or simply  NTFS (opens in new tab).

# NTFS (New Technology File System)
•**Journaling File System** – Stores logs to automatically repair files/folders after a failure.

•**Supports Large Files** – Can store files larger than 4 GB.

•**File & Folder Permissions** – Allows setting specific access permissions.

•**Compression** – Supports file and folder compression to save space.

•**Encryption** – Supports EFS (Encrypting File System) for data security.

•**More Reliable than FAT(file allocation table)** – Better recovery, security, and storage features.

•**Commonly Used In** – Modern Windows operating systems.

## NTFS Permissions

•**Full Control** – Complete access to view, modify, delete, and manage permissions.

•**Modify** – Read, write, and delete files/folders.

•**Read & Execute** – View and run files/programs.

•**List Folder Contents**– View files and subfolders in a folder.

•**Read** – View file contents and properties only.

•**Write** – Create or modify files and folders.

## Alternate Data Streams (ADS)
•**ADS** – NTFS feature that allows a file to contain multiple data streams.

•**Default Stream** – Every file has at least one stream called $DATA.

•**Hidden Data** – ADS data is not visible in Windows Explorer.

•**View ADS** – Can be viewed using PowerShell or third-party tools.

•**Security Risk** – Malware can hide data in ADS.

•**Legitimate Use** – Stores metadata, e.g., marking files downloaded from the Internet

## Windows Folder & Environment Variables
**Windows Folder (C:\Windows)** – Contains the Windows operating system files.

**Location Flexibility** – Windows folder does not have to be on the C: drive; it can be stored elsewhere.

**Environment Variables** – Store important system information and paths.

**%windir%** – System environment variable that points to the Windows directory.

------------
## Uses of Environment Variables
➡Store OS paths
➡Store processor information
➡Store temporary folder locations
➡Help programs locate system resources easily

--------

User accounts can be one of two types on a typical local Windows system: 

1.Administrator user

2.Standard User. 

•The user account type will determine what actions the user can perform on that specific Windows system. 

➡An Administrator can make changes to the system: add users, delete users, modify groups, modify settings on the system, etc. 
➡A Standard User can only make changes to folders/files attributed to the user & can't perform system-level changes, such as install programs.

•Way to access this information, and then some, is using Local User and Group Management. =====lusrmgr.msc
•Username and password for the standard user. It's visible in lusrmgr.msc 

----------

### User Account Control (UAC)

* Most home users use **Administrator accounts**, which can make system changes.
* Running all tasks with admin privileges increases the risk of malware infections.
* If malware infects an admin account, it can also make system-level changes.

### What is UAC?

* **UAC (User Account Control)** is a Windows security feature.
* Introduced in **Windows Vista**.
* Helps protect the system from unauthorized changes.

### How UAC Works

* Even if a user is an Administrator, Windows does **not** run everything with elevated privileges.
* When a task requires admin rights, UAC displays a **confirmation prompt**.
* The user must approve the action before it runs with higher privileges.

### Important Note

* By default, UAC does **not** apply to the built-in Administrator account.

--------

### Security Tab

* The **Security** tab shows users/groups and their permissions for a file or folder.
* Standard users usually have limited permissions compared to Administrators.

-------------

### TASK MANAGER

•The Task Manager provides information about the applications and processes currently running on the system. Other information is also available, such as how much CPU and RAM are being utilized, which falls under Performance. 
➡can access the Task Manager by right-clicking the taskbar. 

keyboard shortcut to open Task Manager? ==== CTRL+SHIFT+ESC






