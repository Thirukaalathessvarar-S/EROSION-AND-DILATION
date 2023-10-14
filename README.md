# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using plt.erode and plt.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:

```
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"ESWAR S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Dilate the image
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```

## Output:

### Display the input Image
![dip10_1](https://github.com/Thirukaalathessvarar-S/EROSION-AND-DILATION/assets/121166390/e5b853ca-5a09-4257-81a4-29db58d41c17)


### Display the Eroded Image
![dip10_2](https://github.com/Thirukaalathessvarar-S/EROSION-AND-DILATION/assets/121166390/b1f63ff0-1c31-481a-a449-795d6caff742)


### Display the Dilated Image
![dip10_3](https://github.com/Thirukaalathessvarar-S/EROSION-AND-DILATION/assets/121166390/4b44d842-004a-4bcb-bea4-ca572b5f1177)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
