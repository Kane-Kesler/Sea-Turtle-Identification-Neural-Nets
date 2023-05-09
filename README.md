# SeaturlteIDHeads-CNN-Model

# Table of Contents  
- [Research Goals](#research-goals)
- [Methodology](#methodology)
- [Data](#data)
- [Results](#results)
- [Installation](#installation)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Research Goals
<div id="research-goals"></div>

Our goal is to build a CNN model that can identify future instances of a given sea turtle based on the images the model is trained on. The model will identify individual sea turtles based on the unique segmeneted patterns on their heads. To train and test our model, we use the [SeaturtleIDHeads dataset](https://www.kaggle.com/code/wildlifedatasets/seaturtleidheads-overview).

![sample images of sea turtle heads](https://github.com/Kane-Kesler/SeaturlteIDHeads-CNN-Model/assets/110169438/d0a4133d-f63a-4be5-acee-3982a461746f)

Note: Each row represents photos of a unique turtle.

Investigating the effects of tourism and social media on wildlife animals
can be done by using CNN models to identify the animals on social media platforms and
tracking the frequency at which they are posted [(Papafitsoros, Adam, and
Schofield 2023)](https://arxiv.org/abs/2211.10307). 

# Methodology
<div id="methodology"></div>
We will first train our model on the well-established CIFAR-10 dataset and measure its performance. We will call this model the CIFAR-10 CNN model.
After, we use the same network architecture to train two models using the SeaturtleIDHeads dataset, the first model splits the data randomly in the training and testing datasets (Random-Split model) and the other splits the data after a certain date-time (Time-cutoff Split model). We do this so we can compare how well our Time-cutoff Split model performs when trying to identify future instances of any given sea turtle as opposed to the 

# Data
### CIFAR-10
<div id="data"></div>
The CIFAR-10 dataset consists of a total of 6,000 32 × 32 images such that they
can be classified into 10 categories: dog, cat, deer, frog, horse, bird, plane, car,
truck and ship. Since this is a standard dataset used to practice different CNN
models, we build our model using this dataset first to gauge performance.

# Results
<div id="results"></div>

CIFAR-10 model: 82.25%

SeaturtleIDHeads Random Split model: 62.15%

SeaturtleIDHeads Time-cutoff Split model: 33.89%

Further analysis of the models are described in the [research paper](https://github.com/Kane-Kesler/SeaturlteIDHeads-CNN-Model/blob/main/Artificial%20Neural%20Networks%20for%20Sea%20Turtle%20Identification%20-%20Kane%20Kesler.pdf).

### SeaturleIDHeads
From the dataset of size ~8,000, we take a subset of data of size 10 corresponding to the turtles
with the most images. We also reduce the size of the images to 32×32 to reduce
the computational burden.

# Installation
<div id="installation"></div>

```
conda install pytorch pandas numpy seaborn
```

# Acknowledgements
<div id="acknowledgements"></div> 

[Patrick Loeber](https://github.com/patrickloeber/pytorchTutorial/blob/master/14_cnn.py) provided the general structure of the model class as well as the training and testing loops.

[GeekAlexis](https://github.com/GeekAlexis/cifar10-cnn/blob/master/CIFAR_10_CNN.ipynb) has a repo containing code on how to plot the loss curves and how to print the average training and validation loss each epoch. Implementations such as learning rate scheduler, bacth normmalisation and dropout were all inspired by this repo.

[Konrad Szafer](https://www.kaggle.com/code/konradszafer/paddy-disease-pytorch-acc-98-0) provided the initial code needed to create a custom dataset.

[Sahar Millis](https://stackoverflow.com/questions/53290306/confusion-matrix-and-test-accuracy-for-pytorch-transfer-learning-tutorial) provided code that plots a confusion matrix.

# License
<div id="license"></div>

Apache-2.0 license 


