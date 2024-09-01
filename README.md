## Object Detection and Tracking Device

The project helps in detecting and tracking the motion of an object in a frame. Arduino microcontroller, two servo motors a webcam, a laptop and a laser are the main hardware involved in this. The Arduino is connected to the Python program via pyserial library. The main algorithm used in this project is Object tracking using contour analysis and baground subtraction. OpenCV is the library used.

In the algorithm, a frame size is defined initially. The current frame is gray scaled and gaussian blur is done on it. Ath the end of the iteration, the current frame is stored as the previous frame before entering next iteration. Then the difference between the current frame and previous frame is taken and the contours are found out. Based on the contour area of the difference of the frames, the contours understands whether the object is in motion or not and if it is in motion, a rectangle is formed around the object. The coordinates of this rectangle in the frame is then sent to the Arduino which maps it to certain angles and rotates the servor motors. As the servo motors rotate based on the angles in two axes, the laser which is mounted on top of the servor motors point to the object in motion. 

***

## Technologies Used
1. Python
2. OpenCV library
3. Pyserial library
4. Arduino 
