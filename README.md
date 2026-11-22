# Image-Segmentation-Using-Thresholding-Techniques-in-OpenCV
## Aim
To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

Global Thresholding Adaptive Thresholding Otsu's Thresholding

## Software Used
Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib

## Algorithm
### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.
### Step 2:
Load the input image using OpenCV.
### Step 3:
Convert the input image into grayscale format.
### Step 4: Global Thresholding
Select a fixed threshold value.
Apply thresholding to separate foreground and background pixels.
Display the thresholded image.
### Step 5: Adaptive Thresholding
Compute threshold values for small regions of the image.
Apply Adaptive Mean Thresholding.
Apply Adaptive Gaussian Thresholding.
Display the segmented images.
### Step 6: Otsu's Thresholding
Automatically determine the optimal threshold value.
Apply Otsu's thresholding technique.
Display the segmented image.
### Step 7:
Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.
## Program
### Developed By : Kirutika K R

### Register No: 212224230128

### original image:
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("garden.png")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
### Gray scale image:
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("garden.png", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
### Global thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("gaden.png", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
### otsu's thresholding:
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("garden.png", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
### adaptive thresholding:
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("garden.png", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
## Output
### Original Image
<img width="653" height="400" alt="image" src="https://github.com/user-attachments/assets/7a38b6c3-ca3f-4670-9021-ee2a5a43851e" />

### Original Grayscale Image
<img width="647" height="397" alt="image" src="https://github.com/user-attachments/assets/2aef4eb1-0f5a-41ff-9d9b-b0b9ed6da0fb" />

### Global Thresholding
<img width="660" height="407" alt="image" src="https://github.com/user-attachments/assets/b01e8dee-dc02-4c07-a4a4-e91d978ebd89" />

### Adaptive Thresholding
<img width="661" height="402" alt="image" src="https://github.com/user-attachments/assets/8785ff60-e122-4aa8-8c76-f10f13c86768" />

### Otsu's Thresholding
<img width="658" height="398" alt="image" src="https://github.com/user-attachments/assets/b0d6d871-baad-4014-85a2-f402fcebe59f" />

## Result
Thus, image segmentation is successfully performed using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques in OpenCV.
