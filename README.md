# Classification of enzymes using Graph Convolutional Networks

## Dataset Description - 

The dataset can be loaded using pytorch_geometric dataset class.  
The dataset contains the following files:  
1. ENZYMES  
_graph_  
indicators - column vector of graph identifiers for all nodes of all
graphs, the value in the i-th line is the graph_id of the node with node_id i  
2. ENZYMEZ_Graph_  
labels – class labels for all graphs in the dataset, the value in the
i-th line is the class label of the graph with graph_id i  
3. ENZYMES_A - sparse (block diagonal) adjacency matrix for all graphs, each line
corresponds to (row, col) resp. (node_id, node_id)  
4. ENZYMES_node_attributes - matrix of node attributes, the comma separated values
in the i-th line is the attribute vector of the node with node_id i  
5. Readme file

The number of data samples included in the dataset is 600.  
The label of this dataset is the 6 enzyme classes.  

## Problem Statement -

The dataset is being used to identify which class of enzyme a particular graph
belongs to.  

## Models -

GCN 1 Layer
GCN 2 Layers
GCN 3 Layers
GCN 4 Layers

## Dataset Preprocessing -

I have used the NormalizeFeatures transformation to normalize the feature
vectors.  
I have also used stratification while splitting the dataset to ensure there is no imbalance
in the proportion of classes in the training and test sets.   

## Training and Test Split -

I have split the dataset into 80% Train, 10% Validation and 10% Test sets.  

## Best Performed Models -

The GCN 4 Layer model with a Learning Rate of 0.001 performs the best out of all the models.
