---
title: Building a virtual data center using VirtualBox and Ubuntu
author: Mike
layout: post
permalink: /2010/08/building-a-virtual-data-center-using-virtualbox-and-ubuntu/
dsq_thread_id:
  - 130182935
views:
  - 281
categories:
  - Tech
tags:
  - ubuntu
  - virtualbox
---
In this guide, I'm going to show you how to create a virtual data center, right on your computer. The virtual servers will be able to communicate with each other in a private network. I'll also be able to communicate with them from the outside as well. Honestly, I hope you have a lot of RAM.

Ok, let's go!

&nbsp;

I'm personally running a Windows 7 PC, but will be bringing up 3 Ubuntu Server instances. These instruction, with a little common sense, should work for any host OS. Because I'm using Ubuntu Server, there won't be any GUIs here to use as a crutch. Dust off those command line skills.

&nbsp;

#### Get and install VirtualBox

<http://www.virtualbox.org/>

VirtualBox is the virtual machine handler that we'll be using to deploy our virtual servers.&nbsp;Download and install the latest version (duh).

&nbsp;

#### Get Ubuntu Server

<http://www.ubuntu.com/server>

If your processor supports hardware virtualization, download the 64-bit image. If it doesn't, or you have no idea what that means, download the 32-bit image.

Ubuntu is a great Debian-based Linux distribution that has some really phenomenal adoption and community support. Download the latest version of Ubuntu Server. We'll use that to install Ubuntu on our VM (virtual machine) instances.

&nbsp;

#### Create the first server

In VirtualBox, select 'New'

Name your machine. I'm calling mine 'head'. Select Linux as the OS, and Ubuntu as the version.

Select how much RAM to allocate. It will depend upon your specific needs (and how much RAM you have total), but the default work for now.

Boot a hard disk, and select to create a new one.

You want dynamically expanding storage.

Finish everything up.

Congrats you now have a virtual machine with nothing on it.

&nbsp;

#### Settings

Select 'Settings' for your server, and go to the Network pane.

Set adapter 1 to bridged mode. Select the appropriate network adapter to bridge it to.

Select the Adapter 2 tab.

Enable it, and attach it to an 'Internal Network'. Name the network whatever you like.

&nbsp;

#### Installing Ubuntu Server

Select your VM and select 'Start'. You'll be walked through the 'First Run Wizard'

Browse for your Ubuntu image you downloaded earlier, and select that. Finish up the wizard.

Go through the installation process for Ubuntu. Default settings will be fine. Select eth0 as your primary network interface.

I'm not going to walk you through the details. There are better guides [here][1].

After the OS installs and you boot for the first time, run ***sudo apt-get update***&nbsp;then&nbsp;***sudo apt-get upgrade&nbsp;***to ensure you have the latest updates for your system.

&nbsp;

&nbsp;

#### Go Headless

<http://www.toptensoftware.com/VBoxHeadlessTray/>

We want to go headless with our little datacenter, so go grab VBoxHeadlessTray to make managing headless VMs a lot easier.

&nbsp;

Install whatever software you need onto the VM. Whatever you install here is going to be present on all future cloned machines.

&nbsp;

#### Clone VMs

Something along the lines of&nbsp;***"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" clonehd db1.vdi db2.vdi***

Obviously, the *.vdi files will be whatever you want them to be. That just happened to be my names.

Create a new VM for each of these cloned hard drives with the same settings as above.

&nbsp;

There you go. Clone as many times as you would like. Once you get their IP addresses from an ifconfig, you're more than welcome to go SSH into them. Makes management a lot easier, especially if you need a lot of boxes.

&nbsp;

Note: If you're having difficulties getting your clones machines onto the network, Ubuntu probably cached the MAC addresses. just run ***sudo rm /etc/udev/rules.d/70-persistent-net.rules*** and reboot

 [1]: https://help.ubuntu.com/