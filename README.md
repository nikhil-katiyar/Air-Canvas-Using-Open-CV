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
Here we have used Erosion and Dilation:
## Basics of Erosion:
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
