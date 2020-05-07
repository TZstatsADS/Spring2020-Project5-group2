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

To detect whether a dog is present in the supplied image ReseNet-50 pre-trained model was used which can identify 1000 categories. Trying this model on a sample dog dataset gave an excellent result, it was able to detect dogs in all of the sample set. 

### 2. Dog breed classification:

After we detecting dog in the image, we want to identity its breed. First of all, we create a CNN to classify dog breed from scratch Training a CNN model, which was built from scratch and gave us a test accuracy of 8.9% which is better than a random guess but still too small to be accepted. So we need some improvement on this model. Use a CNN to classify Dog Breeds Here we are going to train a CNN using transfer learning using the pre-trained VGG-16 model where the last convolutional output of the model is fed as input to our model. So we only need to train the fully connected layer that we added to the VGG-16 model and this resulted in reduced training time without sacrificing accuracy.

The achieved test accuracy was ~43%, a big mprovement compared to the model we built from scratch.Create a CNN to classify dog breeds using Transfer Learning Similar to the above step we will use transfer learning to a CNN model but we'll try to achieve at least 60% accuracy on the test data. For this purpose we are going to use Resnet50 pre-trained model and modify it's architecture by adding our custom fully connected layer.

After several test I was able to reach accuracy of ~72% which is a huge improvement and acceptable metric for his project.



**Contribution statement**: ([default](doc/a_note_on_contributions.md)) All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement.

Team members: Xiewen Jie, Yuyao Wang, Ziyang Zhang, Huizhe Zhu, Qin Zhang

Xiewen Jie：contributed to the app part related to this project, mainly for app.py, responsible for checking the app's function.

Yuyao Wang: Presenter and contributed to the identification algorithm related to this project with Ziyang Zhang

Ziyang Zhang: contributed to the identification algorithm related to this project with Yuyao Wang.

Qin Zhang: contributed to the app part related to this project, mainly for master.html, prediction.html, and help with app.py.

Huizhe Zhu: contributed to the app part related to this project.


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
