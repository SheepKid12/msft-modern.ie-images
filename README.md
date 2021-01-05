# Microsoft modern.ie Images

A resource providing links to VirtualBox images with various versions of IE/Edge on various versions of Windows. These images are provided mainly for developers, but they could be used for anyone who needs a VM for a specific version of Windows.

These images have been tested under Arch Linux with [VirtualBox](https://www.virtualbox.org) 6.1.

- [General notes](#general-notes)
- [Installation](#installation)
- [Available images](#available-images)
- [Activating images](#activating-images)
- [Rearming images](#rearming-images)
- [References](#references)

## Installation
1. After extracting the image, either open the `ovf` file or (from VirtualBox) go to `File` -> `Import Appliance...`.
2. Select the decompressed Open Virtualization Format (`ovf`) file.
3. Review virtual machine name and settings (adjusting to preference if required), then click `Import`.
4. (Optional) Before starting the image, create a snapshot of the current machine state - this will allow you to quickly roll back to a fresh virtual machine once the usage period of the OS expires. You could also attempt to activate the image for longer through *other means*, but you're on your own with that.

## General notes
- Images are **32bit** virtual machines *except* for the following, which are **64 bit**:
	- Windows 8.1
	- Windows 10 Stable  (13.10586 & higher)
	- Windows 10 Preview (14.14342 & higher)
- You may need to update/install the **VirtualBox Guest Additions** after VM startup. **Note:** If not already added, you may need to manually add a virtual CD drive to the VM for this to work.
- It's a smart idea to keep a clean copy of each `ovf` disk image once the OS usage period ends to avoid a full image re-download hit.
- Recommended 1GB minimum (2GB for Win10).
- After installing, you will need to [activate the trial](#activating-images) to get the full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).
- If you have no sound from the VM, switch to `Intel HD Audio`.
- If prompted for a password, enter `Passw0rd!`.
- Win8.1-10: it is possible to convert the enterprise version to pro, but it requires registry tweaking and a reinstall (you can keep data).

## Available images

### Windows XP (Professional Edition w/SP3)

- [IE6 (IA)](https://archive.org/download/ie6.xp.virtualbox/IE6.XP.VirtualBox.zip)

- [IE8 (IA)](https://archive.org/download/ie6.xp.virtualbox/IE8.XP.VirtualBox.zip)

### Windows Vista (Enterprise w/SP2)

- [IE7 (GDrive)](https://drive.google.com/uc?export=download&id=0B6ErFLUmGTfaV1Q0QndxYVViV2c)

### Windows 7 (Enterprise)

- [IE8 (MSFT Link)](https://az792536.vo.msecnd.net/vms/VMBuild_20150916/VirtualBox/IE8/IE8.Win7.VirtualBox.zip)

- [IE9 (IA)](https://archive.org/download/ie9.win7.virtualbox/IE9.Win7.VirtualBox.zip)

- [IE10 (IA)](https://archive.org/download/ie10.win7.virtualbox/IE10.Win7.VirtualBox.zip)

- [IE11 (IA)](https://archive.org/download/ie11.win7.virtualbox/IE11.Win7.VirtualBox.zip)


### Windows 8.1 (Enterpsise)

- [IE11 (IA)](https://archive.org/download/ie11.win81.virtualbox/IE11.Win81.VirtualBox.zip)

- [IE11 (GDrive)\*](https://drive.google.com/uc?export=download&id=0B76gNAvlBE7eUFZEZmlXRTlkeU0)

\* - Windows 8.1 Preview

### Windows 10 (Enterprise)

- [MS Edge - Windows 10 Stable  (13.10586) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20160322/VirtualBox/MSEdge/MSEdge.Win10TH2.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (14.14342) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20160511/VirtualBox/MSEdge/MSEdge.Win10_preview.VirtualBox.zip)

- [MS Edge - Windows 10 Stable  (14.14393) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20160802/VirtualBox/MSEdge/MSEdge.Win10_RS1.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (15.14959) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20161102/VirtualBox/MSEdge/MSEdge.Win10_preview.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (15.15014) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20170126/VirtualBox/MSEdge/MSEdge.Win10_preview.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (15.15063) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20170320/VirtualBox/MSEdge/MSEdge.Win10.RS2.VirtualBox.zip)

- [MS Edge - Windows 10 Stable  (16.16299) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20171019/VirtualBox/MSEdge/MSEdge.Win10.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (17.17074) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20180102/VirtualBox/MSEdge/MSEdge.Win10_preview.VirtualBox.zip)

- [MS Edge - Windows 10 Preview (17.17127) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20180320/VirtualBox/MSEdge/MSEdge.Win10_preview.VirtualBox.zip)

- [MS Edge - Windows 10 Stable  (17.17134) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20180425/VirtualBox/MSEdge/MSEdge.Win10.VirtualBox.zip)

- [MS Edge - Windows 10 Stable  (17.17134) - IA](https://archive.org/download/msedge.win10.virtualbox/MSEdge.Win10.VirtualBox.zip)

- [MS Edge - Windows 10 Stable  (Build 1809) - MSFT Link](https://az792536.vo.msecnd.net/vms/VMBuild_20190311/VirtualBox/MSEdge/MSEdge.Win10.VirtualBox.zip)

## Activating images

- Windows 7-10: once connected to the internet, the license should automatically activate. If not, enter the following from the Command Prompt running as administrator (Start - Right click Command Prompt - Run as administrator):

```
C:\> slmgr /ato
```

After a short delay you should be presented with a dialog telling you your Windows OS has been successfully activated for a 90 day trial.

## Rearming images
For Windows **7** images you *may* be able to extend the initial trial usage period once it has expired via the "rearm" process. Enter the following as an administrator from the command prompt:

```
C:\> slmgr /rearm
```

It is not possible to rearm the trial period of **Windows 8.1 or 10** images.


## References
- https://az792536.vo.msecnd.net/vms/release_notes_license_terms_8_1_15.pdf
- https://blog.reybango.com/2013/02/04/making-internet-explorer-testing-easier-with-new-ie-vms/
- API endpoint returning latest Microsoft Virtual Machine builds (thanks to [Antón Molleda](https://twitter.com/molant) for the tip):
	- https://developer.microsoft.com/en-us/microsoft-edge/api/tools/vms/
- Archived links
    - [Windows Vista](https://gist.github.com/zmwangx/e728c56f428bc703c6f6#gistcomment-3196040)
    - [IA Links](https://gist.github.com/zmwangx/e728c56f428bc703c6f6#gistcomment-3115797)
- [Original source (no longer maintained)](https://github.com/magnetikonline/linux-microsoft-ie-virtual-machines)
