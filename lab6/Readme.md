Deadline: April 24, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**
1. Visualize samples from posterior distribution for linear model with 2 parameters using:
    - MC
    - variational optimization
    - SGLD
    - true dsitribution
    
     
2. Repeat sampling procedure from [paper](https://arxiv.org/abs/1211.4246). Compare sampling with SGLD procedure.

3. [Skorik Sergey] Train at least 100 MLP models on a toy dataset. Visualize their parameter projection onto 2d-space with color corresponding to accuracy.

4. Train multiple MLP models on a toy dataset. Make a random pruning of the models. Visualize their parameter projection onto 2d-space with color corresponding to accuracy.
    

5. Train an MLP model on a toy dataset (at least 3 layers). Make a random pruning of the models. Visualize the binary matrix projection onto 2d-space with color corresponding to accuracy.
   
6. Train deep weight prior on MNIST dataset ane evluate its performance on SVHN dataset (make SVHN gray-colored).

