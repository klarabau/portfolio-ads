# Personal Portfolio
Student name: Klara Baumeister  
Student number: 19029454  
Course: Applied Data Science minor  
Lecturers: Jeroen Vuurens, Tony Andrioli, Gerda in 't Veld, Ruud Vermeij, Brian de Keijzer


## Research project

### Task definition
This portfolio summarizes my individual work and effort for the Nano project of the Applied Data Science minor at The Hague University.

In the Nano project we aim to find a solution for VSParticle, a company that derived from TU Delft's nanotech group. Their work focuses on nanoparticles and, among others, they analyze nanoparticle images to calculate the particle’s sizes. To do this, VSParticle has built an image processing program that results in an edited image which enables the software to calculate the particle’s sizes. Part of the image processing is the thresholding step, where greyscale images are converted into bitmaps using thresholding algorithms and user input. This step distinctly separates the nanoparticles from the background. In combination with our minor, our goal is to automate this step using a Machine Learning model which predicts the best algorithm to use. Our research question reads as follows:
	
> <b> How can a Machine Learning model, that predicts the optimal thresholding algorithm, assist VSParticle to analyze nanoparticle images? </b>
		
To answer our research question in detail, we are going to focus on the following four sub-questions:

1. How does the given data need to be restructured in order to be useful for the model?
2. What features of the dataset should be selected for the model?
3. What type of model do we need and how is it structured?
4. How can the predictions of the model, graded by VSParticle’s user, be employed to improve the model over time?

### Evaluation
In order to achieve our goal, we received a json file from VSParticle containing IDs of each run, parameters of the run, metadata of the image, resulting images of each step, and scores. The scores were our main point of focus: they contain computer generated values that describe the image and evaluate how well each step of the program worked. The json file also included a user score, given manually by the user at the end of each run of the program. Both these scores were intended to be the input features for our thresholding algorithm prediction. However, early on, we had a change of approach: Instead of predicting the thresholding algorithm with the features **and** the user score, we focused on predicting the user score **with** the features. Then we could select the thresholding algorithm that scored the highest user score. Therefore we planned to create one model for each threshold method, with each model predicting the user score the threshold method would give.

### Conclusions
Discuss the results, answer the research question etc. 

### Planning
To make our group work as efficient and agile as possible, we used Scrum. We planned sprint periods of two weeks, including daily standups and retrospectives at the end of each sprint. In order to get an overview of everybody's work progress, we used the platform Jira to create a Scrumboard. All of our completed issues from the sprints can be found [here](https://vsparticle-nano.atlassian.net/jira/software/c/projects/NANO/issues).


## Courses
### DataCamp 
All of the mandatory courses on DataCamp have been fully completed by me, as well as an assigned course on Deep Learning. My DataCamp profile can be found [here.](https://www.datacamp.com/profile/19029454) Please see the content and statement of accomplishement of each course below.

Mandatory courses:
- Introduction to Python: [course description](https://learn.datacamp.com/courses/intro-to-python-for-data-science) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/731540b605e1dea88d26eafaf85f69099951552b)  
- Intermediate Python: [course description](https://learn.datacamp.com/courses/intermediate-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/5a19587a42524b169ec6c005b6dbba22bb3b1432) 
- Python Data Science Toolbox (Part 1): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-1) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/fffeaeabc04f0f84a0f01d5167b83d860a9ef8d7) 
- Python Data Science Toolbox (Part 2): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-2) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/d748c33f42adbbcfb49f67218196f86a97241379) 
- pandas Foundations: [course description](https://learn.datacamp.com/courses/pandas-foundations) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/3ae4299c06df02db4e40704f86613677f7d6e533) 
- Introduction to Data Visualization in Python: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/eb5ac6e59e25bd4890da76504e63230b789abc1b) 
- Manipulating DataFrames with pandas: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/8179c495982e57ac13a8f41416e31c31ef3d4c82) 
- Data Types for Data Science in Python: [course description](https://learn.datacamp.com/courses/data-types-for-data-science-in-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/901955f550ac5650e92ba6dd3d86388b7d3d74ac) 
- Cleaning Data in Python: [course description](https://learn.datacamp.com/courses/cleaning-data-in-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/90c108643c9ea6f31fae869f06be0be6426c456b) 
- Preprocessing for Machine Learning in Python: [course description](https://learn.datacamp.com/courses/preprocessing-for-machine-learning-in-python) | [statement of accomplishment]() 

Not mandatory courses:
- Introduction to Deep Learning with PyTorch: [course description](https://learn.datacamp.com/courses/introduction-to-deep-learning-with-pytorch) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/f4347d080bf8639635aaf765733df2ca7977c667) 



## Domain Knowledge 

### Introduction to the subject field
<i> Write introduction to the subject field with literature references </i>

### Literature research
To see where I informed myself about the topic and what information I gathered, please expand the sections below.

<details><summary>Nanoparticles</summary>

Nanoparticles are particles ranging from one single atom to atomic clusters or bulk crystals of 100nm or less ([Wikipedia][1], [Nanoparticle][12]). They have proved to be of high significance in various fields of work, such as medicine, engineering and chemistry, for products like quantum computers, chemical sensors and photochemical devices such as flat panel displays, among others ([Analysis of Nanoparticle Transmission Electron Microscopy Data...][7], [Nanoparticle][12]).
	
For analysation and documentation, microscopic images of the particles are often saved and used for further research. There are two ways of making the particles visible to the human eye: SEM and TEM. SEM, short for Scanning Electron Microscope, produces images of a sample by scanning the surface with a focused beam of electrons. The electron beam is then scanned in a raster scan pattern, and the position of the beam is combined with the intensity of the detected signal to produce an image ([Wikipedia][2]). TEM, which stands for  Transmission Electron Microscopy, forms an image by transmitting a beam of electrons through a specimen. The specimen is most often an ultrathin section less than 100nm thick, or a suspension on a grid ([Electron Microscopy Techniques ...][9]).
</details>

<details><summary>Thresholding</summary>

Thresholding is differenciated into global and local thresholding methods. Global thresholding focuses on the image histogram, analyzing its peaks, valleys and curves, while local thresholding computes a threshold for each pixel and turns it either black or white ([ImageJ][4]).

Algorithms used in thresholding can be saved for repeated use as thresholding methods. Most methods use image intensity li, j to determine whether a pixel turns white or black. If li, j is smaller than a fixed constant T, the pixel turns black ([Wikipedia][5]). There are multiple methods that have been proved to be very efficient, for example Otsu([A Threshold Selection Method from Gray-Level Histograms][10]), Yen([A new criterion for automatic multilevel thresholding.][11]) and many more([ImageJ][4]).
</details>

<details><summary>Image processing with nanoparticles</summary>
	
F. Li et al. used a multiple thresholding method to classify nanoparticle images into three types: bright, dark and background. This helped them achieve pixel classification and shows that the thresholding step is very important when working with nanoparticle images ([High content image analysis...][6]). 
</details>

<details><summary>VSParticle</summary>
	
VSParticle, a company based in Delft, has conducted a lot of research in the field of nanoparticles over the past years. Calculating the size of nanoparticles using microscopic images is one branch they focus their work on. ([VSParticle][8]). 
</details>

<details><summary>Classification models</summary>

**Logistic regression** allows for classification into binary or multiple categories. It is based on linear regression models and uses a linear decision boundary. However, instead of linear regression models aiming to predict continuous values, logistic regression adds a logarithmic scale in order to predict categories instead([13][]): h_θ (x)=logit(θ^T∙x).
A logistic regression model brings the advantage of being able to deal with continuous-level predictor variables, similarly to the generated scores being used as features in this project. ([14][]) Therefore, especially multivariate logistic regression is relevant to this project, because even if the 10 classes we aim to predict (user scores ranging from 1 to 10) were to be collapsed, keeping a high number of classes leads to a more detailed distinction in the prediction of user scores, which is what we aim for.
![](img)

A **Decision Tree** aims to split the classes as purely as possible. It applies a sine curve with a set of “if-then-else” decision rules, which lead to a tree-like structure. The data is broken down into smaller subsets with each step.([15][]) Decision trees are beneficial in a sense that they are able of interpreting the model and identifying important features, which again can be useful to the design of further research.([16][]) Hence, a decision tree model can show a lot of potential for our project, especially for interpreting the data and recognizing important features to employ.
![](img)

**Random forest** is a so-called ensemble method which combines multiple decision tree models. Each decision tree is trained on a random subset of the training set with its own random subset of features, then it combines the outputs of the trees into a final output. Same as a decision tree, it can be helpful to transform the data into useful signals and find effective parameters. However, a random forest leverages the power of multiple decision trees and therefore, contrary to a single decision tree, does not depend on any specific set of features due to the random selection of such. This leads to a better generalization over the data, which is beneficial to our project to discourage overfitting, especially considering our rather small dataset. [17][]
![](img)

A **multilayer perceptron** is a type of artificial neural network.[18][] As most neural networks, it aims to mimic the neurological structure of a brain through multiple interconnected layers. The features in the input layer are fed forward and transformed in one or multiple hidden layers and then passed on to the output layer, where the hidden layers extract useful features, and the output layer classifies them (Figure 4). The connections between the layers apply weights to the features and are represented by a matrix.[19][][20][][21][] Even though models like these are especially beneficial for pattern recognition tasks in images or audio, it also shows potential for this project’s purpose because of the automatic feature-extraction through the hidden layer(s). Specifically, a multilayer perceptron with one single hidden layer and 100 nodes could prove to be useful for our problem.
![](img)

</details>

[1]: https://en.wikipedia.org/wiki/Nanoparticle
[2]: https://en.wikipedia.org/wiki/Transmission_electron_microscopy
[3]: https://en.wikipedia.org/wiki/Scanning_electron_microscope
[4]: https://imagej.net/Auto_Threshold
[5]: https://en.wikipedia.org/wiki/Thresholding_(image_processing)
[8]: https://vsparticle.com/ 

[6]: https://link.springer.com/article/10.1186/1472-6750-7-66 
[7]: https://journals.tubitak.gov.tr/chem/issues/kim-06-30-1/kim-30-1-1-0508-1.pdf 
[9]: https://www.sciencedirect.com/science/article/pii/B9780323299602000095 
[10]: https://ieeexplore.ieee.org/document/4310076?arnumber=4310076 
[11]: https://ieeexplore.ieee.org/document/366472?arnumber=366472 
[12]: https://www.britannica.com/science/nanoparticle 

[13]: https://www.ahajournals.org/doi/full/10.1161/CIRCULATIONAHA.106.682658 
[14]: https://www.jstor.org/stable/352104?casa_token=j7bD6ebNgZsAAAAA%3A8D4zjOCRVw6h12GyX3M9A7pQ96ulbCiGsDysxjJZ_lI5tQ7GQpHvcBzFYsGmrewaqSR2bnOOuLRZz2eMuU0iKY0m-EQBes-Zc5gNB-REHmP82-zf1g&seq=6#metadata_info_tab_contents
[15]: https://chiragsehra42.medium.com/decision-trees-explained-easily-28f23241248
[16]: https://onlinelibrary.wiley.com/doi/epdf/10.1002/cem.873
[17]: https://www.analyticsvidhya.com/blog/2020/05/decision-tree-vs-random-forest-algorithm/
[18]: https://www.researchgate.net/profile/Youssef_Ghanou2/publication/292996667_Multilayer_Perceptron_Architecture_Optimization_and_Training/links/58318a1208ae138f1c076f8a/Multilayer-Perceptron-Architecture-Optimization-and-Training.pdf
[19]: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.608.2530&rep=rep1&type=pdf
[20]: http://www.informatica.si/ojs-2.4.3/index.php/informatica/article/view/1595
[21]: https://www.biomedres.info/biomedical-research/analysis-of-multilayer-perceptron-machine-learning-approach-in-classifying-protein-secondary-structures.html


### Terminology
Used jargon in the field of nanoparticles and VSParticle's software is listed here:
- Thresholding: method for turning a grayscale / colored images into binary images
- Run: an image being processed once in each step of the software
- ...

My research notes on the thresholding algorithms used by VSParticle can be found [here](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Thresholding%20algorithms.ipynb).


## Most relevant contributions
- filler

## List of all of my notebooks 
For a complete list of all notebooks I created during the project, please expand the sections below.

#### Data explanation
- [Explanation of original json dataset](https://github.com/klarabau/portfolio-ads/blob/main/explanation/data%20explanation.md) 

#### Data preparation 
- [Random Oversampling (manually)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Random%20Oversampling%20Manually.ipynb)
- [N-Fold cross validation](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/k-fold%20cross%20validation.ipynb)

#### Data visualization 
- [Experiment: Feature combinations visualization](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Experiment%20feature%20visualization.ipynb)
- [Experiment: Feature analysation](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Experiment%20feature%20analysis.ipynb)

#### Machine Learning models 
- [Linear/Polynomial Regression model: count vs. user score (full dataset)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20count%20vs%20user%20score.ipynb)
- [Linear/Polynomial Regression model: count vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20count%20vs%20user%20score%20(only%20yen).ipynb) 
- [Linear/Polynomial Regression model: separation vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20separation%20vs%20user%20score%20(only%20yen).ipynb) 
- [Linear/Polynomial Regression model: separation, border vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20separation%20and%20border%20vs%20user%20score%20(only%20yen).ipynb) 
- [Multiclass Logistic Regression model: feature comparison (yen, with help from Yoran)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Multiclass%20logistic%20regression%20feature%20combinations.ipynb)
- [Multiclass Logistic Regression model: separation, intensity, count (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Multiclass%20logistic%20regression.ipynb)
- [Logistic and Polynomial Regression models: Test set comparison](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Logistic%20%26%20Polynomial%20regression%20(compared%20to%20ground%20truth).ipynb)
- [Polynomial Regression example](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Polynomial%20Regression%20example.ipynb)
- [Polynomial Regression experiment](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Polynomial%20Regression%20experiment.ipynb)

#### Contributions to group code 
- [Experiment: Random Oversampling function](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Random%20Oversampling%20Function%20for%20experiment.ipynb)
- [Final model: Confusion matrix]()


## Communication 
### Presentations
- [In week 2](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week2%20internal.pdf): Internal presentation, created and presented by me 
- [In week 3](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week3%20internal.pdf): Internal presentation, created and presented by me 
- [In week 4](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week4%20external.pdf): External presentation, created and presented by Yoran and me
- [In week 8](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week8%20internal.pdf): Internal presentation, created and presented by me
- [In week 11](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week11%20internal.pdf): Internal presentation, created and presented by me
- [In week 14](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week14%20internal.pdf): Internal presentation, created and presented by me
- [In week 15](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week15%20internal.pdf): Internal presentation, created and presented by me
- [In week 16](https://github.com/klarabau/portfolio-ads/blob/main/presentations/week16%20internal.pdf): Internal presentation, created and presented by me


### Research Plan
My contributions to the research paper have been broadly spread out and significant. My contributions ranged from writing detailed chapters like the introduction and individual sub-question descriptions, to general layout. The research plan can be found [here](https://github.com/klarabau/portfolio-ads/blob/main/research%20plan/research%20plan.pdf).

The following contents of the research plan have been made by me:
- Introduction
- Formulation of the research question 
- Formulation of sub-questions (with Oscar)
- Elaboration on sub-questions two, three and four 
- Minor changes in the elaboration of sub-question 4, as we changed our approach after group members left

### Research Paper
My contributions to the research paper have been... The research paper can be found [here]().

The following contributions to the research paper have been fully made by me:
- Creation of file and structure
- Abstract
- Introduction
- Chapter 2.4: Model comparison
- Chapter 2.5: Balancing methods
- Chapter 2.6.2: Evaluation metrics

The following contributions to the research paper have been partly made by me:

Furthermore, the references 1-10 have been found and researched by me.


### Other efforts
Throughout the whole project, I kept notes of each meeting in order to keep record of them for possible questions later on. 

Of course, I also kept my part of the Jira board up to date and documented my work there for an easy overview and communication with my group members.


## Diganostics of the learning process
Our project group definitely learned how important it is to review and check other group member's work, as we realized a couple of weeks into the minor that the csv file we had been working with contained faulty values. Midway through the project the same thing happened and we noticed our assumptions about the dataset were not correct. We could have avoided this by reviewing each others code more in depth before working with the files. However, luckily the changes from the corrupted values were not too high so that the first interpretations we got were not heavily misleading. After updating our old models, which went fairly quick as we simply needed to change the file that the notebook was reading, we could continue where we left off. 

Additionally, we should have cross-validated earlier on early models and experiments, not just the last one. We decided to focus on the models first but it turned out that not cross-validating from the beginning deferred our interpretations on the data. Luckily, we kept our options open until the final experiment in which we cross-validated our data, so we could re-interpret the data rather easily. cuz the conclusions we drew were all on the experiment , which was cross validated , we didn't need to rerun old ones. but also the results were giving us higher hopes than we actually had in the end as results so we started looking into polynomial regression again, which we couldve done earlier if we cross-validated earlier.

...


## Evaluation using STARR
As a User Experience Design student, I have only had short experiences with coding and programming so far. In order to extend them and learn more about statistics and data visualization, I chose this minor.

As I have not had much background knowledge on the topic, the minor started with a lot of new information to take in. It was difficult for me to get an idea of how to start. I quickly realised that even though I was not sure about things, I had to just do them in order to improve and learn. This also mainly reflected from the 360 degree feedback given to me, so I quickly stopped shying away from coding and since then, my understanding of how data science works and how to approach it grew constantly. 

...






