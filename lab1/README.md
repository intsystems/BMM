Deadline: October 21, 23.59.

Save notebooks into lab1/SurnameTask1.ipynb


1. [Reporter: TODO] Visualize posterior covariance matrix for each extremum of mult-extremal classification model. Model: 1-layer neural network. Dataset: on your choice (synthetic dataset is allowed). 
Use normal distribution with diagonal covariance prior. For posterior distribution use Laplace approximation.
* [Hyperparameter optimization, Laplace approximation](http://strijov.com/papers/HyperOptimizationEng.pdf)


2. Visualize posterior and optimizer prior covariance matrix for a classification model. Model: 1-layer neural network. Dataset: on your choice (synthetic dataset is allowed). 
Use normal distribution with diagonal covariance prior. For posterior distribution use Laplace approximation.
* [Hyperparameter optimization, Laplace approximation](http://strijov.com/papers/HyperOptimizationEng.pdf)


3. [Reporter: TODO]  Visualize empricial distribution of model parameters with dependence on the hidden layer neuron number (use different neuro number values, including underparameterized and overparameterized models). Model: 1-layer neural network. Dataset: MNIST or similar.


4. [Reporter: TODO] Visualize Evidence similar to slide 7 from the MDL lecture. The visualization must show the dependence between complexity and hidden layer number.  Model: 1-layer neural network. Dataset: sklearn dataset. Use normal distribution with scalar covariance prior. For posterior distribution use Laplace approximation.
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)
* [hyperparameter optimization](http://strijov.com/papers/HyperOptimizationEng.pdf)
* [презентация](https://github.com/Intelligent-Systems-Phystech/BMM-21/blob/master/slides/slides_3_mdl.pdf)
* [origignal visualization](https://www.inference.org.uk/itprnn/book.pdf)



5. [Reporter: TODO] Visualize empricial distribution of model parameters with dependence on the $p$ in L^p regularization. Model: logistic regression or 1-layer neural network. Dataset: sklearn dataset.
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)


6. [Reporter: TODO] Consider logistic regression on two features. Build a surface with 3 axes: w1, w2, sigma (optimized hyperparameter for the normal prior with scalar variance). Use color of the surface for the posterior value display.  Model: logistic regression. Dataset:  on your choice (synthetic dataset is allowed).  Optimization of sigma: on your choice (Laplace approximation or exhaustive search).
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)

7. [Reporter: TODO]  Build an interactive surface (see references) of the posterior distribution on the model parameters number, sigma  (optimized hyperparameter for the normal prior with scalar variance) and empirical variance of the parameters. The color of the surface must be set according the Evidence value. Model: logistic regression on the polynomial values of one feature.  Dataset:  on your choice (synthetic dataset is allowed). 
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)
* Visualization: [help1](https://matplotlib.org/stable/users/interactive.html),[help2](https://stackoverflow.com/questions/44329068/jupyter-notebook-interactive-plot-with-widgets),[help3](https://towardsdatascience.com/matplotlib-animations-in-jupyter-notebook-4422e4f0e389)

8. [Reporter: TODO] Repeat plot 28.6 from MacKay book. Dataset: sklearn dataset. 
    Prior: normal distribution with scalar covariance. Models: multiple linear regression models:
    1. with optimal hyperparameters
    2. with lowered variance for the prior 
    3. with biased mean for the prior
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)
* [book](http://www.inference.org.uk/itprnn/book.pdf)
* [hyperparameter optimization](http://strijov.com/papers/HyperOptimizationEng.pdf)
* Visualization: [help1](https://matplotlib.org/stable/users/interactive.html),[help2](https://stackoverflow.com/questions/44329068/jupyter-notebook-interactive-plot-with-widgets),[help3](https://towardsdatascience.com/matplotlib-animations-in-jupyter-notebook-4422e4f0e389)

9. [Reporter: TODO] Visualize KDE with KNN depending on neighbour number using interactive plots.
* Visualization: [help1](https://matplotlib.org/stable/users/interactive.html),[help2](https://stackoverflow.com/questions/44329068/jupyter-notebook-interactive-plot-with-widgets),[help3](https://towardsdatascience.com/matplotlib-animations-in-jupyter-notebook-4422e4f0e389)
