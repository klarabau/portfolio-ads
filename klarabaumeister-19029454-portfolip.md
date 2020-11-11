# Personal Portfolio
Student name: Klara Baumeister  
Student number: 19029454  
Course: Applied Data Science minor  
Lecturers: Jeroen Vuurens, Tony Andrioli, Gerda in 't Veld, Ruud Vermeij, Brian de Keijzer

## Research project
### Task definition
This portfolio summarizes my individual work and effort for the Nano project of the Applied Data Science minor.

In the Nano project we aim to help VSParticle, a company that derived from TU Delft's nanotech group. They work with nanoparticles and, among others, analyze nanoparticle images to calculate the particle’s sizes. To do this, VSParticle has built an image processing program that results in an edited image which enables the software to calculate the particle’s sizes. Part of the image processing is the thresholding step, where greyscale images are converted into bitmaps using thresholding algorithms and user input. This step distinctly separates the nanoparticles from the background. In combination with our minor, our goal is to automate this step using a Machine Learning or Deep Learning model which predicts the best algorithm to use. Our research question reads as follows:
	
> <b> How can a Machine Learning model, that predicts the optimal thresholding algorithm, assist VSParticle to analyze nanoparticle images? </b>
		
To answer our research question in detail, we are going to focus on the following four sub-questions:

1. How does the given data need to be restructured in order to be useful for the model?
2. What features of the dataset should be selected for the model?
3. What type of model do we need and how is it structured?
4. How can the predictions of the model, graded by VSParticle’s user, be employed to improve the model over time?

In order to achieve our goal, we have received a json file from VSParticle containing IDs of each run, parameters of the run, metadata of the image, resulting images of each step, and scores. The scores were our point of focus: they contain computer generated values that evaluate how well each step of the program worked, as well as a user score, given manually by the user. These scores were planned to be the input features for our thresholding algorithm prediction. However, early on, we had a change of approach: Instead of predicting the thresholding algorithm with input features like the user score, we focused on predicting the user score with other features. Then we could select the thresholding algorithm that scored the highest user score. 

### Evaluation
Clear and motivated directions for future work

### Conclusions
Discuss results, answer research question etc. 

### Planning
To make our group work as efficiently and agile as possible, we used Scrum. We planned sprint periods of two weeks, including daily standups and retrospectives at the end of each sprint. In order to get an overview of everybody's work progress, we used the platform Jira to create a Scrumboard. All of our completed issues from the sprints can be found [here](https://vsparticle-nano.atlassian.net/jira/software/c/projects/NANO/issues).




## Courses
### DataCamp 
All of the assigned courses on DataCamp have been 100% completed by me, as shown in the screenshots below. My DataCamp profile can be found [here.](https://www.datacamp.com/profile/19029454)
<i> image of account overview and courses </i>

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
- Introduction to Deep Learning with PyTorch: [course description](https://learn.datacamp.com/courses/introduction-to-deep-learning-with-pytorch), [statement of accomplishment]() 


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
- Neural Networks
- Representation Learning

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
<i> Write introduction to the subject field with literature references (?) </i>

### Literature research
<i> Find relevant literature and citate all in-text references </i>

I started out by doing basic research on the topic of nanoparticles and VSParticle. It can be found [here.](https://datascience.hhs.nl:8888/user/19029454/notebooks/nano/Code%20Klara/Research/Project%20research.ipynb) <i> Find sources and write into full text </i>

In order to gain more insights into how the thresholding algorithms operate, I researched how each of the algorithms work. The notes can be found [here.](https://datascience.hhs.nl:8888/user/19029454/notebooks/nano/Code%20Klara/Research/Thresholding%20algorithms.ipynb) <i> Write into full text </i>

As it quickly became clear that we were dealing with imbalanced data, each of us researched a possible solution to our problem. My research on Random Oversampling, including a proof of concept and example code on our dataset, can be found [here.](https://datascience.hhs.nl:8888/user/19029454/notebooks/nano/Code%20Klara/Research/Random%20Oversampling.ipynb)

### Terminology
Used jargon in the field of nanoparticles and VSParticle's software is listed here:
- Thresholding:  
- Run: an image being processed once in each step of the software




## Data preprocessing
### Data exploration
/

### Data explanation
Explanation of original dataset (load json file with markdown explanations up to jupyter)
		
### Data cleansing
/

### Data preparation
Random Oversampling (if we end up using it)

### Data visualization
<i>Improve visualizations according to visualization lecture</i> 

In combination with my research on Random Oversampling, I have visualized the occurences of datapoints for each thresholding method, as shown below:

The Machine Learning models that I have visualized can be found in the next chapter, Predictive models.





## Predictive Analytics
### Machine Learning models
<i> Link to notebooks with markdown explanations </i>

<i> Can't link to the jupyter notebooks with url bc lecturers don't have access, so use nbconvert to either export as pdf or export as Jupiter notebook and upload to GitHub (nicer view) </i>

- Linear regression count vs user score
		2 Versions: All thresholding algorithms and only yen 
		- no correlation: look at plot and coef value 
		- linear regression not applicable to model? 
		- useful features according to correlation matrix: Separation and border 
		
- Linear regression separation vs user score 
		Because correlation matrix and coeff value show higher correlation 
		- higher correlation: look at plot and coef value 
		- linear regression not applicable to model? 
		
- Linear regression separation, border and more vs. user score
		To find out which features are helpful 
		- accuracy changes with set_random value??? 
		- linear regression not very helpful to model because all accuracy scores are low 
		
### My contribution to the final model
<i> Write about any possible contribution, e.g. writing code, evaluating the code, interpreting outcomes, etc. </i>



## Communication 
### Presentations
- Week 2: Internal presentation, created and presented by Klara 
- Week 3: Internal presentation, created and presented by Klara 
- Week 4: External presentation, created and presented by Klara and Yoran
- Week 8: Internal presentation, created and presented by Klara


### Research Plan
My contributions to the research paper have been broadly spread out and significant. My contributions ranged from writing detailed chapters like the introduction and individual sub-question descriptions, to general layout. The research plan can be found here:

The following contents of the research plan have been made by me:
- Introduction
- Literature review 
- Formulation of the research question 
- Formulation of sub-questions (with Oscar)
- Elaboration on sub-questions two, three and four 
- Re-writing sub-question 4, as we changed our approach after group members left


### Research Paper
My contributions to the research paper have been broadly spread out and significant. My contributions ranged from creating the file and its structure in the first place, to writing detailed chapters, to refining grammar and consistency. The research paper can be found here.

The following contents of the research paper have been made by me:


### Other efforts
Throughout the whole project, I kept notes of each meeting in order to record them for possible questions and obscurities later on. 

Obviously, I also kept my part of the Jira board up to date and documented my work for other group members there.




## Diganostics of the learning process (what would I do better)
We definitely learned how important it is to review and check other group member's work, as we realized a couple of weeks into the minor that the csv file we had been working with contained faulty values. We could have avoided this by reviewing Oscar's code before working with the file. However, luckily the changes from the corrupted values were not too high so that the first interpretations we got were not  misleading our project and we could continue where we left off.




## Evaluation using STARR
As a User Experience Design student, I have only had short experiences with coding and programming so far. In order to extend them and learn more about statistics and data visualization, I chose this minor.

As I have not had much background knowledge on the topic, the minor started with a lot of new information to take in. It was difficult for me to get an idea of how to start. I quickly realised that even though I was not sure about things, I had to just do them in order to improve and learn. Since then, my understanding of how data science works and how to approach it grew constantly. 












####################################################################################################################################
Portfolio needs to be controllable. 

The personal portfolios are assessed individually. The contents of your personal portfolio should reflect your contribution to the project, your abilities and what you have learned. Your portfolio should consist of materials that you either realized individually, or in case of a group effort, a clear statement of what your contribution is in this group effort.

It is important to write your (digital) portfolio in a very easily accessible way. The main document should be like a reader's guide that shortly introduces your contributions and links to pages where the contributions are described in detail. Every contribution should be accessible from the reader's guide in a single click. We are not going to browse the folder, so if you do not link to a document from the reader's guide, we will not include it in the assessment.

For us, it is perfectly acceptable if you write down your portfolio in Github using Markdown, no need to do fancy markups.

Include information of the following subjects:
- Courses (add screenshots of the online courses you have finished (e.g. DataCamp))
- Domain Knowledge (Literature, jargon, evaluation, existing data sets, ...)
- Predictive Models
- Data preparation
- Data Visualization
- Data collection
- Evaluation
- Diagnostics of the learning process
- Communication (presentations, summaries, paper, ...)
- Link to the Python Notebooks you have finished (you can dump them to PDF)
- List the tickets from the Scrum backlog that you worked on, linked to deliverables, own experiments, etc.
- Add any other assignment you feel is evidence of your abilities

STARR Method for Self-evaluation of the Internship
 

At the end of the internship, you have to analyze yourself according to STARR method - used widely in education (for example RPL of university, HR management).

S – situation; the circumstances, where the experience was received (for example, description of the workplace or a specific case).

T - task; the assignments and roles, which were completed during the traineeship (which have to be related to what has been learned during the completion curriculum, considering that these tasks should also provide personal development). Here, you can introduce the problem that you will be paying further attention to.

A- activities; activities and methods (techniques, preparation, and principles for selecting the method and its alternatives). When describing activities, please write so the reader can understand what you did, how you did it, and what kind of methods/means you used.

R - results; the most important results (both the best and more surprising outcomes that made you analyze and change your activity), who, how, and based on what assessed, and what was done further with the results.

R - reflection; analysis, where the kind of competences you received and what are the areas that need improvement are reflected upon.




####################################################################################################################################