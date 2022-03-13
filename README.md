# Applied Social Network Analysis Coursera
> Here lies my assignments for course [Applied Social Network Analysis in Python](https://www.coursera.org/learn/python-social-network-analysis).
> There were 4 assignments based on using Python and its libraries for Social Network Analysis.
> Numeration of assignments responds to numeration on Coursera.


## Table of Contents
* [Assignment 1](#assignment-1)
* [Assignment 2](#assignment-2)
* [Assignment 3](#assignment-3)
* [Assignment 4](#assignment-4)
* [List of used libraries](#list-of-used-libraries)
* [Used ML model](#used-ml-model)


## Assignment 1
This assignment is called ***Creating and Manipulating Graphs*** and is based on analysis of 2 datasets. First one stores 3 movies from each of 8 employees of small company that they would most enjoy watching for the upcoming company movie night, and second one has data on the relationships between different coworkers.

For this assignment I:
- Loaded in the bipartite graph from dataset with movie preferences.
- Added to that graph nodes attributes named `type`, which can be `movie` or `employee`.
- Found a weighted projection of previous graph which tells us how many movies different pairs of employees have in common.
- Found the Pearson correlation between employee relationship scores and the number of movies they have in common, which was ***0.788***, which showed that there is correlation between this 2 values.


## Assignment 2
This assignment is called ***Network Connectivity*** and based on analyzing an internal email communication network between employees of a mid-sized manufacturing company.

For this assignment I did basic analysis of given graph:
- searching number of nodes and edges.
- checking for strong and weak connection.
- searching for largest strongly connected component (**G_sc**).
- searching for average distance, diameter, periphery and center in **G_sc**.
- searching for transitivity and average clustering coefficient of undirected graph constructed using **G_sc**.


## Assignment 3
This assignment is about exploring different measures of centrality of network. It is divided in 2 parts.

### Part 1
In this part I searched for the best nodes in terms of degree centrality, closeness centrality, and normalized betweeness centrality in a network of friendships at a university department.

### Part 2
In this part I worked with a directed network of political blogs, where nodes correspond to a blog and edges correspond to links between blogs. Firstly I applied the Scaled Page Rank Algorithm and found 5 nodes with highest Page Rank. Next I applied the HITS Algorithm to find 5 nodes with highest hub scores and 5 nodes with highest authority scores
 
 
## Assignment 4
This assignment is divided in 2 parts.

### Part 1 - Random Graph Identification
For the first part of this assignment I analyzed randomly generated graphs and determined which algorithm created them. There were 3 options which algorithm was used:
- Preferential Attachment
- Small World with low probability of rewiring
- Small World with high probability of rewiring

For the analisis I checked distribution of node degrees and average clustering of graph.

### Part 2 - Company Emails
For the second part of this assignment, I used company's email network where each node corresponds to a person at the company, and each edge indicates that at least one email has been sent between two people.

For this part I had 2 subtasks.

#### Salary Prediction
For this task I identified the people in the network with missing values for the node attribute `ManagementSalary` and predicted whether or not these individuals are receiving a management position salary.

I did this using Random Forrest Classifier and adding additional data to DataFrame, such as:
- degree centrality
- closeness centrality 
- normalized betweeness centrality
- PageRank
- degree of each node

#### New Connections Prediction
For this task I identified the edges in [`future_connections`](https://github.com/Cybersheralt/Social-Network-Analysis-Coursera/blob/main/Assignment%204/Future_Connections.csv) with missing values and predicted whether or not these edges will have a future connection.

I did this using Random Forrest Classifier and adding additional data, such as:
- Preferential Attachment
- Jaccard coefficient
- Resource allocation index
- Adamic-Adar index
- Common neighbors


## List of used libraries
- Pandas
- NetworkX
- Numpy
- Scikit-learn
- pickle
- operator

## Used ML model
- Random Forrest Classifier
