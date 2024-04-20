---
weight: 11
title: n-Shot Learning
bookFlatSection: false
bookCollapseSection: true
---

<div style="text-align: justify;">

# n Shot Learning
N-shot learning is a type of machine learning technique used for tasks where labeled data is scarce. It allows a model to learn and generalize from just a few examples (n examples), rather than needing a massive dataset for training. 

## Need for n-shot learning
Most state-of-the-art deep learning models are trained through supervised learning, which requires many labeled examples of relevant data classes. Models learn by making predictions on a labeled training dataset. These data labels provide both the range of possible answers (number of classes) and the correct answers (ground truth) for each training data sample. While being powerful, supervised learning is impractical in some real-world scenarios. Annotating large amounts of data samples is costly and time-consuming, and in cases like rare diseases and newly discovered species, examples may be scarce or non-existent. 

> For example, consider image recognition tasks: according to one study, humans can recognize approximately 30,000 individually distinguishable object categories. It’s not feasible, in terms of time, cost and computational resources, for artificial intelligence models to remotely approach human capabilities if they must be explicitly trained on labeled data for each class.

Organized and reusable concepts are the essence of human cognition which enable us to quickly adjust to new tasks and make sense of our choices.

> For example, let’s say you have seen a horse but never seen a zebra. If I tell you that a zebra looks like a horse but it has black and white stripes, you will probably immediately recognize a zebra when you see it.

`Developing algorithms capable of generalizing to new tasks with just a few samples is a major problem in narrowing the gap between performance at a machine and human level`. This need for machine learning models to be able to generalize quickly to a large number of semantic categories with minimal training overhead has given rise to n-shot learning.

## Types of n-shot learning
An n-shot learning field includes an ‘n’ number of labelled samples of each ‘K’ class. The entire support set ‘S’ includes n*K total samples. n-shot learning can be divided into three categories: zero-shot learning, one-shot learning and few-shot learning. The choice of application between the three depends upon the availability of training samples. 

> n-shot learning is also used when the dataset is huge, and labelling the data can prove to be costly. Or, when several samples are available, it could be hard to add specific features for each task.

### Zero shot learning
Zero-shot classification refers to the problem setting where we want to recognize objects from classes that our model has not seen during training.

In zero shot learning the data consists of
- **Seen classes**: These are classes for which we have labelled images during training
- **Unseen classes**: These are classes for which labelled images are not present during the training phase.
- **Auxiliary information**: This information consists of descriptions/semantic attributes/word embeddings for both seen and unseen classes at train time. This information acts as a bridge between seen and unseen classes.

Zero-shot learning involves little human intervention, and the models depend on previously trained concepts and additional existing data. This method reduces the time and effort that data labelling takes. Instead of giving training examples, zero-shot learning gives a high-level description of new categories so that the machine can relate it to existing categories that the machine has learned about. 

### One shot learning
### Few shot learning
### K shot learning


</div>