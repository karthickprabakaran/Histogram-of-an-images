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
```python
# Developed By: karthick P
# Register Number: 212222100021
```
### Input Grayscale Image and Color Image
```python
import matplotlib.pyplot as plt
import numpy as np
import cv2
Gray_image = cv2.imread("sea.png")
Color_image = cv2.imread("lake2.jpg")
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
### Histogram of Grayscale Image and any channel of Color Image
```python
plt.imshow(Gray_image)
plt.show()
hist =cv2.calcHist([Gray_image], [0], None, [256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem (hist)
plt.show()
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image], [1], None, [256], [0,256])
plt.figure()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem (hist1)
plt.show()
```
### Histogram Equalization of Grayscale Image.
```python
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image], [1], None, [256], [0,256])
plt.figure()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem (hist1)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/karthickprabakaran/Histogram-of-an-images/assets/166775653/69b3453d-52ac-4810-8e02-0e4da9ced074)

![image](https://github.com/karthickprabakaran/Histogram-of-an-images/assets/166775653/71e768b7-d244-480f-8bf1-300295fd5482)



### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/karthickprabakaran/Histogram-of-an-images/assets/166775653/9d32929e-d048-46ac-bde3-2234486e8e0d)

![image](https://github.com/karthickprabakaran/Histogram-of-an-images/assets/166775653/b5f12363-de40-4d52-9ee0-24adb668acd4)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
