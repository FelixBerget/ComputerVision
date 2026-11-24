# Explanation of project, (NewModel)

## Data Preparation

First data is read, and then i set up dictionaries that are used later to convert back and forth between the ways labels can be represented.
Then i add the paths to images in my custom dataset and labels in number format, and then X and y training and test sets are created.
Then the convertion of tensors begins, first images are turned into numpy array then later turned into tensors and normalized from 0-1.
Then the y aka the labels are turned into tensors for use later in pytorch.

## Model

The model is a simple CNN that convolutes and pools each early layer to analyze the data and also to lower its size.
It is flattened to lower the dimensions, then it is put through linears to lower the size so that it can be predicted.
Also there is a lot of use of ReLU since we need to keep the negative values in check

## Use of Model

First the essentials are created in the model, optimizer and loss function.
The next function is the one that trains the model it goes through batches until done and the returns the loss from the whole learning process
The evaluate function is the function that is used to evaluate, it returns test set loss and accuracy


## Visualization and running of code

This is the end part and it is where i run the code and visualize what is learned
First is the function that finds labels and predictions from the test set and then makes a confusion matrix
Then the code to run everything

- Lists are created based on the measurables
- 10 epochs are run and the measurables is printed out and stored in arrays
- Graph is made based on the loss lists
- Confusion matrix function is used

