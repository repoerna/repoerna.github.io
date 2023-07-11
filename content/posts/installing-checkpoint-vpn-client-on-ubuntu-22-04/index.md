---
title: Installing Checkpoint VPN Client on Ubuntu 22.04
summary: This is a step-by-step guide to install Checkpoint VPN in Ubuntu 22.04 x64-bit version.
slug: installing-checkpoint-vpn-client-on-ubuntu-22-04
date: 2023-03-13T11:10:02Z 
published: true
cover:
  image: "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Check_Point_logo_2022.svg/1200px-Check_Point_logo_2022.svg.png"
  alt: "CheckPointVPN Banner"
  caption: "CheckPointVPN"
  relative: false
draft: false
tags:
- vpn
- checkpoint
- ubuntu
- linux
category:
- tools 
---
# Requirements

Before you begin, ensure that your system meets the following requirements:

Ubuntu 16.04–22.04

Oracle JRE version 8, Oracle JDK version 11–19, or Open JDK version 11–19

Required tools: certutil, openssl, and xterm

```
sudo apt install libnss3-tools
sudo apt-get install openssl
sudo apt-get install xterm
```

Required libraries: libpam0g:i386, libx11-6:i386, libstdc++6:i386, and libstdc++5:i386

```
sudo apt-get install libpam0g:i386
sudo apt-get install libx11-6:i386
sudo apt-get install libstdc++6:i386
sudo apt-get install libstdc++5:i386
```

You can see the full requirements [here](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk119772).

# Installation

## Download Installation Script

To set up Checkpoint VPN on your machine, you need to download two shell script files:

snx_install.sh

cshell_install.sh

You can get these files from your company’s Mobile Access VPN page. Once you’ve logged in, click on the Settings button, and then click on Download for both SSL Network Extender (snx_install.sh) and Check Point Mobile Access Portal Agent (cshell_install.sh).

## Change Permission to Execute the File

Before running the installation scripts, you need to change their permissions to make them executable. Use the following commands:

```
chmod a+rx snx_install.sh
chmod +x cshell_install.sh
```

## Install the Scripts

Now, you can install the scripts using the following commands:

`snx_install.sh`

```
sudo ./snx_install.sh
```

If the installation is successful, you’ll see the message Installation successful.

`cshell_installation.sh`

```
sudo ./cshell_install.sh
```

If the installation is successful, you’ll see the following messages:
```
 Start Check Point Mobile Access Portal Agent installation
 Extracting Mobile Access Portal Agent...
 Done Installing Mobile Access Portal Agent...
 Done Installing certificate...
 Done Starting Mobile Access Portal Agent...
```

## Start the Mobile Access Portal Agent

Finally, you can start the Mobile Access Portal Agent using the following command:

```
/usr/bin/cshell/launcher
```

If the agent starts successfully, you’ll see the following message:

```
LAUNCHER> Starting CShell...
LAUNCHER> CShell Started
```

Congratulations! You’ve successfully installed and started Checkpoint VPN on your Ubuntu 22.04 machine.
