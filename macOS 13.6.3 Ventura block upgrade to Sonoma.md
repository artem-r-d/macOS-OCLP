## macOS 13.6.3 Ventura block upgrade to Sonoma
Although not officially confirmed, there is a recurring bug in 13.6.3 Ventura that seems to ignore upgrade options and may even start Sonoma upgrade .app download when closing notifications about it. Because OCLP systems can be bricked by in-OS system upgrades that lack the neccessary OCLP patches to run propertly, some users may opt out of all system upgrades entirely.

In order to block all macOS system upgrades, security patch upgrades, and software upgrades (such as Safari), you will need to perform these steps:
1. Initialize target system with OSX or macOS. OCLP documentation states:
The patcher application requires OS X Yosemite 10.10 or later to run.
OS X El Capitan 10.11 or later is required to make installers for macOS Ventura and later.
The patcher is designed to target macOS Big Sur 11.x to macOS Sonoma 14.x.
Other versions may work, albeit in a broken state. No support is provided for any version outside of the above.
For most situations, using internet reinstallation of latest supported macOS should satisfy the requirement to get OCLP up and running, in order to create the desired Ventura installer.
2. Use OCLP to create the Ventura installer.
3. Before installation, clear the NVRAM/PRAM by holding Command-Option-P-R.
4. Perform a clean installation of Ventura, including using the "Erase" function on the target disk (you may pick APFS and a name such as "Macintosh HD")
5. During macOS guided setup, carefully choose to explore all the options (do not choose "quick setup" as this may automatically choose undesired defaults)
6. Upon logging in with your only user, verify that wifi is off, and head straight into system settings > upgrade
7. Set all auto upgrade options to off. Make sure everything says "off" and is grey.
If you create another Administrator user make sure to repeat the process for that user as well. Any Administrator type user can set the system into macOS upgrade, even accidentally through bugs.
9. Install Lulu. https://objective-see.org/products/lulu.html
10. Once Lulu is up and running and can block processes from accessing the internet, go head and enable and connect to wifi.
11. Blocking the following processes will disable all upgrades to the system:
betaenrollmentd (has to do with beta updates enrollment, may only show up for iCloud logged in users)
mobileassetd (removes the red (1) in settings cog)
promotedcontentd
softwareupdate_firstrun_tasks
softwareupdated (com.apple.softwareupdated)
softwareupdated (com.apple.mobile.softwareupdated)
12. It is possible that in later versions of Ventura such as 13.6.4, the notification bug will be fixed and Sonoma .app will not be installed outside of proper functions. In that case, disabling Lulu temporarily (with auto updates still set to off) may allow the user to update Safari separately and install security patches without being forced into Sonoma upgrade. More testing is needed.
