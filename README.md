
## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** ADITHYA  M
- **Register Number:** 212224230008

  ### Ex. No. 01

1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```PYTHON
import cv2
import matplotlib.pyplot as plt
```

Read the image using OpenCV
```
img = cv2.imread('VIN.jpeg', cv2.IMREAD_COLOR)
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)#
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Display the image using Matplotlib
```
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
```
Draw a line from top-left to bottom-right
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jepg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
(1536, 941, 3)
```
Draw a rectangle around the Whole image
```
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Add text to the image
```
text_img = cv2.putText(img_rgb, "Opencv Drawing", (10, 35), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```



## Output:

## original image
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/aa57193d-1e2d-4d61-b7ef-5da6f325619c" />


## Image with Line
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/5373b4a1-d973-4908-9792-f5bec876bdd5" />


## Image with Circle
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/d9e94255-262f-4db9-a375-0579fdc16e8f" />

## Image with Rectangle
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/a267c182-aaf9-45ed-b0ff-0f52269f1344" />


## Image with Text
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/0afde0b5-1143-49e7-9b66-7503833900d8" />


## Original RGB Image
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/c85be0ab-cf97-4e2b-8673-669be604c46b" />


## HSV Image
<img width="515" height="319" alt="image" src="https://github.com/user-attachments/assets/dc8c5cb0-9263-48fc-b94b-29440dac26dc" />


## Grayscale Image
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/3fd025c0-f3aa-4f12-92cb-77ddfc28b75c" />

## HSV to RGB Image
<img width="515" height="319" alt="image" src="https://github.com/user-attachments/assets/50ab1f46-20db-4caf-bd61-0cdab65ac4a9" />


## Image with 300x300 White Block
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/577a65f4-ccba-43bf-9f63-ab7bb71e8da9" />


## Resized Image (Half Size)
<img width="493" height="410" alt="image" src="https://github.com/user-attachments/assets/95175af9-4a29-4d2d-aa37-9913711f4e77" />


## Cropped Region of Interest (ROI)
<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/eab45787-5be0-45b6-a258-d84905ad87ac" />

## Flipped Horizontally
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/7a55c830-e685-40af-a341-7534bfeb32a0" />


## Flipped Vertically
<img width="515" height="320" alt="image" src="https://github.com/user-attachments/assets/10081ff6-58a6-4bf8-ba90-169f58e3b895" />



## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

