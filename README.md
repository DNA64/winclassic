  
# winclassic
Run Microsoft Windows on your Classic Mini!

## How to Install Windows 3.x on your S/NES Classic [ROUGH DRAFT]
Tutorial by viral_dna

Let's skip the "Why?" and move right into the "How?!".

**Abbreviated Meanings:**

 - RA = RetroArch
 - H2CE = Hakchi2 CE

**Pre-requisites:** 

First and foremost this guide requires and assumes you have a modded S/NES Classic and already have the [latest build of Hakchi2 CE](https://github.com/TeamShinkansen/Hakchi2-CE/releases/latest). 
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

Make sure you download the file that matches your systems region and configuration (NAND or USB).

You'll also need a copy of Windows 3.x, Obviously for legal reasons I cannot link to these, so you'll have to find those on your own. Windows 3.x comes on six 1.44mb floppy disks. You can find some on ebay if you like. 

You do NOT require DOS for this guide.

**DO NOT USE THE .IMG FILES!**

For best results mount a folder instead of an .img (More on that below). You'll run into less errors. Checkout the Free [ImDisk Toolkit](https://sourceforge.net/projects/imdisk-toolkit) software. This is a fantastic tool that will let you mount HDD and floppy image files with ease. 

You can use it to extract the setup files you'll need from the Windows 3.x installation disk images.

**ATTENTION!!!**

*When un-installing windows you MUST use the un-installation guide below. Hakchi2 CE isn't capable of uninstalling Windows and although the icon will disappear and you won't see the files, they will remain on the system taking up space!*


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

  For Example:
  If you have a North American SNES Classic and are **DONE** installing Windows to the **NAND**, you would download the following dosbox.conf file...  
  https://github.com/DNA64/winclassic/tree/master/DOSBox%20Configs/snes/usa/nand/run/dosbox.conf
  
Make sure you download the file that matches your systems region and configuration (NAND or USB).

Now when you launch Windows 3.x from your home menu you should boot right into Windows 3.x :)

The End.. or is it? 
More exciting things to follow! ;)

# Troubleshooting

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

> The Windows directory is only visible when Windows (or DOSBox) is
> running on the system. Uninstalling DOSBox will not delete the Windows installation.

You should be able to find it at the directory below (varies based on region):

    var/lib/hakchi/games/snes-usa/.storage/CLV-O-HNUZA/WINDOWS/

- When I sync the system using Hakchi2 CE my files aren't updated?

> This drove me crazy when I was testing things. I found transferring
>  files over ftp more reliable.


# Uninstalling Windows

Uninstalling Windows is NOT as simple as removing a game from your system, un-checking it in H2CE and then syncing with the system will remove the icon from your system, but not remove the Windows installation.

In order to remove the Windows installation completely and correctly perform the following steps.

## Step 1.

Select the Windows 3.x program in your H2CE apps list again and press `F4` to locate the `dosbox.conf` file and replace it with the one from the "Un-install" folder on the github page.

## Step 2.

Sync the changes to the system.

## Step 3.

Launch Windows. The un-install script will run and remove the Windows folder.

## Step 4.

You may now un-install Windows through H2CE as you would any game/app, by un-checking the box next to it and syncing with your system.

Windows is now fully and properly un-installed! 
There may still be some files left behind that H2CE wasn't able to remove, to be sure, ftp into the system and check the following directory. If found, remove it.

> var/lib/hakchi/games/snes-usa/.storage/CLV-O-HNUZA/

I will create a module to automate all of this soon.

**Please Note:**

At this point, it's recommended you right click on Windows in the H2CE list and delete it.

You may leave it if you like, however, in order to install windows again, you will need to add the Windows Setup files to the INSTALL folder again (NAND users only) and the appropriate `dosbox.conf` file from the github repo, essentially following the guide above again (You can skip Step 2).