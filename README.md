# Air-Canvas-Using-Open-CV
This is an Air Canvas Project Implemented using OpenCV and Python. It is used to take input from camera using a blue colored object and as the object moves in the image from camera, it draws same on the screen of user in real time. There are options to change color of pen to draw on the screen.


## Algorithm:
1. Start reading the frames and convert the captured frames to HSV color space
(Easy for color detection).
2. Prepare the canvas frame and put the respective ink buttons on it.
3. Adjust the track bar values for finding the mask of the colored marker.
4. Preprocess the mask with morphological operations (Eroding and dilation).
5. Detect the contours, find the center coordinates of largest contour and keep
storing them in the array for successive frames (Arrays for drawing points on
canvas).
6. Finally draw the points stored in an array on the frames and canvas.


Morphological operations are a set of operations that process images based on
shapes. They apply a structuring element to an input image and generate an output
image.
Erosion and Dilation has been sed in the project:
### Basics of Erosion:
● Erodes away the boundaries of foreground object
● Used to diminish the features of an image.
### Working of erosion:
1. A kernel(a matrix of odd size(3,5,7) is convolved with the image.
2. A pixel in the original image (either 1 or 0) will be considered 1 only if
all the pixels under the kernel is 1, otherwise it is eroded (made to zero).
3. Thus all the pixels near the boundary will be discarded depending upon
the size of the kernel.
4. So the thickness or size of the foreground object decreases or simply
white region decreases in the image.

### Basics of dilation:
● Increases the object area
● Used to accentuate features
### Working of dilation:
1. A kernel(a matrix of odd size(3,5,7) is convolved with the image
2. A pixel element in the original image is ‘1’ if atleast one pixel under the
kernel is ‘1’.
3. It increases the white region in the image or size of foreground object
increases

## Working
The air canvas Detects blue colour in the camera frame and whichever object is
detected, that object becomes pen/stylus to draw the objects.(Caution- We should
not have any other blue colour object in camera frame background for air canvas to
work smoothly)
Some pen or objects of blue colour can be used to act as brush to the canvas.

# Images of Working
![image](https://user-images.githubusercontent.com/56537415/132088504-9c41a906-3398-4cd6-9282-a2b690ac51f1.png)
![image](https://user-images.githubusercontent.com/56537415/132088505-6b266946-9ced-46bc-93fd-7306b0286781.png)
![image](https://user-images.githubusercontent.com/56537415/132088507-b279adab-940b-44e2-a907-6c999a478927.png)
![image](https://user-images.githubusercontent.com/56537415/132088509-7301ced1-e4ea-4f74-98c4-7572dfba0616.png)


### Future Work-:
Given more time to deal with this project, we would improve hand contour recognition, investigate our unique Air Canvas objectives, and attempt to comprehend the multicore module. 
To improve hand gesture tracking, we would need to dig more into OpenCV. There are various strategies for contour analysis, yet in this specific algorithm, it very well might be advantageous to investigate the color histogram used to create the contours in question.  Besides, we could explore different interpolation methods. PyGame incorporates a line drawing technique (pygame.draw.line()) that could be valuable in creating smoother, cleaner lines. On a similar vein, implementing a variety of brush shapes, surfaces, and even an eraser would make Air Canvas more powerful as a drawing program. Permitting the client to save their final work or watch their drawing cycle as a playback animation could likewise be remarkable highlights that look like genuine innovative software. Maybe there would even be an approach to interface Air Canvas to genuine computerized drawing projects, for example, Adobe Photoshop, Clip Studio Paint, or GIMP! At last, we could make critical walks by sorting out how multicore processing works with in-order information processing.





### References
[1]https://docs.opencv.org/master/d9/df8/tutorial_root.html

[2]https://www.geeksforgeeks.org/opencv-python-tutorial/

[3]https://www.learnopencv.com/creating-a-virtual-pen-and-eraser-with-opencv/

[4]https://towardsdatascience.com/install-and-configure-opencv-4-2-0-in-windows-10-vc-d132c52063a1

[5]https://docs.opencv.org/3.4/d4/d76/tutorial_js_morphological_ops.html

[6]https://www.wikipedia.org/

