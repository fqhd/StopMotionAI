# StopMotionAI
This is a project aimed to train a neural network that helps increase the FPS of a stop motion film. Feed 2 pictures into the neural network, and the "interpolated" picture in between comes out.

--- 

## ImageTaker
This folder is a simple image taker in javascript. It assisted in the creation of the data to train the AI. It only takes a few thousand images to train the neural network so taking pictures at a 1 second interval for a couple hours should be enough to train the AI.

## StopMotionProcessing
Once you've gathered training datta, this is the folder where the training takes place. It is powered by the Tensorflow C API (accelerated fork for the m1 in my case), but feel free to use the standard Tensorflow API instead.

## Neural Network App
This is the webapp written in javascript which loads the neural network from a file and sets it up using the tensorflow.js library. It takes a series of images in and produces interpolated data out. The images must be grouped in a folder named "src_images" named in their order with the .jpg extension. (e.g, "1.jpg", "2.jpg", "3.jpg"). The outputted images will be submitted in a folder called "out_images".