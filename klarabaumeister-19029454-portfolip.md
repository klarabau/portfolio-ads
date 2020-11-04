# Personal Portfolio
Student name: Klara Baumeister  
Student number: 19029454  
Course: Applied Data Science minor  
Lecturers: Jeroen Vuurens, Tony Andrioli, Gerda in 't Veld, Ruud Vermeij, Brian de Keijzer

## Research project
### Task definition
This is a portfolio summarizing my individual work for the Nano project of the Applied Data Science minor at The Hague University.

In the Nano project we aim to help VSParticle, a company that derived from TU Delft's nanotech group. They work with nanoparticles and, among others, analyze nanoparticle images to calculate the particle’s sizes. To do this, VSParticle has built an image processing program that results in an edited image which enables the software to calculate the particle’s sizes. Part of the image processing is the thresholding step, where greyscale images are converted into bitmaps using thresholding algorithms and user input. This step distinctly separates the nanoparticles from the background. In combination with our minor, our goal is to automate this step using a Machine Learning or Deep Learning model which predicts the best algorithm to use. Our research question reads as follows:
	
> How can a Machine Learning model, that predicts the optimal thresholding algorithm, assist VSParticle to analyze nanoparticle images? 
		
To answer our research question in detail, we are going to focus on the following four sub-questions:

1. How does the given data need to be restructured in order to be useful for the model?
2. What features of the dataset should be selected for the model?
3. What type of model do we need and how is it structured?
4. How can the predictions of the model, graded by VSParticle’s user, be employed to improve the model over time?


In order to achieve our goal, we have received a json file from VSParticle containing IDs of each run (a run being an image being processed once), parameters of the run, metadata of the image, resulting images of each step, and scores. The scores were our point of focus: they contain computer generated values that evaluate how well each step of the program worked, as well as a user score, given manually by the user after each run. This user score was crucial for our approach: We predicted the user score for each available thresholding algorithm, so that then, the thresholding algorithm with the best results could be selected.

### Evaluation
Clear and motivated directions for future work

### Conclusions
Discuss results, answer research question etc. 

### Planning
To make our group work as efficient and flexible as possible, we used Scrum. We planned sprint periods of two weeks, including daily standups and retrospectives at the end of each sprint. In order to get an overview of everybody's work progress, we used the platform Jira to create a Scrumboard, which can be found here: 




## Courses
### DataCamp 
All of the assigned courses on DataCamp have been 100% completed by me, as shown in the screenshots below.
<i> image of account overview and courses </i>

Please see the content and statement of accomplishement of each course here:
- Introduction to Python: [course description](https://learn.datacamp.com/courses/intro-to-python-for-data-science), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/731540b605e1dea88d26eafaf85f69099951552b)  
- Intermediate Python: [course description](https://learn.datacamp.com/courses/intermediate-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/5a19587a42524b169ec6c005b6dbba22bb3b1432) 
- Python Data Science Toolbox (Part 1): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-1), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/fffeaeabc04f0f84a0f01d5167b83d860a9ef8d7) 
- Python Data Science Toolbox (Part 2): [course description](https://learn.datacamp.com/courses/python-data-science-toolbox-part-2), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/d748c33f42adbbcfb49f67218196f86a97241379) 
- pandas Foundations: [course description](https://learn.datacamp.com/courses/pandas-foundations), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/3ae4299c06df02db4e40704f86613677f7d6e533) 
- Introduction to Data Visualization in Python: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/eb5ac6e59e25bd4890da76504e63230b789abc1b) 
- Manipulating DataFrames with pandas: [course description](https://learn.datacamp.com/courses/introduction-to-data-visualization-in-python), [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/eb5ac6e59e25bd4890da76504e63230b789abc1b) 
- Data Types for Data Science in Python: [course description](), [statement of accomplishment]() 
- Cleaning Data in Python: [course description](), [statement of accomplishment]() 
- Preprocessing for Machine Learning in Python: [course description](), [statement of accomplishment]() 
- Merging DataFrames with pandas: [course description](), [statement of accomplishment]() 
- Exploratory Data Analysis in Python: [course description](), [statement of accomplishment]() 
- Hyperparameter Tuning in Python: [course description](), [statement of accomplishment]() 
- Writing Efficient Python Code: [course description](), [statement of accomplishment]() 
- Winning a Kaggle Competition in Python: [course description](), [statement of accomplishment]() 
- Introduction to Deep Learning with PyTorch: [course description](), [statement of accomplishment]() 


### Machine Learning  
short intro + topic list 

### Research  
short intro + topic list 

### Data Visualization  
short intro + topic list 

### Neural Networks  
short intro + topic list 




## Domain Knowledge 
### Introduction to the subject field
Basic research on the topic and VSParticle 

### Literature research
Literature research on the thresholding algorithms 

### Terminology
Used jargon in the field of nanoparticles is listed here:

- Term: Explanation 




## Data preprocessing
### Data exploration
Research on Random oversampling to handle imbalanced data 
		
### Data cleansing


### Data preparation
Replacing the faulty csv file with new csv file in my code

### Data explanation
### Data visualization
<i>Improve visualizations according to visualization lecture</i> 




## Predictive models
<i> Link to notebooks with markdown explanations </i>
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



## Communication 
### Presentations
- Week 2: Internal presentation, created and presented by Klara 
- Week 3: Internal presentation, created and presented by Klara 
- Week 8: Internal presentation, created and presented by Klara
- Week 4: External presentation, created and presented by Klara and Yoran

### Research Plan
- Find research question 
- Find sub-questions with Oscar 
- Refine sub-questions alone 
- Write introduction, schedule etc 
- Write literature review 
- Write about sub-questions 2 and 4 in detail 


### Research Paper
My contributions to the research paper have been broadly spread out and significant. My contributions ranged from writing detailed chapters, to general layout, grammar and consistency. The research paper can be found here.

Contributions made by me:


### Other
- Keep Jira up to date 
- Keep notes of meetings 




## Diganostics of the learning process 
Rough start with a lot of new information to take in and not really an idea of how to start, but then I just started and my understanding of how everything works and is related grew fast. 
	
Change of approach early on: Predict user score for each thresholding algorithm, then pick best scoring algorithm - Yoran's idea 
	
Faulty csv file, we did not validate or review Oscar's code 




## Reflection and Evaluation using STARR













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