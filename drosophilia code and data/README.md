*drosophilia_network_analysis.ipynb*<br/>
uses the EM drosophilia directed edges data *traced-total-connections.csv* which can be obtained from [https://www.janelia.org/project-team/flyem/hemibrain](https://www.janelia.org/project-team/flyem/hemibrain) --> v1.2 release found in the page) or directly from [https://storage.cloud.google.com/hemibrain/v1.2/exported-traced-adjacencies-v1.2.tar.gz](https://storage.cloud.google.com/hemibrain/v1.2/exported-traced-adjacencies-v1.2.tar.gz). It outputs communities and sub-communities(communities within communities), results are saved in directory **EM_communities**.

The folder **EM_communities** consists of:
1. averageComm_drosophilia.csv - all nodes of EM drosophilia being assigned one of the 8 communities numbering 0 to 7.
2. averageSubComm(num)_drosophilia.csv - (num) corresponding to communities 0 to 7. Sub-modules corresponding each community are found and assigned for each of the 8 communities.
3. averageSubComm(num)_drosophilia folder - (num) corresponding to communities 0 to 7. In each folder, the csv files corresponding to each sub-modules are present. In each csv file *average_SS_Comm(num2).csv*, we have sub-sub-modules or modularity applied in depth of level 2, assigned to each neuron.

                                                                                                


*janelia_subnetworks_reconstruction.ipynb*<br/>
In this jupyter notebook, neuromorphological data of each neuron is downloaded in .swc format using [NAVIS](https://navis-org.github.io/navis/) python library and grouped according to communities obtained from EM drosophilia. This jupyter notebook contains code to download swc information of neurons, compute strahler order of neurites/branch points of neuron, compute threshold distance to classify axon terminals and dendrites, using proximity range 1um and 5um reconstruct network using proposed methodology. Finally we apply leiden community detection algorithm to capture the modules within each reconstructed (sub-)networks. 

All the resulting data can be found in folder **zebrafish data & analysis.zip** at  [Connectome_analysis](https://zenodo.org/records/15102704?preview=1&token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6IjliMGQyMDczLTExNTktNDQ2ZS05NmI0LWVhMWJhODQ0N2E0NSIsImRhdGEiOnt9LCJyYW5kb20iOiJiMTg1NjI1ZGNkMGMyYTk1NDVjNDQ3ZDkzMTg4NmMxYiJ9.CTW09V7S8EDh_v7JupktYH5-yJ6GpYNhumSfZee56R2hOezkIQtYMwsb2BxBBrIZm1x5X8A_KOzetTpDeziSlA) . All results are stored under the folders *janelia_Comm(num)* where (num) corresponding to node modules/communities numbering from 0 to 7. 

Each folder **janelia_Comm(num)** consists of:
1. neu_attrJanelia.csv - csv file consisting of attribute information of each neuron
2. **swc** - consists of swc files corresponding to each neuron where spatial coordinates of each branch point of a single neuron are stored.
3. **janelia dataset with strahler lastcolumn** - consists of swc files same as in folder **swc** but with strahler number assigned to each branch point.
4. neu_attrJanelia_updated.csv - same as neu_attrJanelia.csv but with entries of last column being threshold distance(distance value that divides axon terminals and dendrites based on distance distribution with soma) computed for each neuron.
5. network_1.0um.txt, network_5.0um.txt - network reconstructed using our proposed methodology with proximity ranges 1 um and 5 um respectively.
6. SubComm(num)_reconstructed_1.0um.csv, SubComm(num)_reconstructed_5.0um.csv - these files contains modules obtained by applying leiden community detection algorithm to reconstructed networks network_1.0um.txt, network_5.0um.txt respectively.

