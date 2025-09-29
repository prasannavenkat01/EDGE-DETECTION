# EXP-6 EDGE-DETECTION
# NAME: PRASANNA V
# REG NO: 212223240123

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```py
NAME : PRAVESH N
REG NO : 212223230154

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```py
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```py
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```py
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:

### ORIGINAL IMAGE

<img width="562" height="358" alt="Screenshot 2025-09-29 102913" src="https://github.com/user-attachments/assets/2b4603e6-5b0b-4482-9982-e0965b029d52" />


### SOBEL EDGE DETECTOR

<img width="545" height="356" alt="Screenshot 2025-09-29 102947" src="https://github.com/user-attachments/assets/5e52374f-2fee-42d1-9b83-994d917d9df3" />


### LAPLACIAN EDGE DETECTOR

<img width="500" height="336" alt="Screenshot 2025-09-29 103009" src="https://github.com/user-attachments/assets/0b973a79-cfdf-4dec-b010-60cb4e594258" />


### CANNY EDGE DETECTOR

<img width="513" height="350" alt="Screenshot 2025-09-29 103033" src="https://github.com/user-attachments/assets/51df6015-912e-4793-8b95-5ce70570e54a" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
