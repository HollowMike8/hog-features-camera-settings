# hog-features-camera-settings
 
Project to develop an ML model (linear regression/NN..etc) to predict the output for the given input as accurately as possible

### Hyperparameter optimization/tuning:
1. learning rate
2. hidden units/beta_1/mini batch size
3. add hidden layers

### Trial_1:
##### Parameters:
alpha = 0.1 ; n_layers NN = 2 ; hidden_units_1 = 6 ; mini batch size = 64
##### Observation:
1. Training loss and validation loss are close --> no overfitting on training data
##### Tuning:
1. alpha = [0.001,0.1]: learning rates <= 0.0124 give minimal loss --> use alpha = 0.0124 
2. hidden_units_1 = [6, 8, 12, 16, 20] : hidden_units_1 >= 12 give minimal loss --> use hidden_units_1 = 12
3. mini batch size = [64, 128, 256, 512]: all give approx. same minimal loss --> use mini batch size  = 512
##### Next Steps:
Try additional hidden layers

### Trial_2:
##### Parameters:
alpha = 0.0124 ; n_layers NN = 3 ; hidden_units_1 = 12 ; hidden_units_2 = 9 ; mini batch size = 512
##### Observation:
1. Training loss and validation loss are less than previous case
##### Tuning:
1. alpha = [0.001,0.1]: learning rate = 0.01 gives minimal loss --> use alpha = 0.01 
2. hidden_units_2 = [9, 12, 16, 20] : all give approx. same minimal loss  --> use hidden_units_2 = 9
3. mini batch size = [64, 128, 256, 512]: all give approx. same minimal loss --> use mini batch size  = 512
##### Next Steps:
Try additional hidden layers

### Trial_3:
##### Parameters:
alpha = 0.01 ; n_layers NN = 4 ; hidden_units_1 = 12 ; hidden_units_2 = 9 ; hidden_units_3 = 9 ; mini batch size = 512
##### Observation:
1. Training loss and validation loss are approx. same as previous case
##### Tuning:
1. alpha = [0.001,0.1]: learning rate = 0.0143 gives minimal loss --> use alpha = 0.0143 
2. hidden_units_3 = [9, 12, 16, 20] : all give approx. same minimal loss  --> use hidden_units_3 = 9
3. mini batch size = [64, 128, 256, 512]: all give approx. same minimal loss --> use mini batch size  = 512
##### Next Steps:
Try batch gradient descent