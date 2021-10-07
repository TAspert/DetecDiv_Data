This repo contains all the file to recreate our DetecDiv timelapse plateform [biorxiv.org/content/10.1101/2021.10.05.463175v1]
1. CAD files to reproduce the microfluidic device
2. Scheme and components to reproduce the microscope
3. Micromanager scripts for high speed timelapse, notably fast focus

## Datasets & networks ## 
Besides, datasets and trained networks used in this paper are available at:

**Lifespan**: Data: doi.org/10.5281/zenodo.5552642 // Trained Network (CNN+LSTM): doi.org/10.5281/zenodo.5553862 

**Brightfield segmentation**: Data: doi.org/10.5281/zenodo.5553771 // Trained Network (Encoder-Decoder Deeplabv3+): doi.org/10.5281/zenodo.5553851

**Cell-cycle slowdown detection**: Data: doi.org/10.5281/zenodo.5553796 // Trained Network (LSTM): doi.org/10.5281/zenodo.5553829


------------------------------------------
3./
This script is attached to the MDA and performs autofocus on the first position of the position list, then apply the z-offset to the rest of the positions. Applies at each time point before the first channel. It is an efficient method if your loss of focus is homogeneous (example: thermal drift of the stage) to save time in your MDA routine.

How to use it: Set your MDA parameters using the GUI. DISABLE AUTOFOCUS. Set your autofocus method using the autofocus GUI Run the script.

You can change the parameters of the .attachRunnable(frame,position,channel,slide) to adapt it to your need
