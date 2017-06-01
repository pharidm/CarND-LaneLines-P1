# **Finding Lane Lines on the Road**


The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report
Make a pipeline that finds lane lines on the road. Using Canny Edge detection and Hough Transformation identify the lane lines on the on a series of picutures.  Modify the piped code results to work for a video stream. <p>
*

My pipe consisted of the following 5 steps




[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

* Step 1: Bring in the image for processing as an RBG to view both white lane marking and yellow lane marking
* Step 2: Apply a Gaussian Blur to streghthen edges during Canny edge detection
* Step 3: Apply Canny Edge detection to detect the edges in our image
* Step 4: Mask the area of interest
* Step 5: Apply Houghline Transformation and return the composite image


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when you encounter night time driving. Assuming Video feed is workking, The ablity of the system to see lanes would be limited by the overrun of the vehicle's headlights.

Another shortcoming could be turning sharp corners. Under day and night conditions with only one camera the ablity of the system to see the lanes are limited. You could change or alternate the mask area of interest, however the field of view would still be limited. A better option would be to add multiple cameras and overlay the images.

Another shortcoming would be transitioning from the vertical peak of a hill to a sharp downgrade. The solution as currently envisioned would be blind to any lane changes as the vertical peak.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to fix the right lane extrapolation with a more simple solution. Then add multiple camera views to look for curves and transitions.
Another potential improvement could be to use existing GPS data or radar to look for the line markers and overlay that with a video file.
