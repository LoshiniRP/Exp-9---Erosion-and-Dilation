# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

### Developed By

**Name:** R P Loshini

**Register No:** 212225230155

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the dog image in grayscale
img = cv2.imread(r"C:\Users\acer\DIPT\puppy.jpg", 0)

if img is None:
    print("Image not found!")
else:
    # 1. Create a standard smaller kernel (5x5 instead of 31x31)
    kernel = np.ones((5, 5), np.uint8)

    # 2. Apply erosion with iterations=1
    erosion = cv2.erode(img, kernel, iterations=1)

    # 3. Apply dilation with iterations=1
    dilation = cv2.dilate(img, kernel, iterations=1)

    # Display results
    plt.figure(figsize=(15, 6))

    plt.subplot(1, 3, 1)
    plt.imshow(img, cmap='gray')
    plt.title('Original Dog Image')
    plt.axis('off')

    plt.subplot(1, 3, 2)
    plt.imshow(erosion, cmap='gray')
    plt.title('Erosion')
    plt.axis('off')

    plt.subplot(1, 3, 3)
    plt.imshow(dilation, cmap='gray')
    plt.title('Dilation')
    plt.axis('off')

    plt.tight_layout()
    plt.show()
```

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="1097" height="215" alt="image" src="https://github.com/user-attachments/assets/f5c5ef03-bcb9-47eb-bc1c-2214674d813a" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
