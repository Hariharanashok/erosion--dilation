# EX-09-Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Initialize an Empty Image:

Create a black image of size 100x600 pixels.
### Step-2:Add Text to the Image:

Use a specified font to write the word "Dhiyaneshwar" on the image at a defined position.
### Step-3:Display the Original Image:

Show the image containing the text without axis labels.
### Step-4:Create Structuring Elements:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:Erode the Image:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:Dilate the Image:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
```
Developed By: HARIHARAN A
Reference Number : 212222100012
``` 
# Import the necessary packages

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HARIHARAN A',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
## Output:
![image](https://github.com/user-attachments/assets/9c33546c-a3be-423b-8743-702f2040a4c9)




# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
## Output:
![image](https://github.com/user-attachments/assets/c2391ad4-45c3-4d17-b13e-1ecef55a2f08)




# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
## Output:
![image](https://github.com/user-attachments/assets/aeb87cf0-6dfe-483f-a90a-df17cfe901ab)




# Dilate the image

```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:
![image](https://github.com/user-attachments/assets/a1427d47-a3e0-4ff8-b276-c6d9cb86c4dc)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
