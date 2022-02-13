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
alpha = [0.001,0.1] ; n_layers NN = 2 ; hidden_units_1 = 6 ; mini batch size = 64
##### Observation:
1. learning rates <= 0.0124 give minimal loss --> use alpha = 0.0124 for next step
##### Next Steps:
Try different hidden units

### Trial_3:
##### Parameters:
alpha = 0.0124 ; n_layers NN = 2 ; hidden_units_1 = [6, 8, 12, 16, 20] ; mini batch size = 64
##### Observation:
1. hidden_units_1 >= 12 give minimal loss --> use hidden_units_1 = 12 for next step
##### Next Steps:
Try different mini batch sizes

### Trial_4:
##### Parameters:
alpha = 0.0124 ; n_layers NN = 2 ; hidden_units_1 = 12 ; mini batch size = [64, 128, 256, 512]
##### Observation:
1. all mini batch size give approx. minimal loss --> use mini batch size  = 512 for next step
##### Next Steps:
Try additional hidden layers

### Trial_5:
##### Parameters:
alpha = 0.0124 ; n_layers NN = 3 ; hidden_units_1 = 12 ; hidden_units_2 = 9 ; mini batch size = 512
##### Observation:
1. Training loss and validation loss are less than previous case
##### Next Steps:
Try different learning rates

### Trial_6:
##### Parameters:
alpha = [0.001,0.1]; n_layers NN = 3 ; hidden_units_1 = 12 ; hidden_units_2 = 9 ; mini batch size = 512
##### Observation:
1. learning rate = 0.01 gives minimal loss --> use alpha = 0.01 for next step
##### Next Steps:
Try different hidden units for second hidden layer

### Trial_7:
##### Parameters:
alpha = 0.01 ; n_layers NN = 3 ; hidden_units_1 = 12 ; hidden_units_2 = [9, 12, 16, 20] ; mini batch size = 512
##### Observation:
1. Not much difference in losses by changing hidden_units_2 --> use hidden_units_2 = 9 (as before)
##### Next Steps:
Try different mini batch sizes

### Trial_8:
##### Parameters:
alpha = 0.01 ; n_layers NN = 3 ; hidden_units_1 = 12 ; hidden_units_2 = 9 ; mini batch size = [64, 128, 256, 512]
##### Observation:
1. Not much difference in losses by changing mini batch size --> use mini batch size = 512 (as before)
##### Next Steps:
Try additional hidden layers