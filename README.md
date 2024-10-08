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
```
### Step 1: Create a blank image
```
image = np.zeros((300, 600, 3), dtype="uint8")
```
### Step 2: Create the text using cv2.putText
```
text = "Naveen Kumar"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
```
### Step 3: Create a structuring element (5x5 rectangular)
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
### Step 4: Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
### Step 5: Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
### Convert images from BGR to RGB for Matplotlib
```
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
```
### Plot the original, eroded, and dilated images using Matplotlib
```
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()


```


## Output:

![output9](https://github.com/user-attachments/assets/1fdb5281-c34a-4f22-81b4-d4a47da43e79)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
