# ml_project_2025 - Root Node Prediction in Syntactic Dependency Trees
Repository for the 2025 Machine Learning project.

Analyzing the root word in a sentence can provide deeper insight not only into its construction and meaning, but to the language to which it belongs to as well. This project deals with a model that aims to be able to predict the root node of a sentence, regardless of the language in which it is written, by applying a set of centrality functions to the sentence. 

The trees in the data provided are syntactic dependency trees. This means that each sentence in the corpus is represented by a tree whose nodes are the sentence words and edges correspond to syntactic dependencies among those words. The running hypothesis is that the most important word in the sentence (the root word) corresponds to a central node within the tree, so we are going to use centrality scores as features to represent nodes.

<img width="1576" height="896" alt="Знімок екрана 2025-11-18 о 07 13 02" src="https://github.com/user-attachments/assets/a35e1407-6374-4dfe-8703-2aca98f6d459" />

In order to obtain a functional model we began by restructuring the dataset to be able to model the problem as one of classification. We applied different types of data exploration techniques, such as different types of plotting, to better understand the relationship between our inputs and the node value. Feature selection was applied to reduce the number of centrality functions from a wide array down to a smaller, more representative subsection. 

<img width="986" height="669" alt="centrality_ranking" src="https://github.com/user-attachments/assets/50680cda-bc48-4877-b32c-8bc38958135c" />

Finally, in the modelling section we started by applying a simple logistic regression algorithm and gradually improved, managing to obtain a max accuracy of 31.8\% with a random forest model. The best submission and score overall was achieved by using the per-language approach to training (0.36 as public and 0.39 as private score in Kaggle competition). We believe that this result is just the beginning and that different models could yield even better results, especially if they're trained for a particular language instead of a wide array.

The landing page for the competition can be found here: https://www.kaggle.com/competitions/ml-project-2024-2025/overview

