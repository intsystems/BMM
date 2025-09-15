# Projects

## Project list (fall 2025, tentative)

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




## Robusntess + Uncertainty

## TODO: EBM
Your GAN is 
Your classifier is
https://openaccess.thecvf.com/content/CVPR2023/papers/Yang_Towards_Bridging_the_Performance_Gaps_of_Joint_Energy-Based_Models_CVPR_2023_paper.pdf?utm_source=chatgpt.com
https://arxiv.org/abs/2109.09032?utm_source=chatgpt.com
https://arxiv.org/abs/2505.19459?utm_source=chatgpt.com
Score-based?

## TODO: MDL
https://proceedings.mlr.press/v139/perez21a/perez21a.pdf
https://openreview.net/pdf?id=C45YqeBDUM
https://openreview.net/pdf/a054f8be18a5c80dcc3042fafa4b6be3feb62984.pdf
Grokking
https://www.sciencedirect.com/science/article/pii/S0167278925003367
https://arxiv.org/html/2409.01247v1
https://arxiv.org/pdf/2405.05189



## TODO: IRT
IRT
Reinforce/NVIL
Rejection sampling variational inference


## TODO: DWP

## Graph models


