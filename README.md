# hog-features-camera-settings
 
Project to develop an ML model (linear regression/NN..etc) to predict the output for the given input as accurately as possible

### Hyperparameter optimization/tuning:
1. learning rate
2. hidden units/beta_1/mini batch size
3. add hidden layers

### Trial_1:
##### Parameters:
alpha = 0.1 ; n_layers NN = 2 ; hidden_units_1 = 6
##### Observation:
1. Training loss and validation loss are close --> no overfitting on training data
##### Next Steps:
Try different learning rates

### Trial_2:
##### Parameters:
alpha = [0.001,0.1] ; n_layers NN = 2 ; hidden_units_1 = 6
##### Observation:
1. learning rates <= 0.0124 give minimal loss --> use alpha = 0.0124 for next step
##### Next Steps:
Try different hidden units

### Trial_2:
##### Parameters:
alpha = 0.0124 ; n_layers NN = 2 ; hidden_units_1 = [6, 8, 12, 16, 20]
##### Observation:
1. learning rates <= 0.01 give minimal loss --> use alpha = 0.01 for next step
##### Next Steps:
Try different hidden units