# Cloaker

Cloaker is a simple windows utility written in C to allow the cloaking an decloaking of directories. A cloaked directory will only be cloaked, not locked or encrypted, and will thus remain accessible to anyone who knows the path.

## Setup

 1. Get the latest .zip release of Cloaker from the [releases](https://github.com/SteveOhIo/Cloaker/releases) tab
 2. Create a new folder in your program files called **Cloaker**
 3. Extract the contents of the .zip to your **Cloaker** folder
 4. Open an instance of Windows Powershell as an administrator inside the **Cloaker** folder
 5. Run this powershell command to temporarily bypass restrictions on unsigned scripts:

        Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

 6. Run the **register_paths.ps1** powershell script with this command:
        
        .\register_paths.ps1

 7. Run this powershell command to re-restrict unsigned scripts:

        Set-ExecutionPolicy -Scope Process -ExecutionPolicy Restricted

## Usage

To use Cloaker, you first need to have a folder you want to be managed by it. For this example, we will create a new folder on the desktop called "cloaker-test". Let's imagine its path to be 
        
    "C:\Users\MyUser\Desktop\cloaker-test"
We can now run the "CloakerConfig.exe" file inside the **Cloaker** directory. Bear in mind this file requires administrator privileges to run.
Follow the on-screen instructions to pass in the path to your chosen folder. You will eventually be prompted for a keyword. This keyword is what you type after the **cloak** or **decloak** command to reference that folder in particular. So make sure you choose a keyword that you will remember what it is referencing.
Once CloakerConfig has run, you can use the program at any time via powershell, windows terminal, command prompt, or even the Windows Key + R shortcut.
Simply type

    cloak <keyword>
   to cloak your folder, and 
   

    decloak <keyword>
   to decloak it.
