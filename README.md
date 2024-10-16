# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically. 5.Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.
## Program:
```python
Developed By: RICHARDSON A 
Register Number: 212222233005
# 1. Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

# 2. Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)  # Scale by 1.5x

# 3. Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

# 4. Reflection (Flip)
reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)

# 5. Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))

# 6. Cropping
cropped_image = image_rgb[50:300, 100:400]  # Crop a portion of the image

# Plot the original and transformed images
plt.figure(figsize=(12, 8))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')

plt.subplot(2, 3, 2)
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')

plt.subplot(2, 3, 3)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

plt.subplot(2, 3, 4)
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')

plt.subplot(2, 3, 5)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

plt.subplot(2, 3, 6)
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')

plt.tight_layout()
plt.show()

# Plot cropped image separately as its aspect ratio may be different
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()


```
## Output:
### i)Orignal image
<img width="944" alt="Screenshot 2024-10-16 at 4 26 03 PM" src="https://github.com/user-attachments/assets/55918191-ae7c-483b-b48e-76a486f7b16d">

### i)Image Translation
<br>
<img width="622" alt="Screenshot 2024-10-16 at 4 30 42 PM" src="https://github.com/user-attachments/assets/4be825dd-83cf-483e-a26e-c9f0ea00f8c8">
<br>

### ii) Image Scaling
<br>
<br>
<img width="599" alt="Screenshot 2024-10-16 at 4 32 09 PM" src="https://github.com/user-attachments/assets/bd5a353c-bdc1-4f77-9061-8aaeb15fc83b">

<br>
<br>


### iii)Image shearing
<br>
<br>
<img width="603" alt="Screenshot 2024-10-16 at 4 34 40 PM" src="https://github.com/user-attachments/assets/0f5960cd-2297-4a13-87e2-31384d7ec370">

<br>
<br>


### iv)Image Reflection
<br>
<br>
<img width="590" alt="Screenshot 2024-10-16 at 4 34 55 PM" src="https://github.com/user-attachments/assets/962e3715-3ca2-4057-bc2a-cc4fce0e8b21">

<br>
<br>



### v)Image Rotation
<br>
<br>
<img width="523" alt="Screenshot 2024-10-16 at 4 38 27 PM" src="https://github.com/user-attachments/assets/0fdcb3b7-6579-491f-bf88-e99ce919d083">

<br>
<br>



### vi)Image Cropping
<br>
<br>
<img width="333" alt="Screenshot 2024-10-16 at 4 38 44 PM" src="https://github.com/user-attachments/assets/c0b748ea-c0db-4282-a951-35c2af7f802a">

<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
