# ADS Project 5: Dog Breed Identification App

Term: Spring 2020

+ Team 2
+ Projec title: Dog Breed Identification App
+ Team members
	+ Yuyao Wang
	+ Qin Zhang
	+ Ziyang Zhang
	+ Huizhe Zhu
	+ Wenjie Xie
## Project summary: 

In this project, we will develop CNN algorithm that will accept any dog image and return an estimate of the breed of the dog. We used Keras (Tensorflow high level API) and OpenCV (Computer vision library) in our project. In our app, you can upload a picture which has a dog(please make sure there is a dog in your picture.) and this app will help you identity the breed of dog. 

## Datasets:

Dog dataset: https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip

Dog dataset addition: http://vision.stanford.edu/aditya86/ImageNetDogs/

## Content: 

1. dog_app.ipynb - A jupyter notebook file that contains the god breed identification algorithm, here will find the source code of the algorithms
 
2. model directory - model_Resnet50_final.h5: The saved model that contains the model architecture and weight, created using the code in the jupyter notebook

3. helper.py - A python file contains the dog or human identification algorithm, it loads the saved model from the model folder

4. app.py - this is the main flask python file that is responsible for routing and rendering html templates

5. requirements.txt - lists all the dependecies

## Analysis:

### 1. Dog Detection:

	
**Contribution statement**: ([default](doc/a_note_on_contributions.md)) All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement. 

Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.
