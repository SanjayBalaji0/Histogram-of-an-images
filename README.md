# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Sanjay Balaji S
# Register Number: 212223240149
```
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("C:/Users/admin/SanjayBalaji/DIPT/Eaglegray.jpg")
color_image = cv2.imread("C:/Users/admin/SanjayBalaji/DIPT/Colour.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

```
import numpy as np
import cv2
Gray_image = cv2.imread("C:/Users/admin/SanjayBalaji/DIPT/Eaglegray.jpg")
Color_image = cv2.imread("C:/Users/admin/SanjayBalaji/DIPT/Colour.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```
import cv2
gray_image = cv2.imread("C:/Users/admin/SanjayBalaji/DIPT/Eaglegray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/aff284bc-d12f-4ee7-a79b-2aef8da412fb)

![image](https://github.com/user-attachments/assets/fa27b407-6c09-4555-ba4b-bec9b73aab36)

### Histogram of Grayscale Image and any channel of Color Image
## Grayscale image
![image](https://github.com/user-attachments/assets/9b0d5642-a710-4ead-94d3-ecdb90b53028)

## Colour Image
![image](https://github.com/user-attachments/assets/08899956-167a-4898-970b-c5a9e9e75b4c)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/8d0f9148-051d-48c5-98bc-b1bc663dc5b3)

![image](https://github.com/user-attachments/assets/3d57196b-8d76-4329-acf8-dd7735f74745)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
