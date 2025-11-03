# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

```
#NAME: CHARU NETHRA R
#REG NO:212223230035
import cv2
import numpy as np
import matplotlib.pyplot as plt

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Charu",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

<img width="746" height="408" alt="image" src="https://github.com/user-attachments/assets/3137b549-ba9d-45ca-80df-a8b723f64827" />

### Display the result of Opening

<img width="743" height="404" alt="image" src="https://github.com/user-attachments/assets/74d8fc1c-289e-443c-8b94-234900975399" />

### Display the result of Closing

<img width="744" height="402" alt="image" src="https://github.com/user-attachments/assets/0a669330-f217-48d5-a595-2574c141ff6a" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
