# Assignment 3: Utilizing Hyperdimensional Computing
ECE 556: Neuromorphic Computing  
Instructor: Dr. Maryam Parsa  
Term: Spring 2025  

---

## Assignment Summary

For our final assignment, we will be examining a relatively new neuromorphic strategy called hyperdimensional computing (HDC). This strategy is often also referred to as vector symbolic architecture (VSA). 

We will be using yet another library for this task, called torchhd. 

## 0. Preliminaries

As noted above, you will need to install torchhd to complete this project. Additionally, please read the following paper. 

[torchhd](https://github.com/hyperdimensional-computing/torchhd)

[P. Kanerva, "What We Mean When We Say 'What's the Dollar of Mexico?': Prototypes and Mapping in Concept Space", AAAI Fall Symposium, 2010.](https://redwood.berkeley.edu/wp-content/uploads/2020/05/kanerva2010what.pdf)

We will also be making use of the Car Evaluation and Balance Scale UCI classification datasets. 

- [Car Evaluation](https://archive.ics.uci.edu/dataset/19/car+evaluation)
- [Balance Scale](https://archive.ics.uci.edu/dataset/12/balance+scale)

There are also two optional papers to look at for this assignment. These papers demonstrate some of the potential capabilities of VSAs, specifically representing spatial locations and graph data. 

[B. Komer, T. Stewart, A. Voelker, C. Eliasmith, "A Neural Representation of Continuous Space Using Fractional Binding", 41st Meeting of the Cognitive Science Society, July 2019](https://compneuro.uwaterloo.ca/files/publications/komer.2019.pdf)

[P. Poduval, H. Alimohamadi, A. Zakeri, F. Imani, M. H. Najafi, T. Givargis, M. Imani, "GrapHD: Graph-Based Hyperdimensional Memorization for Brain-Like Cognitive Learning", Front. Neurosci., vol 16, 2022.](https://www.frontiersin.org/journals/neuroscience/articles/10.3389/fnins.2022.757125/full)

---

## 1. Exploration of VSA

### 1.1. Balance Scale

We will begin by examining the Balance Scale UCI dataset. Note that the data is categorical across 4 features. 

Your first task is to represent this data using the Multiply Add and Permute (MAP) style hyperdimensional vectors conveniently included in the torchhd library. 

Start by creating hyperdimensional representations for the different features using a strategy of your choosing, and then use the bundle and bind operations to generate a hyperdimensional representation for each class in the classification problem.
If you get stuck, refer to the "What's the Dollar of Mexico" paper or feel free to reach out to me.

Once you have a VSA for each label, create a similarity matrix using cosine similarity (also included in torchhd) comparing each label to every other label. Save this output for your report. 

### 1.2 Car Evaluation

Repeat the VSA label generation and similarity matrix experiment above for the Car Evaluation dataset. 

Once complete, split your data into a train and test set with 20% of the data reserved for testing. From there, rebuild your VSA labels using the training data only. Then, evaluate your ability to classify data in the test set by simply creating a VSA representation for each feature row and choosing the class with the highest cosine similarity label to the feature vector. 

You may notice Car Evaluation has a benchmark results listing on the UCI page. Do not worry if your results are not close to these scores. You are not required to implement a complex solution at this point, just exploring the latent representation capabilities of basic VSAs using only cosine similarity.

---

## 2. Report

Compile your results into a report. This must include: 
- Your label similarity matrix for Balance Scale
- Your label similarity matrix for Car Evaluation
- Your accuracy results for Car Evaluation using MAP vectors

Be sure to discuss in detail how you built your VSA feature representations, including the math behind the bundle and binding operations. Are there ways you could improve your feature structures? Do the similarity scores in your label matrices make sense? Be specific and provide thoughtful analysis on your findings. 

As always, please format your report in a professional manner. 
