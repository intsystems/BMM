Deadline: May 14, 23.59.

Save notebooks into task5/SurnameTask5.ipynb

**IMPORTANT:** the code must not be written in Torch/Tensorflow. For deep learning use Jax.

1. Evaluate cold posterior effect using Variational inference on MNIST (or similar dataset). Plot the model performance from the temperature.
* [Reference](https://arxiv.org/pdf/2002.02405.pdf)
* [Var. inf. for NN](https://papers.nips.cc/paper/4329-practical-variational-inference-for-neural-networks)

2. Repeat "Rényi Divergence Variational Inference" experiment for multiple standard datasets. In addition, evaluate model performance when we add Gaussian noise to it and adversarial attacks. Plot the model performance from noise variance (for Gaussian noise) and eps (for Adv. attacks).
* [Paper](https://proceedings.neurips.cc/paper_files/paper/2016/file/7750ca3559e5b8e1f44210283368fc16-Paper.pdf)
* [Talk](https://github.com/intsystems/BMM/tree/main-23/student_talks/week_4_renyi_divergence)
* [Tutorial on FGSM attacks](https://pytorch.org/tutorials/beginner/fgsm_tutorial.html)

3. Train multiple (many!) MLP models on a toy dataset. Make a random pruning of the models. Visualize their parameter projection onto 2d-space with color corresponding to accuracy using autoencoder.

4.[reporter: Parviz Karimov] Train models for different 1d synthetic datasets (the generating functions must be non-trivial).  Implement F-PCA, visualize projections using U-MAP or similar methods.
* [https://fda.readthedocs.io/en/latest/auto_examples/plot_fpca.html](F-PCA)

5. Evaluate and visualize the model uncertainity for OOD detection using different methods:
* Model confidence
* Model ensembling
* [Dropout MC](https://arxiv.org/pdf/1506.02142.pdf)


6. Compare MCMC and Laplace approximation for hyperparameter optimization. Model: Logistic regression. Hyperparameters: covariance matrix (consider 3 variants: with scalar, diagonal and full matrix). Visalize hyperparameter convergence to the true value as a function from Laplace/MCMC iterations.

* [Reference paper](https://informatica.vu.lt/journal/INFORMATICA/article/817/file/pdf)

