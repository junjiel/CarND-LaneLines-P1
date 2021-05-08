# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: line_image_output.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I blured the image with gaussian blur method. After this, I find the edges by using canny edge detection and then I select a region containing road edges by deploy a polygon region mask. At last, I draw hough lines onto the original image. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by first calculating the slopes of each line and then categorising them into left Xs and Ys and right Xs and Ys. Secondly, I use polyfit function to find the coefficients of left lines and right lines. At last, I draw lines on the original image. 

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be lines can't be detected when the roads are curved. 

Another shortcoming could be it's not robust when there are many vehicles on the road.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to modify the draw_line() function so that it can fit the curved roads.

Another potential improvement could be to utilize a feedback loop control algorithm to boost the robustness of the lane detecting function.
