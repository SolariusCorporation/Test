## Preparing the system for the boot manager unlock process

Before unlocking the boot manager, you will need to tweak some system settings.

**First,** you will need to enable Developer Mode. You can do this by going to ``Settings > System Software Information > Build Information`` and clicking the build number 5 times.
**Next,** you will need to enable USB debugging and OEM unlock. These toggles are located in ``Settings > Developer Options`` under the System Software Modification category.
**Lastly,** you need to back up any important data because boot manager / boot loader modifications could cause permanent damage to your system.

## Reboot device into recovery mode

Once you have changed settings accordingly, you need to reboot your device into Recovery mode to initiate the boot manager / boot loader unlocking process.

# PC

Open command prompt and type ``sudo aspboot.efi --mode=recovery``. The computer will be rebooted into recovery mode.

!!! info
    You will need super user permissions to execute this command.

# Mobile

Hold down the power, volume down, and volume up buttons simultaneously for 7 seconds. The phone will be rebooted into recovery mode.

# Playstation 4

Hold down the Playstation power button for 20 seconds. The console will be rebooted into recovery mode.

## Initiate the unlocking process

When you are in Recovery mode, you need to select ``Advanced options`` and navigate to ``Terminal Prompt``. Once at the terminal prompt, type the following commands in order:

``adb --authenticate-super-user --key={your_device_passcode}``

``adb --unlock-boot-loader``

!!! info
    This command could take up to an hour to complete.

``adb --boot --mod --options=AespaConf[True],AespaBootMgrLdrUnlock[True]``

``diskpart --open``

``diskpart lst dsk``

``diskpart sel dsk /dev/sdb1/boot``

``diskpart clean part $sel``

``diskpart --exit``

``asp --firmware-edit --remove="BootMgrLdrLock"``

``rm /system/efi/boot/bootmgrldrlock.lck``

## Reboot your device

After running the above commands and unlocking your bootloader, reboot your device and you will need to run through the Out Of Box Experience again. Once that is done, you are finished! You have successfully unlocked your boot loader and can install custom OS's, and install custom firmware. You can restore the locked boot manager / loader state at any time by performing the same steps but replacing the second terminal command with ``adb --lock-boot-loader``.