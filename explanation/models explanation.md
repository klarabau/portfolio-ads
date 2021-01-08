Classification models</summary>

**Logistic regression** allows for classification into binary or multiple categories. It is based on linear regression models and uses a linear decision boundary. However, instead of linear regression models aiming to predict continuous values, logistic regression adds a logarithmic scale in order to predict categories instead([13][13]): h_θ (x)=logit(θ^T∙x).
A logistic regression model brings the advantage of being able to deal with continuous-level predictor variables, similarly to the generated scores being used as features in this project. ([14][14]) Therefore, especially multivariate logistic regression is relevant to this project, because even if the 10 classes we aim to predict (user scores ranging from 1 to 10) were to be collapsed, keeping a high number of classes leads to a more detailed distinction in the prediction of user scores, which is what we aim for.
![](img)

A **Decision Tree** aims to split the classes as purely as possible. It applies a sine curve with a set of “if-then-else” decision rules, which lead to a tree-like structure. The data is broken down into smaller subsets with each step.([15][15]) Decision trees are beneficial in a sense that they are able of interpreting the model and identifying important features, which again can be useful to the design of further research.([16][16]) Hence, a decision tree model can show a lot of potential for our project, especially for interpreting the data and recognizing important features to employ.
![](img)

**Random forest** is a so-called ensemble method which combines multiple decision tree models. Each decision tree is trained on a random subset of the training set with its own random subset of features, then it combines the outputs of the trees into a final output. Same as a decision tree, it can be helpful to transform the data into useful signals and find effective parameters. However, a random forest leverages the power of multiple decision trees and therefore, contrary to a single decision tree, does not depend on any specific set of features due to the random selection of such. This leads to a better generalization over the data, which is beneficial to our project to discourage overfitting, especially considering our rather small dataset. [17][17]
![](img)

A **multilayer perceptron** is a type of artificial neural network.[18][18] As most neural networks, it aims to mimic the neurological structure of a brain through multiple interconnected layers. The features in the input layer are fed forward and transformed in one or multiple hidden layers and then passed on to the output layer, where the hidden layers extract useful features, and the output layer classifies them (Figure 4). The connections between the layers apply weights to the features and are represented by a matrix.[19][19][20][20][21][21] Even though models like these are especially beneficial for pattern recognition tasks in images or audio, it also shows potential for this project’s purpose because of the automatic feature-extraction through the hidden layer(s). Specifically, a multilayer perceptron with one single hidden layer and 100 nodes could prove to be useful for our problem.
![](img)


[13]: https://www.ahajournals.org/doi/full/10.1161/CIRCULATIONAHA.106.682658 
[14]: https://www.jstor.org/stable/352104?casa_token=j7bD6ebNgZsAAAAA%3A8D4zjOCRVw6h12GyX3M9A7pQ96ulbCiGsDysxjJZ_lI5tQ7GQpHvcBzFYsGmrewaqSR2bnOOuLRZz2eMuU0iKY0m-EQBes-Zc5gNB-REHmP82-zf1g&seq=6#metadata_info_tab_contents
[15]: https://chiragsehra42.medium.com/decision-trees-explained-easily-28f23241248
[16]: https://onlinelibrary.wiley.com/doi/epdf/10.1002/cem.873
[17]: https://www.analyticsvidhya.com/blog/2020/05/decision-tree-vs-random-forest-algorithm/
[18]: https://www.researchgate.net/profile/Youssef_Ghanou2/publication/292996667_Multilayer_Perceptron_Architecture_Optimization_and_Training/links/58318a1208ae138f1c076f8a/Multilayer-Perceptron-Architecture-Optimization-and-Training.pdf
[19]: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.608.2530&rep=rep1&type=pdf
[20]: http://www.informatica.si/ojs-2.4.3/index.php/informatica/article/view/1595
[21]: https://www.biomedres.info/biomedical-research/analysis-of-multilayer-perceptron-machine-learning-approach-in-classifying-protein-secondary-structures.html