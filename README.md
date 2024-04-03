# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY : Yogabharathi S
REG NO : 212222230179
```
## Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("flower.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
# SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
# SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
# SOBEL X AXIS :
![image](https://github.com/Yogabharathi3/EDGE-DETECTION/assets/118899387/186d6a69-325a-4518-83e4-52aeda939b25)


# SOBEL Y AXIS :

![image](https://github.com/Yogabharathi3/EDGE-DETECTION/assets/118899387/21712dde-3f30-4573-8378-740eaead238b)

# SOBEL XY AXIS :

![image](https://github.com/Yogabharathi3/EDGE-DETECTION/assets/118899387/518e030d-141a-4299-b6e5-630aff029de6)

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/Yogabharathi3/EDGE-DETECTION/assets/118899387/4fcac3af-af78-456c-a878-341e1e278cef)

### CANNY EDGE DETECTOR
![image](https://github.com/Yogabharathi3/EDGE-DETECTION/assets/118899387/9bae9993-1abc-4704-9e02-c7582223ff85)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
