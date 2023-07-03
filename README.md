# Biomimetics Ring Attractors

This repository accompanies the paper "Ring Attractors as the Basis for a Biomimetic Navigation System" Thomas C. Knowles, Anna Summerton, James G.H. Whiting and Martin J. Pearson.

--- link pending ---

## The model in action:

![Animated Ring Attractor Visualisation](https://github.com/TomKnowles1994/GridCellPredNet/blob/main/corrected_vs_uncorrected_short.gif "Animated Ring Attractor Visualisation")

This animation illustrates the model produced. It consists of three spiking Ring Attractors that together model a robot's planar translation. Each ring attractor is sensitive to a component of velocity, with their ring state mapping to coordinates in (x, y) to form the green trace. The goal of the system is to follow the ground truth robot trajectory (blue trace) as closely as possible.

This is supported by sensory data from the robot, synthesised into multisensory `experiences' by a Predictive Coding Network (PCN). The uncorrected model (green error line) can track the trajectory, but is subject to drift. The PCN-corrected model can use sensory data to compensate for drift, by recalling these prior experiences and their locations. Each Cartesian coordinate maps to a given ring state, and vice-versa, providing targets on the rings for corrective input.

## Data

The PCN experiences used to trigger corrective input can be found on the EBRAINS Knowledge Graph [EBRAINS Knowledge Graph](http://doi.org/10.25493/TSTK-AKK "Link to the PCN dataset").

The rat trajectory data used to generate Figure 2 is taken from [Sargolini et al. (2006)](https://www.science.org/doi/10.1126/science.1125572 "Link to the Sargolini et al paper")

## Results

Results generated in the course of this study can be found in the [Results folder](https://github.com/TomKnowles1994/Biomimetics-Ring-Attractors/tree/main/Results "Link to the Results folder").

## Reproducing the study

### Requirements

- Ubuntu 18.04 or higher (native or WSL)
- Python 3 installed
- Jupyter Lab install

### Steps

1. Download the PCN experience files listed under **Data**
2. Use the [environment.yml](https://github.com/TomKnowles1994/Biomimetics-Ring-Attractors/blob/main/environment.yml "Link to the environment file") to create a new virtual environment
3. Run the following:-

   1. Uncorrected.ipynb
   2. Multimodal.ipynb
   3. Visual.ipynb
   4. Tactile.ipynb
   5. Power Consumption.ipynb
  
4. Run Statistics.ipynb to generate the results and accompanying Figures 4, 5 and 6.
