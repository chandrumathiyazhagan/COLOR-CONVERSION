# COLOR-CONVERSION
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
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
<br>

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]).
<br>

### Step5:
Output the image using cv2.imshow("OUTPUT", image).


<br>

## Program:
```python
# Developed By:M.Chandru
# Register Number:212222230026
```
# i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
houseImage = cv2.imread('chan.jpeg')
cv2.imshow('212222230026_MChandru',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```python
import cv2
houseHSVImage = cv2.imread('chan.jpeg')
cv2.imshow('212222230026_MChandru',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```python
import cv2
houseImage = cv2.imread('chan.jpeg')
cv2.imshow('212222230026_MChandru',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iv)Split and Merge RGB Image
```python
import cv2
image = cv2.imread('chan.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('212222230026_Mchandru',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# v) Split and merge HSV Image
```python
import cv2
image = cv2.imread('chan.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('212222230026_Mchandru',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow()
```

## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot from 2023-08-26 22-10-37](https://github.com/chandrumathiyazhagan/COLOR-CONVERSION/assets/119393023/85fd5eb5-726a-4baa-88fd-8ac3646d4038)

<br>
<br>

### ii) HSV to RGB and BGR
![Screenshot from 2023-08-26 22-17-38](https://github.com/chandrumathiyazhagan/COLOR-CONVERSION/assets/119393023/0c10d1d3-5848-4917-9aa7-d08f05d64a8f)

<br>
<br>

### iii) RGB and BGR to YCrCb
![Screenshot from 2023-08-26 22-23-24](https://github.com/chandrumathiyazhagan/COLOR-CONVERSION/assets/119393023/ffc35738-d62b-4286-be94-1024e0e69ac0)

<br>
<br>

### iv) Split and merge RGB Image
![Screenshot from 2023-08-26 22-30-55](https://github.com/chandrumathiyazhagan/COLOR-CONVERSION/assets/119393023/36586677-8586-451f-9103-fcca9fb80fee)

<br>
<br>

### v) Split and merge HSV Image
![Screenshot from 2023-08-26 22-38-38](https://github.com/chandrumathiyazhagan/COLOR-CONVERSION/assets/119393023/76a8c92d-ba63-4db4-923b-6c31982aaff3)

<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
