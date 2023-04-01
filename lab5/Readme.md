Deadline: April 3, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**
1. Consider neural network model selection problem (structure is set by layer number and neuron numbers). Compare multiple approaches for model selection:
    - Using GP
    - Using TPE
    - Using GP wrt. inference runtime [see paper](https://arxiv.org/pdf/1206.2944.pdf)
    - Using TPE wrt. inference runtime
    - Using TPE With pareto-front (see Optuna package)
    

    
2. Consider the following bi-level optimization problem[Kovaleva]:
    - L_train = |h + w|^2
    - L_val = |w|^2
   Run n-order hyperparameter optimization for such a problem (n=0..5).
   Visualize optimization trajectories in two surface plots: (h, w, L_train), (h, w, L_val)
   - [1-order optimization](http://proceedings.mlr.press/v48/luketina16.pdf)
   - [0-order and 1-order optimization](https://arxiv.org/pdf/1806.09055.pdf)
   
   **Note:** for such a simple setting no need to use sophisticated calculation tricks that described in DARTS, for example.
   
3. [Skorik Sergey] Consider the following bi-level optimization problem:
    - L_train = |h + w|^2
    - L_val = |w|^2
   Run DrMAD (hyperparameter optimization with trajectory linearization) and piecewise trajectory linearization modification.
   Visualize optimization trajectories in two surface plots: (h, w, L_train), (h, w, L_val).
   - [DrMAD](https://arxiv.org/pdf/1601.00917.pdf)

4. [Yakovlev Konstantin] Consider the following bi-level optimization problem:
    - L_train = |h + w|^2
    - L_val = |w|^2
   Optimize hyperparameters using hypernetworks (h is sampled).
   Visualize dependency of w on w on the two surface plots: (h, w, L_train), (h, w, L_val).
   - [Hypernetworks](http://www.ipiran.ru/journal/issues/2021_15_01/Vol15_Issue1.pdf)

   
5. [Pyatkin Stanislav] Repeat "learning to learn" experiment on MNIST. Visualize norm of the gradient and norm of the parameter of gradients for optimization steps for different optimzers: SGD, Adam, LSTM.
    - [Learning to learn](https://arxiv.org/pdf/1606.04474.pdf)
    

   
