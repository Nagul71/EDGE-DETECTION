# EDGE-DETECTION
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

## PROGRAM:
```python
DEVELOPED BY: NAGUL K
REGISTER NO: 212222230089
```
```python
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("FLOWER.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
img = cv2.GaussianBlur(gray,(3,3),0)

```
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS ,SOBEL Y AXIS , SOBEL XY AXIS
```python
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1),plt.imshow(img,cmap='gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])
plt.show()
plt.subplot(2,2,1),plt.imshow(sobelx,cmap='gray')
plt.axis('off')
plt.show()
plt.subplot(2,2,1),plt.imshow(sobely,cmap='gray')
plt.axis('off')
plt.show()
plt.subplot(2,2,1),plt.imshow(sobelxy,cmap='gray')
plt.axis('off')
plt.show()

```

### LAPLACIAN EDGE DETECTOR
```python
laplacian=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(laplacian)
plt.subplot(2,2,1),plt.imshow(laplacian,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')
plt.show()
```
### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
## ORIGINAL IMAGE:
![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/1182ddf6-0a4e-4fdf-b11d-d0e0101dd58b)


### SOBEL EDGE DETECTOR
#### SOBEL X AXIS
![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/eb626b3f-598d-4c22-a737-a69708e11f43)




#### SOBEL Y AXIS

![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/91c34a60-10b3-4cc5-8f29-cbff1f4f68ba)



#### SOBEL XY AXIS

![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/9f2cdcbf-af11-4110-85c1-687e39b90b4f)


### LAPLACIAN EDGE DETECTOR

![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/066d962b-ae0f-455f-809a-56657c89ad79)



### CANNY EDGE DETECTOR

![image](https://github.com/Nagul71/EDGE-DETECTION/assets/118661118/f5800066-c26b-4b29-ab61-21b28c01e359)




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
