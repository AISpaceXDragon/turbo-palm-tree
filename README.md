# turbo-palm-tree

## This repository is created as a part of task given by IISC.

This task involves find tuning IBM granite model on solving partial differential equations especially heat equation. 

My approach:

initially I started with understanding what the heat equation is and finding out the solutions from online material and research papers. Then I wrote Python scripts to generate the data required for training the model. the data set that I generated using the scripts is around thousand data points. The scripts mainly generate the data for heat equation in unit square mesh and unit circular domain with various boundary conditions like Neumann,Robin,Dirichlet conditions. 
I fine-tuned the model using lora and peft.