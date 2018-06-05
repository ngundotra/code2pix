# Code2Pix: Generating Graphical User Interfaces from Code 

See the original blog post [here](https://medium.com/@ngundotra/code2pix-deep-learning-compiler-for-graphical-user-interfaces-1256c346950b). This is original research for [Uizard](https:/uizard.io) in collaboration with UC Berkeley's Statistics Undergraduate Student Association [(SUSA)](https://github.com/SUSA-org).

The purpose of this project is to train a differentiable system capable of turning textual description of user interfaces into images of the actual thing. Yes, standard compilers already do this, yes they also go from "code" to "pix". However, this is a useful project because our system, unlike standard compilers, can be used to train other deep learning models. 

Specifically, we believe that code2pix can be used to create a GAN to replace pix2code. This is a  direction for future research that is within reach now having completed this project.

## Contributions

All code presented is written by myself. However, the following members contributed to the pre-production code and project: Samyak Parajuli, Luke Dai, Ajay Raj, Aismit Das, Dennis Yang, and Japjot Singh. 

## Requirements

All that's needed to run these files is `keras` (2.1.4) and `tensorflow` (1.4.1).

## Data

The data used in this repo comes from the [pix2code repo](https://github.com/tonybeltramelli/pix2code). Our directory structure has the dataset folders in our root directory.

```
code2pix/
	ios/
	  training_features/
	  eval_set/
	android/
	  ...
	web/
	  ...
```

## Contents

* Code2Pix.ipynb

This notebook has the code necessary to train code2pix and load in the data. It requires that you run Hydra Autoencoder.ipynb first and save a model structure. Although short, it draws upon work that the previous notebooks provided. For the curious, there are portions of this notebook that draw upon pretrained pix2code models, and pretrained autoencoders. To train the pix2code models, you will have to download/clone the original [pix2code repo](https://github.com/tonybeltramelli/pix2code) and go through the setup steps. 

* Hydra Autoencoder.ipynb

This is where we train our multiheaded autoencoder models that we use in the code2pix model. It's important to run this notebook first before trying out Code2Pix.ipynb.

* Encoder Decoder Visualization.ipynb

This is a notebook that allows the creation of GIFs and images that illustrate the inner workings of the autoencoders. These figures were not included in the final blog post. However, they are interesting enough to constitute a short post on their own. If you've never seen latent space visualizations before, I would **highly recommend** checking this notebook out. I'm biased, but I think the figures are really interesting.
