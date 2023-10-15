# Image Colorization

- Image colorization is the process of taking an input grayscale (black and white) image and then producing an output colorized image that represents the semantic colors and tones of the input.
- Image colorization assigns a color to each pixel of a target grayscale image
- Traditional colorization techniques requires significant user interaction.
- In this process, a fully automated data-driven approach “autoencoders” is used for colorization
- This method requires neither pre-processing nor post-processing.

## AutoEncoders

Autoencoders are a specific type of feedforward neural networks where the input is the same as the output. 
An autoencoder neural network is an Unsupervised Machine learning algorithm that applies backpropagation, setting the target values to be equal to the inputs.

## Backbone

-	Backbone is a term used in models/papers to refer to the feature extractor network.
-	This is a standard convolutional neural network (typically, VGG16 or VGG19) that serves as a feature extractor. The early layers detect low level features (edges and corners), and later layers successively detect higher level features (car, person, sky).
-	Backbone gives you a feature map representation of input
-	Multiple pre trained model used as a backbone for a variety of tasks 

## Code Description

    File Name : DecoderLayers.py
    File Description : Setting up the decoder layers architecture and loading the trained model



    File Name : Engine.py
    File Description : Main class for starting different parts and processes of training and inference lifecycle



    File Name : EncoderLayers.py
    File Description : Setting up the encoder layers architecture and loading the backbone VGG model



    File Name : Inference.py
    File Description : Inference cycle for setting up the end to end pipeline of inferencing and saving the image



    File Name : References.py
    File Description : References class for keeping the constants and reference path to dataset and weights



    File Name : LoadData.py
    File Description : LoadDataset class for loading the image data and converting it to LAB format


## Steps to Run

There are two ways to execute the end to end flow.

- Modular Code
- IPython (Google Colab)

### Modular code

- Create virtualenv
- Install requirements `pip install -r requirements.txt`
- Modify `Engine.py` based on the mode that you are training on "Training" / "Inference"
- Run Code `python Engine.py`

### IPython Google Colab

Follow the instructions in the notebook `Image_Coloring_using_Transfer_Learning.ipynb`

## Steps to Run

### Input images

![t5](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/da95f1e7-3bb0-449d-a66d-134c32f17a7d)
![t4](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/923051a9-99ee-4673-b9b0-ef9f83b9787c)
![t3](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/b0ac7c2b-66f9-4968-af00-c8aef87e691b)
![t2](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/15ac67a9-c2ed-4aa1-9207-ae25f3eec529)
![t1](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/f8236e7b-f177-44f3-8a82-651ad46ee771)


### Output images

![generated_images4](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/08738ae3-9739-4d42-ac89-7bb57849b05e)
![generated_images3](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/1888dd1d-3fe7-4bc6-8df4-598f193abc2c)
![generated_images2](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/04c78575-e171-4114-a7c8-5c76fc349ce5)
![generated_images1](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/a9c9cb71-8ed1-472c-8174-d46ebfba624c)
![generated_images0](https://github.com/vaibhavtiwari/ImageColoring-Autoencoder/assets/84077845/b25e1af7-3cbf-49b0-86ba-57b58e069213)
