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
In order to achieve our goal, we received a json file from VSParticle containing IDs of each run, parameters of the run, metadata of the image, resulting images of each step, and scores. The scores were our point of focus: they contain computer generated values that describe the image and evaluate how well each step of the program worked. The json file also included a user score, given manually by the user at the end of each run of the program. Both these scores were intended to be the input features for our thresholding algorithm prediction. However, early on, we had a change of approach: Instead of predicting the thresholding algorithm with input features like the user score, we focused on predicting the user score with other features. Then we could select the thresholding algorithm that scored the highest user score. Therefore we planned to create one model for each threshold method, with each model predicting the user score the threshold method would give.

### Conclusions
Discuss the results, answer the research question etc. 

### Planning
To make our group work as efficient and agile as possible, we used Scrum. We planned sprint periods of two weeks, including daily standups and retrospectives at the end of each sprint. In order to get an overview of everybody's work progress, we used the platform Jira to create a Scrumboard. All of our completed issues from the sprints can be found [here](https://vsparticle-nano.atlassian.net/jira/software/c/projects/NANO/issues).


## Courses
### DataCamp 
All of the assigned courses on DataCamp have been fully completed by me. My DataCamp profile can be found [here.](https://www.datacamp.com/profile/19029454)

Please see the content and statement of accomplishement of each course here:
- Introduction to Python: [course description](https://learn.datacamp.com/courses/intro-to-python-for-data-science), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/731540b605e1dea88d26eafaf85f69099951552b)  
- Intermediate Python: [course description](https://learn.datacamp.com/courses/intermediate-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/5a19587a42524b169ec6c005b6dbba22bb3b1432) 
- Python Data Science Toolbox (Part 1): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-1), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/fffeaeabc04f0f84a0f01d5167b83d860a9ef8d7) 
- Python Data Science Toolbox (Part 2): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-2), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/d748c33f42adbbcfb49f67218196f86a97241379) 
- pandas Foundations: [course description](https://learn.datacamp.com/courses/pandas-foundations), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/3ae4299c06df02db4e40704f86613677f7d6e533) 
- Introduction to Data Visualization in Python: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/eb5ac6e59e25bd4890da76504e63230b789abc1b) 
- Manipulating DataFrames with pandas: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/8179c495982e57ac13a8f41416e31c31ef3d4c82) 
- Data Types for Data Science in Python: [course description](https://learn.datacamp.com/courses/data-types-for-data-science-in-python), [statement of accomplishment]() 
- Cleaning Data in Python: [course description](https://learn.datacamp.com/courses/cleaning-data-in-python), [statement of accomplishment]() 
- Preprocessing for Machine Learning in Python: [course description](https://learn.datacamp.com/courses/preprocessing-for-machine-learning-in-python), [statement of accomplishment]() 
- Merging DataFrames with pandas: [course description](https://learn.datacamp.com/courses/merging-dataframes-with-pandas), [statement of accomplishment]() 
- Exploratory Data Analysis in Python: [course description](https://learn.datacamp.com/courses/exploratory-data-analysis-in-python), [statement of accomplishment]() 
- Hyperparameter Tuning in Python: [course description](https://learn.datacamp.com/courses/hyperparameter-tuning-in-python), [statement of accomplishment]() 
- Writing Efficient Python Code: [course description](https://learn.datacamp.com/courses/writing-efficient-python-code), [statement of accomplishment]() 
- Winning a Kaggle Competition in Python: [course description](https://learn.datacamp.com/courses/winning-a-kaggle-competition-in-python), [statement of accomplishment]() 
- Introduction to Deep Learning with PyTorch: [course description](https://learn.datacamp.com/courses/introduction-to-deep-learning-with-pytorch), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/f4347d080bf8639635aaf765733df2ca7977c667) 


### Machine Learning  
In the lectures about Machine Learning, I learned about the following topics:
- Regression and classification
- Nearest neighbours
- Loss and cost function
- Linear regression
- Logistic regression
- Decision tree
- Gradient descent
- Training and validation
- Evaluation
- Data preprocessing
- Features

### Deep Learning 
In the lectures about Deep Learning, I learned about the following topics:
- Neural Network components
- Data pipelines
- Transfer learning
- Embeddings
- Training Neural Networks

### Research  
In the lectures about Research, I learned about the following topics:
- ICT research methods
- Research cycle
- Writing research questions
- Quality of research

### Data Visualization  
In the lectures about Data Visualization, I learned about the following topics:
- Scales
- Aesthetics
- Readability

















## Domain Knowledge 
### Introduction to the subject field
<i> Write introduction to the subject field with literature references </i>

### Literature research
To see where I informed myself about the topic and what information I gathered, please expand the sections below.

<details><summary>Nanoparticles</summary>

Nanoparticles are particles ranging from one single atom to atomic clusters or bulk crystals of 100nm or less ([Wikipedia][1]). 
	
In the field of analyzing nanoparticles, there are two ways of making the particles visible to the human eye: SEM and TEM. SEM, short for Scanning Electron Microscope, produces images of a sample by scanning the surface with a focused beam of electrons. The electron beam is then scanned in a raster scan pattern, and the position of the beam is combined with the intensity of the detected signal to produce an image ([Wikipedia][2]). TEM, which stands for  Transmission Electron Microscopy, forms an image by transmitting a beam of electrons through a specimen. The specimen is most often an ultrathin section less than 100nm thick, or a suspension on a grid ([Wikipedia][3]).
</details>

<details><summary>Thresholding</summary>

Thresholding is differenciated into global and local thresholding methods. Global thresholding focuses on the image histogram, analyzing its peaks, valleys and curvations, while local thresholding computes a threshold for each pixel and turns it either black or white ([ImageJ][4]). In our case, VSParticle uses the global thresholding method. 

Algorithms used in thresholding can be saved for repeated use as thresholding methods. Most methods use image intensity li, j to determine whether a pixel turns white or black. If li, j is smaller than a fixed constant T, the pixel turns black ([Wikipedia][5]). 

Li, Zhou, Zhu, Ma, Huang and Wong used a multiple thresholding method to classify nanoparticle images into three types: bright, dark and background. This helped them achieve pixel classification and shows that the thresholding step is very important when working with nanoparticle images ([High content image analysis for human H4 neuroglioma cells exposed to CuO nanoparticles][5]). 
</details>

[1]: https://en.wikipedia.org/wiki/Nanoparticle
[2]: https://en.wikipedia.org/wiki/Transmission_electron_microscopy
[3]: https://en.wikipedia.org/wiki/Scanning_electron_microscope
[4]: https://imagej.net/Auto_Threshold
[5]: https://en.wikipedia.org/wiki/Thresholding_(image_processing)
[6]: https://link.springer.com/article/10.1186/1472-6750-7-66


[x]: https://journals.tubitak.gov.tr/chem/issues/kim-06-30-1/kim-30-1-1-0508-1.pdf

### Terminology
Used jargon in the field of nanoparticles and VSParticle's software is listed here:
- Thresholding: method for turning a grayscale / colored images into binary images
- Run: an image being processed once in each step of the software
- ...

My research notes on the thresholding algorithms used by VSParticle can be found [here]().


## Most relevant notebooks
///


## List of all of my notebooks 
For a complete list of all notebooks I created during the project, please expand the sections below.

<details>
<summary> Data preprocessing </summary>
///
</details>

<details>
<summary> Data exploration </summary>
///
</details>

<details>
<summary> Data explanation </summary>
	
- [Explanation of original json file]() 
</details>

<details>
<summary> Data cleansing </summary>
///
</details>

<details>
<summary> Data preparation </summary>

- [Random Oversampling function]()
</details>

<details>
<summary> Data visualization </summary>
	
- [Occurences of datapoints for each thresholding method]()
</details>

<details>
	<summary> Machine Learning models </summary>
	
- [Linear/Polynomial Regression model: count vs. user score (full dataset)]()
- [Linear/Polynomial Regression model: count vs. user score (yen)]() 
- [Linear/Polynomial Regression model: separation vs. user score (yen)]() 
- [Linear/Polynomial Regression model: separation, border and more vs. user score (yen)]() 
- [Multiclass Logistic Regression model: feature comparison (yen, with help from Yoran)]()
- [Multiclass Logistic Regression model: separation, intensity, count (yen)]()
</details>

<details>
<summary> Contributions to group code </summary>

- [Experiment #1: Random Oversampling function]()
</details>


## Communication 
### Presentations
- [Week 2](): Internal presentation, created and presented by me 
- [Week 3](): Internal presentation, created and presented by me 
- [Week 4](): External presentation, created and presented by Yoran and me
- [Week 8](): Internal presentation, created and presented by me
- [Week 11](): Internal presentation, created and presented by me

### Research Plan
My contributions to the research paper have been broadly spread out and significant. My contributions ranged from writing detailed chapters like the introduction and individual sub-question descriptions, to general layout. The research plan can be found [here]().

The following contents of the research plan have been made by me:
- Introduction
- Literature review
- Formulation of the research question 
- Formulation of sub-questions (with Oscar)
- Elaboration on sub-questions two, three and four 
- Re-writing sub-question 4, as we changed our approach after group members left

### Research Paper
My contributions to the research paper have been .... The research paper can be found [here]().

The following contents of the research paper have been made by me:
- Creation of file and structure (group work with Oscar and Yoran)

### Other efforts
Throughout the whole project, I kept notes of each meeting in order to keep record of them for possible questions later on. 

Of course, I also kept my part of the Jira board up to date and documented my work there for an easy overview and communication with my group members.


## Diganostics of the learning process
Our project group definitely learned how important it is to review and check other group member's work, as we realized a couple of weeks into the minor that the csv file we had been working with contained faulty values. Midway through the project the same thing happened and we noticed our assumptions about the dataset were not correct. We could have avoided this by reviewing each others code more in depth before working with the files. However, luckily the changes from the corrupted values were not too high so that the first interpretations we got were not heavily misleading. After updating our old models, which went fairly quick as we simply needed to change the file that the notebook was reading, we could continue where we left off.

...


## Evaluation using STARR
As a User Experience Design student, I have only had short experiences with coding and programming so far. In order to extend them and learn more about statistics and data visualization, I chose this minor.

As I have not had much background knowledge on the topic, the minor started with a lot of new information to take in. It was difficult for me to get an idea of how to start. I quickly realised that even though I was not sure about things, I had to just do them in order to improve and learn. Since then, my understanding of how data science works and how to approach it grew constantly. 

...




