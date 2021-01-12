# Explanation of original json file

### Structure

We received our data in a json file structured as follows:

(This visualization does not show every single parameter in the json file as to not make it overly complicated and lengthy. It should rather give insight into the general structure of the file.)

<img src="https://github.com/klarabau/portfolio-ads/blob/main/explanation/data%20explanation%20visual.png" width=50%>

### Scores

As visualized above, there are six scores calculated for every step, that are statistics of the image and indiciate whether or not the image has improved. Generally, for most of these scores applies: the higher the value, the better the image. However, the boundaries of each score are different.

The scores are calculated for each possible value for each step, not just the selected ones. However, scores for threshold methods that are not selected in a run are not valuable to our project, since the user score is only calculated for each run, meaning it only relates to the selected parameters. 

In the image below, I visualized the structure of the scores section more in-depth. Again, not every score is displayed here, to not make the image overly lengthy, as they repeat themselves for every possibility of every step. They are indiciated with a small grey dot before the name of the step. The user score, as already mentioned, only relates to the *selected* combination, for example in a random run: invert=true, smooth=0.050, threshold=yen.

<img src="https://github.com/klarabau/portfolio-ads/blob/main/explanation/scores%20visual.png" width=60%>





The scores represent the following indications:

**Bounding box** is the most narrow box around the object (nanoparticles).

**Area spread** is the area for each particle. The score calculates the mean area (divided by deviation). The score increases if the particles are all the same size (low variation).

**Intensity** extracts and flattens the background from original image. If there is a lot of variation in the background, the number will be low (bad).

**Border** labels the binary image: 0=background, 1=1st particle, 2=2nd particle etc., then it detects the edges of the particles. If the separation between the background and foreground is higher, the score also increases.

**Fill** counts the foreground pixels and fills the holes in the particles. It detects these holes by searching for clustered white pixels, where the holes are some small black pixels in between. The highest score possible is 1 (no holes anywhere).

**Count** tells how many particles are in the image using the labels of the border score. Through this, it also checks if the inversion step is done correctly, because if the count is high, that implies there are lots of particles in the image (good, inversion done correctly), but if it is low, that there are not a lot of particles in the image, meaning it should probably be inverted.

**Separation** is the mean pixel value of all particles in total compared to largest value in the background, therefore it represents the contrast between particles and background. The score is limited from 0 to 1.