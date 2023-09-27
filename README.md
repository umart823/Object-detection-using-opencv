# Object-detection-using-opencv

## Step 1: Importing the image
import cv2

import numpy as np

image=cv2.imread("/content/Coins.png",cv2.IMREAD_UNCHANGED)

cv2_imshow(image)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/efb6cd68-1ee3-409f-9af4-92eacd57452d)


## Step 2: Resizing the Image
resized=cv2.resize(image,(256,256),cv2.INTER_AREA)

cv2_imshow(resized)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/5fe1f65c-bbad-410c-93f2-09134bdedc26)


## Step 3: RGB to Grayscale Conversion
grayscale = cv2.cvtColor(resized, cv2.COLOR_BGR2GRAY)

cv2_imshow(grayscale)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/169f71f2-3c16-4375-b3f5-8c3b7d002363)


## Step 4: RGB to Binary Conversion
ret,binary=cv2.threshold(grayscale,160,255,cv2.THRESH_BINARY)

cv2_imshow(binary)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/e48fae4b-2311-413a-9898-9087ee51df44)


## Step 5:  Coin Counting & Segmentation

edges = cv2.dilate(cv2.Canny(binary,0,255),None)

cv2_imshow(edges)

(cnt,_) = cv2.findContours(edges, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)

masked = cv2.drawContours(resized, cnt, -1, (0, 255, 0), 2)

cv2_imshow(masked)

print("The number of coins in the picture is",len(cnt))

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/764757bc-02ad-40af-a598-1532d1bf08a5)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/d41e4e29-7caa-4ef1-919c-c6e1a0aec2d6)

### The number of coins in the picture is 8

