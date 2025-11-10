# OPENING--AND-CLOSING
# Name: K Charan Teja
# Reg No: 212224040163
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
 Import the necessary packages


### Step2:
 Give the input text using cv2.putText()


### Step3:
 Perform opening operation and display the result


### Step4:
 Similarly, perform closing operation and display the result



 
## Program:

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'SIVA DINESH',(5,70), font,2,(255),5,cv2.LINE_AA)

```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation

```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<br>
<br>
<img width="473" height="486" alt="Screenshot 2025-11-10 222411" src="https://github.com/user-attachments/assets/ce594d07-b13f-44b9-ae29-62c83074c8a2" />

<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<img width="670" height="160" alt="image" src="https://github.com/user-attachments/assets/939287e3-0176-49b9-a3de-fa816b7f351f" />

<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="622" height="162" alt="image" src="https://github.com/user-attachments/assets/1dbec49a-11f7-4e77-ab46-0d3040398b09" />

<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
