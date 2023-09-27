# Object-detection-using-opencv

## Introduction

This report presents the results of our image processing assignment, which involves various image processing techniques applied to the input image named "Coins.png." The assignment consists of the following steps:
-	Importing the image
-	Resizing the image
-	Converting the image to grayscale
-	Converting the grayscale image to binary
-	Counting and segmenting the coins in the image

Each step is explained and demonstrated in detail in the following sections.

### Step 1: Importing the image
In the first step, we imported the input image "Coins.png" using the OpenCV library. The original image is displayed below:

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/efb6cd68-1ee3-409f-9af4-92eacd57452d)


### Step 2: Resizing the Image
The second step involved resizing the image to a 256x256 pixel resolution using the OpenCV library. The resized image is displayed below:

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/5fe1f65c-bbad-410c-93f2-09134bdedc26)


### Step 3: RGB to Grayscale Conversion
In this step, we converted the resized RGB image to grayscale. Grayscale conversion simplifies further image processing operations. The grayscale image is displayed below:

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/169f71f2-3c16-4375-b3f5-8c3b7d002363)


### Step 4: RGB to Binary Conversion
The next step involved converting the grayscale image to binary using a thresholding technique. Pixels with values above a certain threshold are set to white, while those below the threshold are set to black. The resulting binary image is displayed below:

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/e48fae4b-2311-413a-9898-9087ee51df44)


### Step 5:  Coin Counting & Segmentation

In the final step, we performed coin counting and segmentation. This involved the following sub-steps:
-	Edge detection using the Canny algorithm.
-	Contour detection to identify individual coins.
-	Drawing contours around the detected coins on the original image.


The resulting image is displayed below:

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/764757bc-02ad-40af-a598-1532d1bf08a5)

![download](https://github.com/umart823/Object-detection-using-opencv/assets/97828137/d41e4e29-7caa-4ef1-919c-c6e1a0aec2d6)

#### The number of coins in the picture is 8

