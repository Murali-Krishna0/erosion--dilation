# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
<br> import the neccesary packages


### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image

 
## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Input Image with Text")
plt.axis('off')
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  
plt.title("Eroded Image")
plt.axis('off')
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

![image](https://github.com/user-attachments/assets/c3c5689b-863f-41b2-8025-6e9c3e464ca2)

![image](https://github.com/user-attachments/assets/0deb8f43-80f6-4153-b186-55c4f1d347a9)

![image](https://github.com/user-attachments/assets/6c99c9ff-991a-4105-907b-353ed7deb17c)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
