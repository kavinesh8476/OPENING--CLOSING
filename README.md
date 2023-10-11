# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening operation
<br>
### Step5:
Use Closing Operation
<br>
## Program:
```
Developed by:Kavinesh M
Register Number:212222230064
```

# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
``` Python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'KAVINESH M',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
``` Python
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
```

# Use Closing Operation

``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image
<br>

![image](https://github.com/kavinesh8476/OPENING--CLOSING/assets/118466561/a31190ad-407b-41ce-be14-d1d68afa89a6)

<br>

### Display the result of Opening
<br>

![image](https://github.com/kavinesh8476/OPENING--CLOSING/assets/118466561/19245638-26ad-46a2-b523-a87540c942b6)

<br>

### Display the result of Closing
<br>

![image](https://github.com/kavinesh8476/OPENING--CLOSING/assets/118466561/713f61a2-dffe-4669-a1f1-7ad2c79fb13b)

<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
