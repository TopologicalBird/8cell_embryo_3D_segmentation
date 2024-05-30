# 8cell_embryo_3D_segmentation
3D embryo membrane segmentation with PH

This notebook shows a method to segment embryo membrane images using persistent homology (PH).

The 2D PH-based mask construction part is related to the following code, but this one is simpler.

https://github.com/TopologicalBird/Persistent_Homological_2D_Membrane_Enhancement

After the 2D mask construction, we use 3D PH to detect the centers of the cells.

Using these centers as markers, we can apply the watershed method for 3D segmentation.

The embryo image shown in this notebook was provided by Dr. Dimitri Fabrèges

used in the following article:

https://doi.org/10.1101/2023.01.24.525420

Joint work with Takafumi Ichikawa (Kyoto Univ.) & Yusuke Imoto (Kyoto Univ.)

