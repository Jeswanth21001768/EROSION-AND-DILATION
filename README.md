# EROSION-AND-DILATION

Implementation-of-Erosion-and-Dilation
# Aim
To implement Erosion and Dilation using Python and OpenCV.
# Software Required
1. Anaconda - Python 3.7
2. OpenCV
# Algorithm:
Step1:
Import necessary packages
Step2:
Create an empty window and add text to it
Step3:
create a structuring element
Step4:
Do the operation
Step5:
Show the output image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np



# Create the Text using cv2.putText
img= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'Jeswanth',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()



# Create the structuring element
# For Erosion
erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))



# Erode the image
# For Dilation
dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

# Erode and show the eroded image
image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate and show dilated the image
image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
212221230042
55
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:

### Display the input Image
<br>
<br><img width="626" alt="image" src="https://github.com/Jeswanth21001768/EROSION-AND-DILATION/assets/94155480/f606bb4e-2993-41f4-a153-237e669ba663">

<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>
<br><img width="607" alt="image" src="https://github.com/Jeswanth21001768/EROSION-AND-DILATION/assets/94155480/1ae0f124-01a1-4823-a1c7-87298664043d">

<br>
<br><img width="591" alt="image" src="https://github.com/Jeswanth21001768/EROSION-AND-DILATION/assets/94155480/6f6ba2bd-8772-4e46-96e0-ec734716b168">

<br>
<br>

### Display the Dilated Image
<br>
<br><img width="565" alt="image" src="https://github.com/Jeswanth21001768/EROSION-AND-DILATION/assets/94155480/3e00bb98-6298-405f-bde0-40d1b1fd71ce">

<br>
<br><img width="590" alt="image" src="https://github.com/Jeswanth21001768/EROSION-AND-DILATION/assets/94155480/ce0b98d3-b49e-413e-9e5e-9fae319d6bed">

<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
