# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.
<br>

### Step2:
Read the original Image.
<br>

### Step3:
Store the required conversion of the image in a variable.
<br>

### Step4:
Show the image stored in the given variable.
<br>

### Step5:
Destroy all the windows and end the program.
<br>

## Program:
python
# Developed By: JEEVAGOWTHAM S 
# Register Number: 212222230053
i) Convert BGR and RGB to HSV and GRAY
```
import cv2

flower_image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', flower_image)

hsv_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_bgr_image)

hsv_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_rgb_image)

gray_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_bgr_image)

gray_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_rgb_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```




# ii)Convert HSV to RGB and BGR
```
import cv2

flower_hsv_image = cv2.imread('flower.jpg')
cv2.imshow('Original HSV Image', flower_hsv_image)

rgb_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB', rgb_image)

bgr_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR', bgr_image)

cv2.waitKey(0)
cv2.destroyAllWindows()



```




# iii)Convert RGB and BGR to YCrCb
```
import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
ycrcb_image_rgb = cv2.cvtColor(image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb', ycrcb_image_rgb)
ycrcb_image_bgr = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb', ycrcb_image_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



# iv)Split and Merge RGB Image
```


import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel', blue)
cv2.imshow('G-Channel', green)
cv2.imshow('R-Channel', red)
merged_bgr = cv2.merge((blue, green, red))
cv2.imshow('Merged BGR Image', merged_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




# v) Split and merge HSV Image
```
import cv2

image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)

hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)

cv2.imshow('Hue - Image', h)
cv2.imshow('Saturation - Image', s)
cv2.imshow('Value - Image', v)

merged_hsv = cv2.merge((h, s, v))
cv2.imshow('Merged HSV Image', merged_hsv)

cv2.waitKey(0)
cv2.destroyAllWindows()


```




## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot 2023-08-26 093221](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/d10a08f6-126d-412a-b036-b59ecfc3d027)
![Screenshot 2023-08-26 093237](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/14a73797-d8f4-4ece-a78a-9d754290031f)
![Screenshot 2023-08-26 093257](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/f2a3ba80-1144-4fce-95d9-bb692d9531b3)
![Screenshot 2023-08-26 093321](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/fa12641c-fa91-4101-9aaa-7e02ae26b536)


<br>
<br>

### ii) HSV to RGB and BGR
![Screenshot 2023-08-26 093504](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/9ebf255a-4765-4d00-9366-fc04010285ba)
![Screenshot 2023-08-26 093517](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/0908f1a6-03b2-4185-899a-ab22229c695b)


<br>
<br>

### iii) RGB and BGR to YCrCb
![Screenshot 2023-08-26 093639](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/18eda8e4-7ae0-4f21-bf8f-c3e691a4d3b3)
![Screenshot 2023-08-26 093631](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/ea4b50f2-d466-4c43-9a45-8c257ddf41f9)


<br>
<br>

### iv) Split and merge RGB Image
![Screenshot 2023-08-26 093921](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/c9968b93-8e7e-4ff5-ae38-7f91adf1976f)
![Screenshot 2023-08-26 093913](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/1280171b-9c0a-4d74-8748-f0b504faa002)
![Screenshot 2023-08-26 093854](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/a39240df-61b1-47de-a1a8-ac00b1a8db82)
![Screenshot 2023-08-26 093905](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/656c5159-8b36-4db1-b1b8-f85e1a5e5ead)



<br>
<br>

### v) Split and merge HSV Image
![Screenshot 2023-08-26 094237](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/62760179-d1d9-4017-bfd2-70f4ce158603)
![Screenshot 2023-08-26 094248](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/038ffcf8-45d0-4a74-8c31-e351d985a459)
![Screenshot 2023-08-26 094258](https://github.com/JeevaGowtham-S/COLOR-CONVERSION/assets/118042624/8fb8c69c-ac6e-4b04-a9a0-1ca15edfe49c)


<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
