## Record-Image-Acquisition-using-Web-Camera-Completion-requirements

## Aim:

To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

* Write the frame as a JPG file
* Display the video
* Display the video by resizing the window
* Rotate and display the video

## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)

## Algorithm:

# Step 1:

Import the required libraries and initialize the webcam using cv2.VideoCapture().

# Step 2:

Capture frames continuously from the webcam.

# Step 3:

Save a frame as a JPG image using cv2.imwrite().

# Step 4:

Display the live video stream using cv2.imshow().

# Step 5:

Resize the frame and rotate it using OpenCV functions, then display the processed frames.

## Program:

Developed By : SAI PRAVEEN C

Register No : 212225230239

## 1. Capture the image:
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
```
```
captured_image = cv2.imread('captured_frame.jpg')
```
```
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```
## 2. Display the video:
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## 3. Display the video by resizing the window:
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## 4. Rotate and display the video:

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## Output:

## 1. Capture the image:

<img width="648" height="516" alt="image" src="https://github.com/user-attachments/assets/71ce7f7f-bba5-4a6a-8a28-86e68cfe3f8b" />

## 2. Display the video:

<img width="655" height="497" alt="image" src="https://github.com/user-attachments/assets/ed671360-8dfb-47e0-8409-35267e7a4c1e" />

## 3. Display the video by resizing the window:

<img width="349" height="488" alt="image" src="https://github.com/user-attachments/assets/ea980784-ef7c-4b74-9a0f-932e9fc79adb" />

## 4. Rotate and display the video:

<img width="367" height="484" alt="image" src="https://github.com/user-attachments/assets/b88f29a8-2434-410e-9e0f-629e4274208b" />

## Result:
           
  Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
