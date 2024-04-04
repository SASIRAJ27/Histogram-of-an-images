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
 Developed By: SASIRAJKUMAR T J
 Register Number: 212222230137
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("doggray.jpeg")
color_image = cv2.imread("vulture1.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("doggray.jpeg")
Color_image = cv2.imread("vulture1.jpeg")
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
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("doggray.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```







## Output:
### Input Grayscale Image and Color Image
![EX 3 DIP](https://github.com/SASIRAJ27/Histogram-of-an-images/assets/113497176/4c2f3ae2-a49e-4629-bc33-4e9c966320bc)



### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![EX3 DIP1](https://github.com/SASIRAJ27/Histogram-of-an-images/assets/113497176/77f46941-b814-4c47-9cac-fd8b179b5c43)

#### Color Image
![EX3 DIP3](https://github.com/SASIRAJ27/Histogram-of-an-images/assets/113497176/cfbd6e15-34ac-4fd3-9116-c63ec45c5b79)



### Histogram Equalization of Grayscale Image.
![EX3 DIP4](https://github.com/SASIRAJ27/Histogram-of-an-images/assets/113497176/4bf6ecd1-f85a-4468-863c-525736ce6d36)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
