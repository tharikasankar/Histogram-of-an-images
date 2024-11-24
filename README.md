# Ex.No 3: Histogram-of-an-images
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
```python
# Developed By: THARIKA S
# Register Number: 212222230159

### Input Grayscale Image and Color Image

import cv2
import matplotlib.pyplot as plt
flower = cv2.imread("image1.webp")
grayscale_image = cv2.cvtColor(flower, cv2.COLOR_BGR2GRAY)
cv2.imshow("Color Image", flower)
cv2.imshow("Gray Image", grayscale_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

### Histogram of Grayscale Image and any channel of Color Image

import matplotlib.pyplot as plt 
hist=cv2.calcHist(grayscale_image,[0],None,[255],[0,255])
plt.figure()
plt.title("Histogram")
plt.xlabel("pixel value")
plt.ylabel("pixel count")
plt.plot(hist)
plt.show()

### Histogram Equalization of Grayscale Image.

gray_resized = cv2.resize(grayscale_image, (500, 400))
equalized_image = cv2.equalizeHist(gray_resized)
cv2.imshow("Original Grayscale Image", gray_resized)
cv2.imshow("Equalized Grayscale Image", equalized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
plt.figure()
plt.title("Equalized Grayscale Image Histogram")
plt.xlabel("Pixel Value")
plt.ylabel("Pixel Count")
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized)
plt.show()


```
## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/c607d68a-24be-491c-a8db-3a6f8144a085)

![image](https://github.com/user-attachments/assets/03cd989d-37dc-41e5-841c-1eabcfca1524)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/user-attachments/assets/16e4ae95-f9a9-4a6c-b15b-1a7be9ac0511)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/f1104fc6-9e14-4e61-9520-044dfc3e5922)

![image](https://github.com/user-attachments/assets/ed5c8e8b-e25b-419a-b5df-36e44cf36c4f)

![image](https://github.com/user-attachments/assets/6cde1434-8c7b-433c-b9b6-676ff6cd999f)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
