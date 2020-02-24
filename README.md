
# winclassic
Run Microsoft Windows on your Classic Mini!

## How to Install Windows 3.1 on your S/NES Classic [ROUGH DRAFT]
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

You'll also need a copy of Windows 3.11, Obviously for legal reasons I cannot link to these, so you'll have to find those on your own. Windows 3.11 comes on six 1.44mb floppy disks. You can find some on ebay if you like. 

You do NOT require DOS for this guide.

**DO NOT USE THE .IMG FILES!**
For best results mount a folder instead of an .img (More on that below). You'll run into less errors. Checkout the Free [ImDisk Toolkit](https://sourceforge.net/projects/imdisk-toolkit) software. This is a fantastic tool that will let you mount HDD and floppy image files with ease. 

You can use it to extract the setup files you'll need from the Windows 3.11 installation disk images.


**Step 1**

Drag and drop the `CLV-O-HNUZA.zip` package onto Hakchi2 CE, then right-click on the newly added `Microsoft Windows 3.11` 
app in the list and click `Show in Windows Explorer` or press F4.

This will open a new window, copy the appropriate `dosbox.conf` file you downloaded from the github repo into this window, then drag and drop the `INSTALL` folder containing the setup files into this window and click `YES`when prompted to confirm overwriting the destination files.

Once the transfer has completed you can close the window and sync the changes to your system using H2CE (Make sure the app has a checkmark so it's sync'd to the system).

**Step 2**

Now before we continue you'll need to connect a Keyboard and Mouse to your system, you can do this using a Micro USB OTG adapter as mentioned above.

Next we'll need to make some changes to RA so the Hotkeys don't interfere with typing in DOSBOX before we can setup windows.

Now there's a few ways to do this, like editing the `retroarch.cfg` on the system, but let's keep it simple. Just launch/open Windows 3.11 and when you see something on the screen press `START`+`SELECT` on the controller to open the RetroArch Quick Menu.

Now using the controller, select `X Close Content` and press `A` on the controller. Then press `B`. Now navigate to `Settings` and select `Input` from the list. Scroll down the list till you see `Hotkey Binds` and press `A`. 
Scroll down this list till you see `Hotkeys`. By default this is set to nul (- - -). Set this to something else. I used `F8` which if I recall correctly was previously set to `Take Screenshot` which I set to `S`.

You can now close RA by pressing `B`,`B` then selecting the `Main Menu` from the options to the left where at the bottom of the list on the right is the option `X Quit RetroArch`. Now if all went well, when we type in the next step you won't end up messing with all the Hotkey functions.


**Step 3**

Launch Windows 3.11 again and if all goes well the setup process should begin!

If you get the following message, make sure you've downloaded the correct `dosbox.conf` file for your system and transferred it to the system correctly.

    ATTENTION!!!
    
    Default dosbox.conf file found!
    
    Please download and use the appropriate dosbox.conf
    file for your system, region and configuration (USB or NAND),
    available here: https://github.com/dna64/winclassic


**Step 4**

Welcome to Setup.
Press `ENTER` to continue the setup process. Press `ENTER` again to use the express setup. Wait for setup to finish copying files.

Enter your Name when prompted. At this point if you don't have a mouse just use `TAB` to highlight `Continue` and press `ENTER`. 
Press `ENTER` again to verify your name is correct. Wait for setup to complete installation.

Since we're not going to setup a Printer you can simply use the `TAB` key to highlight `Install` and press `ENTER` (or press ALT+I). 
Windows will populate the program folders and then ask if you want to run a short tutorial.  You can skip this by pressing ALT+S or `TAB` then `ENTER`.

Setup is now complete!
Since Reboot isn't supported at this point, select the option to exit back to MS-DOS then type `exit` and press `ENTER` to return to RetroArch.

**Step 5**

We're almost done, we just need to replace the `dosbox.conf` file.
    
If needed select the Windows 3.11 program in your H2CE apps list again and press `F4` to locate the `dosbox.conf` file and then 
replace it with the one in the "run" folder on the github page.

  For Example:
  If you have a North American SNES Classic and are **DONE** installing Windows to the **NAND**, you would download the following dosbox.conf file...  
  https://github.com/DNA64/winclassic/tree/master/DOSBox%20Configs/snes/usa/nand/run/dosbox.conf
  
Make sure you download the file that matches your systems region and configuration (NAND or USB).

Now when you launch Windows 3.11 from your home menu you should boot right into Windows 3.11 :)

The End.. or is it? 
More exciting things to follow! ;)

# Troubleshooting

 - If you get a `himem.sys` missing error make sure that `xms=true` in your `dosbox.conf` file.

 - If you get the message *"ERROR: Cannot install the 386 enhanced mode 
expanded-memory driver."* then set `ems=false`

# Uninstalling Windows

Uninstalling Windows is as simple as removing a game from your system, simply uncheck it in H2CE and then sync with the system.
