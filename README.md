# biochem_kinetic_fitting
The repository contains python code to perform kinetic fitting by solving ordinary differential equations (ODEs). It will plot the fit and export the fit

## Purpose
To fit for kinetic, it was specifically written for kinetic that contains a single rate constant, using toehold mediated strand displacement (TMSD) as example, the code cannot be used for TMSD with toehold exchange, as it is a 2 steps kinetics. It will solve an ODEs system to proximate the best rate constant - k_eff and scaling factor - alpha. The code will print out the k_eff, alpha, cov_matrix and equation for the fit in the console.

Depending on the usage, one can redefine the ODEs for the specific condition.

## Packages required
The following packages are needed for the code to run:
  - numpy
  - matplotlib
  - pandas
  - seaborn
  - scipy
  - tkinter

The following packages are optional:
  - palettable [https://jiffyclub.github.io/palettable/]

## File format
To simplify the use, the code is written so that you have a pre-processed data as a typical excel file.
The code will accept an excel from your local computer and will work based on panda's dataframe.
The excel should have the following format, for each sheet:
  - Column A : Time in seconds
  - Column B : Fluorescence signal
  - Column C : Description of the data
  - Column D : Normalised Fluorescence signal

Column D can be computed through code instead

Different samples should be in different sheet, this is so that the dictionary can be compiled. The code will output a graph and an excel of the ODE fit.
## Example fit
The script was used unmodified with the example data to perform the fitting.


Excel Sheet position 1
![Example datafiguredf_1_TMSD_1](https://github.com/chalmers4c/biochem_kinetic_fitting/assets/97460687/b5b88e32-a30a-41f8-9398-e50c81f76ea4)


Excel Sheet position 2
![Example datafiguredf_2_TMSD_2](https://github.com/chalmers4c/biochem_kinetic_fitting/assets/97460687/de5876c3-c73a-43ec-ac16-7f77331e978b)


## Acknowledgement
The code was largely based on previously published code by sulcgroup [https://github.com/sulcgroup/TMSD_fitting]
