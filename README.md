
# Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7

## Algorithm
### Step 1:
Import OpenCV Package.
<br>
### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.
<br>
### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.
<br>
### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.
<br>
### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.
<br>
### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.
<br>

## Program:
``` Python
### Developed By: Thrinesh Royal
### Register No: 212223230226

## i) Write the frame as JPG file
import cv2
cap=cv2.VideoCapture(0)
frame_number=0

while frame_number<5:
    ret,frame=cap.read()
    cv2.imshow('frame',frame)
    cv2.imwrite(f"frame_(frame_number).jpg",frame)
    frame_number+=1
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


## ii) Display the video

videoCaptureObject = cv2.VideoCapture(0)
while True:
    ret, frame = videoCaptureObject.read()
    cv2.imshow('myimage', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()  




## iii) Display the video by resizing the window

import cv2
cap=cv2.VideoCapture(0)
cv2.namedWindow('Video',cv2.WINDOW_NORMAL)
while True:
    ret,frame=cap.read()
    cv2.imshow('Video',frame)
    cv2.resizeWindow('Video',100,200)
    if cv2.waitKey(1) & 0xFF ==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()        



## iv) Rotate and display the video

cap=cv2.VideoCapture(0)
rotation_angel=90

while True:
    ret,frame=cap.read()
    rotated_frame=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video',rotated_frame)
    if cv2.waitKey(1)&0xFF==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()        
```
## Output

### i) Write the frame as JPG image
![image](https://github.com/user-attachments/assets/cd65b37e-66fd-49e2-a34a-e27f94050dab)

</br>
</br>


### ii) Display the video

![Screenshot 2024-09-25 200738](https://github.com/user-attachments/assets/5ac92501-54fd-4b99-8c54-206f96a3162d)

</br>
</br>


### iii) Display the video by resizing the window

![Screenshot 2024-09-25 200450](https://github.com/user-attachments/assets/4bec1481-b6a2-4943-914c-a42a2706115f)

</br>
</br>



### iv) Rotate and display the video

![Screenshot 2024-09-25 200324](https://github.com/user-attachments/assets/ebe9ecd6-2a2a-49fd-8854-e04f5434c112)

</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
