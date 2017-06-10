# **Finding Lane Lines on the Road** 


**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


### Reflection
1. Here is the overall flow of the pipeline.
   - Convert the image to grayscale.
   - Apply gaussian for smoothening the image edges.
   - Perform Canny edge detection.
   - Define and separate out region of intereset.
   - Perform Hough Transformation to detect lane lins in the edge detected image.
   - Draw the detected lane lines on the original image.

2. In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 

   - Using the slope of the lines to separate out right and left lane lines.
   - Then take the weighted average of the lines using their length and slope.
   - Approximate and keep the Y co-ordinates of the lane lines to be constant.
   - Calcualte the X cordinate from the average lane line values.  
   - Use these newly obtained co-ordinates to extrapolate the lane lines.

3. The Folder test_images_output contains the extrapolated lane lines drawn on the original images.

4. The `test_videos_output` folder contains videos for both extrapolated and non-extrapolated lane lines.

### 2. Identify potential shortcomings with your current pipeline
1. The detection has short coming with the lane lines curve.
2. The detection would be poor under various ligthing conditions.




### 3. Suggest possible improvements to your pipeline
- Using better techiques for detecting curvines lanes would help.
- Also using various color spaces might help detection under varying ligthing conditions.
