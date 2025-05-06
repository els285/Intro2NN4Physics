# Practical Activities

The exercises are given as iPython notebooks.

The preferred way to run these is in Google Colab, for two reasons:
1. We have used Colab's additional features to suppress all sections and hide the solutions, making them more readable.
2. You can use a GPU with Colab. This won't be necessary for the ML tasks we present.

To access the exercises, use the following links, and click on the "Open in Colab" button.

[Ex1 - PyTorch Tensors](https://github.com/els285/Aachen_Intro2NN/blob/main/Exercises/1_Tensors.ipynb)

[Ex2 - Regression with Scikit-Learn](https://github.com/els285/Aachen_Intro2NN/blob/main/Exercises/2_Regression_Penguins_SKlearn.ipynb)

[Ex3 - Regression with PyTorch](https://github.com/els285/Aachen_Intro2NN/blob/main/Exercises/3_Regression_Penguins_PyTorch.ipynb)

[Ex4 - Classification](https://github.com/els285/Aachen_Intro2NN/blob/main/Exercises/4_Classification_Penguins.ipynb)

[Main Exercise - Classifying ATLAS OpenData Events](https://github.com/els285/Aachen_Intro2NN/blob/main/Exercises/DNN4HEP_exercise.ipynb)

Alternatively, you can replace `github.com` with `githubtocolab.com` in the URL for automatically opening in Colab.

## Tasks
### Exercise 1
Playing around with `torch.tensors`. Designed to take 25 minutes.

### Exercise 2
Introducing the concept of regression very lightly. Desgined to take 15 minutes

### Exercise 3
Using `torch` to build linear regression models and deep neural networks for regression. Designed to take 30 minutes

### Exercise 4
Looking at a classification task. Designed to take 30 minutes

### Main Exercise
Building a DNN classifier to study ATLAS OpenData. Designed to be started in the first session, and the focus of the second session.

#### Full explanation
At the LHC, we collide protons to create interesting particles and study the universe at very fine scales.
The proton collisions can produce many different particles; the ones we're interested are frequently heavy and unstable and decay to lighter things which we measure with our detectors (like the ATLAS detector where most of the lecturers at this school work!)

A problem is that two different particles might decay into the same final state. The example we will look at considers a Higgs boson which decays (via two intermediate W bosons) into two leptons. This is the signal we want to observe to "discover the Higgs boson". A background process, which we want to suppress, is that of two top quarks decaying to two leptons (again via two intermediate W bosons). Note that alongside the leptons, we will have lots of hadronic matter being created - this is seen in the detector as things called jets - ask the lecturers if you don't know and care what these are!

So our problem is that we have two different processes which have the same final state when measured with the ATLAS detector. We will use a DNN to classify individual proton-proton collisions (called events) as signal (from the Higgs boson) or background (from the top quarks).