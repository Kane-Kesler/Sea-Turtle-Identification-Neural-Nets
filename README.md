# SeaturlteIDHeads-CNN-Model

# Table of Contents  
- [Research Goals](#research-goals)
- [Methodology](#methodology)
- [Data](#data)
- [Usage](#usage)
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
After, we use the same network architecture to train two models using the SeaturtleIDHeads dataset, the first model splits the data randomly in the training and testing datasets (Random-Split model) and the other splits the data after a certain date-time (Time-cutoff Split model). We do this so we can compare how well our Time-cutoff Split model performs when trying to identify future instances of any given sea turtle as oppose to the 

# Data
### CIFAR-10
<div id="data"></div>
The CIFAR-10 dataset consists of a total of 6,000 32 × 32 images such that they
can be classified into 10 categories: dog, cat, deer, frog, horse, bird, plane, car,
truck and ship. Since this is a standard dataset used to practice different CNN
models, we build our model using this dataset first to gauge performance.

### SeaturleIDHeads
From the dataset of size ~8,000, we take a subset of data of size 10 corresponding to the turtles
with the most images. We also reduce the size of the images to 32×32 to reduce
the computational burden.

# Installation
<div id="installation"></div>
Run command '''pip3 install torch torchvision torchaudio in termianl'''

# Usage
<div id="usage"></div>

# Acknowledgements
<div id="acknowledgements"></div>

# License
<div id="license"></div>
