## Project list, fall 2026
### Secret energy-based models

**Number of people in team:**  2-4

**Motivation**:  the project treats *sampling/generation* as the main lens: nearly-standard architectures trained for other purposes (classification, discrimination, denoising) turn out to be energy-based models (EBM), and the same energy view lets you turn them into generators at very different costs — from a free walk on top of an already-trained network to a fully retrained classifier. 


**Algorithms to implement (from simplets to hardest):**
* [Denoising and contrastive autoencoders as EBM](https://arxiv.org/abs/1211.4246)
* [JEM: Your Classifier is Secretly an Energy Based Model and You Should Treat it Like One](https://arxiv.org/abs/1912.03263)
* [Discriminator as EBM](https://arxiv.org/pdf/2003.06060)
* [JEM++](https://arxiv.org/pdf/2109.09032) and [SADA-JEM](https://arxiv.org/pdf/2209.07959): engeneering tricks for training JEM

**Project specifics:** JEM++ and SADA-JEM are strongly dependent on JEM and can be considered as helpers/utils for trianing JEM. These tasks are very co-related.

**Problem details:**  sample quality, especially for JEM, will likely be mediocre (JEM/SGLD training is notoriously unstable). Regardless of generation quality, the library must expose an out-of-distribution detection utility built on the *same* energy function at (near-)zero extra cost ([Liu et al., Energy-based OOD Detection](https://arxiv.org/abs/2010.03759)) for all three host models. 


### Low-variance gradient estimation for arbitary distributions

**Number of people in team:** 2-3

**Motivation**: The vanilla ELBO estimation in generative models like VAE uses reparametrization trick: a method of sampling random variables with low variance of the gradient of parameter distribution. The problem with this method is that it's available only for the limited number of distributions. The goal of this project is to wrap multiple methods describing a solution for this issue into a library performing for (nearly-)arbitary distributions.
 
**Algorithms to implement (from simplets to hardest):**
* [Rejection-sampling variational inference](https://proceedings.mlr.press/v54/naesseth17a.html)
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


###  Low-variance gradient estimation for mixture distributions

**Number of people in team:** 2-4

**Motivation**: Standard reparameterization trick in generative models like VAE works well for basic distributions, but fails for mixture distributions due to discrete component sampling. PyTorch's native `MixtureSameFamily` doesn't support `rsample()` for gradients over mixture parameters. The goal of this project is to build a library implementing continuous, low-variance gradient estimation methods specifically for mixture models.

**Algorithms to implement (from simplest to hardest):**
* [Score-function baseline with Sticking the Landing (STL) trick](https://arxiv.org/abs/1703.09194) ([See also](https://www.jmlr.org/papers/v27/25-2560.html))
* [Stratified mixture estimator (multi-sample)](https://www.jmlr.org/papers/v27/25-2560.html)
* [Implicit reparameterization trick for mixture distributions](https://arxiv.org/abs/1805.08498)
* [Post-stratified mixture estimator (single-sample continuous transport)](https://www.jmlr.org/papers/v27/25-2560.html)

**Recommended stack**: PyTorch (extending `torch.distributions`) or Distrax for JAX.

**Note:** For comparison, methods should be benchmarked on synthetic multimodal targets, Mixture-of-Gaussians VAE, and BNNs with mixture priors (comparing gradient variance vs wall-clock time).

**Other links:**
* [Gradient Estimation for Mixture Variational Inference (JMLR 2026)](https://www.jmlr.org/papers/v27/25-2560.html)
* [Implicit Reparameterization Trick paper](https://arxiv.org/abs/1805.08498)
* [Pathwise Derivatives for Multivariate Distributions paper](https://proceedings.mlr.press/v80/jankowiak18a/jankowiak18a.pdf)
* [Sticking the Landing paper](https://arxiv.org/abs/1703.09194)
* [Previous mixture distribution implementation attempt](https://github.com/vsimkus/torch-reparametrised-mixture-distribution)
* [PyTorch issue on mixture reparameterization](https://github.com/pytorch/pytorch/issues/24249)
