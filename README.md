# EDGE-DETECTION
# EX 6: EDGE-DETECTION
# NAME : MUHAMMED AIMAN S
# REG NO : 212224240097
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
## ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread(r'C:\Users\admin\Desktop\DIPT\dipp img.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
### ORIGINAL IMAGE

<img width="552" height="572" alt="image" src="https://github.com/user-attachments/assets/de38d808-4f94-4923-afc8-353ecfa554ef" />



### SOBEL EDGE DETECTOR

<img width="560" height="577" alt="image" src="https://github.com/user-attachments/assets/44fd3fde-e6e5-4618-8afb-60d8b802b514" />


### LAPLACIAN EDGE DETECTOR
<img width="565" height="576" alt="image" src="https://github.com/user-attachments/assets/bdfadbe2-2d35-44c5-9e4b-f0592e3ede30" />



### CANNY EDGE DETECTOR
<img width="593" height="566" alt="image" src="https://github.com/user-attachments/assets/4d64ccae-ca66-445b-a9a5-cd4f9ade3a8c" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
