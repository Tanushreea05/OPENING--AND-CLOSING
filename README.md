# OPENING--AND-CLOSING
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
# Name: Tanushree A
# Reg No: 212223100057

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Tanushree A', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))

# Use Opening operation
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

# Use Closing Operation
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")




```
## Output:

### Display the input Image
<img width="716" height="159" alt="image" src="https://github.com/user-attachments/assets/9055144a-5f71-42cf-8fbc-f9cfb58eb6b4" />

### Display the result of Opening
<img width="862" height="171" alt="image" src="https://github.com/user-attachments/assets/2c5842bf-0d8a-4e93-a3e2-e0713f151069" />


### Display the result of Closing
<img width="846" height="165" alt="image" src="https://github.com/user-attachments/assets/048d3ea8-28d5-471d-acc5-9b85cd8cbda7" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
