# EXP - 03
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
## Developed By: SHARAN KUMAR G
## Register Number: 212224230260
```python

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('rose.jpeg')

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

<img width="338" height="548" alt="image" src="https://github.com/user-attachments/assets/a36e5828-5cd9-41b2-af05-b6e02294c9a8" />
<img width="342" height="540" alt="image" src="https://github.com/user-attachments/assets/2a886281-11e0-43ed-be1d-37fe511b7c4b" />



### Histogram of Grayscale Image and any channel of Color Image

<img width="728" height="547" alt="image" src="https://github.com/user-attachments/assets/2c661240-90ea-4dcd-9b87-b9d20623fc76" />
<img width="726" height="547" alt="image" src="https://github.com/user-attachments/assets/51b61705-4a48-457c-8743-e1d409d24786" />



### Histogram Equalization of Grayscale Image.

<img width="1347" height="406" alt="image" src="https://github.com/user-attachments/assets/58371cd6-0a57-42c6-a289-0ef5974b6989" />



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
