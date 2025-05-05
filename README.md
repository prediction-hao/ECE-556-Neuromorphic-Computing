# Assignment 1: Spike Trains and the Leaky Integrate-And-Fire Neuron
ECE 556: Neuromorphic Computing  
Instructor: Dr. Maryam Parsa  
Term: Spring 2025   

___

## Assignment Summary

Your first assignment is in two parts. For both parts, we will be utilizing [snnTorch](https://snntorch.readthedocs.io/en/latest/), a well-documented neuromorphic library.

For the first part, we will be examining the encoding and decoding of data, namely the popular MNIST dataset, to and from binary spike trains. 

For the second part, we will do a brief exploration of the leaky integrate-and-fire (LIF) neuron. 

## 0. Preliminaries

To start, take a look at encoding and decoding methods in this paper: 

[B. Petro, N. Kasabov and R. M. Kiss, "Selection and Optimization of Temporal Spike Encoding Methods for Spiking Neural Networks," in IEEE Transactions on Neural Networks and Learning Systems, vol. 31, no. 2, pp. 358-370, Feb. 2020, doi: 10.1109/TNNLS.2019.2906158.](https://ieeexplore.ieee.org/document/8689349)

Pay special attention to the different metrics used to analyze the encoding/decoding methods, as we will be utilizing them in this assignment. 

Next, read over these two tutorials over on the snnTorch documentation page:  
- [Spike Encoding Tutorial](https://snntorch.readthedocs.io/en/latest/tutorials/tutorial_1.html)
- [Leaky Integrate-and-Fire Tutorial](https://snntorch.readthedocs.io/en/latest/tutorials/tutorial_2.html)

You will also need to set up a Python programming environment with snnTorch and [PyTorch](https://pytorch.org/) installed. 

---

## 1. Part 1: Encoding/Decoding

### 1.1 Metrics
First, you will need to write two functions, defined in the B.Petro et. al. paper above, for signal analysis: 

- Root Mean Square Error (RMSE): Computes the error between two signals. 

- Average Firing Rate (AFR): Computes, on average, how often a spike train has a spike. 


### 1.2 Encoding and decoding data

Using snnTorch, access the MNIST training data and perform both rate coding and latency coding on one of each of the 10 digits. Get the AFN of your spike trains for each digit. Then, for the rate coded vectors, reconstruct the signals and compare the reconstruction to the original signals for each digit using RMSE. Do this again for rate coded vectors with a gain of .33. 

---

## 2. Part 2: The LIF Neuron

Write a function implementing the LIF neuron with spiking and reset behavior.

Examine behavior of your neuron for a high signal at t=0, a low signal that switches to high at t=25, and a pulse input that is high from t=15 to t=30.

Make sure your constructed signal is long enough to see behavior over time (e.g. at least 300 time steps or so). 

Adjust and explore the effects of hyperparameters on your neuron, such as the resistance, capacitance, and threshold values.  

---

## 3. Report

Finally, you must compile your results into a report where you discuss and analyze your findings. This report must, at a minimum, include: 
- A table displaying your 10 selected original MNIST digits to their reconstructed counterparts for rate encoding 
- A table showing the RMSE metric value for the original and reconstructed signals.
- A comparison of the rate encoding vs latency encoding average firing rate and its significance 
- Plots of the input signal, membrane potential, and output spikes for your LIF neuron for two different hyperparameter values for each of the three input types.
- A table displaying your chosen hyperparameters for your neuron experiments.
- The math formula for your LIF implementation.

In addition to these figures, your report should explain the mechanisms of what is happening in your figures. Analyze the results and draw conclusions from your findings. Explain the purpose of spike encoding and how it relates to LIF neurons. Also discuss any challenges you encountered during implementation.

Your paper should be compiled as a pdf with professional formatting and should include introduction, methodology, results, and conclusion sections.

Submit your report alongside all code written to generate results. 


