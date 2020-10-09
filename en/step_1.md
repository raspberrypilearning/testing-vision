## Introduction

### What is machine learning?

'Machine learning' is when computer programs get better through experience instead of a programmer having to design and build improvements for them. The program tests a way of doing something, measuring its success somehow, and then changing its approach and tests again, over and over, always trying to improve that measurement of success.

While there are lots of different types of machine learning, this project focuses on **image classification**: an image is taken and the computer has to recognise which class, from a number of 'classes' of image the computer has been taught to recognise, the supplied image is most likely to belong to. 

One of the most famous examples of machine learning is to ask a computer whether a picture contains a cat or a dog. The computer can do this because it has been shown thousands of examples of what cats and dogs look like. From these, it builds a **model** — a set of rules for how to decide that an image contains a dog or a cat. 

A weakness of image classification is that a program that has been trained only on cats and dogs *always* guesses that something is either a cat or a dog. Image classification programs don't have the ability to recognise things that were not part of their training, and they likewise can't decide whether an image contains none of the things they have been trained to recognise.

### What you will make
You will create a Python function to test a computer's recognition of an object, then you will supply a photograph of that object and receieve the computer's guess about what it is. This will be a useful tool for you in future projects, so you can test the models you create, and get the results of others' models when using them as part of an application. You will use Google Colab — an online tool used to write and run machine learning programs — to create this project.

![The complete projec: A numbered list of fifteen items, mostly dog breeds, each followed by a percentage. Number thirteen is different — 'tennis_ball 1.60%'. A picture of a small dog appears below the list.](images/finished_project.png)

--- collapse ---
---
title: What you should already know
---
This project assumes you already know some Python. Specifically, it assumes you know how to use:

+ Variables
+ Lists
+ Functions, including how to create your own function that accepts arguments

--- /collapse ---

--- collapse ---
---
title: What you will need
---

+ A computer
+ An internet connection
+ A Google account — if you don't have one, the next step will tell you how to get one

--- /collapse ---

--- collapse ---
---
title: What you will learn
---

+ What machine learning is
+ What a 'model' is (in the context of machine learning)
+ How the limitations of machine learning could impact your project

--- /collapse ---

--- collapse ---
---
title: Additional information for educators
---

If you need to print this project, please use the [printer-friendly version](https://projects.raspberrypi.org/en/projects/testing-vision/print){:target="_blank"}.

[Here is a link to the resources for this project](http://rpf.io/testing-vision-go).

--- /collapse ---
