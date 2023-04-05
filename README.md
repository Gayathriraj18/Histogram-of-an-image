# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

# Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

# Step3:
Display the histograms with their respective images.

# Step4:
Equalize the grayscale image.

# Step5:
Display the grayscale image.

## Program:
``` Developed By: Gayathri A
Register Number: 212221230028
```
```
import cv2
import matplotlib.pyplot as plt
```
# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("gray.jpg")
cv2.imshow("Gray Image",Gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import cv2
import matplotlib.pyplot as plt
Color_image = cv2.imread("clrr.jpg")
cv2.imshow("Colour_image",Color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# Display the histogram of gray scale image and any one channel histogram from color image

```
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("clrr.jpg")
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
```



# Write the code to perform histogram equalization of the image. 

```
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![dip4 1](https://user-images.githubusercontent.com/94154854/230125834-07601aee-6f83-44e4-9ef1-2f18eca2ce69.png)

![dip4 2](https://user-images.githubusercontent.com/94154854/230125904-4ca5a851-ec42-4cc4-91bd-c213e33c302d.png)



### Histogram of Grayscale Image and any channel of Color Image

![dip4 3](https://user-images.githubusercontent.com/94154854/230126148-bf389f9c-40fa-47ca-9e54-7c3d2ae881b7.png)



![dip4 4](https://user-images.githubusercontent.com/94154854/230125984-5a564a3d-315d-4d10-aac8-b3defb57b6a7.png)



### Histogram Equalization of Grayscale Image



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
