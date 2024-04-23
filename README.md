# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Read and show the image
### Step2
Apply the filtering technique that we want to perform
### Step3
Show the filtered image

## Program:
### Developed By   :  Rakesh V
### Register Number:  212222110036
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel1 = np.ones((11,11),np.float32)/121
box_filter = cv2.filter2D(original_image,-1,kernel1)
cv2.imshow('box_filter',box_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
ii) Using Weighted Averaging Filter
```Python

#ii) Using Weighted Averaging Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
cv2.imshow('weighted_filter',weighted_filter)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
iii) Using Gaussian Filter
```Python
#iii) Using Gaussian Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0,
sigmaY=0)
cv2.imshow('gaussian_filter',gaussian_blur)
cv2.waitKey(0)
cv2.destroyAllWindows()





```

iv) Using Median Filter
```Python

#iv) Using Median Filter
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
median = cv2.medianBlur(src=original_image,ksize = 11)
cv2.imshow('median_filter',median)
cv2.waitKey(0)
cv2.destroyAllWindows()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


#i) Using Laplacian Kernal
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
cv2.imshow('laplacian_kernel',laplacian_kernel)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
ii) Using Laplacian Operator
```Python
#ii) Using Laplacian Operator
import cv2
import numpy as np
image = cv2.imread("cat.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
cv2.imshow('original',original_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()






```

## OUTPUT:
### original image
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/1370b0eb-3512-46d3-8922-f08b574ac61d)


### 1. Smoothing Filters


i) Using Averaging Filter
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/20737097-28ad-4d1d-ad60-e78df18007fe)
ii) Using Weighted Averaging Filter
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/484858e8-1800-4f14-bacf-fb50c9faa635)

iii) Using Gaussian Filter
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/d6b36837-ed24-4762-a65d-380d585e9b4d)

iv) Using Median Filter
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/30e7df1f-c6aa-4589-bb1d-915c2ef3ff1d)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/afab7b25-f3bc-4bf8-9ae6-d5008c2f2136)


ii) Using Laplacian Operator
![image](https://github.com/rakeshcoder2004/Implementation-of-filter/assets/121490890/4fcd617a-afc0-4f40-b67e-946ffe3ff4e0)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
