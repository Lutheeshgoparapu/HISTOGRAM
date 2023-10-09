# Histogram and Histogram Equalization of an image:
## Aim:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255.
Also write the code using OpenCV to perform histogram equalization.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the libraries.
### Step2:
Use cv2.calcHist to find the histogram of the image.
### Step3:
Plot the image and its stem plots using the functions.
### Step4:
Equalize the grayscale image using the in-built function cv2.equalizeHist().
### Step5:
Display the original and equalized image.

## PROGRAM:
~~~
Developed By: G.Lutheesh
Register Number: 212221230029
~~~
# Write your code to find the histogram of gray scale image and color image channels.
~~~
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("1.jfif")
Color_image = cv2.imread("thanos.webp",-1)
cv2.imshow("Gray Image",Gray_image)
cv2.imshow("Colour Image",Color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
~~~

# Display the histogram of gray scale image and any one channel histogram from color image:
~~~
import numpy as np
import cv2
Gray_image = cv2.imread("1.jfif")
Color_image = cv2.imread("thanos.webp",-1)
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()
~~~
# Write the code to perform histogram equalization of the image. 
~~~
import cv2
gray_image = cv2.imread("1.jfif",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows 
~~~
## OUTPPUT:
### Input Grayscale Image and Color Image
![1](https://github.com/Lutheeshgoparapu/HISTOGRAM/assets/94154531/7a96fac4-b997-4a80-9e44-7cafd54157e9)


### Histogram of Grayscale Image and any channel of Color Image
![2](https://github.com/Lutheeshgoparapu/HISTOGRAM/assets/94154531/040f347d-f81b-4471-aa92-f95d8d0e46bf)

![3](https://github.com/Lutheeshgoparapu/HISTOGRAM/assets/94154531/c6fb2007-2ec5-4a53-a25f-e3b1cdf0bd96)

### Histogram Equalization of Grayscale Image
![4](https://github.com/Lutheeshgoparapu/HISTOGRAM/assets/94154531/265a027b-8471-4df0-8ca7-01c006dc5628)

## RESULT: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
