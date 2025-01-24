# turbo-palm-tree

## This repository is created as a part of task given by IISC.

This task involves fine-tuning IBM granite model on solving partial differential equations, especially heat equation. 

My approach:

Initially I started with understanding what the heat equation is and finding out the solutions from online material and research papers. Then I wrote Python scripts to generate the data required for training the model. the data set that I generated using the scripts is around thousand data points. The scripts mainly generate the data for heat equation in unit square mesh and unit circular domain with various boundary conditions like Neumann, Robin, Dirichlet conditions and intial conditions. 

The above idea was taken from a research paper as mentioned below:

[Exploring Datasets to Solve Partial Differential Equations with TensorFlow](references/Borzdynski-Borondo-Curbelo.pdf;jsessionid=5AB5FA56AEC7E6CD9B98E466E24784AE-2.pdf)

Model fine-tuning:

I fine-tuned the model using lora and peft. I didn't use any custom loss metric to fine-tune. I tried to use Meteor Score to fine-tune the model but the model would not report the loss/ not converge properly. I tried to know the reason behind it, but in the view of deadline, I didn't delve deeper into it. I am working on it currently(the competition has come to an end).One more thing I observed intially is that the model was not converging(can be inferred from the training loss and validation loss during fine-tuning). I have not known its reason as of now.

Dataset:

The dataset that I created contains two columns namely "Question" and "Answer". The total number of data points in this dataset are around "1400" question answer pairs. The dataset was converted/formatted into the following format(achieved by using formatting_func()):

```"Question : {question} \n Answer: {answer}<|end_of_text|>" ``` that is then given to the model during fine-tuning.

The dataset could be accessed from the hyperlink below.

-->[Click on this for dataset](dataset/third_merged_dataset.csv)<--

The code files could be accessed from the hyperlinks below.

-->[Click on this for data preprocessing, training, testing notebook]()<--

-->[Click on this for data_generator.ipynb](code/dataset_generator.ipynb)<--




