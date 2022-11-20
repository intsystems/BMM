Deadline: December 11, 23.59.

**All the experiments should be implemented with JAX or sklearn. Not pytorch!**

Save notebooks into lab3/SurnameTask3.ipynb

1. [Reporter: TODO] Repeat plot 28.6 from MacKay book. Dataset: sklearn dataset. 
    Prior: normal distribution with scalar covariance. Models: multiple linear regression models:
    1. with optimal hyperparameters
    2. with lowered variance for the prior 
    3. with biased mean for the prior
* [datasets](https://scikit-learn.org/stable/datasets/toy_dataset.html)
* [book](http://www.inference.org.uk/itprnn/book.pdf)
* [hyperparameter optimization](http://strijov.com/papers/HyperOptimizationEng.pdf)
* Visualization: [help1](https://matplotlib.org/stable/users/interactive.html),[help2](https://stackoverflow.com/questions/44329068/jupyter-notebook-interactive-plot-with-widgets),[help3](https://towardsdatascience.com/matplotlib-animations-in-jupyter-notebook-4422e4f0e389)


2.  [Reporter: TODO] Repeat experiment from Bishop's article (fig. 4) with naive implementation of generative-discriminative model (eq. 12 from article). Visualize discriminative surface as an interactive plot dependent on the number of labeled objects and coefficients for each term.
* [Article](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/05/Bishop-Valencia-07.pdf)

3. [Reporter: TODO] Visualize dependency of classification error on different versions of Dataset Shift. Visualization (multiple plots) must show:
* how the dataset changes from the value of shift
* how the classification error changes from the value of shift

Datasets: multiple synthetic 2d datasets.

* [Article](https://rtg.cis.upenn.edu/cis700-2019/papers/dataset-shift/dataset-shift-terminology.pdf)

4. [Reporter: TODO] repeat the experiment with RBM pretraining and without pretraining  (figure 3 from the article).
* [Article](http://proceedings.mlr.press/v9/erhan10a/erhan10a.pdf)

5. [Reporter: TODO]  repeat the experiment with denoising autoencoder pretraining and without pretraining  (figure 3 from the article). 
* [Article](http://proceedings.mlr.press/v9/erhan10a/erhan10a.pdf)

6. [Reporter: TODO] Visualize sampling from RMB  for MNIST dataset (Gibbs sampling):
	* x_0 - from dataset
	* h_0 ~ p(h_0|x_0)
	* x_1 ~ p(x_1|h_0)
	...
	* x_k ~ p(x_k|h_{k-1})
	
Show how samples are changed for k iterations.

* [DL book](https://www.deeplearningbook.org/contents/generative_models.html)
* [Article on medium](https://medium.com/datatype/restricted-boltzmann-machine-a-complete-analysis-part-3-contrastive-divergence-algorithm-3d06bbebb10c)

7. [Reporter: TODO] Visualize message passing for factor-graph with algorithm Sum-Product. The directions of messages should be visualized in the resulting plots.  Graph and model parameters must be sampled randomly during each run of notebook. Visualization format - plots step by step via interactive plots or animation. 
* [Bishop, Sum product](http://users.isr.ist.utl.pt/~wurmd/Livros/school/Bishop%20-%20Pattern%20Recognition%20And%20Machine%20Learning%20-%20Springer%20%202006.pdf)
* [Animation example](https://jckantor.github.io/CBE30338/A.03-Animation-in-Jupyter-Notebooks.html)


8. [Reporter: TODO] Visualize KL-divergence (for 3 variants: KL(p1,p2), KL(p2,p1) and 0.5 KL(p1,p2) + 0.5 KL(p2,p1)) between true data distribution and GAN distribution. Visulizae dependence of these KL-divergences on the numer of optimization iterations. Dataset: synthetic. 



9. [Repoert: TODO] Plot vector field for autoencoder. Plot heatmap of dataset likelihood from VAE. Compare results. Datasets: multiple synthetic, similar to datasets used in the article.
* [article](https://jmlr.csail.mit.edu/papers/volume15/alain14a/alain14a.pdf)
