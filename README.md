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
# Developed By: YUGABHARATHI M
# Register Number: 212224230314
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('a.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
  
## Output:
### Input Grayscale Image and Color Image

<img width="552" height="415" alt="image" src="https://github.com/user-attachments/assets/f0055634-defa-4143-8f73-f65afbffdbb7" />






<img width="548" height="408" alt="image" src="https://github.com/user-attachments/assets/058b2213-5760-4bea-8487-d24c56b3679f" />




### Histogram of Grayscale Image and any channel of Color Image


<img width="622" height="446" alt="image" src="https://github.com/user-attachments/assets/a600efca-96ca-4d0a-9256-16e85f3e8c33" />



### Histogram Equalization of Grayscale Image.


<img width="637" height="481" alt="image" src="https://github.com/user-attachments/assets/0ffb6252-565f-4a22-81b7-8fcbd70a7945" />









## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
