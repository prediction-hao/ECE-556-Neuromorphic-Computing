# Assignment 2: Training Spiking Neural Networks
ECE 556: Neuromorphic Computing  
Instructor: Dr. Maryam Parsa  
Term: Spring 2025  

---

## Assignment Summary

For this assignment, we will be looking at implementing different ways to train spiking neural networks. 

The first part uses snnTorch for training; however, we will be utilizing a new library for the second part. 

This introduces another challenge within the neuromorphic community: there are many disparate libraries and platforms, each with their own unique strengths and weaknesses. 

## 0. Preliminaries

You should already have snnTorch installed from your last assignment, but you will need to install BindsNet as well. We will also be making use of Gymnasium.

In addition, you are assigned reading of a couple of papers and some snnTorch documentation. It would also likely be beneficial to look at examples in the Bindsnet repo. 

[BindsNet](https://github.com/BindsNET/bindsnet?tab=readme-ov-file)

[Gymnasium](https://gymnasium.farama.org/) (see the Arcade Learning Environment in particular)

[R. V. Florian, "Reinforcement Learning Through Modulation of Spike-Timing-Dependent Synaptic Plasticity," in Neural Computation, vol.19, pp. 1468-1502, 2007, doi: 10.1162/neco.2007.19.6.1468.](https://florian.io/papers/2007_Florian_Modulated_STDP.pdf)

[E. O. Neftci, H. Mostafa and F. Zenke, "Surrogate Gradient Learning in Spiking Neural Networks: Bringing the Power of Gradient-Based Optimization to Spiking Neural Networks," in IEEE Signal Processing Magazine, vol. 36, no. 6, pp. 51-63, Nov. 2019, doi: 10.1109/MSP.2019.2931595.](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8891809)

[Training SNNs  with snnTorch Tutorial](https://snntorch.readthedocs.io/en/latest/tutorials/tutorial_5.html)

---

## 1. Part 1: Surrogate Gradient Descent in snnTorch

To start the assignment, we will again be using the MNIST dataset, with images sized at 28x28. Pick your encoding method, design your network, and set your hyperparameters (e.g. learning rate, batch size, any regularization, etc.), then train your network via surrogate gradient descent. 

Make sure to apply any necessary transformations to the MNIST images, and feel free to train for any number of epochs. Save your training and validation losses for each iteration, as you will need them for your report. 

---

## 2. Part 2: Training with BindsNet

As you may have noticed while reading snnTorch documentation, it focuses heavily on surrogate gradient descent. But there are other ways to train spiking neural networks, which means we will need to use another library to implement them easily. 

One such way is the biologically plausible STDP method. You can also use evolutionary strategies or hebbian learning, which has also become extremely popular for classical machine learning models. Still others exist, with training methods being an active area of research informed by discoveries in neuroscience. 

For this section, we will focus on STDP and reinforcement learning using the Arcade Learning Environment (ALE).  Make sure Gymnasium is installed and look over the Gymnasium and BindsNet examples to guide you on this section. 

You are tasked with implementing a network in Bindsnet and training it with reward modulated STDP with eligibility trace (MSTDPET) to play the game Space Invaders, specifically the "SpaceInvaders-v0" environment.  Again, you can choose an encoding method (use built in methods in BindsNet for simplicity), hyperparameters, and network architecture yourself. Run for a minimum of 100 episodes and record your results. 

Do not worry if you do not get great results. Just be sure to discuss your findings in the report. 

---

## 3. Report

Compile your results into a report. Be sure to discuss what hyperparameters and architecture decisions you ultimately made and why. Provide analysis on your results: were they good or bad, how might they be improved, what is or isn't working and why, etc.

Please include a plot of your training and validation loss curves on MNIST as well as plots of your total training reward each episode of Space Invaders.

Your paper should be compiled as a pdf with professional formatting and should include introduction, methodology, results, and conclusion sections.

Submit your report alongside all code written to generate results. 