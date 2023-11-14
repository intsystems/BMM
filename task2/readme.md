Deadline: November 30, 23.59.

Save notebooks into task2/SurnameTask2.ipynb

**IMPORTANT:** the code must not be written in Torch/Tensorflow. For deep learning use Jax.


1. [Reporter: TODO] Visualize message passing for factor-graph with algorithm Sum-Product. The directions of messages should be visualized in the resulting plots.  Graph and model parameters must be sampled randomly during each run of notebook. Visualization format - plots step by step via interactive plots or animation. 
* [Bishop, Sum product](http://users.isr.ist.utl.pt/~wurmd/Livros/school/Bishop%20-%20Pattern%20Recognition%20And%20Machine%20Learning%20-%20Springer%20%202006.pdf)
* [Animation example](https://jckantor.github.io/CBE30338/A.03-Animation-in-Jupyter-Notebooks.html)
* [Large book about probabilistic models](http://mcb111.org/w06/KollerFriedman.pdf)

2. [Reporter: TODO] Generate Bayesian network randomly. Generate dataset using Bayesian network. Estimate likelihood and compare it with likelihood for random data ("out-of-distribution" data). Convert network to Markov Random Field. Estimate the likelihood of previously generated data and random data. Repeat experiment multiple times.
* [Bishop, Bayesian networks and Markov random fields](http://users.isr.ist.utl.pt/~wurmd/Livros/school/Bishop%20-%20Pattern%20Recognition%20And%20Machine%20Learning%20-%20Springer%20%202006.pdf)
* [Large book about probabilistic models](http://mcb111.org/w06/KollerFriedman.pdf)

3.[Reporter: Marat Khusainov] Visualize KL-divergence (for 3 variants: KL(p1,p2), KL(p2,p1) and 0.5 KL(p1,p2) + 0.5 KL(p2,p1)) and JS distance between true data distribution and GAN distribution. Visulizae dependence of these KL-divergences on the numer of optimization iterations. Dataset: synthetic. 

4. [Reporter: TODO] Repeat M1 and M2 models from Kingma for a dataset with noisy labels. Plots the performance of both models from the percentage of wrong (noisy) labels. Dataset: MNIST or similar dataset.
* [Paper](https://proceedings.neurips.cc/paper/2014/file/d523773c6b194f37b938d340d5d02232-Paper.pdf)

5. [Reporter: TODO] Compare model performance, where models are implemented using Maximum likelihood optimization, MAP + Laplace approximation, ELBO for different dataset shifts: covariate shift, prior probability shift, concept shift. Plot dependency from the dataset shift significance. Model: any model starting from Logistic regression. 

6. [Reporter: TODO] Train VAE. Train vanilla AE to repeat VAE performance using GAN. Sample from AE, analyze sampling performance. Dataset: MNIST or similar dataset.

7. [Reporter: TODO] Plot vectorfield from contractive AE. Plot heatmap for norm of it. Plot VAE density. Compare results. Analyze dependency of density estimation quality of AE from sigma. Dataset: MNIST or similar dataset.
* [Paper](https://www.jmlr.org/papers/volume15/alain14a/alain14a.pdf)


8. [Reporter: TODO] Plot vectorfield from denoysing AE. Plot heatmap for norm of it. Plot VAE density. Compare results. Analyze dependency of density estimation quality of AE from sigma. Dataset: MNIST or similar dataset.
* [Paper](https://www.jmlr.org/papers/volume15/alain14a/alain14a.pdf)


9. [Reporter: Galina Boeva] Repeat two methods of optimization of GAN: using eq 1 and alternative method for better gradients (see paper). Compare the convergence of both models, their losses as well as their generator and discriminator losses.
* [Paper](https://arxiv.org/pdf/1406.2661.pdf)

10. [Reporter: TODO] Train vanilla autoencoder. Approximate latent variable distribution using uniform and normal distribution. Try to sample. Analyze sampling performance.

