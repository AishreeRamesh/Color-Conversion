### EX NO : 03
### DATE  : 12.04.2022
# <p align="center">Color Conversion</p>

## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.
<br>

### Step2:
Read the saved image using cv2.imread("filename.jpg").
<br>

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) 
and similarly for other color formats. 
<br>

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]) 
<br>

### Step5:
Output the image using cv2.imshow("OUTPUT", image)

<br>

## Program:
```python
# Developed By:Aishree Ramesh
# Register Number:212220230003
```
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
house_color_image = cv2.imread('house.jpg')
cv2.imshow('original image',house_color_image)
hsv_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```python

import cv2
img = cv2.imread("Mor.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```python 

import cv2
img = cv2.imread("lucifer.jpg")
img1= cv2.resize(img, (270,190))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCRCB ", img_ycrcb)
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# iv)Split and Merge RGB Image
```python 

import cv2
img = cv2.imread("book.jpg")
img1= cv2.resize(img, (270,190))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# v) Split and merge HSV Image
```python 

import cv2
img = cv2.imread("marvel.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:
### i) BGR and RGB to HSV and GRAY
![image](https://user-images.githubusercontent.com/70213227/162403201-8f947432-d8fa-4bf9-ac04-dcf2341931ba.png)


### ii) HSV to RGB and BGR
![image](https://user-images.githubusercontent.com/70213227/163847117-2023e285-f432-403a-be34-13acb09c69c5.png)

### iii) RGB and BGR to YCrCb
![image](https://user-images.githubusercontent.com/70213227/163847763-383bee04-8d31-4d48-89e9-d9c3ce8303b2.png)

### iv) Split and merge RGB Image
![image](https://user-images.githubusercontent.com/70213227/163847868-3d8d6dd4-68d8-4376-b78e-dde564005d86.png)

### v) Split and merge HSV Image
![image](https://user-images.githubusercontent.com/70213227/163848021-a22238c5-5b9f-47bf-b818-ffb972b087d6.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
