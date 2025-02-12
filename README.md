# PomSeg: A Persistent Homology based tool for the segmentation of embryo membrane images
## Description
This is a 3D embryo membrane segmentation tool with persistent homology.

The 2D PH-based mask construction part is related to the following code, but this one is simpler.

https://github.com/TopologicalBird/Persistent_Homological_2D_Membrane_Enhancement

After the 2D mask construction, we use 3D PH to detect the centers of the cells.

Using these centers as markers, we can apply the watershed method for 3D segmentation.

The embryo image shown in this notebook was provided by Dr. Dimitri Fabrèges

used in the following article:

https://doi.org/10.1101/2023.01.24.525420

Joint work with Takafumi Ichikawa (Kyoto Univ.) & Yusuke Imoto (Kyoto Univ.)

## Method
### Preprocessing
First, we preprocess the image slice by slice using Ridge filter. This allows us to enhance the membrane parts.
### 2D persistent homology
We apply sublevel filtration persistent homology to the 2D slices.

We construct binary mask images for the cell region using the inverse analysis.
### 3D binary image construction
By piling up the 2D binary masks, we make a 3D binary image with cell parts being white.
### 3D persistent homology
We distance transform the 3D binary image and apply sublevel filtration persistent homology.

We choose relevant points in the diagram and retrieve the birth positions of them.
### Finalizing segmentation
We use watershed method with the birth positions above as markers to finalize the segmentation.

## Related Paper
For more detailed explanations, see the paper below.

PAPER LINK HERE!

## Persistent homology calculation
We use HomCloud for the persistent homology calculation. You can install it from the link below.

https://homcloud.dev/index.en.html
