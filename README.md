# OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
Step1:
Import the necessary packages

Step2:
Give the input text using cv2.putText()

Step3:
Perform opening operation and display the result

Step4:
Similarly, perform closing operation and display the result

## Program:
Developed By: Sabari Akash A

Register no: 212222230124
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Datascientist',(5,70), font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

```
# Output:
Display the input Image
![326241337-ecea916f-3d46-47e0-a0d1-3b2844b407eb](https://github.com/Sabariakash22009103/OPENING--AND-CLOSING/assets/119390227/2a87c64d-ba78-4595-81d0-519530b0d116)

Display the result of Opening
![326241342-3a6027e5-f105-437e-a11f-b9e255ba32ae](https://github.com/Sabariakash22009103/OPENING--AND-CLOSING/assets/119390227/e53f4061-6a68-474b-b1c5-98a57c458914)

Display the result of Closing
![326241354-eb44b501-9cdb-4871-bd38-8f40e9e2ffe1](https://github.com/Sabariakash22009103/OPENING--AND-CLOSING/assets/119390227/e1d210c8-9add-4496-8f18-190065c455c0)

# Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
