# Display Driver Uninstaller

![1](https://sun9-1.userapi.com/impg/CVPFaMOP0KDfO2jQPZRZEECooFNtAhKqExT3uA/zhkQhLbbV5Q.jpg?size=770x416&quality=96&proxy=1&sign=8e125eb3a8bc4be379e3cac0cbafcfcc&type=album)


**Display Driver Uninstaller** - is a utility for complete removal of AMD, NVIDIA, INTEL video card drivers from the system, including registry keys, folders and files.

**Display Driver Uninstaller (DDU)** completely removes video card drivers from the system, including their entries in the registry, files and folders, and registration keys. **DDU** removes video card drivers from **AMD, NVIDIA, Intel.** In the arsenal of the utility there are many advanced functions and useful settings: various uninstallation options: "with reboot", "without reboot", "with turning off the PC" (to install a new video card); creating a system restore point before deleting; deleting / saving the root folder with drivers; deleting / saving existing monitors; creating and saving log files in the program folder; correct removal or preservation of additional software installed with the drivers.

# Recommended use
- It is best to completely exclude the DDU folder from any security software to avoid problems.
- Please be aware that NVIDIA / AMD has nothing to do with this, I do not work for NVIDIA / AMD or for NVIDIA / AMD, and they should not be held responsible for anything that might go wrong with this application.
- You have to turn off internet or completely block Windows Update when starting DDU until new drivers are installed.
- DDU should be used when there are problems uninstalling / installing a driver or when switching the GPU brand.
- DDU should not be used every time you install a new driver unless you know what you are doing.
- DDU will not work on a network drive. Please install it to your local drive (C :, D :, or else).
- The tool can be used normally, but for absolute stability when using DDU, Safemode is always the best.
- If you are using the DDU normally, clean, reboot, clean again, reboot.
- Make a system backup or restore (but usually it should be pretty safe).
- It is best to completely exclude the DDU folder from any security software to avoid problems.

![1](https://sun9-47.userapi.com/impg/tu__xwYRr4_Ek-L8N52xEtVQrEsnrAeq2gF7Ig/8ybRMqG37ZY.jpg?size=603x549&quality=96&proxy=1&sign=5739c2f610ced8b76a418ddf33ac2b5e&type=album)

# Using Display Driver Uninstaller

If the video card driver is not removed correctly, system crashes, “blue screens” may occur, and the stability of the **OS** will be impaired. **Display Driver Uninstaller** will help you avoid this. Before removing the drivers, the developers strongly recommend creating a restore point and performing all actions in safe mode. At the first launch, the program will automatically detect the manufacturer of the video card. There is a possibility of manual selection. There are three ways to uninstall drivers:
1. Delete and restart. Recommended method in which the computer will restart after complete removal of drivers and residual files. Allows you to avoid many problems when installing other drivers;
2. Removal without reboot. Removal is performed without further rebooting the system. After uninstalling the video card driver, the screen darkens for a few seconds required to start the standard Windows video driver.
3. Delete and turn off. After uninstalling, the computer automatically turns off. This method is convenient for uninstalling drivers before replacing the video card.

All operations performed are stored in a special journal. You can access it by going to the appropriate tab at the top of the window.


### System requirement:

- Windows Vista SP2 before Windows 10 2004
- GPUs NVIDIA, AMD, Intel
- Microsoft .NET Framework 4.5 or higher

# Benefits of Display Driver Uninstaller

**Display Driver** Uninstaller is compatible with all versions of Windows operating systems. Its capabilities are as follows:
- Complete removal of video card drivers and residual files;
- The ability to bypass the limitations of the operating system, remove "non-removable" or incorrectly installed drivers;
- Uninstalling not only the main driver, but also all previous ones installed earlier;
- Journaling;
- Simple and intuitive interface that allows you to complete the task in two steps.

# List of changes

**18.0.0.6**

- Added support for removing USB Type "C" Nvidia RTX cards;
- Removal of NVIDIA NGX (SDK based on deep learning algorithms);
- Additional removal of remnants of AMD drivers;
- Fixed problem with deleting SharedDlls;
- Changed the logic for deleting devices;
- Bug fixes and additions to remove Realtek drivers;
- Localization update Turkish.xml;
- If FriendlyName is available for the deleted device, then this name is used in the log-file, if not, then the descriptor (description) of the device is used;
- Fixed a small issue with removing USB Type C.

**18.0.0.5**
- New requirement starting with this version: ".NET Framework 4.5 now required".
  Cause: Recently, Windows 10 has been using DCH drivers and these drivers come from their control panel in the Microsoft store App. To remove them, you need some    libraries that are only available in .NET 4.5. This, now, forces us to update too. The disadvantage is the end of support for Windows XP;
- Removal of DCH drivers from Nvidia, Intel, Realtek is now supported;
- Additional cleaning of the Realtek audio driver;
- Removing a new subkey found in HKLM / Software / nvidia corporation / installer2 / (Drivers);
- Removed "CharSet: = CharSet.Unicode" and "MarshalAs (UnmanagedType.LPWStr)" from "Function CM_Get_Device_ID" which gave unexpected results when getting DeviceID using .NET 4.5;
- (DCH) Remove a device class extension and their components.

**18.0.0.4**
- Fixed a bug that affected the removal of the CUDA SDK after using the DDU. Thank you ("Forceflow");
- Cleaning up "NvDLISR" from Geforce Experience 3.16.0.122 Remaining after uninstallation.

**18.0.0.3**

- Removed module paexec.exe (network administration);
- Fixes and improvements for removing Vulkan API libraries. (Thanks Sora);
- Added support for removing Vulkan components in Intel implementation;
- Updating localization files.

**18.0.0.2**

- Additional NVIDIA cleaning;
- Updating localization files;
- System requirements up to Windows 10 October 2018 update 1809 (17763.xx).

**18.0.0.1**

- Additional NVIDIA cleaning;
- Fixed cleaning of system environment paths;
- Updated localization files Slovenian.xml & Turkish.xml;
- The selected combo box is translated again;
- Added many missing "Nothing" checks when using the registry.

**18.0.0.0**

- Added support for uninstalling Realtek audio drivers. (WIP);
- Added very limited removal of SoundBlaster sound driver (not files or registry yet);
- Added command line arguments: -cleanrealtek -cleansoundblaster;
- Fixed possible startup error when a ## character is in the folder name;
- Fixed many possible null exceptions that can be encountered under certain specific code cleanup conditions.

**17.0.9.1**

- Fixed deleting entries in the SharedDlls key of the Windows registry;
- Fixed argument "silent" for pending computer restart;
- Updated localization files Japanese.xml & Swedish.xml;
- Minor improvements to menu options.

**17.0.9.0**

- Re-added the ability to disable driver search when updating Windows as an option;
- Added a version number to the "About" window;
- Minor bugs fixed.

**17.0.8.7**


- Streaming removal of some files and cleaning the registry to improve speed;
- Additional Intel cleaning;
- Additional cleaning Nvidia;
- DDU no longer uses (does not depend on) c: \ windows \ system32 \ sc.exe;
- Windows Update is back to default, so when using DDU, you need to turn off the internet;
- Better path detection;
- The log is now generated even if the DDU does not start correctly and contains more detailed information;
- Bugs fixed;
- Updated Readme file and problem and solution files.

**17.0.8.6**

- Support for Windows 10 1803.
- Added support for upperfilter (fine selection) in SetupAPI for correct device / service removal.
- Numerous code fixes / improvements / Additional cleaning.
- Updated translation of CZ.
- Turkish translation update.
- New Thai. Updated THAI.xml;
- System requirements up to Windows 10 Fall Creator update 1803 (17134.xx).
