# DDPM Text to Image Generator

This project serves as my experimentation with simple text to image generation using a diffusion based model.
The project code in Image_Generator.ipynb consists of 4 major parts:
1. Data loading and helper funstions
2. U Net model
3. Training code 
4. Inference functions

Models contains a saved trained model state dict that can be loaded to generate results
Model_info contains a short summary of my model generated with torchinfo

## Dataset
This model was trained on pytorch's built-in CIFAR-10 dataset. As such it generates 32x32 images using a label from 0-10. It can thus only recognize a few labels and not words, however this could be implemented in a few lines and the project goal was to focus on the ML technicalities. STL-10 was chosen due to hardware constraints and the cost of training on a student budget.
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
* 10 - No lable. Used for CFG
To further differentiation between classes Classifier free guidance was implemented

# Example Images
Some examples of generated images and the provided labels
<p align="center">
Ship
<img width="200" alt="Ship" src="https://github.com/user-attachments/assets/51d4e78b-c8b7-4024-ab83-eb9036ecaf03" />
Frog
<img width="200" alt="Frog" src="https://github.com/user-attachments/assets/475ad492-eddc-49fd-8e48-84acae8cb6bb" />
Horse
<img width="200" alt="Horse" src="https://github.com/user-attachments/assets/40dacd9d-d11c-4f98-9caa-9dbc23661adc" />
</p>
