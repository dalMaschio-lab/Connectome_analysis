# A network-based method for extracting the organization of brain-wide circuits from reconstructed connectome datasets 

Notebooks for the analysis of the paper "A network-based method for extracting the organization of brain-wide circuits from reconstructed connectome datasets" [link](https://www.biorxiv.org/content/10.1101/2023.05.21.541471v1)

At the following [link](https://drive.google.com/drive/folders/1AsEaiju3l62fbwv-SrANfvTJyCqwd_4N?usp=sharing) are available the complete dataset modular structures to download and open in a web browser. 

### Folder *notebooks*
Consists of .ipynb jupyter notebooks containing python code for analyzing Connectome data of larval zebrafish atlas.<br />

At the following link [connectome_analysis](https://zenodo.org/records/15102704?preview=1&token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6IjliMGQyMDczLTExNTktNDQ2ZS05NmI0LWVhMWJhODQ0N2E0NSIsImRhdGEiOnt9LCJyYW5kb20iOiJiMTg1NjI1ZGNkMGMyYTk1NDVjNDQ3ZDkzMTg4NmMxYiJ9.CTW09V7S8EDh_v7JupktYH5-yJ6GpYNhumSfZee56R2hOezkIQtYMwsb2BxBBrIZm1x5X8A_KOzetTpDeziSlA) in the folder **zebrafish data & analysis.zip** there are following folders: 
1. mapzebrain - Aligned neurons dataset (here is the zebrafish light microscopy data)
2. mapzebrain - Aligned neurons dataset with strahler_lastcolumn
3. strhl_num_1_dataset
4. dendrites_axonTermials
5. community_detection

   
*strahler_number_and_threshold_distance.ipynb*<br />
Code for finding the strahler order of the endoints of each neuron(.swc file) present in folder **mapzebrain - Aligned neurons dataset** and finally saving the strahler number for each branch point of neuron in swc file **mapzebrain - Aligned neurons dataset with strahler_lastcolumn**. Computing the threshold to seperate the axon terminals and dendrites of each neuron. Storing the .swc data with unitary value of strahler number of each neuron seperately in the folder **strhl_num_1_dataset**. Storing the .swc data with info of axo terminal and dendrites of each neuron separately in the folder **dendrites_axonTermials**.  

*Directed_model.ipynb*<br />
Code for constructing assymetric adjacency matrix(or directed network) from larval zebrafish using .swc data from folder **dendrites_axonTermials** with proximity range 5um constraint for forming links between any 2 neurons. 

*Undirected_model.ipynb*<br />
Code for constructing symmetric adjacency matrix(or undirected network) from larval zebrafish .swc data from folder **strhl_num_1_dataset** with proximity range 5um for forming links between any 2 neurons.

*plot_GCnodes_vs_proximityRange.ipynb*<br />
Investigating how the fraction of Giant Connected component and No. of connected components varies when the connection parameter proximity range is varied. This is done for both Undirected and directed zebrafish network.

*undirected_directed_analysis.ipynb*<br />
Code for analysing the and computing the network properties for both undirected and directed network of larval zebrafish.

*Leiden_community_detection.ipynb*<br />
Code for finding the modules(or communities, averaged over 10^4 times) of either directed or undirected network of zebrafish using Leiden community detection algorithm. Here it is done only for directed network of zebrafish connectome as an example. The results can be found in folder **community_detection**.

*chord_plots.ipynb*<br />
R code for visualizing using chord plots, the modular structures of both directed and undirected communities of zebrafish. Also, visualising the relation of Leiden communities/modules of these networks with respect to preexisting anatomical regions of larval zebrafish.  


