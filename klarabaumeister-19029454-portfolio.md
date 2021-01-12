# Personal Portfolio
Student name: Klara Baumeister  
Student number: 19029454  
Course: Applied Data Science minor 20/21
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

To answer our research question, we conducted an experiment which calculates scores for all possible combinations of models, number of classes, features, and balancing methods.

### Conclusions
In conclusion, the data needed to be restructured in a way that allows us to have as many samples in one class as possible while still keeping a high class number for detailed class distinction. This was achieved by collapsing the 10 user scores into 5 classes.

Regarding the features, the analysation of the experiment concluded in using count, fill, intensity and separation since these result in a high accuracy in most most model combinations and therefore are reliable, and none of them are collinear with each other which would lead to a potentially unstable model.

Finally, we decided on a logistic regression model as it fits our classification problem and leads to the best result the large majority of all experiment runs. In order to deal with our imbalanced data, we used the XXX technique on our classes in order to get an even class distribution and unbiased results. XXX also has the advantage of creating more data points instead of reducing the dataset like for example Random Undersampling, which is beneficial in regard to our small dataset.

For future work on this project, we recommend three improvements that will perhaps lead to more promising results: During the experiment, a test set should be provided additionally to the training and validation set. The test set enables completely unbiased evaluation of the experiment's results and therefore is strongly advised, however regarding our small dataset we decided against it, as our validation set already consits of only 11 samples. Furthermore, the features derived from other steps than the thresholding step should potentially also be taken into account and implemented into the model, as the user score does not only derive from the thresholding step but the whole run of an image through all steps. The user probably even takes into account the image quality in general, so this needs to be remembered too while evaluating this project. Additionally, this problem could also perhaps be solved with a ranking model instead of classification. However, our dataset dit not provide enough comparable runs, which is why we were not able to fully pursue this idea.<

### Planning
To make our group work as efficient and agile as possible, we used Scrum. We planned sprint periods of two weeks, including daily standups and retrospectives at the end of each sprint. In order to get an overview of everybody's work progress, we used the platform Jira to create a Scrumboard. All of our completed issues from the sprints can be found [here](https://vsparticle-nano.atlassian.net/jira/software/c/projects/NANO/issues).



## Domain Knowledge 
### Introduction to the subject field
The study of nanoparticles continues to be of great significance in various fields of work, including calculating their sizes from microscopic images for further research, as the Dutch company VSParticle does. Our project focuses on finding a Machine Learning model that predicts the optimal threshold method to use in the image processing software created by VSParticle.

### Literature research
To see where I informed myself about the topic and what information I gathered, please expand the sections below.

<details><summary>Nanoparticles</summary>

Nanoparticles are particles ranging from one single atom to atomic clusters or bulk crystals of 100nm or less ([source][1], [source][12]). They have proved to be of high significance in various fields of work, such as medicine, engineering and chemistry, for products like quantum computers, chemical sensors and photochemical devices such as flat panel displays, among others ([source][7], [source][12]).
	
For analysation and documentation, microscopic images of the particles are often saved and used for further research. There are two ways of making the particles visible to the human eye: SEM and TEM. SEM, short for Scanning Electron Microscope, produces images of a sample by scanning the surface with a focused beam of electrons. The electron beam is then scanned in a raster scan pattern, and the position of the beam is combined with the intensity of the detected signal to produce an image ([source][2]). TEM, which stands for  Transmission Electron Microscopy, forms an image by transmitting a beam of electrons through a specimen. The specimen is most often an ultrathin section less than 100nm thick, or a suspension on a grid ([source][9]).
</details>

<details><summary>Thresholding</summary>
	
Thresholding is the process of turning a grayscale / colored image into a binary one with either black or white pixels. It is differenciated into global and local thresholding methods: Global thresholding focuses on the image histogram, analyzing its peaks, valleys and curves, while local thresholding computes a threshold for each pixel and turns it either black or white ([source][4]).

Algorithms used in thresholding can be saved for repeated use as thresholding methods. Most methods use image intensity li, j to determine whether a pixel turns white or black. If li, j is smaller than a fixed constant T, the pixel turns black ([source][5]). There are multiple methods that have been proved to be very efficient, for example Otsu([source][10]), Yen([source][11]) and many more([source][4]).

Regarding the work with nanoparticles, F. Li et al. used a multiple thresholding method to classify nanoparticle images into three types: bright, dark and background. This helped them achieve pixel classification and shows that the thresholding step is very important when working with nanoparticle images ([source][6]). 
</details>

<details><summary>VSParticle</summary>
	
VSParticle, a company based in Delft, has conducted a lot of research in the field of nanoparticles over the past years. Calculating the size of nanoparticles using microscopic images is one branch they focus their work on. ([VSParticle][8]). 
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


### Terminology
Used jargon in the field of nanoparticles and VSParticle's software is listed here:
- **Nanoparticle:** particles of 100nm or less
- **SEM (Scanning Electron Microscope):** a method of producing images of nanoparticles by scanning the surface with a focused beam of electrons
- **TEM (Transmission Electron Microscope):** a method of producing images of nanoparticles by transmitting a beam of electrons through a specimen
- **Colored image:** a digital image with 3 channels (red, green, blue) of 8 bits each
- **Grayscale image:** a digital image with 1 channel of 8 bits, where 0=black and 255=white
- **Bitmap:** a binary image where each pixel has either a value of 0 (black) or 1 (white)
- **Thresholding:** turning grayscale/colored images into binary images
- **Thresholding algorithm/method:** saved parameters used in the thresholding process 
- **Run:** an image being processed once in each step of VSParticle's software



### Explanations
- [Explanation of original json dataset](https://github.com/klarabau/portfolio-ads/blob/main/explanation/data%20explanation.md) 
- [Explanation of thresholding algorithms used by VSParticle (notes)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Thresholding%20algorithms.ipynb)
- [Explanation of popular classification models](https://github.com/klarabau/portfolio-ads/blob/main/explanation/models%20explanation.md)



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
- Preprocessing for Machine Learning in Python: [course description](https://learn.datacamp.com/courses/preprocessing-for-machine-learning-in-python) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/cf7346824ad47e554b657c96c429478a4df49c9d) 

Not mandatory courses:
- Introduction to Deep Learning with PyTorch: [course description](https://learn.datacamp.com/courses/introduction-to-deep-learning-with-pytorch) | [statement of accomplishment](https://www.datacamp.com/statement-of-accomplishment/course/f4347d080bf8639635aaf765733df2ca7977c667) 



## Most relevant contributions

### Random Oversampling
<img src="#">
My research on random oversampling turned out to be extremely helpful as we ended up using it in the final model. It helped us balance out the classes as can be seen in the image above.

### Experiment: Feature visualization
<img src="#">
This visualization I made is easily changeable to display any model/class/balancing method combination used in the experiment. In this case, it visualizes the best feature combinations for a 5-class Logistic Regression model, which is the selection we made for the final model. It therefore shows the best feature combinations to use for it: "bcfis", "cfis", "abcfis" being the top three and achieving nearly the same accuracy scores.

### Final model: Feature selection (correlation check)
<img src="#">
This table shows the linear correlation of all possible features. We can see that border and separation, as well as area spread and fill, are most closely related to each other. This helped us in selecting the final feature combination for the model, as the three highest scoring combinations in the experiment, "cfis", "bcfis" and "abcfis" (where a=area spread, b=border, c=count, f=fill, i=intensity, s=separation), were very close to each other in terms of accuracy. But keeping in mind that collinear features can lead to an unstable and unnecessarily complex model, we concluded that the model performs better in the long-term with using "cfis" instead of "bcifs" or "abcfis", since "bcfis" includes border and separation, and "abcfis" even includes both border and separation and area spread and fill. 







## List of all of my notebooks 

### Data preparation 
- [Random Oversampling (manually)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Random%20Oversampling%20Manually.ipynb)
- [N-Fold cross validation](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/k-fold%20cross%20validation.ipynb)

### Data visualization 
- [Experiment: Feature combinations visualization](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Experiment%20feature%20visualization.ipynb)
- [Experiment: Feature analysation](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Experiment%20feature%20analysis.ipynb)

### Machine Learning models 
- [Linear/Polynomial Regression model: count vs. user score (full dataset)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20count%20vs%20user%20score.ipynb)
- [Linear/Polynomial Regression model: count vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20count%20vs%20user%20score%20(only%20yen).ipynb) 
- [Linear/Polynomial Regression model: separation vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20separation%20vs%20user%20score%20(only%20yen).ipynb) 
- [Linear/Polynomial Regression model: separation, border vs. user score (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/LinReg%20separation%20and%20border%20vs%20user%20score%20(only%20yen).ipynb) 
- [Multiclass Logistic Regression model: feature comparison (yen, with help from Yoran)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Multiclass%20logistic%20regression%20feature%20combinations.ipynb)
- [Multiclass Logistic Regression model: separation, intensity, count (yen)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Multiclass%20logistic%20regression.ipynb)
- [Logistic and Polynomial Regression models: Test set comparison](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Logistic%20%26%20Polynomial%20regression%20(compared%20to%20ground%20truth).ipynb)
- [Polynomial Regression example](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Polynomial%20Regression%20example.ipynb)
- [Polynomial Regression experiment](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Polynomial%20Regression%20experiment.ipynb)

### Contributions to group code 
- [Experiment: Random Oversampling function](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Random%20Oversampling%20Function%20for%20experiment.ipynb)
- [Final model: Feature selection (correlation check)](https://github.com/klarabau/portfolio-ads/blob/main/notebooks/Correlated%20features%20test.ipynb)



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
- Changes in the elaboration of sub-question 4, as we changed our approach after group members left

### Research Paper
At the point of handing in this portfolio, the research paper has not been 100% finished yet. So far, my contributions to the research paper have been widely spread out and useful. The research paper (as its current, unfinished state) can be found [here]().

The following contributions to the research paper have been made by me:
- Creation of structure (group work)
- Abstract
- Introduction
- Chapter 2.2: Model comparison
- Chapter 4.1: Review
- Chapter 4.2: Final model

Furthermore, the references 1-20 have been found and researched by me.


### Other efforts
Throughout the whole project, I kept notes of each meeting in order to keep record of them for possible questions later on. 

Of course, I also kept my part of the Jira board up to date and documented my work there for an easy overview and communication with my group members.





## Reflection
### My learning objectives 
As a User Experience Design student, I have only had short experiences with programming so far. In order to extend them, while furthermore learning about statistics, data visualization and machine learning, I chose this minor. I believed that it would be a good basis for any direction I choose to specify in in the future. Especially data visualization and programming are related to User Experience Design and can prove to be advantageous for many things related to it. Hence, my objective for this minor was to learn more about the whole subject field, which was nearly completely new to me.

As I have not had much background knowledge on the topic, the minor started with a lot of new information to take in. I had never worked in a Scrum environment before, never actually dealt with machine learning, and while having small background knowledge in programming, I also had never worked with Python. Thus, it was difficult for me to get an idea of how to get started and combine the theoretical knowledge from the lectures with the project in practice. However, I quickly realised that even though I was not sure about things, I had to just do them in order to improve and learn. This was especially important when it came to programming. At the start I was a little nervous about doing programming related tasks, as I did not want to make mistakes or take a lot of time on a task that others could do much quicker. Me shying away from programming also mainly reflected from the 360-degree feedback given to me, after which I decided to finally stop hesitating and use the situation as an opportunity to learn instead. 

Since I started being fully active in all parts of the project, including programming tasks, I have improved my knowledge of programming, machine learning and data analysis a lot in comparison to where I was in the beginning of this project. My understanding of how data science and machine learning work grew constantly throughout the project. 

The practical approach of this minor resulted in a lot of project-related knowledge on top of the theoretical information from the lectures, which in combination is very valuable to me. I was able to learn a lot about data science and gain a good understanding of how to tackle problems, analyse data and visualize it.

In reflection, I am content with what I have and am motivated to extend my knowledge further in the future. Especially the programming and data visualization parts are related to my study and can be helpful for many directions of work. However, I could have used the time at the start of the project more wisely and learn even more by actively programming more complicated things earlier on.




### My contributions 
As a User Experience Design student, I have only had short experiences with programming so far. I was aware of the fact that with my background knowledge, I had to learn a lot and work hard in order to be a valuable addition to a team, but I was eager to do this and contribute to a group with people from different study fields. I saw this as an opportunity of perhaps being adding a different background and therefore different perspective to the group work.

Not had much background knowledge on the topic lead to me being hesitant at the start of the project, especially regarding programming related tasks. It took me some time to adjust to the new setting of (online) group work using Scrum, while also being new to the whole topic and project field. Even though in our group, we did not strictly divide assignments, at the start it came naturally that the members more knowledgeable in the programming field would do more programming related tasks, while I would do few minor programming tasks and focus on preparing presentations, writing the research plan and helping out wherever possible. However, after the initial two to three weeks of adjustment, I was able to participate in every part of the project and actively push the project forward.

My activities and contributions ranged from visualizing data, creating machine learning models, analysing their outcomes and giving ideas, to preparing and presenting weekly internal and external presentations, writing parts of the research plan, and in the end writing parts of the research paper. Additionally, I actively took part in daily standups, meetings and Scrum retrospectives, kept notes of every meeting, and kept our Scrumboard up to date. Even though these are minor tasks, not doing them can hamper a project immensely, hence they are also important.

My contributions resulted in an, in my opinion, balanced and successful group project. My work was often beneficial for gathering new directions for future work and also important for the organizational aspect of the project. Meanwhile, I was able to learn a lot throughout the project for possible future tasks and relations to this topic.

Reflecting on how the project went, I could have used the time at the beginning of the project better to actively forward this project early on. I especially should have done more (complicated) programming tasks in order to relieve my group members from a higher workload. However, as the project progressed the work between our group members became more and more evenly distributed and every member took part in every part of the project.



### The group project
As our group consists of two programming-related students (Mechatronics and Computer Science), and me being more of an "allrounder" with professional knowledge of image processing, research, design, and little background knowledge in programming, we were well prepared for this project.

Our project group definitely learned how important it is to review and check other group member's work, as we realized a couple of weeks into the minor that the csv-file we had been working with contained faulty values. Midway through the project the same thing happened again, where we noticed our assumptions about the dataset were not correct. We could have avoided this easily by reviewing each other’s code more in depth before working with the files. However, luckily the changes from the corrupted values were not too high so that the first interpretations we got were not heavily misleading. After updating our old models, which went quick as we simply needed to change one line of code, we could continue where we left off. 

Additionally, we should have cross-validated earlier on early models and experiments, not just the last ones in the project. We decided to focus on the different models first, but it turned out that not cross-validating from the beginning deferred our interpretations on the outcomes. Luckily, we kept our options open until the experiment in which we applied cross-validation. Because the important conclusions were all derived from the experiment, we did not need to rerun old models. However, the false results from not cross-validating were giving us and our project owner unnecessarily high hopes, which was a disappointment we could have avoided.

Another thing we should have handled differently was looking into polynomial regression towards the end of the project. Even though we are dealing with a classification problem, we listened to our problem owner and took valuable time from the end of the project to look into linear regression again, which we had already done in the beginning but concluded to not continue with for multiple reasons. We could have saved time which potentially would have led to more promising classification results if we explained the reasons why we did not continue with it in the first place to our project owner repeatedly.

In reflection, the mistakes we made as a group were all avoidable and cost us time and almost fatally misleading results. We should have avoided this by following the lectures more closely and reviewing each other’s code. However, on a positive note, we learned how important cross-validation, reviewing and following the sprint plan is, and can say that this was the last time any of these mistakes will happen to us.




