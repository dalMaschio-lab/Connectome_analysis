*drosophilia_network_analysis.ipynb*<br/>
uses the EM drosophilia directed edges data *traced-total-connections.csv* which can be obtained from [https://www.janelia.org/project-team/flyem/hemibrain](https://www.janelia.org/project-team/flyem/hemibrain) --> v1.2 release found in the page) or directly from [https://storage.cloud.google.com/hemibrain/v1.2/exported-traced-adjacencies-v1.2.tar.gz](https://storage.cloud.google.com/hemibrain/v1.2/exported-traced-adjacencies-v1.2.tar.gz). It outputs communities and sub-communities(communities within communities), results are saved in directory **EM_communities**.

The folder **EM_communities** consists of:
1. averageComm_drosophilia.csv - all nodes of EM drosophilia being assigned one of the 8 communities numbering 0 to 7.
2. averageSubComm(num)_drosophilia.csv - (num) corresponding to communities 0 to 7. Sub-modules corresponding each community are found and assigned for each of the 8 communities.
3. averageSubComm(num)_drosophilia folder - (num) corresponding to communities 0 to 7. In each folder, the csv files corresponding to each sub-modules are present. In each csv file *average_SS_Comm(num2).csv*, we have sub-sub-modules or modularity applied in depth of level 2, assigned to each neuron.

    
