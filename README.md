## :computer: Image Processing Tasks 

These tasks are performed without using inbuilt Python libraries. The only libraries used are Numpy & PIL

---
### :city_sunset: Image Rotation

The image is rotated by angles which are multiples of 90 degrees. It involves finding the center of the Matrix and shifting along the center using rotation matrix.
  
![Original Image](https://user-images.githubusercontent.com/64036185/92142268-32203080-ee31-11ea-9c30-9fa8f51d3b74.png) 

**Output**
|<img width="316" height="598" src="https://user-images.githubusercontent.com/64036185/92317946-b508dd00-f023-11ea-91df-31e1c6f0caeb.png">|<img width="316" height="598" src="https://user-images.githubusercontent.com/64036185/92317968-e08bc780-f023-11ea-9010-8ff23631f475.png">|
|:---:|:---:|
|90 Degrees Clockwise|270 Degrees Clockwise|

### :sunrise: Applying Kernels

An image kernel is a small matrix used to apply effects like the ones we might find in Photoshop or Gimp, such as blurring, sharpening, outlining or embossing. They're also used in machine learning for 'feature extraction', a technique for determining the most important portions of an image. In this context the process is referred to more generally as "convolution".

We use a 3x3 or 5x5 kernel. For each 3x3 block of pixels in the image, we multiply each pixel by the corresponding entry of the kernel and then take the sum.

You can visit [here](https://setosa.io/ev/image-kernels/) for more information.

The Kernel filters are doing the following tasks:
1. Blurring (Normal Blur, Box Blur & Gaussian Blur)
2. Sharpening the Image

![Original Image](https://user-images.githubusercontent.com/64036185/92143212-8ed01b00-ee32-11ea-8315-c57b111ce552.png)

**Output**
|<img width="300" height="300" src="https://user-images.githubusercontent.com/64036185/92144804-deafe180-ee34-11ea-9ee6-259f5dbe4326.png">|<img width="300" height="300" src="https://user-images.githubusercontent.com/64036185/92144938-14ed6100-ee35-11ea-888f-bb64c2f35fe3.png">|<img width="300" height="300" src="https://user-images.githubusercontent.com/64036185/92143827-6f85bd80-ee33-11ea-831d-e9a08b36d204.png">
|:---:|:---:|:---:|
|Box Filter|Gaussian Filter|Sharpen|

### :city_sunset: Edge Detection

Edge detection is an image processing technique for finding the boundaries of objects within images. It works by detecting discontinuities in brightness. Edge detection is used for image segmentation and data extraction in areas such as image processing, computer vision, and machine vision.

More information can be found [here](https://towardsdatascience.com/edge-detection-in-python-a3c263a13e03)

Following Edge Detections are applied:

    1. Vertical Edge Detection
    2. Horizontal Edge Detection
    3. Sobel Edge Detection
    4. Canny Edge Detection

**Original Images**

![Cube](https://user-images.githubusercontent.com/64036185/92311996-1c9a3a80-efda-11ea-933c-aa736515b5af.jpg)

![Dog](https://user-images.githubusercontent.com/64036185/92312000-3045a100-efda-11ea-94e9-35a21ea14d18.png)

**Output**

|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312033-a8ac6200-efda-11ea-86b2-1f3db1b96094.png">|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312045-c679c700-efda-11ea-8ac1-ca712ed6ae4a.png">|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312054-d98c9700-efda-11ea-8af6-5acf3981e815.png">
|:---:|:---:|:---:|
|Vertical Edge|Horizontal Edge|Sobel|

|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312276-dc888700-efdc-11ea-90e9-2e12632c3c73.png">|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312243-874c7580-efdc-11ea-8983-1cc1474e8d2e.png">|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312246-9501fb00-efdc-11ea-9c1c-559c9d598ffd.png">
|:---:|:---:|:---:|
|Vertical Edge|Horizontal Edge|Sobel|

|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312347-68021800-efdd-11ea-918f-71c0e638f9c2.jpg">|<img width="208" height="203" src="https://user-images.githubusercontent.com/64036185/92312364-836d2300-efdd-11ea-87b3-c6b7c0e6470c.jpg">
|:---:|:---:|
|Cube Canny|Dog Canny|

### :city_sunset: Morphological Transformation

Morphological transformations are some simple operations based on the image shape. It is normally performed on binary images. It needs two inputs, one is our original image, second one is called structuring element or kernel which decides the nature of operation. Two basic morphological operators are Erosion and Dilation. 

Applying dilation and erosion transformation to the image

**Output**

|<img width="112" height="150" src="https://user-images.githubusercontent.com/64036185/93011018-4d690980-f5b0-11ea-8168-08acd58bd1f2.png">|<img width="112" height="150" src="https://user-images.githubusercontent.com/64036185/93011036-670a5100-f5b0-11ea-9a91-3be72e4fa241.png">|<img width="112" height="150" src="https://user-images.githubusercontent.com/64036185/93011042-79848a80-f5b0-11ea-89a4-5661df4730ae.png">|<img width="112" height="150" src="https://user-images.githubusercontent.com/64036185/93011063-a173ee00-f5b0-11ea-9edf-b446a5035966.jpg">
|:---:|:---:|:---:|:---:|
|Input Image|Dilation|Erosion|Edge Detection|

### :city_sunset: Masking

Masking is an image processing method in which we define a small 'image piece' and use it to modify a larger image. Masking is the process that is underneath many types of image processing, including edge detection, motion detection, and noise reduction. To show only blue ball a mask has been applied to the following input image

|<img width="600" height="396" src="https://user-images.githubusercontent.com/64036185/93011170-881f7180-f5b1-11ea-92d6-880b90c759f8.jpg">|<img width="600" height="396" src="https://user-images.githubusercontent.com/64036185/93011179-9e2d3200-f5b1-11ea-854e-f2c43ea8c386.jpeg">
|:---:|:---:|
|Input Image|Masked Image|

### :city_sunset: ROI

A region of interest (ROI) is a portion of an image that you want to filter or perform some other operation on. You define an ROI by creating a binary mask, which is a binary image that is the same size as the image you want to process with pixels that define the ROI set to 1 and all other pixels set to 0.

|<img width="600" height="396" src="https://user-images.githubusercontent.com/64036185/93011235-28759600-f5b2-11ea-8665-00a887f3ea12.jpg">|<img width="600" height="396" src="https://user-images.githubusercontent.com/64036185/93011246-3a573900-f5b2-11ea-80ad-a11b683924cd.jpeg">
|:---:|:---:|
|Input Image|Output Image|