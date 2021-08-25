# How to run the VM

1. If you don't have it already, download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. Download our VM file (entire directory VISSOFTArtifact [here](https://github.com/CelineDknp/VISSOFTArtifact))
3. Import the VM into your VirtualBox: Machine -> Add -> Navigate to our downloaded file -> Select "VISSOFTArtifact" -> Open
4. Select the VM and click "Start"
5. Log into Windows: the user is "VISSOFT" and its password is "VISSOFT2021"
>Note: our VM is configured to run using minimal ressources, just 4GB of RAM and 2 CPU cores. It is sufficient to run our tool, but feel free to change those settings in the "System" tab of the VM if you have a more powerful computer.


# How to run our tool
1. Launch the VF (cf above)
2. On the desktop, start "PharoLauncher"
3. Select the image "VISSOFT Artifact" and click on "Launch"
3. You should see an editor with three pieces of code, each doing something different. To run one piece of code, select it entirely with your mouse, then right click and select "Do it":
	- The fist four lines of code open three examples of our visualisation.
	- The next six lines show unfused version of one of the graph previously shown.
	- The last four lines of code open *all* graphs for every file in our data. Note that this is 57 graphs in 57 different windows. We advise to limit yourself to the examples above, but if you are curious and want to explore, we put all graphs at your disposal.

>Note: Since the data from Raincode and their client is confidential, in this image you will only find the *.dot* files needed as input for our tool, in an obfuscated version (real rule names have been replaced by Rule1, Rule2,...).


# Tool usage, reminder:
*For more details on usage, you can refer to the cheat sheet available in our GitHub.*

## Color meaning:
- Red (node or link): Present in V1 but not in V2 (removed)
- Green (node or link): Present in V2 but not in V1 (added)
- Orange (link only): Probability changed between V1 and V2 (meaning the change of this transition increased or decreased)
- White/light gray (node or link): No change
- Dark gray (node only): Fused node. Click it to see inside (opens another window)

If you want to change the layout of the graph, you can use the buttons in the upper left corner: HorizontalTree is the default, Tree is the same layout but vertically, and Force is a force-based layout. Alternatively, you can drag&drop every node in the graphs.