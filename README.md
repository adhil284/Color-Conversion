# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
   Read an image using imread() and Convert BGR and RGB to HSV and GRAY<br>
  using:<br>
  cv2.cvtColor(image,cv2.COLOR_RGB2HSV)<br>
  cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)<br>
  cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br>
  cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
  
### Step2:
  Convert HSV to RGB and BGR<br>
  using:<br>
  cv2.cvtColor(image,cv2.COLOR_HSV2RGB)<br>
  cv2.cvtColor(image,cv2.COLOR_HSV2BGR)  
### Step3:
  Convert RGB and BGR to YCrCb<br>
    using:<br>
    cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)<br>
    cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
### Step4:
   Split and Merge RGB Image<br>
    using:<br>
    blue = image[:,:,0]<br>
    green = image[:,:,1]<br>
    red = image[:,:,2]<br>
    cv2.merge((blue,green,red))

### Step5:
   Split and merge HSV Image<br>
    using:<br>
    hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br>
    h, s, v = cv2.split(hsv)<br>
    cv2.merge((h,s,v))

## Program:
### Developed By: Mohamed Fashroon Adhil I
### Register Number: 212220230032
```python
# i) Convert BGR and RGB to HSV and GRAY
    import cv2
    color=cv2.imread('tower.jpg')
    hsv=cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
    cv2.imshow('BGR_HSV',hsv)
    hsv2=cv2.cvtColor(color,cv2.COLOR_RGB2HSV)
    cv2.imshow('RGB_HSV',hsv2)
    hsv3=cv2.cvtColor(color,cv2.COLOR_BGR2GRAY)
    cv2.imshow('BGR_GRAY',hsv3)
    hsv4=cv2.cvtColor(color,cv2.COLOR_RGB2GRAY)
    cv2.imshow('RGB_GRAY',hsv4)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR
    rgb=cv2.cvtColor(hsv2,cv2.COLOR_HSV2RGB)
    cv2.imshow('HSV_RGB',rgb)
    bgr=cv2.cvtColor(hsv2,cv2.COLOR_HSV2BGR
    cv2.imshow('HSV_BGR',bgr) 
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb
    ycrcb=cv2.cvtColor(color,cv2.COLOR_RGB2YCrCb)
    cv2.imshow('RGB_YCrCB',ycrcb)
    ycrcb1=cv2.cvtColor(color,cv2.COLOR_BGR2YCrCb)
    cv2.imshow('BGR_YCrCB',ycrcb1)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
    blue=color[:,:,0]
    green=color[:,:,1]
    red=color[:,:,2]
    cv2.merge((blue,green,red))
    cv2.imshow("blue",blue)
    cv2.imshow("green",green)
    cv2.imshow("red",red)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# v) Split and merge HSV Image
  hsv5=cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
  cv2.imshow("ORIGINAL HSV",hsv5)
  h , s, v = cv2.split(hsv5)
  cv2.imshow('h_plane',h)
  cv2.imshow('s_plane',s)
  cv2.imshow('v_plane',v)
  mergedhsv=cv2.merge((h,s,v))
  cv2.imshow('merged',mergedhsv)
  cv2.waitKey(0)

```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (40)](https://user-images.githubusercontent.com/75235759/163123040-5dcabd1a-12e6-4b47-a6d2-15815a3a0f6f.png)



### ii) HSV to RGB and BGR
![Screenshot (41)](https://user-images.githubusercontent.com/75235759/163123079-3bcaa8cb-5e35-41a3-ba04-08fa26e7d563.png)



### iii) RGB and BGR to YCrCb

![Screenshot (42)](https://user-images.githubusercontent.com/75235759/163123137-73988590-33c0-4e9a-90f3-3f99668cc092.png)

### iv) Split and merge RGB Image

![Screenshot (43)](https://user-images.githubusercontent.com/75235759/163123188-b688b75a-2281-463c-80dd-913cf29c7639.png)


### v) Split and merge HSV Image


![Screenshot (44)](https://user-images.githubusercontent.com/75235759/163123232-e32c194d-ffc4-48ac-a891-3aaf2add484a.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
