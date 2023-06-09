## Ex-7  Edge-Detection

### Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

### Software Required:
Anaconda - Python 3.7

### Algorithm:
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
 
### Program:
```
Name : Silambarasan K
Reg No : 212221230101
```
``` Python
# Import the packages 
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
```
```py
# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()


# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()
```
```py
# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()
```
```py
# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("alaskan.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### INPUT IMAGE:
![d1](https://user-images.githubusercontent.com/94525786/232544206-0fb9e8ac-e2e1-4675-89f9-8977592861f9.png)


### SOBEL EDGE DETECTOR:
### SOBEL-X:
![d2](https://user-images.githubusercontent.com/94525786/232544225-e7b77cb3-63f4-4ae6-8ab7-86b9a196ebcc.png)

### SOBEL-Y:

![d3](https://user-images.githubusercontent.com/94525786/232544249-b9df9178-5042-4613-8197-720f361cec79.png)

### SOBEL-XY:
![d4](https://user-images.githubusercontent.com/94525786/232544139-1c5c1982-f9a6-481f-bd64-90e144ad1f8c.png)

### LAPLACIAN EDGE DETECTOR:
![d5](https://user-images.githubusercontent.com/94525786/232544328-52654af0-b642-4df1-9029-0294a4ad1e5f.png)

### CANNY EDGE DETECTOR:
![d6](https://user-images.githubusercontent.com/94525786/232544081-8b02159c-37e3-4bbd-b2bd-8343f98b774a.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
