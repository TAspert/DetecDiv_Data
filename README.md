This repo contains all the file to recreate our DetecDiv timelapse plateform [biorxiv.org/content/10.1101/2021.10.05.463175v1]
1. CAD files to reproduce the microfluidic device
2. Scheme and components to reproduce the microscope
3. Micromanager scripts for high speed timelapse, notably fast focus

4. Besides, it also contains the Zenodo links to the datasets and networks used in the manuscript. (Datasets_Networks.md)


------------------------------------------
3./
This script is attached to the MDA and performs autofocus on the first position of the position list, then apply the z-offset to the rest of the positions. Applies at each time point before the first channel. It is an efficient method if your loss of focus is homogeneous (example: thermal drift of the stage) to save time in your MDA routine.

How to use it: Set your MDA parameters using the GUI. DISABLE AUTOFOCUS. Set your autofocus method using the autofocus GUI Run the script.

You can change the parameters of the .attachRunnable(frame,position,channel,slide) to adapt it to your need
