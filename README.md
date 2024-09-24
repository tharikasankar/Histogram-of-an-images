# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: THARIKA S 
# Register Number: 212222230159


!pip install opencv-python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray_image.jpeg')
color_image = cv2.imread('color_image.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('gray_image.jpeg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color_image.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray_image.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/1d75cf71-cb44-47e0-b206-3b825f80d149)
![image](https://github.com/user-attachments/assets/c56c02ad-30c7-450f-a192-1867c1c18f2a)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/e4f7c0f9-a2fc-4245-b60f-0ab6d51b737c)

![image](https://github.com/user-attachments/assets/7ae17351-df74-4212-9d53-24e04aff2fb8)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/2339f1d9-57fc-4acd-ab07-1810f7d508f0)

![image](https://github.com/user-attachments/assets/b030a54b-562e-4cd3-9738-f7af0f2fa46a)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
