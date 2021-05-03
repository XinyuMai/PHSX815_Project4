# PHSX815_Project4
for Project 4 the measurements must be interpreted in the context of a real physics experiment or analysis. For example, categorical dice rolls could be interpreted as spin measurements, or a Gaussian likelihood could represent the uncertainty in a measurement. It is expected that students will include at least one contemporary citation providing background information about the experimental scenario.

* What are the natural sources of variation in the scenario/measurement under study?
* What is the size of these variations for this measurement? Can the be modeled (even simplistically)?
* What are the sources of measurement uncertainty in the scenario? What are their size? Can this be included in the model and analysis?
* What question is being addressed by the measurement or analysis? Are there different hypotheses being considered? Or a model parameter that is being measured? How accurately can this be achieved?

## Project Description:  Orbit Stability Simulation of Planetary systems
Similar to previous project, we will simulate an idealized planetary system with the Sun at the center, corresponding to orbital parameters samples from Beta distribution. We implement the Hill stability Criterion \cite{Chambers:1996} \cite{Gladman:1993} to calculate fractional orbital separation for examination of stability of two bodies system. 


## This repository contains several types of programs:
* Revised project3/ `Simulation.ipynb`, `Analysis.ipynb` , `Random.py` [under development]


## Code Usage : NO NEED TO RUN IN TERMINAL, GENERATED IN JUPYTER NOTEBOOK.
 
In this project, we can implicitly specify non-default values for the probability of stable outcome (like a coin toss experiment) by specifying two model parameters alpha_{0}.  This simulation is with beta_{0} = 0.5 fixed. Nexp, Nmeasurement, Nsamples can be changed by users.


## For Peer reviewer 
Since my previous projects already interpreted the simulation in the context of a real physics experiment, that is simulating a planetary system [only two planets] with orbital parameters samples from Beta distribution and evaluate stability outcomes from Bernoulli trails. One of the natural sources of variation is the 

