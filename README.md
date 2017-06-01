# **Finding Lane Lines on the Road**


The goals / steps of this project are the following:
*   Make a pipeline that finds lane lines on the road
*   Using Canny Edge detection and Hough Transformation identify the road lane lines with series of pictures.
*   Modify the piped code results to work for a video stream.


---

### 1.  Reflection


* Step 1: Bring in the image for processing as an RBG to view both white lane marking and yellow lane marking
* Step 2: Apply a Gaussian Blur to strengthen edges during Canny edge detection
* Step 3: Apply Canny Edge detection to detect the edges in our image
* Step 4: Mask the area of interest
* Step 5: Apply Hough line Transformation and return the composite image


### 2. Identify potential shortcomings with your current pipeline


My current pipeline is too sensitive to a few edges from the video feeds.  This creates a line that is not on the lane lines for one or two frames during video feeds.  This could be fixed by adding in a solution that throws out the values "y" if the slope conditions are not met.

One potential shortcoming of this solution would be during night time driving. The ability of the system to see lanes would be limited by the overrun of the vehicle's headlights.

Another shortcoming could be turning sharp corners. Under day and night conditions with only one camera the ability of the system to see the lanes are limited. You could change or alternate the mask area of interest, however the field of view would still be limited. A better option would be to add multiple cameras and overlay the images.

Furthermore transitioning from the vertical peak of a hill to a sharp downgrade would be the big safety hazard. The solution as currently envisioned would be blind to any lane changes at the vertical peak.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to fix lane extrapolation with a more simple solution and extrapolate more. Then add multiple camera views to look for curves and transitions.
Another potential improvement could be to use existing GPS data or radar to look for the line markers and overlay that with a video file.
