title: Install Ubuntu 16.04 on VirtualBox
tags:
- Virtualbox
- Ubuntu
- Linux
---
Ubuntu 16.04 LTS is released on [21st April 2016](https://insights.ubuntu.com/2016/04/20/canonical-unveils-6th-lts-release-of-ubuntu-with-16-04/?_ga=1.236707842.248725857.1449202609), let's try it in Oracle VM VirtualBox Manager. Please note that this article is just as a tutorial for newbies.

## Quick Install
For quick installation, all options are left as default.

### Download installation image
Download address: [http://www.ubuntu.com/download](http://www.ubuntu.com/download).

Please download 32bit version if your machine is 32 bit, or you're not sure if your machine support 64bit virtualization.

### Create virtual machine in Virtualbox
* Click `New` tool button in Virtualbox
* Enter `Name` in `Name and operating system` dialog of `Create Virtual Machine`, select `Linux` in `Type` dropdown list, and `Ubuntu (32-bit)` or `Ubuntu (64bit)` in `Version`. If you include `ubuntu` in the `Name`, `Type` and `Version` will be auto selected as above selection. Then click `Next`.
* Click `Next` in `Memory size` dialog if you want the recommended memory size. Or change the size and then continue.
* Click `Create` in `Hard Disk` dialog
* Click `Next` in `Hard disk file type` dialog to use default VDI.
* Click `Next` in followed dialog.
* Click `Create` in `File location and size` dialog. Change location and size if you want before click the button.

Now, you will have a new virtual machine in your Virtualbox list with your entered name.

### Load installation image
* Select the new virtual machine, click `Settings` and there will be Settings dialog.
* Choose `Storage` on the left of the `Settings` dialog, then Select `Empty` under `Controller: IDE` on the midddle side.
* Click the disk image button on the right, select `Choose Virtual Optical Disk File`, then locate your downloaded installation image.
* Finally click `OK` to close `Settings` dialog.

### Install with default options
* Select the new virtual machine if it is not selected, then click `Start` button on the bool bar.
* There will be `Install` window, it lists languages on left, and options `Try Ubuntu` and `Install Ubuntu` on right, let's select the later option.
* Click `Continue` in following `Preparing to install Ubuntu` window.
* Leave all options as default and click `Install Now` button in `Installation type` window. **Please select the last option `Something else` if you are not install in VirtualBox, or it will erase your whole disk and install Ubuntu, you will lose all existing data on your disk, unless you want to do this.**
* `Continue` in `Write the changes to disks` dialog, it will make 2 partitions, one for /, another for swap. There is no need to change it since it is just a virtual machine.
* Select `Where are you` on the map, one click on the map will reach this, then `Continue` or `Next` whatever you see. Oh, don't forget enter required information.
* After installation done, it will ask you to restart. Before restart, do `Load installation image` again, but choose `Remove Disk from Virtual Drive` instead of `Choose Virtual Optical Disk File`, then restart.


## Install Virtualbox additional tools
Virtualbox additional tools will improve performance of your virtual machine, after started your virtual Ubuntu, do as following:
* Click `Insert Guest Additions CD image` in menu `Devices`, then `Run` in the virtual Ubuntu popup dialog.
* It will install automatically after enter your password for your account.

## Make it real full screen
The virtual Ubuntu may cannot be full screen, when you're using a laptop with solution as 1366*768, the screen solution may be only 1024*768, to make it full screen, execute following command in your virtual Ubuntu.

    sudo apt-get install virtualbox-guest-utils virtualbox-guest-x11 virtualbox-guest-dkms

## How to support 64 bit in Virtualbox (*TBD*)

## Other problems (*TBD*)