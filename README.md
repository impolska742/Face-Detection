# Face-Detection

This is a Face-Detection python script working with the use of OpenCV

### OpenCV is a library of programming functions mainly aimed at real-time computer vision. Originally developed by Intel, it was later supported by Willow Garage then Itseez. The library is cross-platform and free for use under the open-source Apache 2 License.

#### In this python project, I've used Haar-Cascade-Frontal-Detection Algorithm.

[Haar Cascade Frontal Face XML](https://raw.githubusercontent.com/opencv/opencv/master/data/haarcascades/haarcascade_frontalface_default.xml "Haar Cascade XML")

```python
classifier = cv2.CascadeClassifier("haarcascade_frontalface_default.xml")
```

[This](face-detect-WebCam.py) app uses our web-cam and helps us detect the faces within the frame. It captures the video in a run-time environment and displays a rectangle marking the face in the frame. 

```python
for face in faces:
	x, y, w, h = face
	frame = cv2.rectangle(frame, (x, y), (x + w, y + h), (255, 0, 0), 10)
	cv2.imshow("My Window", frame)
```

### WebCam Face-Detection.
![Working GIF of Face-Detection using WebCam][web-cam]

[web-cam]: face-detection-webCam.gif "Face-Detection-WebCam"

[This](face-detect-image.py) app reads an image from our computer and helps us detect the faces within that image. Here is an example of such :-

### Image Face-Detection.

![Before][before]
[before]: thor.jpg "Image of a Super Hero"