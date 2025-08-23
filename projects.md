# Projects

## Project list (fall 2025, tentative)
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
