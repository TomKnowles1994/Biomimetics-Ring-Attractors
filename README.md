# Biomimetics Ring Attractors

This repository accompanies the paper "Ring Attractors as the Basis for a Biomimetic Navigation System" Thomas C. Knowles, Anna Summerton, James G.H. Whiting and Martin J. Pearson.

--- link pending ---

## The model in action:

![Animated Ring Attractor Visualisation](https://github.com/TomKnowles1994/GridCellPredNet/blob/main/corrected_vs_uncorrected_short.gif "Animated Ring Attractor Visualisation")

This animation illustrates the model produced. It consists of three spiking Ring Attractors that together model a robot's planar translation. Each ring attractor is sensitive to a component of velocity, with their ring state mapping to coordinates in (x, y) to form the green trace. The goal of the system is to follow the ground truth robot trajectory (blue trace) as closely as possible.

This is supported by sensory data from the robot, synthesised into multisensory `experiences' by a Predictive Coding Network (PCN). The uncorrected model (green error line) can track the trajectory, but is subject to drift. The PCN-corrected model can use sensory data to compensate for drift, by recalling these prior experiences and their locations. Each Cartesian coordinate maps to a given ring state, and vice-versa, providing targets on the rings for corrective input.

## Data

Data generated in the course of this study can be found in the ![Results folder](https://github.com/TomKnowles1994/Biomimetics-Ring-Attractors/tree/main/Results "Link to the Results folder").

The PCN experiences used to trigger corrective input can be found on the EBRAINS Knowledge Graph ![EBRAINS Knowledge Graph](http://doi.org/10.25493/TSTK-AKK "Link to the PCN dataset").

The rat trajectory data used to generate Figure 2 is taken from ![Sargolini et al. (2006)](https://www.science.org/doi/10.1126/science.1125572 "Link to the Sargolini et al paper")

