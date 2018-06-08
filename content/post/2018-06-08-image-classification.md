---
title: Image Classification using Convolutional Neural Networks
subtitle: Deep Learning with Tensorflow
date: 2018-06-08
bigimg: [{src: "/img/postimg/image_class.jpg", desc: "Machine Learning"}]
tags: ["machine learning", "tensorflow","deep learning"]
---

### Introduction
If you know even a very little about Machine Learning and the so called "Artificial intellifence", then you might be aware of the datasets that the programs employing the learning deals with, images, audio/speech, videos and text data.

Machine Learning models can do various things with a given data, they can do handwriting recognition, image recognition, language translation, and speech recognition.

Google's Tensorflow is an open source library for high performance numerical computations, which allows it to handle multi-dimentional datastructures called tensors, and that leads it to be much more efficient in machine learning computation that required a lot of calculations like the Gradient Descent Function for a set of inputs and outputs.

[Google Deepmind](https://deepmind.com/) is [on Tensorflow](https://ai.googleblog.com/2016/04/deepmind-moves-to-tensorflow.html) too.

Some call it the machine learning and deep neural networks library but that is just and understatement, Tensorflow is fairly Scalable as it include package written in a variety of languages.

There are deep learning libraries that might do better than Tensorflow like PyTorch, Theano and Keras. I prefer Tensorflow as I find it much easier to use and visulize neural networks and if you ever want to see the data flow graph, there is always [Tensorboard Graph Visualization](https://www.tensorflow.org/programmers_guide/graph_viz). Besides this, Tensorflow has proven itself to be fairly good at reinforcement learning models and the community embraces openness, clean APIs, useful modules, and helpful people on the internet sure helps Tensorflow to come out as the best option as of now.

An image classifier with Tensorflow takes only 2 minutes to code.

I'm going to use [Transfer Learning](https://towardsdatascience.com/what-is-transfer-learning-8b1a0fa42b4?gi=a6b0723e4d51) with Inception which is a deep convolutional neural network (CNN) architecture that achieves the new state of the art for classification and detection on the ImageNet dataset and it is pre-trained. We'll have to retrain the final layers for our image dataset and we'll be good to go, while the pre-trained layers of the neural network will help us recognize higher level abstract image patterns. 

For that we'll have to write some code and set Hyper-Parameters for our new model, but before that we need a **lot** of images and to download them we'll use batch image downloader script.

I'll be training the last layer _final_training_ops_ in the figure, while all the previous layers retain their already-trained state.

![CNN](/img/cnn.png)

After we have our images, _retrain.py_ and _label_image.py_ scipts from the github repo cloned onto our system in a folder, we can use the below commands - 

### Directory Structure

1. Create a new directory with the name - "tf_files" in the current directory containing _retrain.py_ and _label_image.py_ initially.

2. Create the Training images directory in tf_files. In my case it is - `tf_files/cluster_photos`.

3. Create another Testing images directory in tf_files. In my case it is - `tf_files/test_photos`.

4. Do make a note here that the tf_files directory has to be there for _retrain.py_ to work, do not try and snip paths of the directories inside the tf_files directory.

### Set command line parameters

```
SET IMAGE_SIZE=224									
SET ARCHITECTURE="mobilenet_0.50_%IMAGE_SIZE%"		# or, SET ARCHITECTURE="inception_v3%IMAGE_SIZE%" for Inception v3
```

### Retraining using the specified Architecture and Directory Structure

Make sure to pass these as one line only.

> **Bottleneck** - stores final layer data of the neural network, just before the output layer.

> **--image_dir** - change this to the path to the directory where the images are. 


If the _scripts_ folder module is placed in the current directory already. 

```
python -m scripts.retrain \
--bottleneck_dir=tf_files/bottlenecks \
--how_many_training_steps=500 \
--model_dir=tf_files/models/ \
--summaries_dir=tf_files/training_summaries/%ARCHITECTURE% \
--output_graph=tf_files/retrained_graph.pb \
--output_labels=tf_files/retrained_labels.txt \
--architecture="%ARCHITECTURE%" \
--image_dir=tf_files/cluster_photos
```

If the _retrain.py_ script is available in our current working directory and there is no _script folder_, then from the current directory - 

```
python retrain.py \
--bottleneck_dir=tf_files/bottlenecks \
--how_many_training_steps=500 \
--model_dir=tf_files/models/ \
--summaries_dir=tf_files/training_summaries/%ARCHITECTURE% \
--output_graph=tf_files/retrained_graph.pb \
--output_labels=tf_files/retrained_labels.txt \
--architecture="%ARCHITECTURE%" \
--image_dir=tf_files/cluster_photos
```

### Training will take approximately 30-40 mins depending upon the hyperparameters, architecture, and the number and resolution of training images.


### Testing

After the model is finished training, input an image for it to classify - 

```
python -m scripts.label_image  --graph=tf_files/retrained_graph.pb  --image=tf_files/test_photos/1.jpg

# or from the directory as -

python label_image.py --image=tf_files/test_photos/2.jpg
```

And the output predictions will be displayed on the terminal.


### Conclusion


#### Further Reading and Recommended Links

	* Rethinking the Inception Architecture for Computer Vision - [Cornell University Library](https://arxiv.org/abs/1512.00567)
	* We Need to Go Deeper: A Practical Guide to Tensorflow and Inception - [Medium](https://medium.com/initialized-capital/we-need-to-go-deeper-a-practical-guide-to-tensorflow-and-inception-50e66281804f)
	* Train your own image classifier with Inception in TensorFlow - [Google AI Blog](https://ai.googleblog.com/2016/03/train-your-own-image-classifier-with.html)