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
Developed By: VINOD KUMAR S
Register Number: 212222240116
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("rose.jpg")
color_image = cv2.imread("newyork.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("rose.jpg")
Color_image = cv2.imread("newyork.jpg")
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
gray_image = cv2.imread("rose.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
![Screenshot 2024-03-15 152008](https://github.com/vinodkumar-s/Histogram-of-an-images/assets/113497226/55d5308f-dab7-4569-bf41-d8bd61209d1c)

![Screenshot 2024-03-15 152021](https://github.com/vinodkumar-s/Histogram-of-an-images/assets/113497226/a3f91be3-4dd4-46c2-9967-54e4b0b8386f)

### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -

![Screenshot 2024-03-15 151920](https://github.com/vinodkumar-s/Histogram-of-an-images/assets/113497226/308f75c4-6449-4c8e-a74d-6c27121e4aa2)

#### Color Image -

![Screenshot 2024-03-15 151939](https://github.com/vinodkumar-s/Histogram-of-an-images/assets/113497226/3cdd0474-d11c-403e-ad09-35628d20cd84)


### Histogram Equalization of Grayscale Image :

![Screenshot 2024-03-15 151849](https://github.com/vinodkumar-s/Histogram-of-an-images/assets/113497226/31c273ad-17cb-4b42-9ec9-4806b3d4234c)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
