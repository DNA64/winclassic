
# winclassic
Run Microsoft Windows on your Classic Mini!

**Table of contents:**
 - [How to Install Windows 3.x on your NES, SNES & SEGA Classic!](https://github.com/DNA64/winclassic/blob/master/README.md#how-to-install-windows-3x-on-your-nes-snes--sega-classic)
 - [How to Install Windows 3.x on your PlayStation Classic with Project Eris](https://github.com/DNA64/winclassic#how-to-install-windows-3x-on-your-playstation-classic-with-project-eris)
 - [Windows 3.x Installation](https://github.com/DNA64/winclassic#windows-3x-installation)
 - [Troubleshooting Windows 3.x](https://github.com/DNA64/winclassic#troubleshooting-windows-3x)
 - [Un-installing Windows 3.x](https://github.com/DNA64/winclassic#uninstalling-windows-3x)
 - [Migrating your installation to another system](https://github.com/DNA64/winclassic#migrating-your-installation-to-another-system)
 - [Installing other operating systems](https://github.com/DNA64/winclassic#installing-other-operating-systems)


# How to Install Windows 3.x on your NES, SNES & SEGA Classic!
Tutorial written and maintained by viral_dna

Let's skip the "Why?" and move right into the "How?!".

**Abbreviated Meanings:**

 - RA = RetroArch
 - H2CE = Hakchi2 CE

**Pre-requisites:** 

First and foremost this guide requires and assumes you have a modded NES, SNES or SEGA Classic and already have the [latest build of Hakchi2 CE](https://github.com/TeamShinkansen/Hakchi2-CE/releases/latest). 
(Tested on Hakchi2 CE 3.5.3 and 3.7) 

You'll also need a OTG adapter of some sort, and Keyboard and Mouse. Though the mouse is optional, it will make the process much easier. 

I use a [Mini-Wireless Keyboard with a Trackpad](https://www.amazon.ca/dp/B00I5SW8MC/) though there are [cheaper options](https://www.amazon.ca/dp/B074M5HLBD/),  and a Simple [OTG MicroUSB Y Cable](https://www.amazon.ca/dp/B01IERUNL6/).

Another great option are [these little adapters](https://www.amazon.ca/dp/B07Q6VCDDB) which can turn a [small powered hub like this one](https://www.bestbuy.ca/en-ca/product/surge-4-port-charging-hub-for-switch/13885754) into an OTG Hub for the minis.

Next, if you haven't already you'll need to download and install RetroArch as well as the DOSBOX-SVN Core onto your classic system either using Hakchi2 CE or via [ModMyClassic.com](https://modmyclassic.com/category/snesc/snesc_mod_repo/).



**Required Files:**

Download the following files from my github page here: https://github.com/DNA64/winclassic
- CLV-O-HNUZA.zip
- dosbox.conf

The dosbox.conf file you'll need to install Windows will be in a folder labeled "install" on the github page.

For Example:
If you have a North American SNES Classic and are installing Windows to the NAND, you would download the following dosbox.conf file...  

https://github.com/DNA64/winclassic/tree/master/DOSBox%20Configs/snes/usa/nand/install/dosbox.conf

Make sure you download the file that matches your system, region and configuration (NAND or USB).

You'll also need a copy of Windows 3.x, Obviously for legal reasons I cannot link to these, so you'll have to find those on your own. Windows 3.x comes on six 1.44mb floppy disks. You can find some on ebay if you like. 

You do NOT require DOS for this guide.

**DO NOT USE THE .IMG FILES!**

For best results mount a folder instead of an .img (More on that below). Checkout the Free [ImDisk Toolkit](https://sourceforge.net/projects/imdisk-toolkit) software. This is a fantastic tool that will let you mount HDD and floppy image files with ease. 

You can use it to extract the setup files you'll need from each of the Windows 3.x installation disk images. Copy the extracted files from each disk into a new folder labeled "INSTALL" (The files from all 6 installation disks should be extracted into the INSTALL folder, not to individual folders).

**ATTENTION!!!**

*When un-installing windows you MUST use the un-installation guide below. Hakchi2 CE isn't capable of uninstalling Windows by default and although the icon will disappear and you won't see the files, they will remain on the system taking up space!*

# How to Install Windows 3.x on your PlayStation Classic with Project Eris

If you're looking for a guide to install Windows on the PlayStation Classic using Project Eris, I will have a guide up soon, it's really simple!

# Windows 3.x Installation

## Step 1

Drag and drop the `CLV-O-HNUZA.zip` package onto Hakchi2 CE, then right-click on the newly added `Microsoft Windows 3.11` 
app in the list and click `Show in Windows Explorer` or press F4.

This will open a new window, copy the appropriate `dosbox.conf` file you downloaded from the github repo into this window, then drag and drop the `INSTALL` folder containing the setup files into this window and click `YES`when prompted to confirm overwriting the destination files.

Once the transfer has completed you can close the window and sync the changes to your system using H2CE (Make sure the app has a checkmark so it's sync'd to the system).

Now before we continue you'll need to connect a Keyboard and Mouse to your system, you can do this using a Micro USB OTG adapter as mentioned above.

## Step 2

Next we'll need to make some changes to RA so the Hotkeys don't interfere with typing in DOSBOX before we can setup windows.

Now there's a few ways to do this, like editing the `retroarch.cfg` on the system, but let's keep it simple. Just launch/open Windows 3.x and when you see something on the screen press `START`+`SELECT` on the controller to open the RetroArch Quick Menu.

Now using the controller, select `X Close Content` and press `A` on the controller. Then press `B`. Now navigate to `Settings` and select `Input` from the list. Scroll down the list till you see `Hotkey Binds` and press `A`. 
Scroll down this list till you see `Hotkeys`. By default this is set to nul (- - -). Set this to something else. I used `F8` which if I recall correctly was previously set to `Take Screenshot` which I set to `S`.

You can now close RA by pressing `B`,`B` then selecting the `Main Menu` from the options to the left where at the bottom of the list on the right is the option `X Quit RetroArch`. Now if all went well, when we type in the next step you won't end up messing with all the Hotkey functions.


## Step 3

Launch Windows 3.x again and if all goes well the setup process should begin!

If you get the following message, make sure you've downloaded the correct `dosbox.conf` file for your system and transferred it to the system correctly.

    ATTENTION!!!
    
    Default dosbox.conf file found!
    
    Please download and use the appropriate dosbox.conf
    file for your system, region and configuration (USB or NAND),
    available here: https://github.com/dna64/winclassic

For any other errors, please see the [troubleshooting section](https://github.com/DNA64/winclassic#troubleshooting) below..


## Step 4

Welcome to Setup.
Press `ENTER` to continue the setup process. Press `ENTER` again to use the express setup. Wait for setup to finish copying files.

Enter your Name when prompted. At this point if you don't have a mouse just use `TAB` to highlight `Continue` and press `ENTER`. 
Press `ENTER` again to verify your name is correct. Wait for setup to complete installation.

Since we're not going to setup a Printer you can simply use the `TAB` key to highlight `Install` and press `ENTER` (or press ALT+I). 
Windows will populate the program folders and then ask if you want to run a short tutorial.  You can skip this by pressing ALT+S or `TAB` then `ENTER`.

Setup is now complete!

Select the option to exit back to MS-DOS then type `exit` and press `ENTER` to return to RetroArch (Press B, UP, A to exit RA), or type `win` and press enter to load back into Windows.

## Step 5

We're almost done, we just need to remove the INSTALL folder and replace the `dosbox.conf` file.
    
If needed select the Windows 3.x program in your H2CE apps list again and press `F4` to locate the `INSTALL` folder and delete it. Then locate the `dosbox.conf` file and replace it with the one from the "run" folder on the github page.

  **For Example:**
  If you have a North American SNES Classic and are **DONE** installing Windows to the **NAND**, you would download the following dosbox.conf file...  
  https://github.com/DNA64/winclassic/tree/master/DOSBox%20Configs/snes/usa/nand/run/dosbox.conf
  
Make sure you download the file that matches your systems region and configuration (NAND or USB).

Now when you launch Windows 3.x from your home menu you should boot right into Windows 3.x :)

The End.. or is it? 
More exciting things to follow! ;)

# Troubleshooting Windows 3.x

- If the Windows setup doesn't start automatically in Step 3 simply type `setup` at the command prompt and press enter.

>     c:\setup

- If after Step 5, Windows doesn't automatically boot when launched and leaves you at the command prompt, simply type `win` and press ENTER.

 - If you get a `himem.sys` missing error make sure that `xms=true` in your `dosbox.conf` file.

 - If you get the message *"ERROR: Cannot install the 386 enhanced mode 
expanded-memory driver."* then set `ems=false`

- Windows setup shows I'm installing Windows 3.1 but I'm using Windows 3.11 disks. What gives?

> The changes between 3.1 & 3.11 were so minor that a lot of the version
> information wasn't updated.

- Hakchi2 CE errors when transferring files?
If you happen to run into this issue just FTP the files to the system.

- Where is the Windows directory located?

> The Windows directory may only be visible when Windows (or DOSBox) is
> running on the system. Uninstalling DOSBox will not delete the Windows installation.

You should be able to find it at the directory below (varies based on system, region and configuration):

    NAND: var/lib/hakchi/games/snes-usa/.storage/CLV-O-HNUZA/WINDOWS/
    USB:  media/hakchi/games/snes-usa/000/CLV-O-HNUZA/WINDOWS/

- When I sync the system using Hakchi2 CE my files aren't updated?

> This drove me crazy when I was testing things. I found transferring
>  files over ftp more reliable. Just remember, any future syncs may remove files ftp'd over and cause issues if you don't re-copy them again after syncing.

- Getting errors using a USB drive?

Aside from the typical issues one might face, if you have installed windows to your system and have placed it into a folder, at this time you'll need to manually edit the dosbox.conf files with the proper destination address. This will be fixed in a future update. Just change the part in bold below in the dosbox.conf files to match the proper destination on your USB drive: 
"/media/hakchi/games/snes-usa/**000**/CLV-O-HNUZA"


# Uninstalling Windows 3.x

Uninstalling Windows is NOT as simple as removing a game from your system. Un-checking it in H2CE and then syncing with the system will remove the icon from your system, but not remove the Windows installation.

In order to remove the Windows installation completely and correctly, perform the following steps.

## Step 1.

Select the Windows 3.x program in your H2CE apps list again and press `F4` to locate the `dosbox.conf` file and replace it (Drag & Drop) with one from the appropriate "Un-install" folder on the github page.

*For example, if you have a North American SNES Classic and installed Windows to a USB drive, you would use:*
 `DOSBox Configs/snes/usa/usb/un-install/dosbox.conf`

## Step 2.

Sync the changes to the system.

## Step 3.

Launch the Windows Icon on your classic. 
The un-install script will run and remove the Installation and any related items.

## Step 4.

You may now un-install Windows through H2CE as you would any game/app, by un-checking the box next to it and syncing with your system.

Windows should now be fully and properly un-installed! 
Just to be sure, you can always ftp into the system using Hakchi2 CE (Tools > Open FTP Client) and check the following directory (Below). If found, you may safely remove it and any contents.

NAND:
> var/lib/hakchi/games/snes-usa/.storage/CLV-O-HNUZA/

USB:
> /media/hakchi/games/snes-usa/000/CLV-O-HNUZA

I will create a module (.hmod) to automate all of this soon.

**Please Note:**

At this point, it's recommended you right click on Windows in the H2CE list and delete it.

You may leave it if you like, however, in order to install windows again, you will need to add the Windows Setup files to the INSTALL folder again (NAND users only) and the appropriate `dosbox.conf` file from the github repo, essentially following the guide above again (You can skip Step 2).

# Migrating your installation to another system

If you've already installed Windows 3.x to one of your systems and want to do the same for another system, the process is about as simple as copying the Windows directory to the new system.

# Installing other operating systems

Windows 3.x isn't the only OS you can run on these systems. Aside from DOS and Windows 3.x I've also run Windows 95 and 98, and am working on several others, including something quite impressive. I will update this page with more supported Operating Systems and details as I complete testing and work on the guides. Obviously due to hardware limitations there are some performance issues running the newer stuff, and the PlayStation Classic is the best system to play around with this stuff.

Stay tuned for more info as I continue to work on and update this page.

Cheers!
viral_dna
