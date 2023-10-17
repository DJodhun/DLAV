# Creating Autonomous Vehicles using Deep Learning

## Background

Machine Learning, in particular, Deep Learning, models can be used to make principled decisions in lieu of a human driver in a vehicle. CNNs are well suited to process image data, which allows for computer vision. Being able to 'see' means the model will be able to 'react' and make decisions accordingly. Such decisions can be built in to the CNN, so that the vehicle stops for obstructions and turns when it is supposed to, based on what is being seen by tha camera. 

This project consisted of two phases: the first was a Kaggle competition was used to establish a theoretical best model without limitations on the model size, and the second was live testing using a SunFounder PiCar where the model size and decision speed mattered. The live testing element had 12 driving tasks, such as driving straight, stopping at a red light, following a figure of eight and being able to drive around an oval at speed. 

## Models Used

Two models were used in this project, and both used transfer learning. The first was a modified Inception-ResNetV2 model, used in the Kaggle competition. The second was a modified MobileNet model. Despite it being a light model, MobileNet still took around 1200 ms to make decisions in most cases, which is quite slow for the driving tasks. 

## Results

The Kaggle model placed 4th out of 15 teams on Kaggle, with a loss of 0.01455, and the live testing model placed joint 7th with a score of 21/36 in the 12 driving tasks. 

## Future Work and Improvements

There were several key areas of improvement, however, these were mainly due to time constraints since the model was plagued with various errors: 
- Lowering the image size from 224x224 to a smaller image
- Use edge detection to remove irrelevant data from the images
- Use of bounding boxes for object identification
- Try to use the NVIDIA model that was the lightest of all.

## What This Repository Contains

The debugatti.ipynb notebook contains the code to train and test the models. Running the model on the car requires running the code from the command line, and requires the SunFounder PiCar to run it on. Results figures and model summaries will be added soon.
