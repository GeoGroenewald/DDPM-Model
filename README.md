#DDPM Text to Image Generator

This project serves as my experimentation with simple text to image generation using a diffusion based model.
The project code in Image_Generator.ipynb consists of 4 major parts:
1. Data loading and helper funstions
2. U Net model
3. Training code 
4. Inference functions

Models contains a saved trained model state dict that can be loaded to generate results
Model_info contains a short summary of my model generated with torchinfo

##Dataset##
This model was trained on pytorch's built-in STL-10 dataset. As such it generates 32x32 images using a label from 0-10. It can thus only recognize a few labels and not words, however this could be implemented in a few lines and the project goal was to focus on the ML technicalities. STL-10 was chosen due to hardware constraints and the cost of training on a student budget.
The label numbers correlate to these words
* 0 - plane
* 1 - car
* 2 - bird
* 3 - cat 
* 4 - deer
* 5 - dog
* 6 - toad
* 7 - horse
* 8 - ship
* 9 - truck
To further differentiation between classes Classifier free guidance was implemented

#Example Images#
