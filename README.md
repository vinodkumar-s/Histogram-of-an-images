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
Developed By: NAGUL K
Register Number: 212222230089
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("flower.jpg")
color_image = cv2.imread("sphere.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("flower.jpg")
Color_image = cv2.imread("sphere.jpg")
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
```

### Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("flower.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
![Screenshot 2024-03-15 155449](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/5127d331-2e26-4512-b2bf-83ff196f811d)
![Screenshot 2024-03-15 155432](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/6e179fdc-fd1b-42af-afec-533d682b93a4)


### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -

![image](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/bc1588dd-a382-4d2c-b566-05c9c1a77437)
![image](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/c403abd1-51f8-4f27-a7b7-1e1cefb45036)



#### Color Image -

![image](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/faa2e159-b979-46c7-8f97-fc1991aff506)
![image](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/9c169fe0-660e-4ca2-9a1a-faf3f207b5c0)



### Histogram Equalization of Grayscale Image :
![Screenshot 2024-03-15 155737](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/9558d94a-3036-4e7b-9fdb-61fbf1651ae8)
![Screenshot 2024-03-15 155745](https://github.com/Nagul71/Histogram-of-an-images/assets/113497226/639b4a4b-38ff-4138-a64e-5b47ad2f5046)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
