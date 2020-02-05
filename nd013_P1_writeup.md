# **Finding Lane Lines on the Road** 

## Udacity course nd013 Project 1 writeup.

### CarND-LaneLines-P1
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./output_test_images/output_solidWhiteCurve.jpg "Grayscale"

---

### Reflection

### 1. The Pipeline description and the modifications to the draw_lines() function.

The pipeline exercises the Helper Functions provided.
I added a little tooling to better understand the operation of the functions provided.
The first checkin to git captures the essential discovery phase
that resulted in line identification and result output file using the provided funtions.
It was obvious that cleanup of the output would be necessary to reduce
the code checkin to only the essential elements.
 jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace P1.ipynb

Much googleneering was undertaken to isolate the parameter values to be used
for color thresholding (which I abandoned)
as well as the key values in canny and hough functions that generated adequate results.
I found the youtube PyData session by Ross Kippenbrock most enlightening.
As an exercise I experimented with a combination of L channels
from each of LUV and LAB color spaces which isolated the lane lines quiet nicely. 
After a chat with mentor Michael I reverted to simpler mechanisms for this first project.
I will exercise my weakest muscle (patience) and trust the course plan.

![alt text][image1]

### 2. Identify potential shortcomings with your current pipeline
The initial listdir returned additional artifacts on this macos 
eg: .DStore that required some refinement to better isolate
just the jpeg files in the test_images folder.
I created a separate output_ prefix directory to keep the intermediate output files separate. 
I did have some initial RGB vs BGR heartache as a result of prior cv2.imread experience.
I use hungarian notation in my code to enhance the type separation of the intermediate images in the pipeline.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...

### 4. Workflow
workon jupyter
jupyter notebook
deactivate
jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace P1.ipynb
git status
git add P1.ipynb
git commit -m "commit message"

