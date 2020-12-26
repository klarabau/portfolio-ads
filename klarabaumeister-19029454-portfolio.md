# Personal Portfolio
Student name: Klara Baumeister  
Student number: 19029454  
Course: Applied Data Science minor  
Lecturers: Jeroen Vuurens, Tony Andrioli, Gerda in 't Veld, Ruud Vermeij, Brian de Keijzer



<b> IN GENERAL: Write about where the input for what I did came from and where the output went. Make it interconnected, tell a story. Write markdown input before each jupyter file and markdown output after each file. For most important notebooks write it also in this portfolio. </b>


## Research project
- see paper

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














## Domain Knowledge 
- see paper

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

G. H. Woehrle et al. ... ([Analysis of Nanoparticle Transmission Electron...](7))
</details>

<details><summary>VSParticle</summary>
	
VSParticle, a company based in Delft, has conducted a lot of research in the field of nanoparticles over the past years. Calculating the size of nanoparticles using microscopic images is one branch they focus their work on. ([VSParticle][8]). 
</details>

[1]: https://en.wikipedia.org/wiki/Nanoparticle
[2]: https://en.wikipedia.org/wiki/Transmission_electron_microscopy
[3]: https://en.wikipedia.org/wiki/Scanning_electron_microscope
[4]: https://imagej.net/Auto_Threshold
[5]: https://en.wikipedia.org/wiki/Thresholding_(image_processing)
[8]: https://vsparticle.com/ 3

[6]: https://link.springer.com/article/10.1186/1472-6750-7-66 2
[7]: https://journals.tubitak.gov.tr/chem/issues/kim-06-30-1/kim-30-1-1-0508-1.pdf 1
[9]: https://www.sciencedirect.com/science/article/pii/B9780323299602000095 4
[10]: https://ieeexplore.ieee.org/document/4310076?arnumber=4310076 7
[11]: https://ieeexplore.ieee.org/document/366472?arnumber=366472 6

[12]: . https://www.britannica.com/science/nanoparticle 8
[13]: . https://link.springer.com/chapter/10.1007/978-3-642-11216-4_12 5

. = not included in text above yet.



### Terminology
Used jargon in the field of nanoparticles and VSParticle's software is listed here:
- Thresholding: method for turning a grayscale / colored images into binary images
- Run: an image being processed once in each step of the software
- ...

My research notes on the thresholding algorithms used by VSParticle can be found [here]().


## Most relevant contributions
- also include ideas from me, not just notebooks


## List of all of my notebooks 
For a complete list of all notebooks I created during the project, please expand the sections below.

Link test:
[N-Fold cross validation](k-fold cross validation.ipynb)

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
	
- [Explanation of original json file received from VSParticle]() 
</details>

<details>
<summary> Data cleansing </summary>
///
</details>

<details>
<summary> Data preparation </summary>

- [Random Oversampling function]()
- [K-fold cross validation]()
</details>

<details>
<summary> Data visualization </summary>
	
- [Occurences of datapoints for each thresholding method]()
- [Experiment: Feature combinations]()
- [Experiment: Feature analysation]()
</details>

<details>
	<summary> Machine Learning models </summary>
	
- [Linear/Polynomial Regression model: count vs. user score (full dataset)]()
- [Linear/Polynomial Regression model: count vs. user score (yen)]() 
- [Linear/Polynomial Regression model: separation vs. user score (yen)]() 
- [Linear/Polynomial Regression model: separation, border and more vs. user score (yen)]() 
- [Multiclass Logistic Regression model: feature comparison (yen, with help from Yoran)]()
- [Multiclass Logistic Regression model: separation, intensity, count (yen)]()
- [Polynomial Regression model: Test set comparison]()
- [Polynomial Regression experiment]()
</details>

<details>
<summary> Contributions to group code </summary>

- [Experiment: Random Oversampling function]()
- [Final model: Confusion matrix]()
</details>


## Communication 
### Presentations
- [Week 2](): Internal presentation, created and presented by me 
- [Week 3](): Internal presentation, created and presented by me 
- [Week 4](): External presentation, created and presented by Yoran and me
- [Week 8](): Internal presentation, created and presented by me
- [Week 11](): Internal presentation, created and presented by me
- [Week 14](): Internal presentation, created and presented by me
- [Week 15](): Internal presentation, created and presented by me


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
My contributions to the research paper have been... The research paper can be found [here]().

The following contributions to the research paper have been fully made by me:
- Abstract
- Introduction
- Creation of file and structure

The following contributions to the research paper have been partly made by me:


Furthermore, the references 1-8 have been found and researched by me.


### Other efforts
Throughout the whole project, I kept notes of each meeting in order to keep record of them for possible questions later on. 

Of course, I also kept my part of the Jira board up to date and documented my work there for an easy overview and communication with my group members.


## Diganostics of the learning process
Our project group definitely learned how important it is to review and check other group member's work, as we realized a couple of weeks into the minor that the csv file we had been working with contained faulty values. Midway through the project the same thing happened and we noticed our assumptions about the dataset were not correct. We could have avoided this by reviewing each others code more in depth before working with the files. However, luckily the changes from the corrupted values were not too high so that the first interpretations we got were not heavily misleading. After updating our old models, which went fairly quick as we simply needed to change the file that the notebook was reading, we could continue where we left off. 

Additionally, we should have cross-validated earlier on early models and experiments, not just the last one. We decided to focus on the models first but it turned out that not cross-validating from the beginning deferred our interpretations on the data. Luckily, we kept our options open until the final experiment in which we cross-validated our data, so we could re-interpret the data rather easily. cuz the conclusions we drew were all on the experiment , which was cross validated , we didn't need to rerun old ones. but also the results were giving us higher hopes than we actually had in the end as results so we started looking into polynomial regression again, which we couldve done earlier if we cross-validated earlier.

...


## Evaluation using STARR
As a User Experience Design student, I have only had short experiences with coding and programming so far. In order to extend them and learn more about statistics and data visualization, I chose this minor.

As I have not had much background knowledge on the topic, the minor started with a lot of new information to take in. It was difficult for me to get an idea of how to start. I quickly realised that even though I was not sure about things, I had to just do them in order to improve and learn. Since then, my understanding of how data science works and how to approach it grew constantly. 

Include 360 degree feedback!

...






