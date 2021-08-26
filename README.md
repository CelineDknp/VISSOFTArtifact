# What does the artifact do ?

This artifact is contained in a Windows VM. On the VM is installed PharoLauncher, a tool that will allow you to launch a pre-installed Pharo image containing our tool as well as all data needed to reproduce the experiment described in our paper. You'll simply have to run the Pharo VM and execute the code that is pre-loaded in it.

# Where can I find the VM ?

The VM is available on Zenodo in open access, at [this link](https://zenodo.org/record/5266434). Simply download the file, unzip it, and load it into VirtualBox. For more detail on the installation process, see our `INSTALL.md` file.

# How to reproduce the results found in the paper ?

First, import our VM into VirtualBox, start it and log into Windows as described in `INSTALL.md` (User: VISSOFT; Password: VISSOFT2021). When you are in, the steps are:

1. Start PharoLauncher from the icon on the desktop
2. Select the image "VISSOFT Artifact" and click on "Launch" (small green arrow in the top menu, all the way left)
3. You should see an editor *Playgroud* in Pharo, whith three pieces of code.
4. Highlight the first 4 lines of code, right click and choose "Do it".
5. What you see is the first view that we presented to the engineers: a Summary window with details on rules added or removed on the entire migration, along with three example graphs.
6. Highlight the next block of 6 lines of code, right click and choose "Do it" again.
7. What you see is the unfused version of the previously shown "PRCP223.COB" graph. This was used in our validation to confirm that our merging algorithm is an improvement over the unfused graphs.

If you wish to see the graph used for Figures 4 and 7 of our paper, you can run the following code for the fused version (Fig. 7):
```
var1 := LogDiffer with: 'FullData2/OFCB376.COB/OFCB376.COB.v1.dot' and: 'FullData2/OFCB376.COB/OFCB376.COB.v2.dot'.
var1 createGraphDiff.
var1 createFused. 
var1 postProcess.
var2 := DiffDrawer with: var1.
(var2 drawAndColapse: RSCanvas new) open.
```
And this one for the unfused Fig. 4:
```
var1 := LogDiffer with: 'FullData2/OFCB376.COB/OFCB376.COB.v1.dot' and: 'FullData2/OFCB376.COB/OFCB376.COB.v2.dot'.
var1 createGraphDiff. 
var1 postProcess.
var2 := DiffDrawer with: var1.
(var2 drawIndividual: RSCanvas new) open.
```
>Note: Since the data from Raincode and their client is confidential, in this image you will only find the *.dot* files needed as input for our tool, in an obfuscated version (real rule names have been replaced by Rule1, Rule2,...). Therefore, the image you get will differ slightly from what you see in the paper.

Finally, if you want to explore further and see graphs that were not shown to the engineers or in our paper, you can either: 
- Take the above two pieces of code and replace the filenames ("OFCB376.COB" in the example) by other names that you can find in the "FullData" folder (shortcut available on the desktop for ease of use). A worthy mention would be the file "PRCP905.COB" that, in its fused version, produces a single fused node (outlier mentionned in our metrics)
- Highlight and execute the last 4 lines of code to open *all* available graphs and explore them all. Note that this is 57 graphs in 57 different windows. While it runs in a few seconds only, it is fairly overwhelming and not the intended use of the tool. We advise to limit yourself to the examples above, but provide these lines for easy access.

# Tool usage, reminder:
*For more details on usage, you can refer to the cheat sheet available in our GitHub.*

## Color meaning:
- Red (node or link): Present in V1 but not in V2 (removed)
- Green (node or link): Present in V2 but not in V1 (added)
- Orange (link only): Probability changed between V1 and V2 (meaning the change of this transition increased or decreased)
- White/light gray (node or link): No change
- Dark gray (node only): Fused node. Click it to see inside (opens another window)

If you want to change the layout of the graph, you can use the buttons in the upper left corner: HorizontalTree is the default, Tree is the same layout but vertically, and Force is a force-based layout. Alternatively, you can drag&drop every node in the graphs.