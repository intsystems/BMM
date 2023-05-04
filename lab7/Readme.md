Deadline: May 9, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**

1. [Skorik Sergey] Consider [Hinton](https://arxiv.org/abs/1503.02531) distillation, but without dataset labels (only teacher output for distillation).

Dataset: MNIST. Consider case, when we have two teacher trained only on class subsets (0,..,4) and (5,..,9): Loss = lambda * Dist_1 + (1-lambda) * Dist_2

Visualize accuracy of the model with 3 axes:
   - Accuracy
   - Temperature
   - Lambda
    

2. [Barabanshchikova Polina][Visualize 3 types of dataset shift](https://rtg.cis.upenn.edu/cis700-2019/papers/dataset-shift/dataset-shift-terminology.pdf) for linear regression task with 1d or 2d dataset. For each type of dataset shift plot the RMSE dependency on the dataset shift.

3. Repeat [knowledge distillation without dataset](https://arxiv.org/pdf/1710.07535.pdf) for MNIST dataset using top layer and all-layer statistics.

4. Visualize repeat-copy task using LSTM with schedules: from large length to small length and vice versa.
Number of repeats is constant, set to 1.

Visualize model performance wrt optimization iterations.

5. Visualize repeat-copy task using LSTM with schedule: from small number of repeats to large number of repeats. Compare with no-schedule baseline (number of repeats is random).
Length is constant, set to 30.

Visualize model performance wrt optimization iterations.


6. Demonstrate Task-IL, Domain-IL and Class-IL continual learning problems for MNIST. Compare results with scheme results from [paper](https://arxiv.org/pdf/1803.10123.pdf). 
