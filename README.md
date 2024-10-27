# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV  
## Algorithm:
### Step1:
Import the necessary pacakages
### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Erode the image
### Step5:
Dilate the image
## Program:
#### Developed by : SRINITHI V
#### Register.No  : 212222110046
### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = np.zeros((100, 500), dtype='uint8')
```
### Create the Text using cv2.putText
```python
cv2.putText(img, 'SRINITHI V', (60, 70), cv2.FONT_HERSHEY_COMPLEX, 2, (255), 5)
```
### Create the structuring element
```python
kernel_size = (5, 5)  
structuring_element = cv2.getStructuringElement(cv2.MORPH_RECT, kernel_size)

eroded_image = cv2.erode(img, structuring_element, iterations=1)

dilated_image = cv2.dilate(img, structuring_element, iterations=1)

plt.figure(figsize=(9, 3))
```
### Display the input Image
```python
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')
plt.show()
```
### Output:
![Screenshot 2024-10-27 214641](https://github.com/user-attachments/assets/8340c94d-6a82-4893-9bf2-92c74b62aaf9)

### Display the Eroded Image
```python
plt.figure(figsize=(9, 3))
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')
```
### Output:
![Screenshot 2024-10-27 214658](https://github.com/user-attachments/assets/66ad819a-2548-49d9-832a-71acb6ed1c77)

### Display the Dilated Image
```python
plt.figure(figsize=(9, 3))
plt.imshow(dilated_image, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')
```
### Output:
![Screenshot 2024-10-27 214712](https://github.com/user-attachments/assets/568e4301-c894-4f38-9362-91108487e4ca)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
