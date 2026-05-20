# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.
## NAME : Mukesh Raj D
## REG NO : 212224100038
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program


# Load the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

```

# Read the Image and convert to grayscale
```
image = cv2.imread("C:\\Users\\admin\\Downloads\\My image.png")  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  

```



# Convert from BGR to RGB for display
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
```
# Use Global thresholding to segment the image
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

```

# Use Adaptive thresholding to segment the image

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)


```


# Use Otsu's method to segment the image 
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```



# Display the results

# Global Thresholding
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()

```


## Output

### Original Image

<img width="763" height="402" alt="image" src="https://github.com/user-attachments/assets/0425aba2-4976-4985-94e6-307bba759a43" />


### Global Thresholding
<img width="672" height="373" alt="image" src="https://github.com/user-attachments/assets/d11f10bf-cd31-4e98-b382-af30d8a2b7ad" />


### Adaptive Thresholding
<img width="332" height="373" alt="image" src="https://github.com/user-attachments/assets/a11dfb05-a7df-4f14-9b57-f2408231e0c2" />


### Optimum Global Thesholding using Otsu's Method

<img width="292" height="358" alt="image" src="https://github.com/user-attachments/assets/4c550004-55a4-4fad-bc70-a1529f78cafe" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
