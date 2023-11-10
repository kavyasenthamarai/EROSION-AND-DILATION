# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it
### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np


# Create the Text using cv2.putText

IMg= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'M.Rajeshkannan',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element



# Erode the image

erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Dilate the image


dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image
![CRE](https://github.com/JEEVAABI/EROSION-AND-DILATION/assets/93427098/65fb2909-7484-423f-8d74-e6d31c4bbf22)


### Display the Eroded Image
![ER2](https://github.com/JEEVAABI/EROSION-AND-DILATION/assets/93427098/e5eec47d-e8a4-454e-a4b2-e6cf9ca5e12e)
![ER1](https://github.com/JEEVAABI/EROSION-AND-DILATION/assets/93427098/24a4e38e-8eca-4180-aeea-6bedc25d9be5)

### Display the Dilated Image

![DI2](https://github.com/JEEVAABI/EROSION-AND-DILATION/assets/93427098/86d07aef-081c-4261-b3be-c1cdf4f646e1)
![DI1](https://github.com/JEEVAABI/EROSION-AND-DILATION/assets/93427098/6e428054-95c0-4fa7-9577-ef071e31f648)

## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.
