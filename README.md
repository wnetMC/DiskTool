# DiskTool
Bathfile encryption tool using the AES algorithm. (Designed for USB Sticks but works on any drive.). Supports 1 and 2 layer encryption & file compressing.

# Functioning
1 layer encryption encrypts every file in the filevault directory using AES; 2 layer encryption does the same but then adds every file to a .7z archive, compresses it, and encrypts it using a different encryption key for a second layer of protection.  
Decryption is all automatic. DiskTool detects if you used 1 or 2 layer encryption automatically, asks for your defined password and decrypts your files.

# Installation
Installation is very simple, just edit the DiskTool.cmd file and change the %VaultPath% variable to the path of the folder which contents will be encrypted (encrypts all subfolders too), when you're done, change the %pass% variable in the DiskTool.cmd file on line 30:

```batch
if NOT %pass%== YOURPASSWORD goto :Fail rem change YOURPASSWORD to your preferred password.
```

# Usage
DiskTool uses the following commands to work:  
"encrypt" will encrypt the selected folder on your drive.  
"decrypt" will decrypt the selected folde ron your drive if the passwrd is enetered correctly.  
"newkey" will create a text file in %vaultpath%/Keys/ with your specified content so that it can be encrypted and stored safely. (Made to store information such as mnemonic keys safely.)  
"help" will display all commands and their usage.  
"clear" will clear the DiskTool console.
"exit" will... exit.  

# My setup on my disk
![Picture1](https://i.ibb.co/zVRz64v/73lzau0n.png)  
(I hide aes.exe, 7z.exe & 7z.dll)
