---
title: Image Classification using Convolutional Neural Networks
subtitle: Deep Learning with Tensorflow
date: 2018-06-08
bigimg: [{src: "/img/postimg/image_class.jpg", desc: "Machine Learning"}]
tags: ["machine learning", "tensorflow","deep learning"]
---

## Introduction
If you know even a very little about Machine Learning and the so called "Artificial intellifence", then you might be aware of the datasets that the programs employing the learning deals with, images, audio/speech, videos and text data.

Machine Learning models can do various things with a given data, they can do handwriting recognition, image recognition, language translation, and speech recognition.

Google's Tensorflow is an open source library for high performance numerical computations, which allows it to handle multi-dimentional datastructures called tensors, and that leads it to be much more efficient in machine learning computation that required a lot of calculations like the Gradient Descent Function for a set of inputs and outputs.

[Google Deepmind](https://deepmind.com/) is [on Tensorflow](https://ai.googleblog.com/2016/04/deepmind-moves-to-tensorflow.html) too.

Some call it the machine learning and deep neural networks library but that is just and understatement, Tensorflow is fairly Scalable as it include package written in a variety of languages.

There are deep learning libraries that might do better than Tensorflow like PyTorch, Theano and Keras. I prefer Tensorflow as I find it much easier to use and visulize neural networks and if you ever want to see the data flow graph, there is always [Tensorboard Graph Visualization](https://www.tensorflow.org/programmers_guide/graph_viz). Besides this, Tensorflow has proven itself to be fairly good at reinforcement learning models and the community embraces openness, clean APIs, useful modules, and helpful people on the internet sure helps Tensorflow to come out as the best option as of now.

An image classifier with Tensorflow takes only 2 minutes to code.

I'm going to use [Transfer Learning](https://towardsdatascience.com/what-is-transfer-learning-8b1a0fa42b4?gi=a6b0723e4d51) with Inception which is a deep convolutional neural network (CNN) architecture that achieves the new state of the art for classification and detection on the ImageNet dataset and it is pre-trained. We'll have to retrain the final layers for our image dataset and we'll be good to go, while the pre-trained layers of the neural network will help us recognize higher level abstract image patterns. 

For that we'll have to write some code and set Hyper-Parameters for our new model, but before that we need a **lot** of images and to download them we'll use batch image downloader script.









### Conclusion


#### Further Reading and Recommended Links
