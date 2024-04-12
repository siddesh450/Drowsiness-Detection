<h1>Drowsiness Detection Using ML and Open CV </h1>

<h2>Application :</h2>

<li>This Code can detect eyes, mouth movement and alert that user is in drowsy state.</li>
<br>
<h2>Code Requirement:</h2> 

This code in in Python
<br>

<h2>Dependencies</h2>
<li> import datetime </li>
<li> import matplotlib.pyplot </li>
<li> import matplotlib.animation </li>
<li> import cv2 </li>
<li> import playsound </li>
<li> import numpy </li>
<li> import pandas </li>

<h2> Alogrithm </h2>
 Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye (as if you were looking at the person), and then working clockwise around the eye.
 Similarly mouth is represented by coordinates.

 It checks 20 consecutive frames and if the Eye/ Mouth Aspect ratio is less than 0.25, Alert is generated.

## Results: 
The GUI has been created using basic HTML, CSS and JavaScript and we have used Flask to render the python code into the website. Tkinter has also been used in order to make things simpler. It has 2 buttons: Run and Exit. The GUI looks like: 
![df01ae7c-afc9-4676-b95b-b6cec592ddf0 (online-video-cutter com) (1)](https://user-images.githubusercontent.com/35571958/87902089-589f2d80-ca76-11ea-9eda-a53a83662721.gif)

The outputs of the working system detecting drowsiness is shown as: <br>
![frame_yawn1](https://user-images.githubusercontent.com/35571958/87904322-ab2f1880-ca7b-11ea-97d2-82f9dd0c318a.jpg) ![Screenshot (405)](https://user-images.githubusercontent.com/35571958/87904406-dd407a80-ca7b-11ea-982d-1852e2228765.png)

Also, in order to keep a proof of the moment when the person was sleeping or yawning, we kept a seperate folder where those frames are stored as: <br>
![Screenshot (408)](https://user-images.githubusercontent.com/35571958/87904688-7e2f3580-ca7c-11ea-839b-c049bace332f.png)

## Streaming using Phone Camera 
We have used and Android App available for free in Play Store, named IP Webcam. It can be downloaded from this <a href = "https://play.google.com/store/apps/details?id=com.pas.webcam&hl=en_IN">link</a>. After downloading it, open the app and scroll down to the option <b>Start Server</b>. It will look like: <br>
<img src = "https://user-images.githubusercontent.com/35571958/88623867-83673280-d0c3-11ea-9efd-63559024c0bd.jpg">

After starting the server, an IP will be displayed on the screen. Open the file <b>android_cam.py</b>. In <b>line 36</b> put the given IP. 
```python
url = "http://<YOUR_IP_HERE>/shot.jpg"
```
<b>Also, make sure that the phone and PC/Laptop is connected to the same network.</b>

Then, run the system in the same way as mentioned above. Click on the <b>Run Using Phone Cam</b> button to see the results:<br> 
<img src = "https://user-images.githubusercontent.com/35571958/88624933-7b0ff700-d0c5-11ea-87da-3f6bf1516cc3.png">

Also, in order to toggle between the front and back camera, type the IP upto "http://<YOUR_IP_HERE>" in the search bar of yor browser and explore the page which will look like this: <br>
<img src = "https://user-images.githubusercontent.com/35571958/88626505-5f5a2000-d0c8-11ea-88f0-e1d4481eb9d9.png">

Also, we have tried plotting the MAR and EAR graph Vs. Time in order to make the working clearer to the audience. The graph looks like: <br> 
<img src = "https://user-images.githubusercontent.com/35571958/88627012-42721c80-d0c9-11ea-860a-51b7a1f2961b.png">

 ## References: 
[1]Facial landmarks with dlib, OpenCV and Python: https://www.pyimagesearch.com/2017/04/03/facial-landmarks-dlib-opencv-python/ <br>
[2]Eye blink detection with OpenCV, Python, and dlib: https://www.pyimagesearch.com/2017/04/24/eye-blink-detection-opencv-python-dlib/ <br>
[3]Drowsiness Detection with OpenCV: https://www.pyimagesearch.com/2017/05/08/drowsiness-detection-opencv/ <br>
[4]Real-Time Eye Blink Detection using Facial Landmarks: http://vision.fe.uni-lj.si/cvww2016/proceedings/papers/05.pdf 
