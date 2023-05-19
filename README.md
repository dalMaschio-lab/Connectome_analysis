# Connectome_analysis


At the following [link](https://drive.google.com/drive/folders/1AsEaiju3l62fbwv-SrANfvTJyCqwd_4N?usp=sharing) are available the complete dataset modular structures. 

### Folder *notebooks*
Consists of .ipynb jupyter notebooks containing python code for analyzing Connectome data of larval zebrafish atlas as well as EM drosophilia<br />

*strahler_number_and_threshold_distance.ipynb*<br />
Code for finding the strahler order of the endoints of each neuron(.swc file). Computing the threshold to seperate the axon terminals and dendrites of each neuron. Storing the .swc data with unitary value of strahler number of each neuron seperately. Storing the .swc data with info of axo terminal and dendrites of eachg neuron separately.  

*Directed_model.ipynb*<br />
Code for constructing assymetric adjacency matrix(or directed network) from larval zebrafish .swc data with proximity range 5um constraint for forming links between any 2 neurons. 

*Undirected_model.ipynb*<br />
Code for constructing symmetric adjacency matrix(or undirected network) from larval zebrafish .swc data with proximity range 5um for forming links between any 2 neurons.

*plot_GCnodes_vs_proximityRange.ipynb*<br />
Investigating how the fraction of Giant Connected component and No. of connected components varies when the connection parameter proximity range is varied. This is done for both Undirected and directed zebrafish network.

*undirected_directed_analysis.ipynb*<br />
Code for analysing the and computing the network properties for both undirected and directed network of larval zebrafish.

*Leiden_community_detection.ipynb*<br />
Code for finding the modules(or communities, averaged over 10^4 times) of either directed or undirected network of zebrafish using Leiden community detection algorithm. Here it is done only for directed network of zebrafish connectome as an example.

*chord_plots.ipynb*<br />
R code for visualizing using chord plots, the modular structures of both directed and undirected communities of zebrafish. Also, visualising the relation of Leiden communities/modules of these networks with respect to preexisting anatomical regions of larval zebrafish.  


