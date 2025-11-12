# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Load the input image using cv2.imread().

### Step2:
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().

### Step3:
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.

### Step4:
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.

### Step5:
Use plt.subplot() to show the original, opening, and closing images side by side.

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,700),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Priya Varshini",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image

<img width="880" height="416" alt="Screenshot 2025-11-12 110843" src="https://github.com/user-attachments/assets/f3f16950-6d5b-4bc2-98b3-82d52f1925fa" />



### Display the result of Opening

<img width="881" height="417" alt="Screenshot 2025-11-12 111003" src="https://github.com/user-attachments/assets/6c743f6b-09df-4156-814a-3db5aebc6635" />



### Display the result of Closing

<img width="878" height="418" alt="image" src="https://github.com/user-attachments/assets/b896cd18-587e-4fd3-bf26-53f05dadb294" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
