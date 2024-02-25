Deadline: March 1, 23.59.

Save notebooks into task3/SurnameTask3.ipynb

**IMPORTANT:** the code must not be written in Torch/Tensorflow. For deep learning use Jax.

1. [reporter: Timofey Chernikov] Implement 1-st order DARTS for CIFAR-10 dataset. Compare with random structure selection. Model: 3-layer network. Structure: binary mask for each parameter. Plots: model peformance, mask. **NOTE:** binary mask won't work with unconstrained parameter optimization, think how to overcome this limitation.
    * [DARTS paper](https://arxiv.org/abs/1806.09055)
    
2. [reporter: Dmitry Protasov] Implement ENAS for CIFAR-10 dataset. Compare with random structure selection. Model: 3-layer network. Structure: binary mask for each parameter. Plots: model peformance, mask.
    * [ENAS paper](https://arxiv.org/abs/1802.03268)

3. [reporter: Marat Khusainov] Implement naive-RMAD (without information loss restoring) for 2d problem (the loss surface must be nontrivial). Plot the forward trajectory and restored trajectory for different number of epoch and different momentum (mu = 0, 0.5, 0.9, 0.99).
    * [RMAD](https://proceedings.mlr.press/v37/maclaurin15.pdf)
    * [Talk slides](https://www.robots.ox.ac.uk/seminars/Extra/2015_07_23_DavidDuvenaud.pdf)
    
4. [reporter: Parviz Karimov] Consider Bayesian linear regression. Restore covariance matrix using Bayesian optimization methods. The covariance matrix must be full-ranked. Plot the dependence of the restoration performance from number of iterations for different data dimmensions.
    * [Bishop](https://www.microsoft.com/en-us/research/uploads/prod/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)
    * [Optuna, recommended for BO](https://optuna.org/)
    
5. [reporter: TODO] Consider Bayesian linear regression. Restore covariance matrix using HOAG method. Consider full-ranked and 1-ranked covariance matrix. Plot the dependence of the restoration performance from number of iterations for different data dimmensions.
    * [Bishop](https://www.microsoft.com/en-us/research/uploads/prod/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)
    * [HOAG](https://arxiv.org/abs/1602.02355)
   
6. [reporter: TODO] Implement greedy hyperparameter optimization for logistic regression on FASHION-MNIST. Compare two types of hyperparameters:
    * Binary mask for each parameter
    * l2-coefficients for each parameter.
    
    **NOTE:** binary mask won't work with unconstrained parameter optimization, think how to overcome this limitation.
    
    Compare results and hyperparameters.
    * [Greedy optimization](https://arxiv.org/abs/1511.06727)
    * [DARTS paper, uses the same hyperparameter optimization method](https://arxiv.org/abs/1806.09055)
    
7. [reporter: Boeva Galina] Implement a genetic algorithm for model structure selection for CIFAR-10 dataset. Compare with random structure selection. Model: 3-layer network. Structure: binary mask for each parameter. Plots: model peformance, mask. 

8. [reporter: TODO] Implement a ENAS-based symbolic regression.
    * [ENAS paper](https://arxiv.org/abs/1802.03268)
    * [symbolic regression idea](http://www.machinelearning.ru/wiki/images/5/53/Varfolomeeva2015MsPresentation.pdf)
   
9. [reporter: Kseniia Petrushina] Consider Bayesian linear regression. Restore covariance matrix using Bayesian optimization methods. The covariance rank matrix must vary from 1 to full-rank. Plot the dependence of the restoration performance from number of iterations for different ranks.
    * [Bishop](https://www.microsoft.com/en-us/research/uploads/prod/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)
    * [Optuna, recommended for BO](https://optuna.org/)
    
