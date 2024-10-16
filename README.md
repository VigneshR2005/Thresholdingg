# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale

### Step3:
Use Global thresholding to segment the image

### Step4:
 Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image and display results.

## Program
### Name: R VIGNESH
### Register number: 212222230172
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Otsu's thresholding
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

# Display the Otsu thresholding result
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()

# Read the Image and convert to grayscale
image = cv2.imread('dog.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(image)
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
                                    cv2.THRESH_BINARY, 11, 2)
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()


```
## Output

### Original Image

![dog](https://github.com/user-attachments/assets/47112254-e94a-4073-a37e-fce0e9b744d3)


### Global Thresholding
![download](https://github.com/user-attachments/assets/fb353c33-3dd5-497c-bd0a-7742325df9cd)



### Adaptive Thresholding
![download](https://github.com/user-attachments/assets/41c40259-5a2c-44b1-bbb7-c6d9db5e2f7a)



### Optimum Global Thesholding using Otsu's Method

![download](https://github.com/user-attachments/assets/7980aeec-448a-49cf-979c-3fa260efe105)



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
