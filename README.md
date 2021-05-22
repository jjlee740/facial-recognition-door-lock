# Facial Recognition Door Lock System

Created as the final project of an embedded systems course (CMPT433 with Dr. Brian Fraser), this facial recognition door lock system is is used to trigger the unlocking or locking of an electric door lock using an user's face as the password.


[Photo of the system in action](https://i.imgur.com/f8x9k4h.png)

[Another photo of the system in action](https://i.imgur.com/wzFxmR6.png)



## System Design

The facial recognition door lock system is built based off multiple components that are dependent with each other. First, we have our front end webpage that is used to direct the traffic between elements of the system. It is used as a GUI to display the current status of the system, allows the user to see the current image processing screen and also can manually trigger the webcam to take a picture, stop the system, resume the system or force open the doorlock. The attached webcam is used to take the photos and an attached microphone is used to trigger photos to be took by the camera. 

Once a picture has been taken by either a loud sound detected by the microphone or if it detects a face, the image is read by our Python program that is running in the background. If the photo is a photo it recognizes (based off a library of recognized faces using OpenCV), it will send a response back stating if it is a valid face or not. At this point, the appropriate response to our Beaglebone computer will be sent and will process this response and send the according lock or unlock signal to the electric door lock. 

## Credits

JJ Lee: Node.js web page and server developer, embedded developer of the microphone, camera and door lock mechanisms.

Parker Tian: Developer of the door lock mechanisms, tester.

Ken Ni: Developer of the facial recognition Python mechanism .
