# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed by :  P Ramsai
Register no  : 212221240041
```

### Convert image to grayscale and remove noise:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("ramss.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### Sobel Edge Detector:
#### SOBEL X AXIS: 
```python
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

#### SOBEL Y AXIS:
```python 
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

#### SOBEL XY AXIS: 
```python 
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

### laplacian edge Detector:
```python
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

### Canny Edge Detector:
```python 
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
### SOBEL EDGE DETECTOR :
#### SOBEL X AXIS :
![image](https://github.com/Ramsai1234/EDGE-DETECTION/assets/94269989/4f2ee139-9243-4ed9-9722-09b6c3736e94)

#### SOBEL Y AXIS :
![image](https://github.com/Ramsai1234/EDGE-DETECTION/assets/94269989/61331dea-6801-48f5-ae0f-92e1f6972773)

#### SOBEL XY AXIS :
![image](https://github.com/Ramsai1234/EDGE-DETECTION/assets/94269989/e9b4fa98-0538-4028-81b4-03b54a378bb4)

### LAPLACIAN EDGE DETECTOR :
![image](https://github.com/Ramsai1234/EDGE-DETECTION/assets/94269989/e4eb979f-c137-41a2-a20d-7a55f3fa357f)

### CANNY EDGE DETECTOR :
![image](https://github.com/Ramsai1234/EDGE-DETECTION/assets/94269989/cb6fff33-c60a-4f3d-982b-de1160f0a749)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
