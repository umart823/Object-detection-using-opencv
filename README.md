# Object-detection-using-opencv

## Step 1: Importing the image:
import cv2

image=cv2.imread("/content/Coins.png",cv2.IMREAD_UNCHANGED)
cv2_imshow(image)

## Step2: Resizing the Image:
resized=cv2.resize(image,(256,256),cv2.INTER_AREA)
cv2_imshow(resized)

## Step3: RGB to Grayscale:
grayscale = cv2.cvtColor(resized, cv2.COLOR_BGR2GRAY)
cv2_imshow(grayscale)

## Step4: RGB to Binary Conversion:
ret,binary=cv2.threshold(grayscale,160,255,cv2.THRESH_BINARY)
cv2_imshow(binary)

## Step 5:  Coin Counting & Segmentation:
import numpy as np
edges = cv2.dilate(cv2.Canny(binary,0,255),None)
cv2_imshow(edges)
(cnt,_) = cv2.findContours(edges, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)

masked = cv2.drawContours(resized, cnt, -1, (0, 255, 0), 2)
cv2_imshow(masked)
print("The number of coins in the picture is",len(cnt))
