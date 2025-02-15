## Program Overview

This program implements an HLLC Riemann solver for the full shallow water equations, coded from scratch based on the methodology described by [Hou et al. (2015)](https://www.sciencedirect.com/science/article/pii/S1364815214003648). The case study in the paper simulates the 1993 tsunami that struck Okushiri Island, off the west coast of Hokkaido, Japan. The focus is Monai Valley on the island’s southwestern coast, where an extreme vertical runup of 30 metres was recorded. The current simulation predicts a maximum runup of approximately 32 metres (to scale), closely matching field observations. For more details, visit the [NOAA Centre for Tsunami Research](https://nctr.pmel.noaa.gov/benchmark/Laboratory/Laboratory_MonaiValley/index.html).

https://github.com/user-attachments/assets/d9607e87-75a9-42ac-a661-9e77c2a880c6

![](https://github.com/user-attachments/assets/d179f6e4-ec49-4eb8-a6a9-c8f6309749a2)

## Program Files

|    File    | Purpose                                                                                                                                                                  |
| :--------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  main.f90  | Main program containing functions and subroutines for flow solver.                                                                                                       |
| monai.py\* | Pre-processing program to set up initial conditions for Monai Valley case study.                                                                                         |
|  read.py   | Post-processing program to create flow animation with Plotly.                                                                                                            |
| b_raw.txt  | [Raw bathymetry data](https://nctr.pmel.noaa.gov/benchmark/Laboratory/Laboratory_MonaiValley/MonaiValley_Bathymetry.txt) for Monai Valley case study used in monai.py.   |
| ht_raw.txt | [Raw inflow height data](https://nctr.pmel.noaa.gov/benchmark/Laboratory/Laboratory_MonaiValley/MonaiValley_InputWave.txt) for Monai Valley case study used in monai.py. |
| monai.geo  | File containing geometric information to generate mesh in [Gmsh](https://gmsh.info/#Download).                                                                           |
| monai.su2  | File containing mesh information to input to main program.                                                                                                               |

\* Run `monai.py` if running the case study for the first time, or when there is a change in mesh size or time step.

## Solver Theory

![](https://github.com/user-attachments/assets/a157f8a5-8359-49f8-b0ca-327876429fae)

## References

[1] Hou et al. (2015). _An Efficient Unstructured MUSCL Scheme for Solving the 2D Shallow Water Equations._  
[2] Song et al. (2011). _A Robust Well-Balanced Finite Volume Model for Shallow Water Flows with Wetting and Drying over Irregular Terrain._
