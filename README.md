# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
```python
### Developed By: Raja R
### Register Number: 212222100041
```

## Output:

<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    !pip install google-colab
from google.colab.patches import cv2_imshow
    
    import cv2
    image=cv2.imread('green.jpg',1)
    image=cv2.resize(image,(500,300))
    cv2_imshow(image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>
    
### OUTPUT:
![Screenshot 2024-02-15 153749](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/0c3de497-12a6-43de-97b0-86e94ecbc28a)

  </td>
  </tr>
 
   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('green.jpg',0)
    cv2.imwrite('d.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/1f07ecec-e724-4ae7-a9ac-5a386f40adf8)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('green.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/2d975d21-4c91-41a3-bc13-5d4e75800cd7)


  </td>
  </tr>
  <tr>
    <td>

### iv)Access rows and columns
```Python
   !pip install google-colab
from google.colab.patches import cv2_imshow
import random
import cv2
image=cv2.imread('green.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
  for j in range(image.shape[1]):
    image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/242b0118-f410-4fd8-860f-bc7db56dc8cf)



  </td>
  </tr>
  <tr>
    <td width=50%>

### v)Cut and paste portion of image

 ```Python
    !pip install google-colab
from google.colab.patches import cv2_imshow
import cv2
import numpy as np
image=cv2.imread('green.jpg',1)
image = cv2.resize(image, (400, 400))
print(image.shape)
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2_imshow(image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/194e6cfb-05e4-4e3f-9a1e-51461f55cd05)



  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('green.jpg',1)
img = cv2.resize(img,(300,200))
cv2_imshow(img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2_imshow(hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2_imshow(hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2_imshow(gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2_imshow(gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
  <td>
    
### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/51f6fa0e-82e5-4908-bdb0-9fe998f93f52)

![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/de509fa8-0a64-420c-bd3d-4bc745f30251)


</td>
  </tr>
</table>


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('green.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2_imshow(img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2_imshow(RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2_imshow(BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/aa17b39f-63d0-4b6d-bf7a-e90c6d376f87)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('green.jpg')
img = cv2.resize(img,(300,200))
cv2_imshow(img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2_imshow(YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2_imshow(YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/f424a3a4-b512-4525-97c8-32ed24c045f1)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('green.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2_imshow(R)
cv2_imshow(G)
cv2_imshow(B)
merged = cv2.merge((B,G,R))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/99f3ed63-5f2a-4b2b-923e-7d5dfa59d52c)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("green.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2_imshow(H)
cv2_imshow(S)
cv2_imshow(V)
merged = cv2.merge((H,S,V))
cv2_imshow(merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![image](https://github.com/Raja8334/COLOR_CONVERSIONS_OF-IMAGE/assets/120719634/603fc1e1-3e14-42fa-abb4-bbad100cd4d7)





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







