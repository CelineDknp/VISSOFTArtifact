# Install

## Step 1: Get the VM running
1. If you don't have it already or have an older version, download [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (! You need version 6.1, or the image will not run !)
2. Download our VM files [here](https://zenodo.org/record/5266434)
3. Unzip the files (somewhere easy to find)
4. Import the VM into your VirtualBox: Machine -> Add -> Navigate to our downloaded file -> Select the "VISSOFTArtifact.vbox" -> Open
5. Select the VM and click "Start"
6. Log into Windows: the user is "VISSOFT" and its password is "VISSOFT2021"
>Note: our VM is configured to run using minimal ressources, just 4GB of RAM and 2 CPU cores. It is sufficient to run our tool, but feel free to change those settings in the "System" tab of the VM if you have a more powerful computer.

>If you are using MacOS, and a fresh install of VirtualBox, you might run on some issue when launching the VM. A restart is often required, see [this page](https://www.howtogeek.com/658047/how-to-fix-virtualboxs-%E2%80%9Ckernel-driver-not-installed-rc-1908-error/) for more details.

## Step 2: Basic usage

When you log into the VISSOFT account in the VM, you should arrive on the Desktop. Two shortcuts are available: PharoLauncher and a pointer to the "FullData" folder. 

1. Start PharoLauncher
2. Select the image "VISSOFT Artifact" and click on "Launch" (small green arrow in the top menu, all the way left)
3. You should see an editor *Playgroud* in Pharo, whith three pieces of code. 
4. To confirm everything is working, highlight the first 4 lines of code, right click and select "Do it".
5. Expected behaviour is opening 4 windows: 
	- Summary (containing only text)
	- OFCB982.COB a graph represention of the diff, with a fairly high amount of nodes
	- ALCP577.COB graph of another diff with a moderate amount of nodes
	- PRCP223.COB graph of a third diff with a small amount of nodes
