Deadline: Febraury 22, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**

Save notebooks into lab4/SurnameTask4.ipynb

1. [Barabanshchikova Polina] Visualize uncertainity estimation using multiple neural networks. Data: simple regression model: Y = WX + eps. Model: a one-layer neural netwok. Plot: uncertainity with different number of neural networks (see [slide 21](https://raw.githubusercontent.com/intsystems/BMM/main-22/slides/slides10_ens.pdf)).


2. Visualize ECE using multiple neural networks. Data: a toy-dataset from sklearn. Model: a one-layer neural netwok. Plot: ECE with different number of neural networks.
(see [slides about ECE](https://raw.githubusercontent.com/intsystems/BMM/main-22/slides/slides10_ens.pdf)).

3. Compare optimal brain damage procdure using diagonal hessian and full-rank hessian. Model: linear regression model. Data: simple dataset (not more than 50 variables). Plot: dependence of the model performance on the number of removed features. 
* [OBD paper](https://proceedings.neurips.cc/paper/1989/file/6c9882bbac1c7093bd25041881277658-Paper.pdf)

4. [Yakovlev Konstantin] Build multiple (not less than 10) 1-layer neural networks for a dataset using bagging. Make a weighted ensemble of the models. Train ensemble weights in different regimes:
    - Using Softmax
    - Using Gumbel-softmax with lowering temperature
    
Visualize the performance of the ensembler from the optimization iteration. Visualize the weights of the ensemble with dependence on the optimization iteration. 


5. [Kovaleva Maria] Demonstrate the lottery ticket hypothesis. Train a 3-layer network on a CIFAR-10. For p=[10, 20, ... 90] select multiple subnetworks with p% of parameters. And retrain them. For each percentage select the network with best performance. Visualize performance depndency on p. 


6. Implement 1-st order DARTS for CIFAR-10 dataset. Model: 3-layer network. Structure: binary mask for each parameter. Plots: model peformance, mask.

7. Implement ENAS for CIFAR-10 dataset. Model: 3-layer network. Structure: binary mask for each parameter. Plots: model peformance, mask.


