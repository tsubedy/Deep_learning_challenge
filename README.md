# Overview

The purpose of this project is to attempt to predict whether the applicants will be successful if funded by the Alphabet Soup Co. The applicants will be funded if the Alphabet co have better predictions of their success in advance. A neural network is created by Data preprocessing, creating training and testing sets, and finally optimizing the models.


# Results:

### Data Processing 

In order to process the data to create model removed the EIN and NAME columns.
The varibales being considered for the model are as follows: 'STATUS', 'ASK_AMT', 'IS_SUCCESSFUL', 'APPLICATION_TYPE', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT'. I dropped "USE_CASE_Other","AFFILIATION_Other" columns.

The Dependent varible is "IS_SUCCESFUL" as the goal of the project is to get a highly accurate prediction of the applicants  be successful.


### Compiling, Training, and Evaluating the Model 

#### Attempt - 1

2 Hidden Layers
80 neurons (Layer1), 30 neurons(Layer2)
Used Relu and Sigmoid Activations Functions as sigmoid function is considered the best for binary classifcation problems and Relu for nonlinear datasets.

Some of the noisy features including "USE_CASE_Other","AFFILIATION_Other" are removed before creating the model.

The results obtained as follows:
Loss:0.5788350105285645, Accuracy: 0.7279883623123169


#### Attempt - 2

3 Hidden Layers
80 neurons (Layer1), 30 neurons(Layer2), 15 neurons(Layer3)
Used the same functions as in attempt -1 with additional 3rd layer of 15 neurons. 

The results obtained as follows:
Loss:0.5859888792037964, Accuracy: 0.7294460535049438

In this model, both the loss and accuracy have slightly increased. 

#### Attempt - 3

Changing Activation Function

3 Hidden Layers

80 neurons(Layer1), 30 neurons(Layer2), 15 neurons (Layer3)

The activation functions are changed for 2nd and 3rd layers and obtained the following results.

Loss:0.5733916163444519, Accuracy: 0.7271137237548828

In this model, the model scores have slightly decreased.  


#### Attempt - 4

Original data with redistribution of the neurons.

3 Hidden Layers
80 neurons (Layer1), 35 neurons(Layer2), 10 neurons (Layer3)

The activation functions are kept as in the original data and the neurons are redistributed. 

The model score obtained are as follows:

Loss:0.5806168913841248, Accuracy: 0.7306122183799744

Original data with redistribution of neurons gives the higher accuracy score. 


# Summary: 

A various attempts are made to see if the model score improves towards 75%, but in this dataset and modeling processing highest the score remains as 73% which will be considered as an optimized model. It seems like more features are needed to see the optimum results. 
 
