Deadline: November 12, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**

Save notebooks into lab1/SurnameTask2.ipynb


1. [Reporter: Ksenofontov Grigorii] Visualize posterior covariance matrix for each extremum of mult-extremal classification model. Model: 1-layer neural network. Dataset: on your choice (synthetic dataset is allowed). 
Use normal distribution with diagonal covariance prior. For posterior distribution use Laplace approximation.
* [Hyperparameter optimization, Laplace approximation](http://strijov.com/papers/HyperOptimizationEng.pdf)

2. [Reporter: TODO] Repeat plot 28.6 from MacKay book. Dataset: sklearn dataset. 
    Prior: normal distribution with scalar covariance. Models: multiple linear regression models:
    1. with optimal hyperparameters
    2. with lowered variance for the prior 
    3. with biased mean for the prior
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)
* [book](http://www.inference.org.uk/itprnn/book.pdf)
* [hyperparameter optimization](http://strijov.com/papers/HyperOptimizationEng.pdf)
* Visualization: [help1](https://matplotlib.org/stable/users/interactive.html),[help2](https://stackoverflow.com/questions/44329068/jupyter-notebook-interactive-plot-with-widgets),[help3](https://towardsdatascience.com/matplotlib-animations-in-jupyter-notebook-4422e4f0e389)

3. [Reporter: Yakovlev Konstantin] 
Reimplement experiment from the article "Early stopping as nonparametric variational inference". Compare the results with the results from article.
* [article](https://arxiv.org/abs/1504.01344)


4. [Reporter: Gregory Polyakov]
Reimplement experiment from the article "Variational Inference with Gradient Flows". Compare the results with the results from article and vanilla VAE.
* [article](http://approximateinference.org/accepted/AltieriDuvenaud2015.pdf)


5. [Reporter: Kovaleva Maria]
Visualize (using interactive plots) convergence of invertible gaussian reparametrization (IGR). Optimize KL(q|p) -> min, where q and p are IGR, the parameters of IGR are sampled randomly each run. Plot: simplex (triangle) with PDF changes during optimization.
* [IGR](https://arxiv.org/pdf/1912.09588.pdf)
* [Simplex visualization example](http://blog.bogatron.net/blog/2014/02/02/visualizing-dirichlet-distributions/)



6. [Reporter: Barabanshchikova Polina]
Implement VAE with variational distribution different from Normal using implicit reparametrization.  Compare the results with vanilla VAE.
* [article](https://proceedings.neurips.cc/paper/2018/file/92c8c96e4c37100777c7190b76d28233-Paper.pdf)


7. [Reporter: Skorik Sergey]
Implement ELBO for regression problem with known posterior. Visualize KL(q|posterior), KL(q|prior), KL(posterior|q), KL(prior|q), JS(q,prior), JS(q, posterior)
* [basic ELBO (article)](https://www.cs.toronto.edu/~graves/nips_2011.pdf)


8. [Reporter: TODO]
Implement ELBO for regression problem with known posterior. Optimize hyperparameters naively, using maximum likelihood method (see article). 
Visuzlie difference between optimized hyperparameters and tru hyperparameters.
* [basic ELBO (article)](https://www.cs.toronto.edu/~graves/nips_2011.pdf)

