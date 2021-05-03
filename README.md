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
Begin with `OrbitSim.py`, it will call from random class, samples from beta distribution by alpha and beta to calculate Delta_critical. Then numeriacally calculate the probability of being stable and pass to bernoulli probabaility distribution. A result of stable or unstable outcome is simulated by specifying number of systems and number of experiments you wish to evaluate. This program will generate simulated stable/untable systems indicating as '0' ot '1' and pipe it to a text file. 

	*  Options can be called from the command line with the -h 
	*  eg: `python3.8 python/OrbitSim.py -a 0.5 -b 0.5 -Nsystem 100 -Nexp 10000 -output H0.txt `
	*  -a alpha value
	*  -b beta value
	*  -output [filename]  name of file for hypothesis

It will also generate a distribution of Delta_{cr} samples from Beta distribution for two different set of shape parameters, alpha = 0.5 and beta = 0.5, click to see plot below: 

* ![plot](delta_cr_0.5_0.5.pdf)

Next step, we will use the text file data (fixed), analyze the simulated data to find the value of \\alpha and \\beta that maximizes L(alpha, beta|X) (the data is ”fixed” in an experiment), I am also planning to run the Neyman construction to compare the true value of alpha with calculated value. 

* project 2 `SimAnalysis.py` usage: `python3.8 python/SimAnalysis.py -a0 0.5 -b0 0.5 -a1 3.0 -b1 3.0 -input0 H0.txt -input1 H1.txt`
* A background paper extracted from paper 2 is provided for reviewer to know this simulation details.


