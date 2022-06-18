# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the Text using cv2.putText.
### Step3:
Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation



 
## Program:

``` Python
Developed by: NITHISHWAR S
Register num: 212221230071
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,' NITHISHWAR ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)



```
## Output:

### Display the input Image:

![image](https://user-images.githubusercontent.com/94164665/174433869-725012cd-9f7c-40a7-821b-498c5e960c78.png)

### Display the result of Opening:
![image](https://user-images.githubusercontent.com/94164665/174433860-304d7df1-898b-49df-8857-9784e8695195.png)


### Display the result of Closing:
![image](https://user-images.githubusercontent.com/94164665/174433855-5ea90ff6-2266-415e-956b-60ddbf449da0.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
