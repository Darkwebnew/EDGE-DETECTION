# EX-06 EDGE-DETECTION
## Date: 05-04-2024
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
Developed By: Sriram.V
Register No: 212222103002

# Import the packages
import cv2

# Load the image, Convert to grayscale and remove noise
i=cv2.imread('land.jpeg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()


# LAPLACIAN EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### ORIGINAL IMAGE

![Blue Moon](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/cd89118b-95d6-49b0-aa80-e01b6bd1e1f4)

### SOBEL EDGE DETECTOR

![Screenshot 2024-04-12 142100](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/6cef316b-b83a-4843-b7c7-eb2cd15850d1)
![Screenshot 2024-04-12 142122](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/c1951fb9-e949-47a3-b3d1-935e7dc5e285)
![Screenshot 2024-04-12 142131](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/e2e94e52-8827-44e0-826f-756d5bbf51f9)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-04-12 142142](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/82321c3a-bddf-4407-b306-7016395ee3e7)

### CANNY EDGE DETECTOR

![Screenshot 2024-04-12 142151](https://github.com/Darkwebnew/EDGE-DETECTION/assets/143114486/d32ba108-76f7-481e-8fd5-344cd7ef6e4f)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
