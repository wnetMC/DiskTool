# DiskTool
Bathfile encryption tool using the AES algorithm. (Designed for USB Sticks but works on any hard drive.)

# Installation and Setup
Installation is very simple, just edit the DiskTool.cmd file and change the %VaultPath% variable to the path of the folder which contents will be encrypted (encrypts all subfolders too), when you're done, change the %pass% variable in the DiskTool.cmd file as such:

```batch
if NOT %pass%== YOURPASSWORD goto :Fail rem change YOURPASSWORD to your preferred password.
```
