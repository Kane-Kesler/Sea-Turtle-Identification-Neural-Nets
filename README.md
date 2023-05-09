# SeaturlteIDHeads-CNN-Model

This repo contains code and observations taken based on my dissertation.

Investigating the effects of tourism and social media on wildlife animals
can be done by identifying the animals on social media platforms and
tracking the frequency at which they are posted [(Papafitsoros, Adam, and
Schofield 2023)](https://arxiv.org/abs/2211.10307). This repo contains the CNN model that are built to identify individual sea turtles based on the unique segmeneted patterns on their heads. To train and test our model, we use the [SeaturtleIDHeads dataset](https://www.kaggle.com/code/wildlifedatasets/seaturtleidheads-overview).

![sample images of sea turtle heads](https://github.com/Kane-Kesler/SeaturlteIDHeads-CNN-Model/assets/110169438/d0a4133d-f63a-4be5-acee-3982a461746f)

Note: Each row represents photos of a unique turtle.

We first compare its accuracy rate with the same model but trained on the well-established CIFAR-10 dataset. 
