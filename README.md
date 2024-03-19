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
 Developed By: SRI KARTHICKEYAN GANAPATHY
 Register Number: 212222240102
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
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
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image:
![Screenshot 2024-03-19 111825](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/74657ff8-c2fb-4b0c-8aea-dc56305a5b1c)

![Screenshot 2024-03-19 111213](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/a568f09d-3166-4e64-b67d-06ac67f91ad6)
### Histogram of Grayscale Image and any channel of Color Image
#### Grayscale Image
![download](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/233b16e2-5f48-443a-8382-b148f5ad7aff)
![download](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/e3d32911-b2d1-4f25-b21b-3887916908ff)

#### Color Image
![download](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/12b80e1a-779b-4f7f-8594-e4d46ed3e487)
![download](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/384e5a5f-3353-4566-b6b6-f0332bcd361f)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-19 111422](https://github.com/srikarthickeyanganapathy/Histogram-of-an-images/assets/119393842/046333e4-9bb6-45cb-b961-6f970a97c11c)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
