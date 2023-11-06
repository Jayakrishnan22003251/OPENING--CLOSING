# OPENING--CLOSING
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
Use Closing Operation.

 
## Program:
```
NAME : JAYAKRISHNAN
REGISTER NUMBER : 212222230052
```

### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

```


### Create the Text using cv2.putText
```
# Create the text using cv2.putText
img = np.zeros((100, 550), dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JAYAKRISHNAN', (5, 70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

```


### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11, 11))

```


### Use Opening operation

```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)

```


### Use Closing Operation

```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)

```
## Output:

### Display the input Image
![Untitled-1](https://github.com/Jayakrishnan22003251/OPENING--CLOSING/assets/120232371/5f46d786-d2a4-439d-bae2-3b7617d1de31)


### Display the result of Opening
![Untitled](https://github.com/Jayakrishnan22003251/OPENING--CLOSING/assets/120232371/f3014f30-3591-4ba6-a125-27487868a90b)


### Display the result of Closing
![Untitled-1](https://github.com/Jayakrishnan22003251/OPENING--CLOSING/assets/120232371/f73db783-2e40-42ef-b67e-c8dbc1058f73)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
