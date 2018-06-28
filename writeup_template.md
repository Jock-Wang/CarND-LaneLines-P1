# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_image_output/test_solidWhiteCurve.jpg
[image2]: ./test_image_output/test_solidWhiteRight.jpg
[image3]: ./test_image_output/test_solidYellowCurve.jpg
[image4]: ./test_image_output/test_solidYellowCurve2.jpg
[image5]: ./test_image_output/test_solidYellowLeft.jpg
---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I use Gaussian to filter the image,I choose the kernel size is 5; and the use the canny function to detect the edge;the low threshold is 30 and the high threshold is 150;and use the fillpoly function to make a polygon region,and the use the HoughLinesP function to detect the lines,and use the draw_lines function to draw the lines;  

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by calculating the average of slopes and the points on each side of the road ,and then draw the lines.

If you'd like to include images to show how the pipeline works, here is how to include an image:
![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the front of the car appear in the video.

Another shortcoming could be the threshold can't fit all situations.


### 3. Suggest possible improvements to your pipeline

Now I can't think how to improve my pipline.