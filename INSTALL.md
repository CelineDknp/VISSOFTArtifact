# Install

## Step 1: Get the VM running
1. If you don't have it already, download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. Download our VM files [here](https://github.com/CelineDknp/VISSOFTArtifact)
3. Unzip the files (somewhere easy to find)
4. Import the VM into your VirtualBox: Machine -> Add -> Navigate to our downloaded file -> Select the "VISSOFTArtifact.vbox" -> Open
5. Select the VM and click "Start"
6. Log into Windows: the user is "VISSOFT" and its password is "VISSOFT2021"
>Note: our VM is configured to run using minimal ressources, just 4GB of RAM and 2 CPU cores. It is sufficient to run our tool, but feel free to change those settings in the "System" tab of the VM if you have a more powerful computer.

## Step 2: Basic usage

When you log into the VISSOFT account in the VM, you should arrive on the Desktop. Two shortcuts are available: PharoLauncher and a pointer to the "FullData" folder. 

1. Start PharoLauncher
2. Select the image "VISSOFT Artifact" and click on "Launch" (small green arrow in the top menu, all the way left)
3. You should see an editor *Playgroud* in Pharo, whith three pieces of code. 
4. To confirm everything is working, highlight the first 4 lines of code, right click and select "Do it".
5. Expected behaviour is opening 4 windows: 
	- Summary (containing only text)
	- OFCB982.COB
	- ALCP577.COB
	- PRCP223.COB