# Projects

## Project activities
Each team must assign roles for all teammates. Each activity is evaluated independently, thus number of activites per each teammate must be ~equal.

* Project planning: the student must describe (or gather with the team) a document with the following information:
	* Project name
	* Project scope (what algorithms will be implemented)
	* Project stack (what libraries will be used,  how the project will be integrated with other libraries)
	* A scheme of the project (no certain requirements for the format, but you can use IDEF or UML for better clarity if you want)
	* Present this plan
	* **Evaluation criterion:** presentation at Tech. meeting 1
  
* Benchmark. This code must implement baseline algorithms on a (maybe simplified) to dataset. Further this benchmark must be used as a basis of the library demo.
 * This benchmark must also implement (**maybe in a very simplified version**) one of the proposed algorithms.
 * The goal of this activity is an early check that the plan is possible to implement, and all the proposed algorithms can be further reported.
 * **Evaluation criterion:** presentation  at Tech. meeting 2


* Algorithm implementation (1 activity per teammate)
	*  **Evaluation criterion:** presentation at Tech. meeting 1, cross-review, presentation, tests correctly run the algorithm,  presentation at Tech. meeting 3
* Project wrapping:
	* Making the code uniform acros all the teammates
	* Controling the code quality/consistency
	* Wrapping the code into library, repository creation and support
	* **Evaluation criterion:** cross-review,  presentation, the links are correct, the code can be installed without problems, all the workflows are setup, short presentation at Checkpoint, full presentation at tech. meeting 3

  
* Tests writing
	* **Evaluation criterion:** test coverage > 90%,  presentation at Tech. meeting 3
* Documentation writing
	* **Evaluation criterion:** cross-review,   presentation at Tech. meeting 2 (intermediate version), presentation at Tech. meeting 3
* Cross-review (1 activity per teammate)
* Making a final demo based on the basic code
	* **Evaluation criterion:** cross-review,  presentation
  
* Blog post and tech. report
* Blog post must be published at some platform (habr, medium, etc)
* Short message: up to 10 minutes
* **Evaluation criterion:** ,  presentation at Tech. meeting 2 (intermediate version), ,presentation at Tech. meeting 3, possibely external review

 
* Tech. report: must contain a short version of technical paper: abstract, introduction, methods, experiments. The length: 3-5 pages.
* **Evaluation criterion:** ,  presentation at Tech. meeting 2 (intermediate version), ,presentation at Tech. meeting 3, possibely external review


For the team of 2 people it means that each teammate must have 5 acitvities
For the team of 4 people each teammate must have 3 or 4 activities




## Project list, fall 2025

### Stochastic gating

**Number of people in team:** 2-4

 **Motivation**: One of the methods of proper feature/variable/parameter selection is called [Stochastic gating](http://proceedings.mlr.press/v119/yamada20a/yamada20a.pdf).The principle is the following: multiply each parameter of the model (or the feature if we are working with linear models) with some discrete variable and optimize both the parameter and the distribution of the discrete variable. Due to the continuity of the optimization, the discrete variable must be replaced with some kind of relaxation. 
 
**Algorithms to implement (from simplets to hardest):**
* Feature selection with L2 regularization and straight-through estimation [see here for example](https://arxiv.org/pdf/2006.06880) , see also [basic paper for ST-estimator](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=62c76ca0b2790c34e85ba1cce09d47be317c7235) 
* Gumbel-softmax for gating [see here](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123720239.pdf) 
* [Original stochastic gating](https://proceedings.mlr.press/v119/yamada20a/yamada20a.pdf) 
* [Correlated features in stochastic gating](https://openreview.net/pdf?id=oDFvtxzPOx)
  
**Other links:**
* [Stochasting gating library](https://runopti.github.io/stg/)

**Problem details:** the team must decide the structure of the project: are the modules they propose are just layer classes (like dropout layers) or they propose some "solvers"? What's more preferable for reproducibility and furhter usage? 


### Bayesian ensembling

**Number of people in team:**  2-4

**Motivation**:  the project proposes to develop the library that unifies different approaches for Bayesian model selection. The focus here more on the model ensembling: each algorithm proposes different strategies to sample models from posterior distribution. As a bonus for the 4th member of the team we propose to adapt Renyi divergence optimization for the model selection.

**Algorithms to implement (from simplets to hardest):**
* [A baseline ELBO: proposed by Graves in 2011](https://papers.nips.cc/paper/4329-practical-variational-inference-for-neural-networks). Must be implemented with [local reparameterization trick](https://arxiv.org/abs/1506.02557) , hyperparameter optimization and pruning.
* [Alternative method: scalable Laplace approximation](https://discovery.ucl.ac.uk/id/eprint/10080902/1/kflaplace.pdf) 
* [Renyi divergence: a generalization of the ELBO which can potentially plugged into the algorithms 1 and 2 and make models more extendable](https://arxiv.org/abs/1602.02311) 
* [Bayes backprop](https://arxiv.org/abs/1502.05336]

**Links**:
* [Most parts of the algorithms are implemented here](https://github.com/JavierAntoran/Bayesian-Neural-Networks) 
* [Renyi](https://docs.pyro.ai/en/1.9.1/_modules/pyro/infer/renyi_elbo.html) 
* [Torch uncertainty](https://torch-uncertainty.github.io/)

**Problem details:** At least two additional algorithms must be implemented as baseline (maybe just using pyro): HMC and [McDropout](https://arxiv.org/abs/1506.02142). HMC is a very long running algorithm for posterio sampling/model selection, but with limits to short chains it can evaluate our Evidence and can be considered as a ground truth. See [some papers that evaluate model Evidence with HMC](https://arxiv.org/pdf/2002.02405) and [this one, but it uses a very heavy HMC, we don't need it](http://proceedings.mlr.press/v139/izmailov21a/izmailov21a.pdf).

Since the algorithms implementation can be already found, the main problem of this project is to wrap everthing into one simple interface. Think what methods/functionality can be useful for the user.



### Secret energy-based models

**Number of people in team:**  2-4

**Motivation**:  the project proposes to consider multiple nearly-standard architectures and reveal their sampling properties: generalized (non-variational) autoencoders, classification neural networks and GAN's discriminator are proven to be energy-based models (EBM) that can be potentially used for generative tasks (sampling, out-of-domain detection, density estimation).

**Algorithms to implement (from simplets to hardest):**
* [Denoising and contrastive autoencoders as EBM](https://arxiv.org/abs/1211.4246)
* [JEM: Your Classifier is Secretly an Energy Based Model and You Should Treat it Like One](https://arxiv.org/abs/1912.03263)
* [Discriminator as EBM](https://arxiv.org/pdf/2003.06060)
* [JEM++](https://arxiv.org/pdf/2109.09032) and [SADA-JEM](https://arxiv.org/pdf/2209.07959): engeneering tricks for training JEM


**Project specifics:** JEM++ and SADA-JEM are strongly dependent on JEM and can be considered as helpers/utils for trianing JEM. These tasks are very co-related.

**Problem details:**  Think about how to combine the modules and make them reusable. Also, what should provide EBM models?


### Neural compression

**Number of people in team:**  2-4

**Motivation**:  information theory and Bayesian models are deeply tied. Here we propose to implement multiple variational and neural compression methods for losesless (and nearly-loseless) compression.

**Algorithms to implement:**
* [Var. inference-based](https://arxiv.org/pdf/1901.04866)
* [Gradient flows-based](https://arxiv.org/pdf/1905.07376)
* [Transformer-based](https://openreview.net/forum?id=Hygi7xStvS)
* [Lossy compression](https://proceedings.neurips.cc/paper/2021/file/7535bbb91c8fde347ad861f293126633-Paper.pdf)


**Note:** good start is to look at [this](https://github.com/facebookresearch/NeuralCompression) and [this repo](https://github.com/fahaihi/NNLCB?tab=readme-ov-file)

### Low-variance gradient estimation for arbitary solutions

**Number of people in team:** 2-4

**Motivation**: The vanilla ELBO estimation in generative models like VAE uses reparametrization trick: a method of sampling random variables with low variance of the gradient of parameter distribution. The problem with this method is that it's available only for the limited number of distributions. The goal of this project is to wrap multiple methods describing a solution for this issue into a library performing for (nearly-)arbitary distributions.
 
**Algorithms to implement (from simplets to hardest):**
* [Rejection-sampling variational inference](https://proceedings.mlr.press/v54/naesseth17a.html)
* [Implicit reparametrization trick: cases for Gaussian distribution, Student distribtuion and a mixture](https://arxiv.org/abs/1805.08498)
* [Implicit reparametrization trick: case for factorized distribution]((https://arxiv.org/abs/1805.08498)
* [Transort equation-based reparametrization trick](https://proceedings.mlr.press/v80/jankowiak18a/jankowiak18a.pdf)


**Recommended stack**: one can use pytorch/pyro (both have interfaces for distributions) or distrax for JAX. Other stack can also be used.

**Note:** for the comparison it's recommended to implement REINFORCE-based methods, as well as some numerical low-dimmesnional methods.

**Other links:**
* [Previous project attemp](https://github.com/intsystems/implicit-reparameterization-trick)
* [Discussion of IRP in the TF probability thread](https://github.com/tensorflow/probability/issues/51?ref=https://githubhelp.com)
* [Some more discussions in the pytorch thread](https://discuss.pytorch.org/t/pytorch-reparametrization-method-for-gamma-dirichlet-von-mises-distribution/109472)
* [Mixutre distribution implementation](https://github.com/vsimkus/torch-reparametrised-mixture-distribution) 
* [Lab on the implementation of IRT](https://github.com/intsystems/BMM/blob/main-22/lab2/BarabanshchikovaTask2.ipynb)


### Relaxit 1.5

**Number of people in team:** 2-4

 **Motivation**: For lots of mathematical problems we need an ability to sample discrete random variables. The problem is that due to continuos nature of deep learning optimization, the usage of truely discrete random variables is infeasible. Thus we use different relaxation method. One of them, [Concrete distribution](https://arxiv.org/abs/1611.01144) or [Gumbel-softmax](https://arxiv.org/abs/1611.00712)  (this is one distribution proposed in parallel by two research groups) is implemented in different DL packages. 
 The previous year our studnet group made a [relaxit](github.com/intsystems/relaxit) library that considers multiple alternatives to this distribtuion.  The goal of this project is to update the library with more algorithms.

**Algorithms to implement:**
* [Generalized GS](https://arxiv.org/abs/2003.01847)
* [Surrogate-based](https://arxiv.org/pdf/1711.00123)
* [REBAR](https://arxiv.org/pdf/1703.07370)
* [ST-GS](https://arxiv.org/abs/2410.13331)

**Note:** since this is a continuation of the old project, the main focus here is to make a good demo/baselines. This is essnetial here.
Strongly recommended to compare the methods with [ReinMax](https://github.com/microsoft/ReinMax)  or integrate it into the library.
  
