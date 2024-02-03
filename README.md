# 2024_quantinuum
Quantinuum repository for iQuHACK 2024

![Quantinuum Logo__horizontal black](https://github.com/iQuHACK/2024_planning_quantinuum/assets/106914305/44e677cf-8523-4157-a248-89968215ee34)

## Useful Links to get you started with TKET are:
 - [pytket user manual](https://tket.quantinuum.com/user-manual/)
 - [pytket API docs](https://tket.quantinuum.com/api-docs/)
 - [pytket Notebook Examples](https://tket.quantinuum.com/examples/Getting_started.html)

## Quantinuum Nexus: An Integrated Quantum Computing Platform
To access the Quantinuum H1-1 emulator, you will be using [Quantinuum Nexus](https://nexus.quantinuum.com/). Quantinuum Nexus will allow you to develop, execute, manage, and share all your quantum projects on one easy-to-use cloud platform.
Once the challenge begins, you'll be invited to set up a Quantinuum Nexus account.

### Useful Links to get you started with Quantinuum Nexus are:
(Please note these links require a Quantinuum Nexus account - see below)

 - [Cloud Jupyter environment with pre-installed software](https://nexus.quantinuum.com/hub)
 - [Nexus API docs and example notebooks](https://nexus.quantinuum.com/docs)


## Eligibility
Quantinuum employees are not eligible to participate in the Quantinuum MIT iQuHACK challenge.
For the general rules on eligibility and hackathon participation, please take a look at the official rules.


# Quantinuum Challenge: Quantum Phase Estimation

Quantum Phase Estimation (QPE) is an important subroutine in many quantum algorithms. An implementation of QPE is provided in the [phase_estimation.ipynb](https://github.com/iQuHACK/2024_planning_quantinuum/blob/main/challenge_resources/phase_estimation_challenge.ipynb) jupyter notebook. For reading purposes, you may prefer to view this version of the notebook -> https://tket.quantinuum.com/examples/phase_estimation.html.

1. The notebook provided implements the standard form of QPE. There are several other variants. Experiment with the following variants of QPE and compare their performance to the variant in the notebook using the Quantinuum simulator.

    * Implement iterative QPE - This is a variant of QPE that uses a single ancillary qubit that is repeatedly measured. This is less resource intensive for near term quantum hardware than the standard QPE variant. 

    * Implement the Bayesian variant of QPE from https://arxiv.org/pdf/1508.00869.pdf

2. The paper [Some improvements to product formula circuits for Hamiltonian simulation](https://arxiv.org/pdf/2310.12256.pdf) proposes some more efficient circuit templates for QPE-type applications. 

    * Implement the improved circuit templates from section 3.2 for some Hamiltonian operator $H$ (to be provided) and compare the size of the circuits to those in the notebook provided. Run some simulations to compare the performance of the two methods of realising the time evolution operator $U(t) = e^{i H t}$.

    * In section 3.3 the paper also proposes using parallel controlled rotations. Implement the proposed decomposition for the controlled $e^{- i \theta Z}$ rotation gates and compare the circuit size and depth to the compiled circuit produced by TKET.
  
## Resources for background on Phase estimnation

* [Online notebook](https://tket.quantinuum.com/examples/phase_estimation.html) - Perhaps easier to read than the version in this repository
* [Stack exchange post](https://quantumcomputing.stackexchange.com/questions/32594/how-would-you-draw-the-phase-estimation-circuit-for-the-eigenvalues-of-u-mat/32598#32598) explaining the phase estimation circuit.
* Nathan Wiebe lecture on iterative phase estimation - https://www.youtube.com/watch?v=ks9yjamHJno
* Qiskit video on iterative phase estimation - https://www.youtube.com/watch?v=aLSM0_H8hUE
* Quantinuum paper on Bayesian phase estimation with the iceberg error correction code - https://arxiv.org/pdf/2306.16608.pdf

## Challenge Guidance 

The aim of this challenge is to explore variants of the quantum phase estimation algorithm and smart/efficient ways of running this algorithm using the Quantinuum Nexus platform.

The above two questions suggest ideas for building on the notebook provided. These do not need to be strictly adhered to. Other approaches to QPE will also be considered. For example, you may wish to explore error correction/detection with QPE-type circuits or use phase estimation as a subroutine in a larger algorithm ( for example, Shor's algorithm for factoring or the HHL algorithm for solving systems of equations).

The challenge will be judged on the following...

* The degree to which you explore different variants of QPE and related algorithms (Going beyond the example notebook provided).
* The use of simulations to evaluate the performance of algorithms. This includes considerations such as circuit depth and gate count which influence performance when device noise is present.
* The quality of explanation in your presentation. Ideally, back up any claims with data from simulations.

## When you are ready to begin

* One member of the team should fork this repository and share the URL with team members. 
* When the challenge begins you will get an email inviting you to set up an account on the Quantinuum Nexus website.
* Follow the instructions on the invite email and visit [https://nexus.quantinuum.com](https://nexus.quantinuum.com). 
* Once you've logged in, click on the burger menu in the top left corner and select 'Lab'.
* Select 'Start' to boot up your hosted workspace.
* Once in the workspace, click on the Git icon in the left-most panel and clone your team's forked repo using the URL from above.
* Run through the Quantinuum Nexus tutorial in [start_here_nexus_tutorial.ipynb](https://github.com/iQuHACK/2024_planning_quantinuum/blob/main/challenge_resources/start_here_nexus_tutorial.ipynb) to get started with the Quantinuum Nexus platform.
* Run through the challenge tutorial in [phase_estimation_challenge.ipynb](https://github.com/iQuHACK/2024_planning_quantinuum/blob/main/challenge_resources/phase_estimation_challenge.ipynb) for an introduction to the phase estimation algorithm. This notebook can also serve as an optional base for any variants on QPE you end up implementing in the challenge (you don't have to start from scratch). Code in this notebook file is also available as a Python script called `phase_estimation_challenge.py`.
* When you are ready to submit your project, send a link to your fork of this repository in the quantinuum challenge slack before the time limit.
