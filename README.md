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
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Show the images using cv2.imshow().
 
## Program:
```
/*
Developed by   : DHANASEKAR.G
Register Number: 212220230009
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,800),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Dineshkumar V",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Display the input Image

![xc1](https://user-images.githubusercontent.com/75264748/172206873-2880a80c-9f6f-4ad4-9acf-b1977af90935.jpg)


### Display the result of Opening


![xc2](https://user-images.githubusercontent.com/75264748/172206877-aa192cf3-8d21-40c2-a41d-c92630481bc7.jpg)

### Display the result of Closing
![xc3](https://user-images.githubusercontent.com/75264748/172206896-4d3eeaa4-59bf-4dda-9da5-aade05a1b2b1.jpg)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
