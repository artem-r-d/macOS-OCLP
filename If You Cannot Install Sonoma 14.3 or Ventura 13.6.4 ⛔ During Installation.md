⛔ During Installation 

Your firmware needs to be updated via the Internet Recovery option. My best guess at the moment is firmware can be put into a bad state if you do a raw Windows install and then install bootcamp inside Windows, which is supposed to manage dualboot options on a single drive Mac. This may put your firmware into a weird state, especially if you install Windows onto a clean disk and its the only OS on your Mac. For some reason bootcamp may confuse the firmware into booting impropertly when it comes back to MacOS, including both OCLP and regular supported versions of MacOS.

Workaround:
If using Windows on a single drive mac, install the bootcamp drivers individually and DO NOT install BootCamp.msi in Apple folder as this is the program responsible for managing Apple/Windows dualboot settings and installing it will not harm your Windows install but it may absolutely wreck your ability to install MacOS outside of Internet Recovery (which may not be a thing in the future). Just install the bootcamp drivers individually to get full Windows functionality and skip BootCamp.msi. 

Resetting your SMC may also fix this issue so try that "Press and hold Shift, Control, and Option on the left side of the keyboard. At the same time, press the power button."

If you cannot install MacOS OCLP and during the installation you see the :no_entry_sign: symbol at the step where the installation is supposed to continue from the hard drive:
1. Turn the machine off
2. Reset pram with "press and hold the Option, Command, P, and R keys on your keyboard"
3. Boot into internet recovery with "Option-Command-R or Shift-Option-Command-R"
4. Complete macos installation of whatever macos is supported on that device. You will actually see the :no_entry_sign: again but don't touch anything. Install process will see it and reboot into firmware update mode and fix your firmware. 
5. After your macos is reinstalled you can either OCLP from there or go back to using your prepared OCLP installation media (it should complete installation processes fine now).

If you have stuff on the drive that you can't lose you may try Internet Recovery install onto an external drive just to get the firmware fixed then boot back into your system.
