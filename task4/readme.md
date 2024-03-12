Deadline: April 5, 23.59.

Save notebooks into task4/SurnameTask4.ipynb

**IMPORTANT:** the code must not be written in Torch/Tensorflow. For deep learning use Jax.

1. [reporter: TODO] Train deep weight prior on MNIST dataset ane evluate its performance on SVHN dataset (make SVHN gray-colored).
* [Paper](https://arxiv.org/abs/1810.06943)

2. [reporter: Kseniia Petrushina] Repeat [knowledge distillation without dataset](https://arxiv.org/pdf/1710.07535.pdf) for MNIST dataset using top layer and all-layer statistics. 


3.  [reporter: TODO] Visualize repeat-copy task using LSTM with schedule: from small number of repeats to large number of repeats. Compare with no-schedule baseline (number of repeats is random).
Length is constant, set to 30. Visualize model performance wrt optimization iterations.


4. [reporter: TODO]  Demonstrate Task-IL, Domain-IL and Class-IL continual learning problems for MNIST. Compare results with scheme results from [paper](https://arxiv.org/pdf/1803.10123.pdf). 

5.  [reporter: TODO] Analyze stability of Learning2Learn method under different dataset shifts. Basic dataset: MNIST. Consider all dataset shift types and different dataset augmentations: inverting colors, adding noise into dataset, training LSTM only on classes subset.
* [Paper](https://proceedings.neurips.cc/paper_files/paper/2016/file/fb87582825f9d28a8d42c5e5e5e8b23d-Paper.pdf)

6. [reporter: Boeva Galina] Reimplement sinusoidal toy example from MAML. Compare MAML with its modification: instead of second-order optimization use  first-order optimization. Visualize obtained initial parameter values and training progress (see Fig 1 from MAML+ for reference).
* [MAML+](https://arxiv.org/pdf/1810.09502.pdf)
* [Talk by Dmitry Protasov](https://github.com/intsystems/BMM/blob/main-23/student_talks/week3_sem2_maml/MAML__.pdf)

7. [reporter: TODO] Compare In-context learning with Fine-tuning model similar to [paper](https://arxiv.org/pdf/2212.10559.pdf). Plot the Accuracy, SimAOU, SimAM, and Rec2FTP as a function from number of training examples. You can use any framework for the task. You can use any LLM.
* [Talk by Sergey Skorik](https://github.com/intsystems/BMM/blob/main-22/student_talks/week_17_sgd_attention/Dual_form_of_SGD_via_Attention.pdf) 

8. [reporter: TODO] Repeat approach from [https://arxiv.org/abs/1904.05835](KT with MI). Use second-order hyperparameter optimization from [Luketina](https://arxiv.org/abs/1511.06727) to optimize lambda hyperparameters (or from DARTS).  Teacher and student models can be found [here](https://github.com/passalis/probabilistic_kt/tree/master/exp_cifar).

9. [reporter: TODO] Implement [Hierarchical Bayesian Domain Adaptation](https://aclanthology.org/N09-1068.pdf) for synthetic dataset. Model: linear regression.  Compare the approach with baselines: one model per one domain, one model per all domains. Goal: is to make a very simple illustrative example, so try to focus on the illustrations.

10. [reporter: TODO]  Repeat approach from [https://arxiv.org/abs/1904.05835](KT with MI) sequentially complicating variational distribution. Teacher and student models can be found [here](https://github.com/passalis/probabilistic_kt/tree/master/exp_cifar). 
    
