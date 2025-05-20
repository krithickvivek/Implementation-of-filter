# Implementation-of-filter

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By: Krithick Vivekananda 
### Register Number: 212223240075
</br>

### 1. Smoothing Filters

#### i) Using Averaging Filter

```Python
import cv2
import numpy as np
import matplotlib.pyplot as 
image = cv2.imread('DarkKnight.png', cv2.IMREAD_GRAYSCALE)
kernel = np.ones((4, 4), np.float32) / 9
averaged_image = cv2.filter2D(image, -1, kernel)
plt.imshow(averaged_image, cmap='gray')
plt.title("Averaging Filter")
plt.axis('off')
plt.show()
```

#### ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

#### iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

#### iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters

#### i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

#### ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:

### Original image
![image](https://github.com/user-attachments/assets/ac384aee-e66a-47cc-8b99-af60ebc0b656)

### 1. Smoothing Filters
</br>

#### i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/8bd30110-0232-4622-aa06-17743b64e997)
#### ii) Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/9e8053a8-691f-4e45-b5d3-9bc33fbaf834)
#### iii) Using Gaussian Filter
![image](https://github.com/user-attachments/assets/042a0330-fd8d-4a63-9ce9-b46d96c8b90e)
#### iv) Using Median Filter
![image](https://github.com/user-attachments/assets/e3070b53-6eb1-4476-ae0e-326cdd381ae6)
### 2. Sharpening Filters
</br>

#### i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/2a3a4d15-dbab-43d4-978b-959f8025dfc9)
#### ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/f75f1e38-6d50-4316-99b0-9a4a7d94569e)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
